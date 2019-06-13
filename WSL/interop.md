---
title: Interoperabilidade do Windows com o Linux
description: Descreve a interoperabilidade do Windows com distribuições do Linux em execução no subsistema do Windows para Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040821"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Subsistema do Windows para interoperabilidade do Linux com o Windows

> **Atualizado para o Fall Creators Update.**  
Se você estiver executando a atualização para criadores ou atualização de aniversário, vá para o [seção de atualização de criadores/aniversário](interop.md#creators-update-and-anniversary-update).

O subsistema Windows para Linux (WSL) está continuamente aprimorando a integração entre o Windows e Linux.  Você pode:

1. Invocar os binários do Windows no console do Linux.
1. Invocar os binários do Linux em um console do Windows.
1. **Compilações do Windows Insiders 17063 +** compartilham variáveis de ambiente entre o Linux e Windows.

Isso fornece uma experiência perfeita entre o Windows e o WSL.  Detalhes técnicos são sobre o [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Executar ferramentas do Linux em uma linha de comando do Windows

Executar binários de Linux do usando Prompt de comando do Windows (CMD ou PowerShell) `wsl.exe <command>`.

Binários invocados desta forma:

1. Use o mesmo diretório de trabalho como o atual prompt CMD ou o PowerShell.
1. Execute como usuário padrão WSL.
1. Ter os mesmos direitos administrativos do Windows como o processo de chamada e o terminal.

Por exemplo:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

O seguinte comando de Linux `wsl.exe` é tratado como qualquer comando executado no WSL.  As coisas como sudo, tubulação e redirecionamento de arquivo funcionam.

Exemplo usando o sudo:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Exemplos de combinação de comandos WSL e Windows:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Os comandos são passados para `wsl.exe` são encaminhadas para o processo WSL sem modificação.  Caminhos de arquivo devem ser especificados no formato WSL.

Exemplo com caminhos:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Executar ferramentas do Windows de WSL

WSL pode invocar os binários do Windows diretamente na linha de comando de WSL usando `[binary name].exe`.  Por exemplo, `notepad.exe`.  Para facilitar a execução de executáveis do Windows, o caminho do Windows está incluído no Linux `$PATH` no Fall Creators Update.

Aplicativos executados dessa maneira tem as seguintes propriedades:

1. Manter o diretório de trabalho como o prompt de comando WSL (na maior parte, as exceções são explicadas abaixo).
1. Ter os mesmos direitos de permissão que o processo WSL.
1. Executado como o usuário do Windows Active Directory.
1. São exibidos no Gerenciador de tarefas do Windows como se executado diretamente no prompt de comando.

Exemplo:

``` BASH
$ notepad.exe
```

Arquivos executáveis do Windows executados no WSL são tratadas da mesma forma para executáveis de Linux nativo – pipe, redirecionamentos e até mesmo backgrounding trabalho conforme o esperado.

Exemplos usando pipes:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Exemplo usando comandos do Windows e WSL misto:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Binários do Windows devem incluir a extensão de arquivo, corresponder ao uso de arquivo e ser executável.  Incluindo arquivos executáveis não scripts em lote.  Como comandos nativos de CMD `dir` pode ser executado com `cmd.exe /C` comando.

Exemplos:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Parâmetros são passados para o Windows binária sem modificações.

Por exemplo, os comandos a seguir abrirá `C:\temp\foo.txt` em `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Modificando arquivos localizados em VolFs (arquivos não está `/mnt/<x>`) com um Windows application no WSL não tem suporte.

Por padrão, o WSL tenta manter o diretório de trabalho do que o Windows binária como o diretório atual do WSL, mas fará o fallback no diretório de criação de instância se o diretório de trabalho estiver em VolFs.

Por exemplo; `wsl.exe` inicialmente é iniciada no `C:\temp` e diretório WSL atual é alterado para casa do usuário.  Quando `notepad.exe` é chamado de diretório de base do usuário, WSL é revertida automaticamente para `C:\temp` como o diretório de trabalho notepad.exe:

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Variáveis de ambiente de compartilhamento entre o Windows e o WSL

> Disponível em compilações do Windows Insider 17063 e posteriores.

Antes de 17063, apenas variável de ambiente Windows que foi possível acessar o WSL foi `PATH` (portanto, você também pode iniciar executáveis do Win32 em WSL).

A partir de 17063, WSL e Windows compartilham `WSLENV`, uma variável de ambiente especial criada para acabar com distribuições de Linux e Windows em execução no WSL.

Propriedades de `WSLENV`:

* Ele é compartilhado; ela existe em ambientes Windows e WSL.
* É uma lista de variáveis de ambiente para compartilhar entre o Windows e o WSL.
* Ele pode formatar as variáveis de ambiente para funcionar bem em Windows e WSL.

Há quatro sinalizadores disponíveis no `WSLENV` para influenciar como essa variável de ambiente é convertido.

`WSLENV` sinalizadores:

* `/p` -Converte o caminho entre caminhos no estilo WSL/Linux e os caminhos do Win32.
* `/l` -indica que a variável de ambiente é uma lista de caminhos.
* `/u` -indica que essa variável de ambiente só deve ser incluído ao executar o WSL do Win32.
* `/w` -indica que essa variável de ambiente só deve ser incluído durante a execução Win32 do WSL.

Sinalizadores podem ser combinados conforme necessário.

## <a name="disable-interop"></a>Desabilitar a interoperabilidade

Os usuários podem desabilitar a capacidade de executar os binários do Windows para uma única sessão WSL, executando o comando a seguir como raiz:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Para habilitar novamente o Windows binários saia de todas as sessões WSL e execute novamente o bash.exe ou execute o comando a seguir como raiz:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Desabilitando a interoperabilidade não serão mantidos entre sessões WSL – interoperabilidade será habilitada novamente quando uma nova sessão é iniciada.

## <a name="creators-update-and-anniversary-update"></a>Atualização para criadores e atualização de aniversário

Enquanto a pré-queda de experiência de interoperabilidade Creators Update é semelhante para experiências de interoperabilidade mais recentes, há algumas diferenças importantes.

Resumo:

* `bash.exe` foi preterido e substituído pelo `wsl.exe`.
* `-c` para executar um comando único não é necessária com a opção `wsl.exe`.
* Caminho do Windows está incluído no WSL `$PATH`

O processo para desabilitar a interoperabilidade é inalterado.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Invocar WSL da linha de comando do Windows

Binários do Linux podem ser invocados no Prompt de comando do Windows ou do PowerShell.  Binários invocados dessa maneira tem as seguintes propriedades:

1. Use o mesmo diretório de trabalho como o prompt CMD ou o PowerShell.
1. Execute como usuário padrão WSL.
1. Ter os mesmos direitos administrativos do Windows como o processo de chamada e o terminal.

Exemplo:

```console
C:\temp> bash -c "ls -la"
```

Comandos do Linux chamados dessa forma são tratados como qualquer outro aplicativo do Windows.  As coisas como entrada, tubulação e redirecionamento de arquivo funcionam conforme o esperado.

Exemplos:

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

Os comandos WSL passado para `bash -c` são encaminhadas para o processo WSL sem modificação.  Caminhos de arquivo devem ser especificados no formato WSL e tome cuidado para escapar caracteres relevantes. Exemplo:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Invocar os binários do Windows de WSL

O subsistema Windows para Linux pode invocar os binários do Windows diretamente da linha de comando WSL.  Aplicativos executados dessa maneira tem as seguintes propriedades:

1. Reter o diretório de trabalho como o prompt de comando WSL, exceto no cenário explicado abaixo.
1. Ter os mesmos direitos de permissão que o `bash.exe` processo. 
1. Executado como o usuário do Windows Active Directory.
1. São exibidos no Gerenciador de tarefas do Windows como se executado diretamente no prompt de comando.

Exemplo:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

WSL, esses executáveis são tratados semelhante para executáveis de Linux nativo.  Isso significa adicionar diretórios para o caminho do Linux e tubulação entre works comandos conforme o esperado.  Exemplos:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

O binário do Windows deve incluir a extensão de arquivo, corresponder ao uso de arquivo e ser executável.  Incluindo arquivos executáveis não scripts em lote e de comandos, como `dir` pode ser executado com `/mnt/c/Windows/System32/cmd.exe /C` comando.

Exemplos:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Parâmetros são passados para o Windows binária sem modificações.  

Por exemplo, os comandos a seguir abrirá `C:\temp\foo.txt` em `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Modificando arquivos localizados em VolFs (arquivos não está `/mnt/<x>`) com um Windows application não tem suporte.  Por padrão, o WSL tenta manter o diretório de trabalho do que o Windows binária como o diretório atual do WSL, mas fará o fallback no diretório de criação de instância se o diretório de trabalho estiver em VolFs.

Por exemplo; `bash.exe` inicialmente é iniciada no `C:\temp` e diretório WSL atual é alterado para casa do usuário.  Quando `notepad.exe` é chamado de diretório de base do usuário, WSL é revertida automaticamente para `C:\temp` como o diretório de trabalho notepad.exe:

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
