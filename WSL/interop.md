---
title: Interoperabilidade do Windows com Linux
description: Descreve a interoperabilidade do Windows com distribuições do Linux em execução no subsistema do Windows para Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040821"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="2e97f-103">Subsistema do Windows para interoperabilidade do Linux com o Windows</span><span class="sxs-lookup"><span data-stu-id="2e97f-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="2e97f-104">**Atualizado para a atualização de criadores de outono.**</span><span class="sxs-lookup"><span data-stu-id="2e97f-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="2e97f-105">Se você estiver executando a atualização de criadores ou atualização de aniversário, vá para a [seção criadores/atualização de aniversário](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="2e97f-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="2e97f-106">O subsistema do Windows para Linux (WSL) está melhorando continuamente a integração entre o Windows e o Linux.</span><span class="sxs-lookup"><span data-stu-id="2e97f-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="2e97f-107">Você pode:</span><span class="sxs-lookup"><span data-stu-id="2e97f-107">You can:</span></span>

1. <span data-ttu-id="2e97f-108">Invoque os binários do Windows no console do Linux.</span><span class="sxs-lookup"><span data-stu-id="2e97f-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="2e97f-109">Invocar binários do Linux de um console do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e97f-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="2e97f-110">O **Windows insiders compila 17063 +** Compartilhe variáveis de ambiente entre o Linux e o Windows.</span><span class="sxs-lookup"><span data-stu-id="2e97f-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="2e97f-111">Isso proporciona uma experiência simples entre o Windows e o WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="2e97f-112">Os detalhes técnicos estão no [blog do WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="2e97f-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="2e97f-113">Executar ferramentas do Linux a partir de uma linha de comando do Windows</span><span class="sxs-lookup"><span data-stu-id="2e97f-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="2e97f-114">Execute binários do Linux no prompt de comando do Windows (CMD ou `wsl.exe <command>`PowerShell) usando o.</span><span class="sxs-lookup"><span data-stu-id="2e97f-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="2e97f-115">Binários invocados desta maneira:</span><span class="sxs-lookup"><span data-stu-id="2e97f-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="2e97f-116">Use o mesmo diretório de trabalho que o Prompt CMD ou PowerShell atual.</span><span class="sxs-lookup"><span data-stu-id="2e97f-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="2e97f-117">Execute como o usuário padrão WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="2e97f-118">Ter os mesmos direitos administrativos do Windows que o processo de chamada e o terminal.</span><span class="sxs-lookup"><span data-stu-id="2e97f-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="2e97f-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e97f-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="2e97f-120">O comando do Linux `wsl.exe` a seguir é tratado como qualquer comando executado no WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="2e97f-121">Coisas como sudo, tubulação e redirecionamento de arquivo funcionam.</span><span class="sxs-lookup"><span data-stu-id="2e97f-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="2e97f-122">Exemplo usando sudo:</span><span class="sxs-lookup"><span data-stu-id="2e97f-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="2e97f-123">Exemplos que misturam comandos WSL e do Windows:</span><span class="sxs-lookup"><span data-stu-id="2e97f-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="2e97f-124">Os comandos passados para `wsl.exe` são encaminhados para o processo WSL sem modificação.</span><span class="sxs-lookup"><span data-stu-id="2e97f-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="2e97f-125">Os caminhos de arquivo devem ser especificados no formato WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="2e97f-126">Exemplo com caminhos:</span><span class="sxs-lookup"><span data-stu-id="2e97f-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="2e97f-127">Executar ferramentas do Windows do WSL</span><span class="sxs-lookup"><span data-stu-id="2e97f-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="2e97f-128">WSL pode invocar binários do Windows diretamente da linha de `[binary name].exe`comando do WSL usando.</span><span class="sxs-lookup"><span data-stu-id="2e97f-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="2e97f-129">Por exemplo, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="2e97f-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="2e97f-130">Para facilitar a execução dos executáveis do Windows, o caminho do Windows está incluído `$PATH` na atualização do Linux no outono Creators.</span><span class="sxs-lookup"><span data-stu-id="2e97f-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="2e97f-131">Os aplicativos executados dessa maneira têm as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="2e97f-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="2e97f-132">Mantenha o diretório de trabalho como o prompt de comando WSL (na maior parte, as exceções são explicadas abaixo).</span><span class="sxs-lookup"><span data-stu-id="2e97f-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="2e97f-133">Ter os mesmos direitos de permissão que o processo WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="2e97f-134">Executar como usuário ativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e97f-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="2e97f-135">Aparece no Gerenciador de tarefas do Windows como se fosse executado diretamente no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="2e97f-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="2e97f-136">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e97f-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="2e97f-137">Os executáveis do Windows executados no WSL são tratados de forma semelhante aos executáveis do Linux nativos – tubulação, redirecionamentos e até mesmo o trabalho em segundo plano conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="2e97f-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="2e97f-138">Exemplos usando pipes:</span><span class="sxs-lookup"><span data-stu-id="2e97f-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="2e97f-139">Exemplo usando comandos mistos do Windows e do WSL:</span><span class="sxs-lookup"><span data-stu-id="2e97f-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="2e97f-140">Os binários do Windows devem incluir a extensão do arquivo, corresponder o caso do arquivo e ser executável.</span><span class="sxs-lookup"><span data-stu-id="2e97f-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="2e97f-141">Não executáveis, incluindo scripts do lote.</span><span class="sxs-lookup"><span data-stu-id="2e97f-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="2e97f-142">Comandos nativos cmd como `dir` o podem ser executados `cmd.exe /C` com o comando.</span><span class="sxs-lookup"><span data-stu-id="2e97f-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="2e97f-143">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="2e97f-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="2e97f-144">Os parâmetros são passados para o binário do Windows não modificado.</span><span class="sxs-lookup"><span data-stu-id="2e97f-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="2e97f-145">Por exemplo, os seguintes comandos serão abertos `C:\temp\foo.txt` no: `notepad.exe`</span><span class="sxs-lookup"><span data-stu-id="2e97f-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="2e97f-146">Não há suporte para a modificação de arquivos localizados `/mnt/<x>`em VolFs (arquivos que não estão em) com um aplicativo do Windows em WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="2e97f-147">Por padrão, o WSL tenta manter o diretório de trabalho do binário do Windows como o diretório WSL atual, mas fará fallback no diretório de criação da instância se o diretório de trabalho estiver em VolFs.</span><span class="sxs-lookup"><span data-stu-id="2e97f-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="2e97f-148">Como exemplo; é inicialmente iniciado a `C:\temp` partir do e o diretório WSL atual é alterado para a página inicial do usuário. `wsl.exe`</span><span class="sxs-lookup"><span data-stu-id="2e97f-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="2e97f-149">Quando `notepad.exe` é chamado do diretório inicial do usuário, o WSL é revertido automaticamente para `C:\temp` como o diretório de trabalho do Notepad. exe:</span><span class="sxs-lookup"><span data-stu-id="2e97f-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="2e97f-150">Compartilhar variáveis de ambiente entre o Windows e o WSL</span><span class="sxs-lookup"><span data-stu-id="2e97f-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="2e97f-151">Disponível no Windows Insider Builds 17063 e posterior.</span><span class="sxs-lookup"><span data-stu-id="2e97f-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="2e97f-152">Antes de 17063, somente a variável de ambiente do Windows que WSL `PATH` poderia acessar era (portanto, você poderia iniciar os executáveis do Win32 em WSL).</span><span class="sxs-lookup"><span data-stu-id="2e97f-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="2e97f-153">A partir do 17063, WSL e Windows `WSLENV`share, uma variável de ambiente especial criada para a ponte de distribuições Windows e Linux em execução no WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="2e97f-154">Propriedades de `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="2e97f-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="2e97f-155">Ele é compartilhado; Ele existe em ambientes Windows e WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="2e97f-156">É uma lista de variáveis de ambiente a serem compartilhadas entre o Windows e o WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="2e97f-157">Ele pode formatar variáveis de ambiente para funcionar bem no Windows e no WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="2e97f-158">Há quatro sinalizadores disponíveis no `WSLENV` para influenciar como essa variável de ambiente é traduzida.</span><span class="sxs-lookup"><span data-stu-id="2e97f-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="2e97f-159">`WSLENV`flags</span><span class="sxs-lookup"><span data-stu-id="2e97f-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="2e97f-160">`/p`– Converte o caminho entre os caminhos do estilo WSL/Linux e os caminhos do Win32.</span><span class="sxs-lookup"><span data-stu-id="2e97f-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="2e97f-161">`/l`-indica que a variável de ambiente é uma lista de caminhos.</span><span class="sxs-lookup"><span data-stu-id="2e97f-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="2e97f-162">`/u`-indica que essa variável de ambiente só deve ser incluída ao executar WSL do Win32.</span><span class="sxs-lookup"><span data-stu-id="2e97f-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="2e97f-163">`/w`-indica que essa variável de ambiente só deve ser incluída ao executar o Win32 em WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="2e97f-164">Os sinalizadores podem ser combinados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="2e97f-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="2e97f-165">Desabilitar interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="2e97f-165">Disable Interop</span></span>

<span data-ttu-id="2e97f-166">Os usuários podem desabilitar a capacidade de executar binários do Windows para uma única sessão WSL executando o seguinte comando como raiz:</span><span class="sxs-lookup"><span data-stu-id="2e97f-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="2e97f-167">Para reabilitar os binários do Windows, saia de todas as sessões WSL e execute o bash. exe novamente ou execute o seguinte comando como raiz:</span><span class="sxs-lookup"><span data-stu-id="2e97f-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="2e97f-168">Desabilitar a interoperabilidade não persiste entre as sessões WSL--a interoperabilidade será habilitada novamente quando uma nova sessão for iniciada.</span><span class="sxs-lookup"><span data-stu-id="2e97f-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="2e97f-169">Atualização de aniversários e atualização para criadores</span><span class="sxs-lookup"><span data-stu-id="2e97f-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="2e97f-170">Embora a experiência de interoperabilidade que o criadores de pré-Outono atualize seja semelhante às experiências de interoperabilidade mais recentes, há algumas diferenças importantes.</span><span class="sxs-lookup"><span data-stu-id="2e97f-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="2e97f-171">Para resumir:</span><span class="sxs-lookup"><span data-stu-id="2e97f-171">To summarize:</span></span>

* <span data-ttu-id="2e97f-172">`bash.exe`foi preterido e substituído por `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="2e97f-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="2e97f-173">`-c`a opção para executar um único comando não é `wsl.exe`necessária com.</span><span class="sxs-lookup"><span data-stu-id="2e97f-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="2e97f-174">O caminho do Windows está incluído no WSL`$PATH`</span><span class="sxs-lookup"><span data-stu-id="2e97f-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="2e97f-175">O processo para desabilitar a interoperabilidade não é alterado.</span><span class="sxs-lookup"><span data-stu-id="2e97f-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="2e97f-176">Invocando WSL da linha de comando do Windows</span><span class="sxs-lookup"><span data-stu-id="2e97f-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="2e97f-177">Os binários do Linux podem ser invocados no prompt de comando do Windows ou no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e97f-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="2e97f-178">Os binários invocados dessa forma têm as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="2e97f-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="2e97f-179">Use o mesmo diretório de trabalho que o prompt do CMD ou do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e97f-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="2e97f-180">Execute como o usuário padrão WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="2e97f-181">Ter os mesmos direitos administrativos do Windows que o processo de chamada e o terminal.</span><span class="sxs-lookup"><span data-stu-id="2e97f-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="2e97f-182">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e97f-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="2e97f-183">Os comandos do Linux chamados dessa maneira são tratados como qualquer outro aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e97f-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="2e97f-184">Coisas como entrada, tubulação e redirecionamento de arquivo funcionam conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="2e97f-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="2e97f-185">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="2e97f-185">Examples:</span></span>

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

<span data-ttu-id="2e97f-186">Os comandos WSL passados `bash -c` para o são encaminhados para o processo WSL sem modificação.</span><span class="sxs-lookup"><span data-stu-id="2e97f-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="2e97f-187">Os caminhos de arquivo devem ser especificados no formato WSL e devem ser levados em atenção para escapar os caracteres relevantes.</span><span class="sxs-lookup"><span data-stu-id="2e97f-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="2e97f-188">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e97f-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="2e97f-189">Invocando binários do Windows do WSL</span><span class="sxs-lookup"><span data-stu-id="2e97f-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="2e97f-190">O subsistema do Windows para Linux pode invocar binários do Windows diretamente da linha de comando WSL.</span><span class="sxs-lookup"><span data-stu-id="2e97f-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="2e97f-191">Os aplicativos executados dessa maneira têm as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="2e97f-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="2e97f-192">Mantenha o diretório de trabalho como o prompt de comando WSL, exceto no cenário explicado abaixo.</span><span class="sxs-lookup"><span data-stu-id="2e97f-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="2e97f-193">Ter os mesmos direitos de permissão que `bash.exe` o processo.</span><span class="sxs-lookup"><span data-stu-id="2e97f-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="2e97f-194">Executar como usuário ativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e97f-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="2e97f-195">Aparece no Gerenciador de tarefas do Windows como se fosse executado diretamente no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="2e97f-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="2e97f-196">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="2e97f-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="2e97f-197">No WSL, esses executáveis são tratados de forma semelhante aos executáveis do Linux nativo.</span><span class="sxs-lookup"><span data-stu-id="2e97f-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="2e97f-198">Isso significa que adicionar diretórios ao caminho do Linux e o pipe entre comandos funciona conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="2e97f-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="2e97f-199">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="2e97f-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="2e97f-200">O binário do Windows deve incluir a extensão do arquivo, corresponder ao caso do arquivo e ser executável.</span><span class="sxs-lookup"><span data-stu-id="2e97f-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="2e97f-201">Os não executáveis, incluindo scripts do lote e `dir` comandos like podem ser `/mnt/c/Windows/System32/cmd.exe /C` executados com o comando.</span><span class="sxs-lookup"><span data-stu-id="2e97f-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="2e97f-202">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="2e97f-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="2e97f-203">Os parâmetros são passados para o binário do Windows não modificado.</span><span class="sxs-lookup"><span data-stu-id="2e97f-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="2e97f-204">Por exemplo, os seguintes comandos serão abertos `C:\temp\foo.txt` no: `notepad.exe`</span><span class="sxs-lookup"><span data-stu-id="2e97f-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="2e97f-205">Não há suporte para a modificação de arquivos localizados `/mnt/<x>`em VolFs (arquivos que não estão em) com um aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="2e97f-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="2e97f-206">Por padrão, o WSL tenta manter o diretório de trabalho do binário do Windows como o diretório WSL atual, mas fará fallback no diretório de criação da instância se o diretório de trabalho estiver em VolFs.</span><span class="sxs-lookup"><span data-stu-id="2e97f-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="2e97f-207">Como exemplo; é inicialmente iniciado a `C:\temp` partir do e o diretório WSL atual é alterado para a página inicial do usuário. `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="2e97f-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="2e97f-208">Quando `notepad.exe` é chamado do diretório inicial do usuário, o WSL é revertido automaticamente para `C:\temp` como o diretório de trabalho do Notepad. exe:</span><span class="sxs-lookup"><span data-stu-id="2e97f-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
