---
title: Interoperabilidade do Windows com o Linux
description: Descreve a interoperabilidade do Windows com distribuições do Linux em execução no Subsistema Windows para Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122728"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Subsistema Windows para interoperabilidade do Linux com o Windows

> **Atualização do Fall Creators Update.**  
Se você estiver executando a Atualização para Criadores ou a Atualização de Aniversário, vá para a [seção Atualização de Aniversário/Atualização para Criadores](interop.md#creators-update-and-anniversary-update).

O WSL (Subsistema Windows para Linux) está melhorando continuamente a integração entre o Windows e o Linux.  Você pode:

1. Invocar os binários do Windows no console do Linux.
1. Invocar os binários do Linux no console do Windows.
1. **Windows Insiders Builds 17063 e posteriores** Compartilhar variáveis de ambiente entre o Linux e o Windows.

Isso proporciona uma experiência simples entre o Windows e o WSL.  Os detalhes técnicos estão no [blog do WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Execute ferramentas do Linux usando uma linha de comando do Windows

Execute binários do Linux no prompt de comando do Windows (CMD ou PowerShell) usando o `wsl.exe <command>`.

Binários invocados desta maneira:

1. Use o mesmo diretório de trabalho que o prompt do CMD ou do PowerShell atual.
1. Execute como usuário padrão do WSL.
1. Tenha os mesmos direitos administrativos do Windows que o processo de chamada e o terminal.

Por exemplo:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

O comando do Linux após `wsl.exe` é tratado como qualquer comando executado no WSL.  Coisas como sudo, piping e redirecionamento de arquivo funcionam.

Exemplo usando o sudo:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Exemplos que misturam comandos do WSL e do Windows:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Os comandos passados para `wsl.exe` são encaminhados para o processo do WSL sem modificação.  Os caminhos de arquivo devem ser especificados no formato do WSL.

Exemplo com caminhos:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Executar ferramentas do Windows usando o WSL

O WSL pode invocar os binários do Windows diretamente da linha de comando do WSL usando `[binary name].exe`.  Por exemplo, `notepad.exe`.  Para facilitar a execução dos executáveis do Windows, o caminho do Windows está incluído no Linux `$PATH` no Fall Creators Update.

Os aplicativos executados dessa maneira têm as seguintes propriedades:

1. Mantenha o diretório de trabalho como o prompt de comando do WSL (em grande parte – as exceções são explicadas abaixo).
1. Tenha os mesmos direitos de permissão que o processo do WSL.
1. Execute como usuário ativo do Windows.
1. É exibido no Gerenciador de Tarefas do Windows como se fosse executado diretamente no prompt do CMD.

Exemplo:

``` BASH
$ notepad.exe
```

Os executáveis do Windows executados no WSL são tratados de forma semelhante aos executáveis do Linux nativos – piping, redirecionamentos e até mesmo o trabalho em segundo plano conforme o esperado.

Exemplo usando pipes:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Exemplo usando comandos mistos do Windows e do WSL:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Os binários do Windows devem incluir a extensão do arquivo, corresponder o caso do arquivo e ser executáveis.  Não executáveis, incluindo scripts do lote.  Comandos nativos do CMD, como `dir`, podem ser executados com o comando `cmd.exe /C`.

Exemplos:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Os parâmetros são passados para o binário do Windows não modificado.

Por exemplo, os seguintes comandos abrirão `C:\temp\foo.txt` no `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

A modificação de arquivos localizados em VolFs (arquivos que não estão em `/mnt/<x>`) com um aplicativo do Windows no WSL não é compatível.

Por padrão, o WSL tenta manter o diretório de trabalho do binário do Windows como o diretório do WSL atual, mas fará fallback no diretório de criação da instância se o diretório de trabalho estiver em VolFs.

Por exemplo, `wsl.exe` é inicialmente iniciado de `C:\temp` e o diretório do WSL atual é alterado para a página inicial do usuário.  Quando `notepad.exe` é chamado do diretório base do usuário, o WSL é revertido automaticamente para `C:\temp` como o diretório de trabalho do notepad.exe:

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>Compartilhar variáveis de ambiente entre o Windows e o WSL

> Disponível no Participante do Programa Windows Insider builds 17063 e posteriores.

Antes do 17063, a única variável de ambiente do Windows que o WSL podia acessar era `PATH` (portanto, era possível iniciar os executáveis do Win32 no WSL).

Começando no 17063, o WSL e o Windows compartilham o `WSLENV`, uma variável de ambiente especial criada para vincular distribuições do Windows e do Linux em execução no WSL.

Propriedades de `WSLENV`:

* Ele é compartilhado e existe em ambientes do Windows e do WSL.
* É uma lista de variáveis de ambiente a serem compartilhadas entre o Windows e o WSL.
* Pode formatar variáveis de ambiente para funcionamento no Windows e no WSL.

Há quatro sinalizadores disponíveis no `WSLENV` para influenciar como essa variável de ambiente é convertida.

`WSLENV` sinalizadores:

* `/p` – converte o caminho entre os caminhos do estilo WSL/Linux e os caminhos do Win32.
* `/l` – indica que a variável de ambiente é uma lista de caminhos.
* `/u` – indica que essa variável de ambiente só deve ser incluída ao executar o WSL usando o Win32.
* `/w` – indica que essa variável de ambiente só deve ser incluída ao executar o Win32 usando o WSL.

Os sinalizadores podem ser combinados conforme necessário.

## <a name="disable-interop"></a>Desabilitar interoperabilidade

Os usuários podem desabilitar a capacidade de executar binários do Windows para uma única sessão do WSL executando o seguinte comando como raiz:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Para reabilitar os binários do Windows, saia de todas as sessões do WSL e execute o bash.exe novamente ou execute o seguinte comando como raiz:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Desabilitar a interoperabilidade não persistirá entre as sessões do WSL – a interoperabilidade será habilitada novamente quando uma nova sessão for iniciada.

## <a name="creators-update-and-anniversary-update"></a>Atualização para Criadores e Atualização de Aniversário

Embora a experiência de interoperabilidade que a atualização anterior ao Falls Creator Update seja semelhante às experiências de interoperabilidade mais recentes, há algumas diferenças importantes.

Para resumir:

* `bash.exe` foi preterido e substituído por `wsl.exe`.
* A opção `-c` para executar um único comando não é necessária com o `wsl.exe`.
* O caminho do Windows está incluído no WSL `$PATH`

O processo para desabilitar a interoperabilidade não é alterado.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Como invocar o WSL da linha de comando do Windows

Os binários do Linux podem ser invocados no prompt de comando do Windows ou no PowerShell.  Os binários invocados dessa maneira têm as seguintes propriedades:

1. Use o mesmo diretório de trabalho que o prompt do CMD ou do PowerShell.
1. Execute como usuário padrão do WSL.
1. Tenha os mesmos direitos administrativos do Windows que o processo de chamada e o terminal.

Exemplo:

```console
C:\temp> bash -c "ls -la"
```

Os comandos do Linux chamados dessa maneira são tratados como qualquer outro aplicativo do Windows.  Coisas como inserção, piping e redirecionamento de arquivo funcionam.

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

Os comandos do WSL passados para `bash -c` são encaminhados para o processo do WSL sem modificação.  Os caminhos de arquivo devem ser especificados no formato do WSL e é necessário ter cuidado com os caracteres de escape relevantes. Exemplo:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Como invocar binários do Windows usando o WSL

O Subsistema Windows para Linux pode invocar os binários do Windows diretamente da linha de comando do WSL.  Os aplicativos executados dessa maneira têm as seguintes propriedades:

1. Mantenha o diretório de trabalho como o prompt de comando do WSL, exceto no cenário explicado abaixo.
1. Tenha os mesmos direitos de permissão que o processo `bash.exe`. 
1. Execute como usuário ativo do Windows.
1. É exibido no Gerenciador de Tarefas do Windows como se fosse executado diretamente no prompt do CMD.

Exemplo:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

No WSL, esses executáveis são tratados de forma semelhante aos executáveis do Linux nativos.  Isso significa que adicionar diretórios ao piping e ao caminho do Linux entre comandos funciona conforme o esperado.  Exemplos:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

O binário do Windows deve incluir a extensão do arquivo, corresponder o caso do arquivo e ser executável.  Os não executáveis, incluindo scripts do lote e comandos como `dir`, podem ser executados com o comando `/mnt/c/Windows/System32/cmd.exe /C`.

Exemplos:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Os parâmetros são passados para o binário do Windows não modificado.  

Por exemplo, os seguintes comandos abrirão `C:\temp\foo.txt` no `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

A modificação de arquivos localizados em VolFs (arquivos que não estão em `/mnt/<x>`) com um aplicativo do Windows não é compatível.  Por padrão, o WSL tenta manter o diretório de trabalho do binário do Windows como o diretório do WSL atual, mas fará fallback no diretório de criação da instância se o diretório de trabalho estiver em VolFs.

Por exemplo, `bash.exe` é inicialmente iniciado de `C:\temp` e o diretório do WSL atual é alterado para a página inicial do usuário.  Quando `notepad.exe` é chamado do diretório base do usuário, o WSL é revertido automaticamente para `C:\temp` como o diretório de trabalho do notepad.exe:

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
