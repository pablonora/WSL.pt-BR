---
title: Interoperabilidade do Windows com o Linux
description: Descreve a interoperabilidade do Windows com distribuições do Linux em execução no Subsistema Windows para Linux.
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: f8b0150c044f5011b84e80cac4befd752c4dc552
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "71269800"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="46ccf-103">Subsistema Windows para interoperabilidade do Linux com o Windows</span><span class="sxs-lookup"><span data-stu-id="46ccf-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="46ccf-104">**Atualização do Fall Creators Update.**</span><span class="sxs-lookup"><span data-stu-id="46ccf-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="46ccf-105">Se você estiver executando a Atualização para Criadores ou a Atualização de Aniversário, vá para a [seção Atualização de Aniversário/Atualização para Criadores](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="46ccf-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="46ccf-106">O WSL (Subsistema Windows para Linux) está melhorando continuamente a integração entre o Windows e o Linux.</span><span class="sxs-lookup"><span data-stu-id="46ccf-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="46ccf-107">Você pode:</span><span class="sxs-lookup"><span data-stu-id="46ccf-107">You can:</span></span>

1. <span data-ttu-id="46ccf-108">Invocar os binários do Windows no console do Linux.</span><span class="sxs-lookup"><span data-stu-id="46ccf-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="46ccf-109">Invocar os binários do Linux no console do Windows.</span><span class="sxs-lookup"><span data-stu-id="46ccf-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="46ccf-110">**Windows Insiders Builds 17063 e posteriores** Compartilhar variáveis de ambiente entre o Linux e o Windows.</span><span class="sxs-lookup"><span data-stu-id="46ccf-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="46ccf-111">Isso proporciona uma experiência simples entre o Windows e o WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="46ccf-112">Os detalhes técnicos estão no [blog do WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="46ccf-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="46ccf-113">Execute ferramentas do Linux usando uma linha de comando do Windows</span><span class="sxs-lookup"><span data-stu-id="46ccf-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="46ccf-114">Execute binários do Linux no prompt de comando do Windows (CMD ou PowerShell) usando o `wsl.exe <command>`.</span><span class="sxs-lookup"><span data-stu-id="46ccf-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="46ccf-115">Binários invocados desta maneira:</span><span class="sxs-lookup"><span data-stu-id="46ccf-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="46ccf-116">Use o mesmo diretório de trabalho que o prompt do CMD ou do PowerShell atual.</span><span class="sxs-lookup"><span data-stu-id="46ccf-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="46ccf-117">Execute como usuário padrão do WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="46ccf-118">Tenha os mesmos direitos administrativos do Windows que o processo de chamada e o terminal.</span><span class="sxs-lookup"><span data-stu-id="46ccf-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="46ccf-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="46ccf-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="46ccf-120">O comando do Linux após `wsl.exe` é tratado como qualquer comando executado no WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="46ccf-121">Coisas como sudo, piping e redirecionamento de arquivo funcionam.</span><span class="sxs-lookup"><span data-stu-id="46ccf-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="46ccf-122">Exemplo usando o sudo:</span><span class="sxs-lookup"><span data-stu-id="46ccf-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="46ccf-123">Exemplos que misturam comandos do WSL e do Windows:</span><span class="sxs-lookup"><span data-stu-id="46ccf-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="46ccf-124">Os comandos passados para `wsl.exe` são encaminhados para o processo do WSL sem modificação.</span><span class="sxs-lookup"><span data-stu-id="46ccf-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="46ccf-125">Os caminhos de arquivo devem ser especificados no formato do WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="46ccf-126">Exemplo com caminhos:</span><span class="sxs-lookup"><span data-stu-id="46ccf-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="46ccf-127">Executar ferramentas do Windows usando o WSL</span><span class="sxs-lookup"><span data-stu-id="46ccf-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="46ccf-128">O WSL pode invocar os binários do Windows diretamente da linha de comando do WSL usando `[binary name].exe`.</span><span class="sxs-lookup"><span data-stu-id="46ccf-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="46ccf-129">Por exemplo, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="46ccf-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="46ccf-130">Para facilitar a execução dos executáveis do Windows, o caminho do Windows está incluído no Linux `$PATH` no Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="46ccf-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="46ccf-131">Os aplicativos executados dessa maneira têm as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="46ccf-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="46ccf-132">Mantenha o diretório de trabalho como o prompt de comando do WSL (em grande parte – as exceções são explicadas abaixo).</span><span class="sxs-lookup"><span data-stu-id="46ccf-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="46ccf-133">Tenha os mesmos direitos de permissão que o processo do WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="46ccf-134">Execute como usuário ativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="46ccf-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="46ccf-135">É exibido no Gerenciador de Tarefas do Windows como se fosse executado diretamente no prompt do CMD.</span><span class="sxs-lookup"><span data-stu-id="46ccf-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="46ccf-136">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="46ccf-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="46ccf-137">Os executáveis do Windows executados no WSL são tratados de forma semelhante aos executáveis do Linux nativos – piping, redirecionamentos e até mesmo o trabalho em segundo plano conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="46ccf-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="46ccf-138">Exemplo usando pipes:</span><span class="sxs-lookup"><span data-stu-id="46ccf-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="46ccf-139">Exemplo usando comandos mistos do Windows e do WSL:</span><span class="sxs-lookup"><span data-stu-id="46ccf-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="46ccf-140">Os binários do Windows devem incluir a extensão do arquivo, corresponder o caso do arquivo e ser executáveis.</span><span class="sxs-lookup"><span data-stu-id="46ccf-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="46ccf-141">Não executáveis, incluindo scripts do lote.</span><span class="sxs-lookup"><span data-stu-id="46ccf-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="46ccf-142">Comandos nativos do CMD, como `dir`, podem ser executados com o comando `cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="46ccf-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="46ccf-143">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="46ccf-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="46ccf-144">Os parâmetros são passados para o binário do Windows não modificado.</span><span class="sxs-lookup"><span data-stu-id="46ccf-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="46ccf-145">Por exemplo, os seguintes comandos abrirão `C:\temp\foo.txt` no `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="46ccf-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="46ccf-146">A modificação de arquivos localizados em VolFs (arquivos que não estão em `/mnt/<x>`) com um aplicativo do Windows no WSL não é compatível.</span><span class="sxs-lookup"><span data-stu-id="46ccf-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="46ccf-147">Por padrão, o WSL tenta manter o diretório de trabalho do binário do Windows como o diretório do WSL atual, mas fará fallback no diretório de criação da instância se o diretório de trabalho estiver em VolFs.</span><span class="sxs-lookup"><span data-stu-id="46ccf-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="46ccf-148">Por exemplo, `wsl.exe` é inicialmente iniciado de `C:\temp` e o diretório do WSL atual é alterado para a página inicial do usuário.</span><span class="sxs-lookup"><span data-stu-id="46ccf-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="46ccf-149">Quando `notepad.exe` é chamado do diretório base do usuário, o WSL é revertido automaticamente para `C:\temp` como o diretório de trabalho do notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="46ccf-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="46ccf-150">Compartilhar variáveis de ambiente entre o Windows e o WSL</span><span class="sxs-lookup"><span data-stu-id="46ccf-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="46ccf-151">Disponível no Participante do Programa Windows Insider builds 17063 e posteriores.</span><span class="sxs-lookup"><span data-stu-id="46ccf-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="46ccf-152">Antes do 17063, a única variável de ambiente do Windows que o WSL podia acessar era `PATH` (portanto, era possível iniciar os executáveis do Win32 no WSL).</span><span class="sxs-lookup"><span data-stu-id="46ccf-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="46ccf-153">Começando no 17063, o WSL e o Windows compartilham o `WSLENV`, uma variável de ambiente especial criada para vincular distribuições do Windows e do Linux em execução no WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="46ccf-154">Propriedades de `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="46ccf-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="46ccf-155">Ele é compartilhado e existe em ambientes do Windows e do WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="46ccf-156">É uma lista de variáveis de ambiente a serem compartilhadas entre o Windows e o WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="46ccf-157">Pode formatar variáveis de ambiente para funcionamento no Windows e no WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="46ccf-158">Há quatro sinalizadores disponíveis no `WSLENV` para influenciar como essa variável de ambiente é convertida.</span><span class="sxs-lookup"><span data-stu-id="46ccf-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="46ccf-159">`WSLENV` sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="46ccf-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="46ccf-160">`/p` – converte o caminho entre os caminhos do estilo WSL/Linux e os caminhos do Win32.</span><span class="sxs-lookup"><span data-stu-id="46ccf-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="46ccf-161">`/l` – indica que a variável de ambiente é uma lista de caminhos.</span><span class="sxs-lookup"><span data-stu-id="46ccf-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="46ccf-162">`/u` – indica que essa variável de ambiente só deve ser incluída ao executar o WSL usando o Win32.</span><span class="sxs-lookup"><span data-stu-id="46ccf-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="46ccf-163">`/w` – indica que essa variável de ambiente só deve ser incluída ao executar o Win32 usando o WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="46ccf-164">Os sinalizadores podem ser combinados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="46ccf-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="46ccf-165">Desabilitar interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="46ccf-165">Disable Interop</span></span>

<span data-ttu-id="46ccf-166">Os usuários podem desabilitar a capacidade de executar binários do Windows para uma única sessão do WSL executando o seguinte comando como raiz:</span><span class="sxs-lookup"><span data-stu-id="46ccf-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="46ccf-167">Para reabilitar os binários do Windows, saia de todas as sessões do WSL e execute o bash.exe novamente ou execute o seguinte comando como raiz:</span><span class="sxs-lookup"><span data-stu-id="46ccf-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="46ccf-168">Desabilitar a interoperabilidade não persistirá entre as sessões do WSL – a interoperabilidade será habilitada novamente quando uma nova sessão for iniciada.</span><span class="sxs-lookup"><span data-stu-id="46ccf-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="46ccf-169">Atualização para Criadores e Atualização de Aniversário</span><span class="sxs-lookup"><span data-stu-id="46ccf-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="46ccf-170">Embora a experiência de interoperabilidade que a atualização anterior ao Falls Creator Update seja semelhante às experiências de interoperabilidade mais recentes, há algumas diferenças importantes.</span><span class="sxs-lookup"><span data-stu-id="46ccf-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="46ccf-171">Para resumir:</span><span class="sxs-lookup"><span data-stu-id="46ccf-171">To summarize:</span></span>

* <span data-ttu-id="46ccf-172">`bash.exe` foi preterido e substituído por `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="46ccf-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="46ccf-173">A opção `-c` para executar um único comando não é necessária com o `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="46ccf-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="46ccf-174">O caminho do Windows está incluído no WSL `$PATH`</span><span class="sxs-lookup"><span data-stu-id="46ccf-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="46ccf-175">O processo para desabilitar a interoperabilidade não é alterado.</span><span class="sxs-lookup"><span data-stu-id="46ccf-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="46ccf-176">Como invocar o WSL da linha de comando do Windows</span><span class="sxs-lookup"><span data-stu-id="46ccf-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="46ccf-177">Os binários do Linux podem ser invocados no prompt de comando do Windows ou no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46ccf-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="46ccf-178">Os binários invocados dessa maneira têm as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="46ccf-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="46ccf-179">Use o mesmo diretório de trabalho que o prompt do CMD ou do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46ccf-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="46ccf-180">Execute como usuário padrão do WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="46ccf-181">Tenha os mesmos direitos administrativos do Windows que o processo de chamada e o terminal.</span><span class="sxs-lookup"><span data-stu-id="46ccf-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="46ccf-182">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="46ccf-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="46ccf-183">Os comandos do Linux chamados dessa maneira são tratados como qualquer outro aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="46ccf-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="46ccf-184">Coisas como inserção, piping e redirecionamento de arquivo funcionam.</span><span class="sxs-lookup"><span data-stu-id="46ccf-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="46ccf-185">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="46ccf-185">Examples:</span></span>

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

<span data-ttu-id="46ccf-186">Os comandos do WSL passados para `bash -c` são encaminhados para o processo do WSL sem modificação.</span><span class="sxs-lookup"><span data-stu-id="46ccf-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="46ccf-187">Os caminhos de arquivo devem ser especificados no formato do WSL e é necessário ter cuidado com os caracteres de escape relevantes.</span><span class="sxs-lookup"><span data-stu-id="46ccf-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="46ccf-188">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="46ccf-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="46ccf-189">Como invocar binários do Windows usando o WSL</span><span class="sxs-lookup"><span data-stu-id="46ccf-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="46ccf-190">O Subsistema Windows para Linux pode invocar os binários do Windows diretamente da linha de comando do WSL.</span><span class="sxs-lookup"><span data-stu-id="46ccf-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="46ccf-191">Os aplicativos executados dessa maneira têm as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="46ccf-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="46ccf-192">Mantenha o diretório de trabalho como o prompt de comando do WSL, exceto no cenário explicado abaixo.</span><span class="sxs-lookup"><span data-stu-id="46ccf-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="46ccf-193">Tenha os mesmos direitos de permissão que o processo `bash.exe`.</span><span class="sxs-lookup"><span data-stu-id="46ccf-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="46ccf-194">Execute como usuário ativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="46ccf-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="46ccf-195">É exibido no Gerenciador de Tarefas do Windows como se fosse executado diretamente no prompt do CMD.</span><span class="sxs-lookup"><span data-stu-id="46ccf-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="46ccf-196">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="46ccf-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="46ccf-197">No WSL, esses executáveis são tratados de forma semelhante aos executáveis do Linux nativos.</span><span class="sxs-lookup"><span data-stu-id="46ccf-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="46ccf-198">Isso significa que adicionar diretórios ao piping e ao caminho do Linux entre comandos funciona conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="46ccf-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="46ccf-199">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="46ccf-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="46ccf-200">O binário do Windows deve incluir a extensão do arquivo, corresponder o caso do arquivo e ser executável.</span><span class="sxs-lookup"><span data-stu-id="46ccf-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="46ccf-201">Os não executáveis, incluindo scripts do lote e comandos como `dir`, podem ser executados com o comando `/mnt/c/Windows/System32/cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="46ccf-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="46ccf-202">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="46ccf-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="46ccf-203">Os parâmetros são passados para o binário do Windows não modificado.</span><span class="sxs-lookup"><span data-stu-id="46ccf-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="46ccf-204">Por exemplo, os seguintes comandos abrirão `C:\temp\foo.txt` no `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="46ccf-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="46ccf-205">A modificação de arquivos localizados em VolFs (arquivos que não estão em `/mnt/<x>`) com um aplicativo do Windows não é compatível.</span><span class="sxs-lookup"><span data-stu-id="46ccf-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="46ccf-206">Por padrão, o WSL tenta manter o diretório de trabalho do binário do Windows como o diretório do WSL atual, mas fará fallback no diretório de criação da instância se o diretório de trabalho estiver em VolFs.</span><span class="sxs-lookup"><span data-stu-id="46ccf-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="46ccf-207">Por exemplo, `bash.exe` é inicialmente iniciado de `C:\temp` e o diretório do WSL atual é alterado para a página inicial do usuário.</span><span class="sxs-lookup"><span data-stu-id="46ccf-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="46ccf-208">Quando `notepad.exe` é chamado do diretório base do usuário, o WSL é revertido automaticamente para `C:\temp` como o diretório de trabalho do notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="46ccf-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
