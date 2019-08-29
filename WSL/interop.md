---
title: Interoperabilidade do Windows com Linux
description: Descreve a interoperabilidade do Windows com distribuições do Linux em execução no subsistema do Windows para Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122728"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Subsistema do Windows para interoperabilidade do Linux com o Windows

> **Atualizado para a atualização de criadores de outono.**  
Se você estiver executando a atualização de criadores ou atualização de aniversário, vá para a [seção criadores/atualização de aniversário](interop.md#creators-update-and-anniversary-update).

O subsistema do Windows para Linux (WSL) está melhorando continuamente a integração entre o Windows e o Linux.  Você pode:

1. Invoque os binários do Windows no console do Linux.
1. Invocar binários do Linux de um console do Windows.
1. O **Windows insiders compila 17063 +** Compartilhe variáveis de ambiente entre o Linux e o Windows.

Isso proporciona uma experiência simples entre o Windows e o WSL.  Os detalhes técnicos estão no [blog do WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Executar ferramentas do Linux a partir de uma linha de comando do Windows

Execute binários do Linux no prompt de comando do Windows (CMD ou `wsl.exe <command>`PowerShell) usando o.

Binários invocados desta maneira:

1. Use o mesmo diretório de trabalho que o Prompt CMD ou PowerShell atual.
1. Execute como o usuário padrão WSL.
1. Ter os mesmos direitos administrativos do Windows que o processo de chamada e o terminal.

Por exemplo:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

O comando do Linux `wsl.exe` a seguir é tratado como qualquer comando executado no WSL.  Coisas como sudo, tubulação e redirecionamento de arquivo funcionam.

Exemplo usando sudo:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Exemplos que misturam comandos WSL e do Windows:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Os comandos passados para `wsl.exe` são encaminhados para o processo WSL sem modificação.  Os caminhos de arquivo devem ser especificados no formato WSL.

Exemplo com caminhos:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Executar ferramentas do Windows do WSL

WSL pode invocar binários do Windows diretamente da linha de `[binary name].exe`comando do WSL usando.  Por exemplo, `notepad.exe`.  Para facilitar a execução dos executáveis do Windows, o caminho do Windows está incluído `$PATH` na atualização do Linux no outono Creators.

Os aplicativos executados dessa maneira têm as seguintes propriedades:

1. Mantenha o diretório de trabalho como o prompt de comando WSL (na maior parte, as exceções são explicadas abaixo).
1. Ter os mesmos direitos de permissão que o processo WSL.
1. Executar como usuário ativo do Windows.
1. Aparece no Gerenciador de tarefas do Windows como se fosse executado diretamente no prompt de comando.

Exemplo:

``` BASH
$ notepad.exe
```

Os executáveis do Windows executados no WSL são tratados de forma semelhante aos executáveis do Linux nativos – tubulação, redirecionamentos e até mesmo o trabalho em segundo plano conforme o esperado.

Exemplos usando pipes:

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

Os binários do Windows devem incluir a extensão do arquivo, corresponder o caso do arquivo e ser executável.  Não executáveis, incluindo scripts do lote.  Comandos nativos cmd como `dir` o podem ser executados `cmd.exe /C` com o comando.

Exemplos:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Os parâmetros são passados para o binário do Windows não modificado.

Por exemplo, os seguintes comandos serão abertos `C:\temp\foo.txt` no: `notepad.exe`

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Não há suporte para a modificação de arquivos localizados `/mnt/<x>`em VolFs (arquivos que não estão em) com um aplicativo do Windows em WSL.

Por padrão, o WSL tenta manter o diretório de trabalho do binário do Windows como o diretório WSL atual, mas fará fallback no diretório de criação da instância se o diretório de trabalho estiver em VolFs.

Como exemplo; é inicialmente iniciado a `C:\temp` partir do e o diretório WSL atual é alterado para a página inicial do usuário. `wsl.exe`  Quando `notepad.exe` é chamado do diretório inicial do usuário, o WSL é revertido automaticamente para `C:\temp` como o diretório de trabalho do Notepad. exe:

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

> Disponível no Windows Insider Builds 17063 e posterior.

Antes de 17063, somente a variável de ambiente do Windows que WSL `PATH` poderia acessar era (portanto, você poderia iniciar os executáveis do Win32 em WSL).

A partir do 17063, WSL e Windows `WSLENV`share, uma variável de ambiente especial criada para a ponte de distribuições Windows e Linux em execução no WSL.

Propriedades de `WSLENV`:

* Ele é compartilhado; Ele existe em ambientes Windows e WSL.
* É uma lista de variáveis de ambiente a serem compartilhadas entre o Windows e o WSL.
* Ele pode formatar variáveis de ambiente para funcionar bem no Windows e no WSL.

Há quatro sinalizadores disponíveis no `WSLENV` para influenciar como essa variável de ambiente é traduzida.

`WSLENV`flags

* `/p`– Converte o caminho entre os caminhos do estilo WSL/Linux e os caminhos do Win32.
* `/l`-indica que a variável de ambiente é uma lista de caminhos.
* `/u`-indica que essa variável de ambiente só deve ser incluída ao executar WSL do Win32.
* `/w`-indica que essa variável de ambiente só deve ser incluída ao executar o Win32 em WSL.

Os sinalizadores podem ser combinados conforme necessário.

## <a name="disable-interop"></a>Desabilitar interoperabilidade

Os usuários podem desabilitar a capacidade de executar binários do Windows para uma única sessão WSL executando o seguinte comando como raiz:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Para reabilitar os binários do Windows, saia de todas as sessões WSL e execute o bash. exe novamente ou execute o seguinte comando como raiz:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Desabilitar a interoperabilidade não persiste entre as sessões WSL--a interoperabilidade será habilitada novamente quando uma nova sessão for iniciada.

## <a name="creators-update-and-anniversary-update"></a>Atualização de aniversários e atualização para criadores

Embora a experiência de interoperabilidade que o criadores de pré-Outono atualize seja semelhante às experiências de interoperabilidade mais recentes, há algumas diferenças importantes.

Para resumir:

* `bash.exe`foi preterido e substituído por `wsl.exe`.
* `-c`a opção para executar um único comando não é `wsl.exe`necessária com.
* O caminho do Windows está incluído no WSL`$PATH`

O processo para desabilitar a interoperabilidade não é alterado.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Invocando WSL da linha de comando do Windows

Os binários do Linux podem ser invocados no prompt de comando do Windows ou no PowerShell.  Os binários invocados dessa forma têm as seguintes propriedades:

1. Use o mesmo diretório de trabalho que o prompt do CMD ou do PowerShell.
1. Execute como o usuário padrão WSL.
1. Ter os mesmos direitos administrativos do Windows que o processo de chamada e o terminal.

Exemplo:

```console
C:\temp> bash -c "ls -la"
```

Os comandos do Linux chamados dessa maneira são tratados como qualquer outro aplicativo do Windows.  Coisas como entrada, tubulação e redirecionamento de arquivo funcionam conforme o esperado.

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

Os comandos WSL passados `bash -c` para o são encaminhados para o processo WSL sem modificação.  Os caminhos de arquivo devem ser especificados no formato WSL e devem ser levados em atenção para escapar os caracteres relevantes. Exemplo:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Invocando binários do Windows do WSL

O subsistema do Windows para Linux pode invocar binários do Windows diretamente da linha de comando WSL.  Os aplicativos executados dessa maneira têm as seguintes propriedades:

1. Mantenha o diretório de trabalho como o prompt de comando WSL, exceto no cenário explicado abaixo.
1. Ter os mesmos direitos de permissão que `bash.exe` o processo. 
1. Executar como usuário ativo do Windows.
1. Aparece no Gerenciador de tarefas do Windows como se fosse executado diretamente no prompt de comando.

Exemplo:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

No WSL, esses executáveis são tratados de forma semelhante aos executáveis do Linux nativo.  Isso significa que adicionar diretórios ao caminho do Linux e o pipe entre comandos funciona conforme o esperado.  Exemplos:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

O binário do Windows deve incluir a extensão do arquivo, corresponder ao caso do arquivo e ser executável.  Os não executáveis, incluindo scripts do lote e `dir` comandos like podem ser `/mnt/c/Windows/System32/cmd.exe /C` executados com o comando.

Exemplos:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Os parâmetros são passados para o binário do Windows não modificado.  

Por exemplo, os seguintes comandos serão abertos `C:\temp\foo.txt` no: `notepad.exe`

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Não há suporte para a modificação de arquivos localizados `/mnt/<x>`em VolFs (arquivos que não estão em) com um aplicativo do Windows.  Por padrão, o WSL tenta manter o diretório de trabalho do binário do Windows como o diretório WSL atual, mas fará fallback no diretório de criação da instância se o diretório de trabalho estiver em VolFs.

Como exemplo; é inicialmente iniciado a `C:\temp` partir do e o diretório WSL atual é alterado para a página inicial do usuário. `bash.exe`  Quando `notepad.exe` é chamado do diretório inicial do usuário, o WSL é revertido automaticamente para `C:\temp` como o diretório de trabalho do Notepad. exe:

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
