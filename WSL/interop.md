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
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="1f67f-103">Subsistema do Windows para interoperabilidade do Linux com o Windows</span><span class="sxs-lookup"><span data-stu-id="1f67f-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="1f67f-104">**Atualizado para o Fall Creators Update.**</span><span class="sxs-lookup"><span data-stu-id="1f67f-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="1f67f-105">Se você estiver executando a atualização para criadores ou atualização de aniversário, vá para o [seção de atualização de criadores/aniversário](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="1f67f-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="1f67f-106">O subsistema Windows para Linux (WSL) está continuamente aprimorando a integração entre o Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="1f67f-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="1f67f-107">Você pode:</span><span class="sxs-lookup"><span data-stu-id="1f67f-107">You can:</span></span>

1. <span data-ttu-id="1f67f-108">Invocar os binários do Windows no console do Linux.</span><span class="sxs-lookup"><span data-stu-id="1f67f-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="1f67f-109">Invocar os binários do Linux em um console do Windows.</span><span class="sxs-lookup"><span data-stu-id="1f67f-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="1f67f-110">**Compilações do Windows Insiders 17063 +** compartilham variáveis de ambiente entre o Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="1f67f-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="1f67f-111">Isso fornece uma experiência perfeita entre o Windows e o WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="1f67f-112">Detalhes técnicos são sobre o [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="1f67f-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="1f67f-113">Executar ferramentas do Linux em uma linha de comando do Windows</span><span class="sxs-lookup"><span data-stu-id="1f67f-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="1f67f-114">Executar binários de Linux do usando Prompt de comando do Windows (CMD ou PowerShell) `wsl.exe <command>`.</span><span class="sxs-lookup"><span data-stu-id="1f67f-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="1f67f-115">Binários invocados desta forma:</span><span class="sxs-lookup"><span data-stu-id="1f67f-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="1f67f-116">Use o mesmo diretório de trabalho como o atual prompt CMD ou o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1f67f-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="1f67f-117">Execute como usuário padrão WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="1f67f-118">Ter os mesmos direitos administrativos do Windows como o processo de chamada e o terminal.</span><span class="sxs-lookup"><span data-stu-id="1f67f-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="1f67f-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1f67f-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="1f67f-120">O seguinte comando de Linux `wsl.exe` é tratado como qualquer comando executado no WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="1f67f-121">As coisas como sudo, tubulação e redirecionamento de arquivo funcionam.</span><span class="sxs-lookup"><span data-stu-id="1f67f-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="1f67f-122">Exemplo usando o sudo:</span><span class="sxs-lookup"><span data-stu-id="1f67f-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="1f67f-123">Exemplos de combinação de comandos WSL e Windows:</span><span class="sxs-lookup"><span data-stu-id="1f67f-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="1f67f-124">Os comandos são passados para `wsl.exe` são encaminhadas para o processo WSL sem modificação.</span><span class="sxs-lookup"><span data-stu-id="1f67f-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="1f67f-125">Caminhos de arquivo devem ser especificados no formato WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="1f67f-126">Exemplo com caminhos:</span><span class="sxs-lookup"><span data-stu-id="1f67f-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="1f67f-127">Executar ferramentas do Windows de WSL</span><span class="sxs-lookup"><span data-stu-id="1f67f-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="1f67f-128">WSL pode invocar os binários do Windows diretamente na linha de comando de WSL usando `[binary name].exe`.</span><span class="sxs-lookup"><span data-stu-id="1f67f-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="1f67f-129">Por exemplo, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="1f67f-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="1f67f-130">Para facilitar a execução de executáveis do Windows, o caminho do Windows está incluído no Linux `$PATH` no Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="1f67f-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="1f67f-131">Aplicativos executados dessa maneira tem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="1f67f-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="1f67f-132">Manter o diretório de trabalho como o prompt de comando WSL (na maior parte, as exceções são explicadas abaixo).</span><span class="sxs-lookup"><span data-stu-id="1f67f-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="1f67f-133">Ter os mesmos direitos de permissão que o processo WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="1f67f-134">Executado como o usuário do Windows Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f67f-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="1f67f-135">São exibidos no Gerenciador de tarefas do Windows como se executado diretamente no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="1f67f-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="1f67f-136">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1f67f-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="1f67f-137">Arquivos executáveis do Windows executados no WSL são tratadas da mesma forma para executáveis de Linux nativo – pipe, redirecionamentos e até mesmo backgrounding trabalho conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="1f67f-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="1f67f-138">Exemplos usando pipes:</span><span class="sxs-lookup"><span data-stu-id="1f67f-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="1f67f-139">Exemplo usando comandos do Windows e WSL misto:</span><span class="sxs-lookup"><span data-stu-id="1f67f-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="1f67f-140">Binários do Windows devem incluir a extensão de arquivo, corresponder ao uso de arquivo e ser executável.</span><span class="sxs-lookup"><span data-stu-id="1f67f-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="1f67f-141">Incluindo arquivos executáveis não scripts em lote.</span><span class="sxs-lookup"><span data-stu-id="1f67f-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="1f67f-142">Como comandos nativos de CMD `dir` pode ser executado com `cmd.exe /C` comando.</span><span class="sxs-lookup"><span data-stu-id="1f67f-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="1f67f-143">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="1f67f-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="1f67f-144">Parâmetros são passados para o Windows binária sem modificações.</span><span class="sxs-lookup"><span data-stu-id="1f67f-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="1f67f-145">Por exemplo, os comandos a seguir abrirá `C:\temp\foo.txt` em `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="1f67f-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="1f67f-146">Modificando arquivos localizados em VolFs (arquivos não está `/mnt/<x>`) com um Windows application no WSL não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="1f67f-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="1f67f-147">Por padrão, o WSL tenta manter o diretório de trabalho do que o Windows binária como o diretório atual do WSL, mas fará o fallback no diretório de criação de instância se o diretório de trabalho estiver em VolFs.</span><span class="sxs-lookup"><span data-stu-id="1f67f-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="1f67f-148">Por exemplo; `wsl.exe` inicialmente é iniciada no `C:\temp` e diretório WSL atual é alterado para casa do usuário.</span><span class="sxs-lookup"><span data-stu-id="1f67f-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="1f67f-149">Quando `notepad.exe` é chamado de diretório de base do usuário, WSL é revertida automaticamente para `C:\temp` como o diretório de trabalho notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="1f67f-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="1f67f-150">Variáveis de ambiente de compartilhamento entre o Windows e o WSL</span><span class="sxs-lookup"><span data-stu-id="1f67f-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="1f67f-151">Disponível em compilações do Windows Insider 17063 e posteriores.</span><span class="sxs-lookup"><span data-stu-id="1f67f-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="1f67f-152">Antes de 17063, apenas variável de ambiente Windows que foi possível acessar o WSL foi `PATH` (portanto, você também pode iniciar executáveis do Win32 em WSL).</span><span class="sxs-lookup"><span data-stu-id="1f67f-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="1f67f-153">A partir de 17063, WSL e Windows compartilham `WSLENV`, uma variável de ambiente especial criada para acabar com distribuições de Linux e Windows em execução no WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="1f67f-154">Propriedades de `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="1f67f-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="1f67f-155">Ele é compartilhado; ela existe em ambientes Windows e WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="1f67f-156">É uma lista de variáveis de ambiente para compartilhar entre o Windows e o WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="1f67f-157">Ele pode formatar as variáveis de ambiente para funcionar bem em Windows e WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="1f67f-158">Há quatro sinalizadores disponíveis no `WSLENV` para influenciar como essa variável de ambiente é convertido.</span><span class="sxs-lookup"><span data-stu-id="1f67f-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="1f67f-159">`WSLENV` sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="1f67f-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="1f67f-160">`/p` -Converte o caminho entre caminhos no estilo WSL/Linux e os caminhos do Win32.</span><span class="sxs-lookup"><span data-stu-id="1f67f-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="1f67f-161">`/l` -indica que a variável de ambiente é uma lista de caminhos.</span><span class="sxs-lookup"><span data-stu-id="1f67f-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="1f67f-162">`/u` -indica que essa variável de ambiente só deve ser incluído ao executar o WSL do Win32.</span><span class="sxs-lookup"><span data-stu-id="1f67f-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="1f67f-163">`/w` -indica que essa variável de ambiente só deve ser incluído durante a execução Win32 do WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="1f67f-164">Sinalizadores podem ser combinados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="1f67f-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="1f67f-165">Desabilitar a interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="1f67f-165">Disable Interop</span></span>

<span data-ttu-id="1f67f-166">Os usuários podem desabilitar a capacidade de executar os binários do Windows para uma única sessão WSL, executando o comando a seguir como raiz:</span><span class="sxs-lookup"><span data-stu-id="1f67f-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="1f67f-167">Para habilitar novamente o Windows binários saia de todas as sessões WSL e execute novamente o bash.exe ou execute o comando a seguir como raiz:</span><span class="sxs-lookup"><span data-stu-id="1f67f-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="1f67f-168">Desabilitando a interoperabilidade não serão mantidos entre sessões WSL – interoperabilidade será habilitada novamente quando uma nova sessão é iniciada.</span><span class="sxs-lookup"><span data-stu-id="1f67f-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="1f67f-169">Atualização para criadores e atualização de aniversário</span><span class="sxs-lookup"><span data-stu-id="1f67f-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="1f67f-170">Enquanto a pré-queda de experiência de interoperabilidade Creators Update é semelhante para experiências de interoperabilidade mais recentes, há algumas diferenças importantes.</span><span class="sxs-lookup"><span data-stu-id="1f67f-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="1f67f-171">Resumo:</span><span class="sxs-lookup"><span data-stu-id="1f67f-171">To summarize:</span></span>

* <span data-ttu-id="1f67f-172">`bash.exe` foi preterido e substituído pelo `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="1f67f-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="1f67f-173">`-c` para executar um comando único não é necessária com a opção `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="1f67f-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="1f67f-174">Caminho do Windows está incluído no WSL `$PATH`</span><span class="sxs-lookup"><span data-stu-id="1f67f-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="1f67f-175">O processo para desabilitar a interoperabilidade é inalterado.</span><span class="sxs-lookup"><span data-stu-id="1f67f-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="1f67f-176">Invocar WSL da linha de comando do Windows</span><span class="sxs-lookup"><span data-stu-id="1f67f-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="1f67f-177">Binários do Linux podem ser invocados no Prompt de comando do Windows ou do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1f67f-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="1f67f-178">Binários invocados dessa maneira tem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="1f67f-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="1f67f-179">Use o mesmo diretório de trabalho como o prompt CMD ou o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1f67f-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="1f67f-180">Execute como usuário padrão WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="1f67f-181">Ter os mesmos direitos administrativos do Windows como o processo de chamada e o terminal.</span><span class="sxs-lookup"><span data-stu-id="1f67f-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="1f67f-182">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1f67f-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="1f67f-183">Comandos do Linux chamados dessa forma são tratados como qualquer outro aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="1f67f-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="1f67f-184">As coisas como entrada, tubulação e redirecionamento de arquivo funcionam conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="1f67f-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="1f67f-185">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="1f67f-185">Examples:</span></span>

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

<span data-ttu-id="1f67f-186">Os comandos WSL passado para `bash -c` são encaminhadas para o processo WSL sem modificação.</span><span class="sxs-lookup"><span data-stu-id="1f67f-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="1f67f-187">Caminhos de arquivo devem ser especificados no formato WSL e tome cuidado para escapar caracteres relevantes.</span><span class="sxs-lookup"><span data-stu-id="1f67f-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="1f67f-188">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1f67f-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="1f67f-189">Invocar os binários do Windows de WSL</span><span class="sxs-lookup"><span data-stu-id="1f67f-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="1f67f-190">O subsistema Windows para Linux pode invocar os binários do Windows diretamente da linha de comando WSL.</span><span class="sxs-lookup"><span data-stu-id="1f67f-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="1f67f-191">Aplicativos executados dessa maneira tem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="1f67f-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="1f67f-192">Reter o diretório de trabalho como o prompt de comando WSL, exceto no cenário explicado abaixo.</span><span class="sxs-lookup"><span data-stu-id="1f67f-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="1f67f-193">Ter os mesmos direitos de permissão que o `bash.exe` processo.</span><span class="sxs-lookup"><span data-stu-id="1f67f-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="1f67f-194">Executado como o usuário do Windows Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f67f-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="1f67f-195">São exibidos no Gerenciador de tarefas do Windows como se executado diretamente no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="1f67f-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="1f67f-196">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1f67f-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="1f67f-197">WSL, esses executáveis são tratados semelhante para executáveis de Linux nativo.</span><span class="sxs-lookup"><span data-stu-id="1f67f-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="1f67f-198">Isso significa adicionar diretórios para o caminho do Linux e tubulação entre works comandos conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="1f67f-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="1f67f-199">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="1f67f-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="1f67f-200">O binário do Windows deve incluir a extensão de arquivo, corresponder ao uso de arquivo e ser executável.</span><span class="sxs-lookup"><span data-stu-id="1f67f-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="1f67f-201">Incluindo arquivos executáveis não scripts em lote e de comandos, como `dir` pode ser executado com `/mnt/c/Windows/System32/cmd.exe /C` comando.</span><span class="sxs-lookup"><span data-stu-id="1f67f-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="1f67f-202">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="1f67f-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="1f67f-203">Parâmetros são passados para o Windows binária sem modificações.</span><span class="sxs-lookup"><span data-stu-id="1f67f-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="1f67f-204">Por exemplo, os comandos a seguir abrirá `C:\temp\foo.txt` em `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="1f67f-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="1f67f-205">Modificando arquivos localizados em VolFs (arquivos não está `/mnt/<x>`) com um Windows application não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="1f67f-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="1f67f-206">Por padrão, o WSL tenta manter o diretório de trabalho do que o Windows binária como o diretório atual do WSL, mas fará o fallback no diretório de criação de instância se o diretório de trabalho estiver em VolFs.</span><span class="sxs-lookup"><span data-stu-id="1f67f-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="1f67f-207">Por exemplo; `bash.exe` inicialmente é iniciada no `C:\temp` e diretório WSL atual é alterado para casa do usuário.</span><span class="sxs-lookup"><span data-stu-id="1f67f-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="1f67f-208">Quando `notepad.exe` é chamado de diretório de base do usuário, WSL é revertida automaticamente para `C:\temp` como o diretório de trabalho notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="1f67f-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
