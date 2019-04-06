---
title: Notas de versão do subsistema do Windows para Linux
description: Notas de versão para o subsistema Windows para Linux.  Atualizada semanalmente.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 3eee7ff6d1f8302e98cde84fccabf5d9113c83f2
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063624"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="46124-105">Notas de versão do subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="46124-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18342"></a><span data-ttu-id="46124-106">Compilação 18342</span><span class="sxs-lookup"><span data-stu-id="46124-106">Build 18342</span></span>
<span data-ttu-id="46124-107">Para Windows geral informações sobre compilação 18342, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="46124-107">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-108">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-108">WSL</span></span>
* <span data-ttu-id="46124-109">Adicionamos a capacidade dos usuários acessar os arquivos do Linux em uma distribuição WSL do Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-109">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="46124-110">Esses arquivos podem ser acessados por meio da linha de comando e também aplicativos do Windows, como o Explorador de arquivos, VSCode, etc. podem interagir com esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="46124-110">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="46124-111">Acessar seus arquivos, navegando até \\ \\$ wsl\\< distro_name >, ou ver uma lista de execução de distribuições, navegando até \\ \\$ wsl</span><span class="sxs-lookup"><span data-stu-id="46124-111">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="46124-112">Adicionar marcas de informações adicionais de CPU e corrigir os valores de Cpus_allowed [ lista] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="46124-112">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="46124-113">Suporte a execução de thread não líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="46124-113">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="46124-114">Tratar falhas de atualização de configuração como não-fatais [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="46124-114">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="46124-115">Atualizar binfmt para lidar adequadamente com deslocamentos [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="46124-115">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="46124-116">Habilitar o mapeamento unidades de rede para planejar 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="46124-116">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="46124-117">Suporte ao Windows -> Linux e tradução de caminho do Windows para montagens -> do Linux</span><span class="sxs-lookup"><span data-stu-id="46124-117">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="46124-118">Criar seções somente leitura para mapeamentos em arquivos abertos somente leitura</span><span class="sxs-lookup"><span data-stu-id="46124-118">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="46124-119">Compilação 18334</span><span class="sxs-lookup"><span data-stu-id="46124-119">Build 18334</span></span>
<span data-ttu-id="46124-120">Para Windows geral informações sobre compilação 18334, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="46124-120">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-121">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-121">WSL</span></span>
* <span data-ttu-id="46124-122">Reestruturação da maneira que a zona de tempo do Windows é mapeada para um fuso horário do Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="46124-122">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="46124-123">Corrigir vazamentos de memória e adicionar novas funções de conversão de cadeia de caracteres [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="46124-123">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="46124-124">SIGCONT em um threadgroup sem threads é não operacional [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="46124-124">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="46124-125">Exibir corretamente os descritores de arquivo de soquete e epoll em /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="46124-125">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="46124-126">Compilação 18305</span><span class="sxs-lookup"><span data-stu-id="46124-126">Build 18305</span></span>
<span data-ttu-id="46124-127">Para Windows geral informações sobre compilação 18305, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="46124-127">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-128">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-128">WSL</span></span>
* <span data-ttu-id="46124-129">pthreads perder o acesso aos arquivos quando o thread primário é encerrado [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="46124-129">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="46124-130">TIOCSCTTY deve ignorar o parâmetro "force", a menos que seja necessário [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="46124-130">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="46124-131">aprimoramentos de linha de comando wsl.exe e adição de importação / exportação de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="46124-131">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="46124-132">Compilação 18277</span><span class="sxs-lookup"><span data-stu-id="46124-132">Build 18277</span></span>
<span data-ttu-id="46124-133">Para Windows geral informações sobre compilação 18277, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="46124-133">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-134">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-134">WSL</span></span>
* <span data-ttu-id="46124-135">Corrigir o erro "nenhuma interface deste tipo suportada" apresentado na compilação 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="46124-135">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="46124-136">Ignorar o sinalizador de MNT_FORCE unmount syscall [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="46124-136">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="46124-137">Alternar a interoperabilidade do WSL para usar a API oficial do CreatePseudoConsole</span><span class="sxs-lookup"><span data-stu-id="46124-137">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="46124-138">Não manter nenhum valor de tempo limite quando FUTEX_WAIT é reiniciado</span><span class="sxs-lookup"><span data-stu-id="46124-138">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="46124-139">Compilação 18272</span><span class="sxs-lookup"><span data-stu-id="46124-139">Build 18272</span></span>
<span data-ttu-id="46124-140">Para Windows geral informações sobre compilação 18272, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="46124-140">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-141">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-141">WSL</span></span>
* <span data-ttu-id="46124-142">**AVISO:** Há um problema nesta compilação que faz o WSL inoperável.</span><span class="sxs-lookup"><span data-stu-id="46124-142">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="46124-143">Ao tentar iniciar sua distribuição, você verá um erro "Nenhuma interface deste tipo suportada".</span><span class="sxs-lookup"><span data-stu-id="46124-143">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="46124-144">O problema foi corrigido e estará no build Insider rápido da próxima semana.</span><span class="sxs-lookup"><span data-stu-id="46124-144">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="46124-145">Se você tiver instalado essa compilação, você pode reverter para a compilação anterior do Windows usando "Ir para a versão anterior do Windows 10" nas configurações -> atualização de & segurança -> Recovery.</span><span class="sxs-lookup"><span data-stu-id="46124-145">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="46124-146">Compilação 18267</span><span class="sxs-lookup"><span data-stu-id="46124-146">Build 18267</span></span>
<span data-ttu-id="46124-147">Para Windows geral informações sobre compilação 18267, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="46124-147">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-148">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-148">WSL</span></span>
* <span data-ttu-id="46124-149">Corrija o problema em que o processo zumbi não pode ser reaped e permanecerão enfileirados indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="46124-149">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="46124-150">WslRegisterDistribution trava se a mensagem de erro excede o tamanho máximo [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="46124-150">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="46124-151">Permitir fsync bem-sucedido para arquivos somente leitura em DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="46124-151">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="46124-152">Certifique-se de que pastas /bin e /sbin existem antes de criar links simbólicos dentro de [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="46124-152">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="46124-153">Adicionado um mecanismo de tempo limite de encerramento de instância para instâncias WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-153">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="46124-154">Atualmente, o limite é definido como 15 segundos, que significa que a instância será encerrada 15 segundos após o último processo WSL é encerrado.</span><span class="sxs-lookup"><span data-stu-id="46124-154">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="46124-155">Para encerrar uma distribuição imediatamente, use:</span><span class="sxs-lookup"><span data-stu-id="46124-155">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="46124-156">Compilar 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="46124-156">Build 17763 (1809)</span></span>
<span data-ttu-id="46124-157">Para Windows geral informações sobre compilação 17763, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="46124-157">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-158">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-158">WSL</span></span>
* <span data-ttu-id="46124-159">Verificação de permissão de syscall SetPriority muito restrita para alterar a prioridade do thread mesmo [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="46124-159">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="46124-160">Certifique-se de que o tempo de interrupção não polarizada é usado para o tempo de inicialização para evitar o retorno de valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="46124-160">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="46124-161">Tratar links simbólicos no interpretador WSL binfmt [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="46124-161">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="46124-162">Melhor tratamento de limpeza de descritor de arquivo threadgroup líder.</span><span class="sxs-lookup"><span data-stu-id="46124-162">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="46124-163">Alternar WSL usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter de kernel para evitar estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="46124-163">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="46124-164">Ptrace conexão pode fazer com que o valor de retorno incorreto de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="46124-164">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="46124-165">Correção relacionada AF_UNIX vários problemas [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="46124-165">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="46124-166">Correção do problema que poderia causar a interoperabilidade do WSL falhar se o diretório de trabalho atual é menor que 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="46124-166">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="46124-167">Evitar um atraso de segundo, as conexões de loopback às portas não existente [GH 3286] com falha</span><span class="sxs-lookup"><span data-stu-id="46124-167">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="46124-168">Adicionar arquivo de stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="46124-168">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="46124-169">Informações mais precisas do escopo de IPV6.</span><span class="sxs-lookup"><span data-stu-id="46124-169">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="46124-170">Suporte PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="46124-170">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="46124-171">Sistema de arquivos do pipe limpando inadvertidamente o evento de borda disparada epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="46124-171">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="46124-172">Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="46124-172">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="46124-173">Melhor suporte de zumbi [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="46124-173">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="46124-174">Adicionar entradas de wsl.conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="46124-174">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="46124-175">Correção para getsockname nem sempre retornar o tipo de família do soquete UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="46124-175">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="46124-176">Adicionar suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="46124-176">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="46124-177">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="46124-177">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="46124-178">Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="46124-178">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="46124-179">Corrigir o problema na pasta raiz [GH 3304] de verificação de permissão</span><span class="sxs-lookup"><span data-stu-id="46124-179">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="46124-180">Suporte limitado para TTY teclado ioctls KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="46124-180">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="46124-181">Aplicativos de interface do usuário do Windows devem ser executado mesmo quando iniciado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="46124-181">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="46124-182">Adicione a opção wsl -u ou --usuário [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="46124-182">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="46124-183">Corrigir problemas de inicialização WSL inicialização rápida está habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="46124-183">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="46124-184">Soquetes do UNIX precisam manter credenciais de par desconectada [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="46124-184">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="46124-185">Soquetes do Unix sem-bloqueio apresentando indefinidamente EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="46124-185">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="46124-186">Caso = off, é os novo drvfs padrão [2937 de GH, 3212, 3328] do tipo de montagem</span><span class="sxs-lookup"><span data-stu-id="46124-186">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="46124-187">Ver [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="46124-187">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="46124-188">Adicionar wslconfig / encerrar para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="46124-188">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="46124-189">Corrigi o problema com o contexto de shell WSL entradas de menu que não tratar corretamente os caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="46124-189">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="46124-190">Expor diferenciação por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="46124-190">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="46124-191">ARM64: Emule as operações de manutenção do cache.</span><span class="sxs-lookup"><span data-stu-id="46124-191">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="46124-192">Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="46124-192">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="46124-193">DrvFs: unescape apenas caracteres no intervalo particular que correspondem ao caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="46124-193">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="46124-194">Corrigir o erro off-by-one na validação de comprimento ELF analisador interpretador [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="46124-194">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="46124-195">Temporizadores WSL absolutos com um tempo no passado não disparam [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="46124-195">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="46124-196">Certifique-se recentemente de arquivos esparsos criados estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="46124-196">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="46124-197">Atomicamente Crie diretórios diferencia maiusculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="46124-197">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="46124-198">Foi corrigido um problema adicional em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="46124-198">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="46124-199">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="46124-199">[GH 2712]</span></span>
* <span data-ttu-id="46124-200">WSL fixa inicie falha quando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="46124-200">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="46124-201">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="46124-201">[GH 3020]</span></span>
* <span data-ttu-id="46124-202">Adicione menu de contexto do explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="46124-202">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="46124-203">Para usar, mantenha a tecla shift e clique com botão direito quando estiver em uma janela do explorer.</span><span class="sxs-lookup"><span data-stu-id="46124-203">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="46124-204">Corrigir o comportamento de não bloqueio de soquete Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="46124-204">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="46124-205">Correção de travamento comando NETLINK conforme relatado na 2026 GH.</span><span class="sxs-lookup"><span data-stu-id="46124-205">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="46124-206">Adicione suporte para sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="46124-206">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="46124-207">Corrigi o problema com eventos de inotify não causam truncamento [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="46124-207">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="46124-208">Adicione--opção de exec para wsl.exe invocar um binário único sem um shell.</span><span class="sxs-lookup"><span data-stu-id="46124-208">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="46124-209">Adicione--opção de distribuição para wsl.exe selecionar uma distribuição específica.</span><span class="sxs-lookup"><span data-stu-id="46124-209">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="46124-210">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="46124-210">Limited support for dmesg.</span></span> <span data-ttu-id="46124-211">Aplicativos agora podem fazer dmesg.</span><span class="sxs-lookup"><span data-stu-id="46124-211">Applications can now log to dmesg.</span></span> <span data-ttu-id="46124-212">Driver WSL registra informações limitadas dmesg.</span><span class="sxs-lookup"><span data-stu-id="46124-212">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="46124-213">No futuro, isso pode ser estendido para executar outro informações/diagnóstico do driver.</span><span class="sxs-lookup"><span data-stu-id="46124-213">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="46124-214">Observação: dmesg é suportado atualmente por meio de `/dev/kmsg` interface de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46124-214">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="46124-215">ainda não há suporte para a interface de syscall.</span><span class="sxs-lookup"><span data-stu-id="46124-215">syscall interface is not yet supported.</span></span> <span data-ttu-id="46124-216">E, portanto, algumas da `dmesg` opções de linha de comando como `-S`, `-C` não funcionam.</span><span class="sxs-lookup"><span data-stu-id="46124-216">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="46124-217">Alterar gid padrão e o modo de dispositivos seriais para corresponder nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="46124-217">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="46124-218">DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="46124-218">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="46124-219">Observação: DrvFs tem algumas limitações no nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="46124-219">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="46124-220">Alguns caracteres (como '/', ':' e '\*') não são permitido e estendidos nomes de atributo não diferenciam maiusculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="46124-220">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="46124-221">Compilação 18252 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="46124-221">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="46124-222">Para Windows geral informações sobre compilação 18252, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="46124-222">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-223">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-223">WSL</span></span>
* <span data-ttu-id="46124-224">Mova os binários de init e bsdtar fora lxssmanager dll e em uma pasta de ferramentas separadas</span><span class="sxs-lookup"><span data-stu-id="46124-224">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="46124-225">Corrigir a corrida em torno de fechar o descritor de arquivo ao usar CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="46124-225">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="46124-226">Lidar com campos opcionais no /proc/pid/mountinfo ao traduzir DrvFs caminhos</span><span class="sxs-lookup"><span data-stu-id="46124-226">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="46124-227">Permitir mknod DrvFs seja bem-sucedida sem suporte de metadados para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="46124-227">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="46124-228">Arquivos somente leitura criados em DrvFs devem ter o atributo somente leitura definido [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="46124-228">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="46124-229">Adicionar /sbin/mount.drvfs auxiliar para lidar com a montagem de DrvFs</span><span class="sxs-lookup"><span data-stu-id="46124-229">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="46124-230">Use DrvFs renomeação POSIX.</span><span class="sxs-lookup"><span data-stu-id="46124-230">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="46124-231">Permita a tradução de caminho em volumes sem um GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="46124-231">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="46124-232">Compilar 17738 (rápida)</span><span class="sxs-lookup"><span data-stu-id="46124-232">Build 17738 (Fast)</span></span>
<span data-ttu-id="46124-233">Para Windows geral informações sobre compilação 17738, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="46124-233">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-234">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-234">WSL</span></span>
* <span data-ttu-id="46124-235">Verificação de permissão de syscall SetPriority muito restrita para alterar a prioridade do thread mesmo [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="46124-235">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="46124-236">Certifique-se de que o tempo de interrupção não polarizada é usado para o tempo de inicialização para evitar o retorno de valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="46124-236">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="46124-237">Tratar links simbólicos no interpretador WSL binfmt [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="46124-237">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="46124-238">Melhor tratamento de limpeza de descritor de arquivo threadgroup líder.</span><span class="sxs-lookup"><span data-stu-id="46124-238">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="46124-239">Compilar 17728 (rápida)</span><span class="sxs-lookup"><span data-stu-id="46124-239">Build 17728 (Fast)</span></span>
<span data-ttu-id="46124-240">Para Windows geral informações sobre compilação 17728, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="46124-240">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-241">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-241">WSL</span></span>
* <span data-ttu-id="46124-242">Alternar WSL usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter de kernel para evitar estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="46124-242">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="46124-243">Ptrace conexão pode fazer com que o valor de retorno incorreto de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="46124-243">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="46124-244">Correção de a que um número de AF_UNIX relacionadas problemas [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="46124-244">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="46124-245">Correção do problema que poderia causar a interoperabilidade do WSL falhar se o diretório de trabalho atual é menor que 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="46124-245">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="46124-246">Compilação 18204 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="46124-246">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="46124-247">Para Windows geral informações sobre compilação 18204, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="46124-247">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-248">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-248">WSL</span></span>
* <span data-ttu-id="46124-249">Redirecionar inadvertenly de sistema de arquivos, limpando o evento de borda disparada epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="46124-249">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="46124-250">Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="46124-250">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="46124-251">Compilar 17723 (rápida)</span><span class="sxs-lookup"><span data-stu-id="46124-251">Build 17723 (Fast)</span></span>
<span data-ttu-id="46124-252">Para Windows geral informações sobre compilação 17723, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="46124-252">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-253">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-253">WSL</span></span>
* <span data-ttu-id="46124-254">Evitar um atraso de segundo, as conexões de loopback às portas não existente [GH 3286] com falha</span><span class="sxs-lookup"><span data-stu-id="46124-254">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="46124-255">Adicionar arquivo de stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="46124-255">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="46124-256">Informações mais precisas do escopo de IPV6.</span><span class="sxs-lookup"><span data-stu-id="46124-256">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="46124-257">Suporte PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="46124-257">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="46124-258">Redirecionar inadvertenly de sistema de arquivos, limpando o evento de borda disparada epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="46124-258">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="46124-259">Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="46124-259">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="46124-260">Compilação 17713</span><span class="sxs-lookup"><span data-stu-id="46124-260">Build 17713</span></span>
<span data-ttu-id="46124-261">Para Windows geral informações sobre compilação 17713, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="46124-261">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-262">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-262">WSL</span></span>
* <span data-ttu-id="46124-263">Melhor suporte de zumbi [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="46124-263">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="46124-264">Adicionar entradas de wsl.conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="46124-264">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="46124-265">Correção para getsockname nem sempre retornar o tipo de família do soquete UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="46124-265">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="46124-266">Adicionar suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="46124-266">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="46124-267">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="46124-267">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="46124-268">Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="46124-268">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="46124-269">Corrigir o problema na pasta raiz [GH 3304] de verificação de permissão</span><span class="sxs-lookup"><span data-stu-id="46124-269">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="46124-270">Suporte limitado para TTY teclado ioctls KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="46124-270">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="46124-271">Aplicativos de interface do usuário do Windows devem ser executado mesmo quando iniciado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="46124-271">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="46124-272">Compilação 17704</span><span class="sxs-lookup"><span data-stu-id="46124-272">Build 17704</span></span>
<span data-ttu-id="46124-273">Para Windows geral informações sobre compilação 17704, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="46124-273">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-274">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-274">WSL</span></span>
* <span data-ttu-id="46124-275">Adicione a opção wsl -u ou --usuário [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="46124-275">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="46124-276">Corrigir problemas de inicialização WSL inicialização rápida está habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="46124-276">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="46124-277">Soquetes do UNIX precisam manter credenciais de par desconectada [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="46124-277">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="46124-278">Soquetes do Unix sem-bloqueio apresentando indefinidamente EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="46124-278">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="46124-279">Caso = off, é os novo drvfs padrão [2937 de GH, 3212, 3328] do tipo de montagem</span><span class="sxs-lookup"><span data-stu-id="46124-279">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="46124-280">Ver [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="46124-280">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="46124-281">Adicionar wslconfig / encerrar para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="46124-281">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="46124-282">Compilação 17692</span><span class="sxs-lookup"><span data-stu-id="46124-282">Build 17692</span></span>
<span data-ttu-id="46124-283">Para Windows geral informações sobre compilação 17692, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="46124-283">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-284">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-284">WSL</span></span>
* <span data-ttu-id="46124-285">Corrigi o problema com o contexto de shell WSL entradas de menu que não tratar corretamente os caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="46124-285">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="46124-286">Expor diferenciação por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="46124-286">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="46124-287">ARM64: Emule as operações de manutenção do cache.</span><span class="sxs-lookup"><span data-stu-id="46124-287">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="46124-288">Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="46124-288">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="46124-289">DrvFs: unescape apenas caracteres no intervalo particular que correspondem ao caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="46124-289">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="46124-290">Compilação 17686</span><span class="sxs-lookup"><span data-stu-id="46124-290">Build 17686</span></span>
<span data-ttu-id="46124-291">Para Windows geral informações sobre compilação 17686, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="46124-291">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-292">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-292">WSL</span></span>
* <span data-ttu-id="46124-293">Corrigir o erro off-by-one na validação de comprimento ELF analisador interpretador [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="46124-293">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="46124-294">Temporizadores WSL absolutos com um tempo no passado não disparam [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="46124-294">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="46124-295">Certifique-se recentemente de arquivos esparsos criados estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="46124-295">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="46124-296">Atomicamente Crie diretórios diferencia maiusculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="46124-296">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="46124-297">Compilação 17677</span><span class="sxs-lookup"><span data-stu-id="46124-297">Build 17677</span></span>
<span data-ttu-id="46124-298">Para Windows geral informações sobre compilação 17677, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="46124-298">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-299">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-299">WSL</span></span>
* <span data-ttu-id="46124-300">Foi corrigido um problema adicional em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="46124-300">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="46124-301">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="46124-301">[GH 2712]</span></span>
* <span data-ttu-id="46124-302">WSL fixa inicie falha quando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="46124-302">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="46124-303">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="46124-303">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="46124-304">Compilação 17666</span><span class="sxs-lookup"><span data-stu-id="46124-304">Build 17666</span></span>
<span data-ttu-id="46124-305">Para Windows geral informações sobre compilação 17666, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="46124-305">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-306">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-306">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="46124-307">AVISO: Há um problema, impedindo que o WSL seja executado em alguns chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="46124-307">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="46124-308">Uma correção está pronto e fazendo seu caminho para o branch de Build do Insider.</span><span class="sxs-lookup"><span data-stu-id="46124-308">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="46124-309">Adicione menu de contexto do explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="46124-309">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="46124-310">Para usar shift espera e o botão direito do mouse quando estiver em uma janela do explorer.</span><span class="sxs-lookup"><span data-stu-id="46124-310">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="46124-311">Corrigir o comportamento de não bloqueio de soquete unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="46124-311">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="46124-312">Correção de travamento comando NETLINK conforme relatado na 2026 GH.</span><span class="sxs-lookup"><span data-stu-id="46124-312">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="46124-313">Adicione suporte para sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="46124-313">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="46124-314">Corrigi o problema com eventos de inotify não causam truncamento [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="46124-314">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="46124-315">Adicione--opção de exec para wsl.exe invocar um binário único sem um shell.</span><span class="sxs-lookup"><span data-stu-id="46124-315">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="46124-316">Adicione--opção de distribuição para wsl.exe selecionar uma distribuição específica.</span><span class="sxs-lookup"><span data-stu-id="46124-316">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="46124-317">Compilação 17655 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="46124-317">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="46124-318">Para Windows geral informações sobre compilação 17655, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="46124-318">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-319">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-319">WSL</span></span>
* <span data-ttu-id="46124-320">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="46124-320">Limited support for dmesg.</span></span> <span data-ttu-id="46124-321">Aplicativos agora podem fazer dmesg.</span><span class="sxs-lookup"><span data-stu-id="46124-321">Applications can now log to dmesg.</span></span> <span data-ttu-id="46124-322">Driver WSL registra informações limitadas dmesg.</span><span class="sxs-lookup"><span data-stu-id="46124-322">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="46124-323">No futuro, isso pode ser estendido para executar outro informações/diagnóstico do driver.</span><span class="sxs-lookup"><span data-stu-id="46124-323">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="46124-324">Observação: dmesg é suportado atualmente por meio de `/dev/kmsg` interface de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46124-324">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="46124-325">ainda não há suporte para a interface sycall.</span><span class="sxs-lookup"><span data-stu-id="46124-325">sycall interface is not yet supported.</span></span> <span data-ttu-id="46124-326">E, portanto, algumas da `dmesg` opções de linha de comando como `-S`, `-C` não funcionam.</span><span class="sxs-lookup"><span data-stu-id="46124-326">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="46124-327">Corrigido um problema em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="46124-327">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="46124-328">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="46124-328">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="46124-329">Compilação 17639 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="46124-329">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="46124-330">Para Windows geral informações sobre compilação 17639, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="46124-330">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-331">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-331">WSL</span></span>
* <span data-ttu-id="46124-332">Alterar gid padrão e o modo de dispositivos seriais para corresponder nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="46124-332">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="46124-333">DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="46124-333">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="46124-334">Observação: DrvFs tem algumas limitações no nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="46124-334">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="46124-335">Em particular, alguns caracteres (como '/', ':' e '\*') não são permitido e estendidos nomes de atributo não diferenciam maiusculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="46124-335">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="46124-336">Compilar 17133 (rápida)</span><span class="sxs-lookup"><span data-stu-id="46124-336">Build 17133 (Fast)</span></span>
<span data-ttu-id="46124-337">Para Windows geral informações sobre compilação 17133, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="46124-337">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-338">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-338">WSL</span></span>
* <span data-ttu-id="46124-339">Correção de suspensão no WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-339">Fix for hang in WSL.</span></span> <span data-ttu-id="46124-340">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="46124-340">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="46124-341">Compilar 17128 (rápida)</span><span class="sxs-lookup"><span data-stu-id="46124-341">Build 17128 (Fast)</span></span>
<span data-ttu-id="46124-342">Para Windows geral informações sobre compilação 17128, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="46124-342">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-343">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-343">WSL</span></span>
* <span data-ttu-id="46124-344">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="46124-344">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="46124-345">Compilação 17627 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="46124-345">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="46124-346">Para Windows geral informações sobre compilação 17627, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="46124-346">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-347">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-347">WSL</span></span>
* <span data-ttu-id="46124-348">Adicione suporte para as operações de reconhecimento de pi futex.</span><span class="sxs-lookup"><span data-stu-id="46124-348">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="46124-349">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="46124-349">[GH 1006]</span></span>
    * <span data-ttu-id="46124-350">Observe que as prioridades não são atualmente suporte para o recurso WSL portanto, há limitações, mas o uso padrão deve ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="46124-350">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="46124-351">Suporte ao firewall do Windows para processos WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-351">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="46124-352">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="46124-352">[GH 1852]</span></span>
    * <span data-ttu-id="46124-353">Por exemplo, para permitir que o WSL python processar para escutar em qualquer porta, use o cmd do Windows com privilégios elevados:</span><span class="sxs-lookup"><span data-stu-id="46124-353">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd:</span></span>
```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * <span data-ttu-id="46124-354">Para obter detalhes adicionais sobre como adicionar regras de firewall, consulte [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="46124-354">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="46124-355">Respeite o shell padrão do usuário ao usar wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="46124-355">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="46124-356">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="46124-356">[GH 2372]</span></span>
* <span data-ttu-id="46124-357">Relatar todas as interfaces de rede ethernet.</span><span class="sxs-lookup"><span data-stu-id="46124-357">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="46124-358">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="46124-358">[GH 2996]</span></span>
* <span data-ttu-id="46124-359">Uma melhor manipulação do arquivo /etc/passwd corrompido.</span><span class="sxs-lookup"><span data-stu-id="46124-359">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="46124-360">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="46124-360">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="46124-361">Console</span><span class="sxs-lookup"><span data-stu-id="46124-361">Console</span></span>
* <span data-ttu-id="46124-362">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-362">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-363">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-363">LTP Results:</span></span>
<span data-ttu-id="46124-364">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-364">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="46124-365">Compilação 17618 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="46124-365">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="46124-366">Para Windows geral informações sobre compilação 17618, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="46124-366">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-367">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-367">WSL</span></span>
* <span data-ttu-id="46124-368">Introduzir pseudoconsole funcionalidades para interoperabilidade do NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="46124-368">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="46124-369">O mecanismo de instalação herdada (lxrun.exe) foi preterido.</span><span class="sxs-lookup"><span data-stu-id="46124-369">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="46124-370">O mecanismo com suporte para a instalação de distribuições é por meio do Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="46124-370">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="46124-371">Console</span><span class="sxs-lookup"><span data-stu-id="46124-371">Console</span></span>
* <span data-ttu-id="46124-372">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-372">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-373">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-373">LTP Results:</span></span>
<span data-ttu-id="46124-374">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-374">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="46124-375">Compilação 17110</span><span class="sxs-lookup"><span data-stu-id="46124-375">Build 17110</span></span>
<span data-ttu-id="46124-376">Para Windows geral informações sobre compilação 17110, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="46124-376">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-377">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-377">WSL</span></span>
* <span data-ttu-id="46124-378">Permitir /init ser encerrado de Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="46124-378">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="46124-379">DrvFs agora usa por diretório diferenciar maiusculas de minúsculas por padrão (equivalente a "caso = dir" opção de montagem).</span><span class="sxs-lookup"><span data-stu-id="46124-379">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="46124-380">Usando "caso = force" (o comportamento antigo) requer a definição de uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="46124-380">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="46124-381">Execute o seguinte comando para habilitar "caso = force" Se você precisar usá-lo: reg adicionar HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="46124-381">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="46124-382">Se você tiver criados com o WSL na versão mais antiga do Windows que precisam ser diferencia maiusculas de minúsculas de diretórios existentes, use fsutil.exe para marcá-los em maiusculas e minúsculas: fsutil.exe arquivo setcasesensitiveinfo <path> habilitar</span><span class="sxs-lookup"><span data-stu-id="46124-382">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="46124-383">Cadeias de caracteres retornadas de syscall o uname terminadas com NULL.</span><span class="sxs-lookup"><span data-stu-id="46124-383">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="46124-384">Console</span><span class="sxs-lookup"><span data-stu-id="46124-384">Console</span></span>
* <span data-ttu-id="46124-385">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-385">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-386">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-386">LTP Results:</span></span>
<span data-ttu-id="46124-387">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-387">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="46124-388">Compilação 17107</span><span class="sxs-lookup"><span data-stu-id="46124-388">Build 17107</span></span>
<span data-ttu-id="46124-389">Para Windows geral informações sobre compilação 17107, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="46124-389">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-390">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-390">WSL</span></span>
* <span data-ttu-id="46124-391">Suporte a TCSETSF e TCSETSW em pontos de extremidade mestre pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="46124-391">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="46124-392">Iniciar os processos simultâneos de interoperabilidade pode resultar em EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="46124-392">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="46124-393">Corrigi PTRACE_ATTACH para mostrar o status de rastreamento apropriado no /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="46124-393">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="46124-394">Corrida de correção em que os processos de curta duração clonados com os CLEARTID SETTID sinalizadores e pode ser fechado sem limpar o endereço TID.</span><span class="sxs-lookup"><span data-stu-id="46124-394">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="46124-395">Exiba uma mensagem ao atualizar os diretórios de sistema de arquivos do Linux, ao mover de uma compilação de pré-17093.</span><span class="sxs-lookup"><span data-stu-id="46124-395">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="46124-396">Para obter mais detalhes sobre as alterações do sistema de 17093 arquivo, consulte as notas de versão para [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="46124-396">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="46124-397">Console</span><span class="sxs-lookup"><span data-stu-id="46124-397">Console</span></span>
* <span data-ttu-id="46124-398">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-398">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-399">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-399">LTP Results:</span></span>
<span data-ttu-id="46124-400">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-400">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="46124-401">Compilação 17101</span><span class="sxs-lookup"><span data-stu-id="46124-401">Build 17101</span></span>
<span data-ttu-id="46124-402">Para Windows geral informações sobre compilação 17101, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="46124-402">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-403">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-403">WSL</span></span>
* <span data-ttu-id="46124-404">Suporte para signalfd.</span><span class="sxs-lookup"><span data-stu-id="46124-404">Support for signalfd.</span></span> <span data-ttu-id="46124-405">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="46124-405">[GH 129]</span></span>
* <span data-ttu-id="46124-406">Suporte a nomes de arquivo que contém caracteres inválidos de NTFS, codificá-los como caracteres de Unicode particulares.</span><span class="sxs-lookup"><span data-stu-id="46124-406">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="46124-407">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="46124-407">[GH 1514]</span></span>
* <span data-ttu-id="46124-408">Montagem automática usarão somente leitura quando não há suporte para gravação.</span><span class="sxs-lookup"><span data-stu-id="46124-408">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="46124-409">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="46124-409">[GH 2603]</span></span>
* <span data-ttu-id="46124-410">Permitir a colagem dos pares substitutos de Unicode (como caracteres emoji).</span><span class="sxs-lookup"><span data-stu-id="46124-410">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="46124-411">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="46124-411">[GH 2765]</span></span>
* <span data-ttu-id="46124-412">Arquivos pseudo /proc e /sys devem retornar leitura e gravação pronto para de select, sondagem, epoll, et al. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="46124-412">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="46124-413">Corrija o problema que poderia fazer com que o serviço entrar em loop infinito quando o registro foi violado ou corrompido.</span><span class="sxs-lookup"><span data-stu-id="46124-413">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="46124-414">Corrija as mensagens netlink para trabalhar com a versão mais recente (upstream 4.14) iproute2.</span><span class="sxs-lookup"><span data-stu-id="46124-414">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="46124-415">Console</span><span class="sxs-lookup"><span data-stu-id="46124-415">Console</span></span>
* <span data-ttu-id="46124-416">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-416">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-417">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-417">LTP Results:</span></span>
<span data-ttu-id="46124-418">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-418">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="46124-419">Compilação 17093</span><span class="sxs-lookup"><span data-stu-id="46124-419">Build 17093</span></span>
<span data-ttu-id="46124-420">Para Windows geral informações sobre compilação 17093, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-420">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="46124-421">Importante:</span><span class="sxs-lookup"><span data-stu-id="46124-421">Important:</span></span>
<span data-ttu-id="46124-422">Ao iniciar o WSL pela primeira vez após a atualização para esta compilação, ele precisará executar algum trabalho atualizando os diretórios de sistema de arquivos do Linux.</span><span class="sxs-lookup"><span data-stu-id="46124-422">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="46124-423">Isso pode levar vários minutos, portanto, pode parecer WSL iniciam lentamente.</span><span class="sxs-lookup"><span data-stu-id="46124-423">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="46124-424">Isso deve ocorrer apenas uma vez para cada distribuição têm instalado da loja.</span><span class="sxs-lookup"><span data-stu-id="46124-424">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="46124-425">Suporte aprimorado de maiusculas e minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="46124-425">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="46124-426">DrvFs agora dá suporte a diferenciação de maiusculas por diretório.</span><span class="sxs-lookup"><span data-stu-id="46124-426">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="46124-427">Isso é um novo sinalizador que pode ser definido em diretórios para indicar que todas as operações nesses diretórios devem ser tratadas como diferencia maiusculas de minúsculas, que permite que até mesmo aplicativos Windows corretamente abrir arquivos que diferem somente maiusculas.</span><span class="sxs-lookup"><span data-stu-id="46124-427">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="46124-428">DrvFs possui novas opções de montagem, controlando a diferenciação de maiusculas em uma base por diretório</span><span class="sxs-lookup"><span data-stu-id="46124-428">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="46124-429">Caso = força: todos os diretórios são tratados como diferencia maiusculas de minúsculas (exceto para a raiz da unidade).</span><span class="sxs-lookup"><span data-stu-id="46124-429">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="46124-430">Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="46124-430">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="46124-431">Esse é o comportamento herdado, exceto para marcar os novos diretórios diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="46124-431">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="46124-432">Caso = dir: somente diretórios com o sinalizador de diferenciação de maiusculas por diretório diferenciam maiusculas e minúsculas; outros diretórios diferenciam maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="46124-432">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="46124-433">Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="46124-433">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="46124-434">Caso = desativado: somente diretórios com o sinalizador de diferenciação de maiusculas por diretório diferenciam maiusculas e minúsculas; outros diretórios diferenciam maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="46124-434">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="46124-435">Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="46124-435">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="46124-436">Observação: diretórios criados pelo WSL em versões anteriores não têm esse sinalizador definido, portanto, não será tratada como diferencia maiusculas de minúsculas se você usar o "caso = dir" opção.</span><span class="sxs-lookup"><span data-stu-id="46124-436">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="46124-437">Uma maneira de definir esse sinalizador nos diretórios existentes em breve.</span><span class="sxs-lookup"><span data-stu-id="46124-437">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="46124-438">Exemplo de montagem com as seguintes opções (para as unidades existentes, você deve primeiro desmontar antes de montar com opções diferentes): sudo mount -t drvfs c: mnt/c -o caso = dir</span><span class="sxs-lookup"><span data-stu-id="46124-438">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="46124-439">Por enquanto, caso = força ainda é a opção padrão.</span><span class="sxs-lookup"><span data-stu-id="46124-439">For now, case=force is still the default option.</span></span> <span data-ttu-id="46124-440">Isso será alterado para caso = dir no futuro.</span><span class="sxs-lookup"><span data-stu-id="46124-440">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="46124-441">Agora você pode usar barras "/" em caminhos do Windows ao montar DrvFs, por exemplo: -t drvfs //server/share /mnt/share de montagem sudo</span><span class="sxs-lookup"><span data-stu-id="46124-441">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="46124-442">Agora, o WSL processa o arquivo /etc/fstab durante a inicialização de instância [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="46124-442">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="46124-443">Isso é feito antes de montar automaticamente DrvFs unidades; todas as unidades que já foram montadas por fstab serão não remontadas automaticamente, permitindo que você altere o ponto de montagem para unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="46124-443">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="46124-444">Esse comportamento pode ser desativado usando wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="46124-444">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="46124-445">Os arquivos de montagem, mountinfo e mountstats no /proc corretamente escapar caracteres especiais como barras invertidas e de espaços [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="46124-445">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="46124-446">Arquivos especiais criados com DrvFs como links simbólicos do WSL, ou fifos e soquetes quando os metadados estiverem habilitados, agora podem ser copiados e movidos do Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-446">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="46124-447">WSL é mais configurável com wsl.conf</span><span class="sxs-lookup"><span data-stu-id="46124-447">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="46124-448">Adicionamos um método para que você configure automaticamente algumas funcionalidades em WSL que será aplicada sempre que iniciar o subsistema.</span><span class="sxs-lookup"><span data-stu-id="46124-448">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="46124-449">Isso inclui opções de montagem automática e a configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="46124-449">This includes automount options and network configuration.</span></span> <span data-ttu-id="46124-450">Saiba mais sobre isso em nossa postagem de blog em: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="46124-450">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="46124-451">AF_UNIX permite conexões de soquete entre processos do Linux no WSL e processos nativos do Windows</span><span class="sxs-lookup"><span data-stu-id="46124-451">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="46124-452">Aplicativos WSL e o Windows agora podem se comunicar entre si em soquetes do Unix.</span><span class="sxs-lookup"><span data-stu-id="46124-452">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="46124-453">Imagine que você deseja executar um serviço no Windows e torná-lo disponível para aplicativos do Windows e WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-453">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="46124-454">Agora, que é possível com soquetes do Unix.</span><span class="sxs-lookup"><span data-stu-id="46124-454">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="46124-455">Leia mais em nosso blog postagem em https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="46124-455">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-456">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-456">WSL</span></span>
* <span data-ttu-id="46124-457">Suporte mmap() com MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="46124-457">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="46124-458">Suporte CLONE_PTRACE e CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="46124-458">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="46124-459">Lidar com sinal de encerramento não SIGCHLD em clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="46124-459">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="46124-460">/Proc/sys/fs/inotify/max_user_instances de stub e /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="46124-460">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="46124-461">Erro ao carregar os binários do ELF que contêm cabeçalhos de carga com deslocamentos diferente de zero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="46124-461">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="46124-462">Zerar à direita de bytes de página ao carregar imagens.</span><span class="sxs-lookup"><span data-stu-id="46124-462">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="46124-463">Reduzir casos em que execve silenciosamente encerra o processo</span><span class="sxs-lookup"><span data-stu-id="46124-463">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="46124-464">Console</span><span class="sxs-lookup"><span data-stu-id="46124-464">Console</span></span>
* <span data-ttu-id="46124-465">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-465">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-466">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-466">LTP Results:</span></span>
<span data-ttu-id="46124-467">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-467">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="46124-468">Build 17083</span><span class="sxs-lookup"><span data-stu-id="46124-468">Build 17083</span></span>
<span data-ttu-id="46124-469">Para Windows geral informações sobre compilação 17083, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-469">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-470">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-470">WSL</span></span>
* <span data-ttu-id="46124-471">Fixa de verificação de bugs relacionada a epoll [2798 de GH, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="46124-471">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="46124-472">Fixos travamentos quando desativar ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="46124-472">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="46124-473">Certifique-se de operações mmap aparecem atômica [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="46124-473">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="46124-474">Console</span><span class="sxs-lookup"><span data-stu-id="46124-474">Console</span></span>
* <span data-ttu-id="46124-475">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-475">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-476">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-476">LTP Results:</span></span>
<span data-ttu-id="46124-477">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-477">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="46124-478">Build 17074</span><span class="sxs-lookup"><span data-stu-id="46124-478">Build 17074</span></span>
<span data-ttu-id="46124-479">Para Windows geral informações sobre compilação 17074, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-479">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-480">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-480">WSL</span></span>
* <span data-ttu-id="46124-481">Formato de armazenamento fixa de metadados DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="46124-481">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="46124-482">**Importante:** Metadados de DrvFs criado antes desta compilação serão exibidos incorretamente ou não.</span><span class="sxs-lookup"><span data-stu-id="46124-482">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="46124-483">Para corrigir arquivos afetados, use chmod e alterar o proprietário para reaplicar os metadados.</span><span class="sxs-lookup"><span data-stu-id="46124-483">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="46124-484">Correção do problema com vários sinais e syscalls reinicializável.</span><span class="sxs-lookup"><span data-stu-id="46124-484">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="46124-485">Console</span><span class="sxs-lookup"><span data-stu-id="46124-485">Console</span></span>
* <span data-ttu-id="46124-486">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-487">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-487">LTP Results:</span></span>
<span data-ttu-id="46124-488">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-488">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="46124-489">Build 17063</span><span class="sxs-lookup"><span data-stu-id="46124-489">Build 17063</span></span>
<span data-ttu-id="46124-490">Para Windows geral informações sobre compilação 17063, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-490">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46124-491">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-491">WSL</span></span>
* <span data-ttu-id="46124-492">DrvFs dá suporte a metadados adicionais de Linux.</span><span class="sxs-lookup"><span data-stu-id="46124-492">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="46124-493">Isso permite definir o proprietário e o modo de arquivos usando chmod/alterar o proprietário e também a criação de arquivos especiais, como fifos, soquetes do unix e arquivos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46124-493">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="46124-494">Isso está desabilitado por padrão por enquanto, pois é ainda experimental.</span><span class="sxs-lookup"><span data-stu-id="46124-494">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="46124-495">**Observação:**  Corrigimos um bug no formato de metadados usado pelo DrvFs.</span><span class="sxs-lookup"><span data-stu-id="46124-495">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="46124-496">Enquanto trabalha metadados nessa compilação para experimentação, os builds futuros não corretamente lerá metadados criados por essa compilação.</span><span class="sxs-lookup"><span data-stu-id="46124-496">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="46124-497">Talvez você precise atualizar manualmente o proprietário de arquivos modificados e dispositivos com uma ID de dispositivo personalizada precisa ser recriada.</span><span class="sxs-lookup"><span data-stu-id="46124-497">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="46124-498">Para habilitar a montagem DrvFs com a opção de metadados (para habilitá-lo em uma montagem existente, você deve primeiro desmontá-la):</span><span class="sxs-lookup"><span data-stu-id="46124-498">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="46124-499">Permissões de Linux são adicionadas como metadados adicionais no arquivo; elas não afetam as permissões do Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-499">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="46124-500">Lembre-se de que a edição de um arquivo usando um editor do Windows pode remover os metadados.</span><span class="sxs-lookup"><span data-stu-id="46124-500">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="46124-501">Nesse caso, o arquivo será revertido para suas permissões padrão.</span><span class="sxs-lookup"><span data-stu-id="46124-501">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="46124-502">Opções de montagem adicionado para DrvFs para controlar arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="46124-502">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="46124-503">UID: a ID de usuário usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="46124-503">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="46124-504">GID: a ID do grupo usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="46124-504">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="46124-505">umask: uma máscara de permissões para excluir todos os arquivos e diretórios de octal.</span><span class="sxs-lookup"><span data-stu-id="46124-505">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="46124-506">fmask: uma máscara de permissões para excluir todos os arquivos regulares de octal.</span><span class="sxs-lookup"><span data-stu-id="46124-506">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="46124-507">dmask: uma máscara de permissões para excluir para todos os diretórios de octal.</span><span class="sxs-lookup"><span data-stu-id="46124-507">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="46124-508">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="46124-508">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="46124-509">Combine com a opção de metadados para especificar as permissões padrão de arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="46124-509">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="46124-510">Introduzida uma nova variável de ambiente, `WSLENV`, para configurar como as variáveis de ambiente fluam entre WSL e Win32.</span><span class="sxs-lookup"><span data-stu-id="46124-510">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="46124-511">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="46124-511">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` <span data-ttu-id="46124-512">é uma lista delimitada por dois-pontos das variáveis de ambiente que pode ser incluído ao iniciar processos WSL do Win32 ou Win32 do WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-512">is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="46124-513">Cada variável pode ser sufixado com uma barra invertida seguida por sinalizadores para especificar como ele é convertido.</span><span class="sxs-lookup"><span data-stu-id="46124-513">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="46124-514">p: O valor é um caminho que deve ser traduzido entre os caminhos de Win32 e WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-514">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="46124-515">l: O valor é uma lista de caminhos.</span><span class="sxs-lookup"><span data-stu-id="46124-515">l: The value is a list of paths.</span></span> <span data-ttu-id="46124-516">Em WSL, é uma lista delimitada por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="46124-516">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="46124-517">No Win32, é uma lista delimitada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="46124-517">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="46124-518">u: O valor só deve ser incluído ao invocar o WSL do Win32</span><span class="sxs-lookup"><span data-stu-id="46124-518">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="46124-519">gravação: O valor só deve ser incluído ao invocar Win32 de WSL</span><span class="sxs-lookup"><span data-stu-id="46124-519">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="46124-520">Você pode definir `WSLENV` em. bashrc ou no ambiente do Windows personalizado para o usuário.</span><span class="sxs-lookup"><span data-stu-id="46124-520">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="46124-521">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="46124-521">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="46124-522">links simbólicos de drvfs relatam o tamanho correto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="46124-522">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="46124-523">leitura/gravação funciona para tamanhos de e/s muito grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="46124-523">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="46124-524">waitpid funciona com IDs (GH 2534) do grupo de processo</span><span class="sxs-lookup"><span data-stu-id="46124-524">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="46124-525">desempenho significativamente aprimorado mmap para regiões de reserva grande; melhora o desempenho de ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="46124-525">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="46124-526">dá suporte a personalidade para READ_IMPLIES_EXEC; corrige maxima e clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="46124-526">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="46124-527">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="46124-527">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="46124-528">correções de falhas de página no modo; de excesso de alocação correções sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="46124-528">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="46124-529">Clone dá suporte a mais combinações de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="46124-529">clone supports more flags combinations</span></span>
* <span data-ttu-id="46124-530">Suporte a select/epoll de arquivos epoll (anteriormente não operacional).</span><span class="sxs-lookup"><span data-stu-id="46124-530">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="46124-531">Notificar ptrace de syscalls não implementada.</span><span class="sxs-lookup"><span data-stu-id="46124-531">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="46124-532">Ignorar as interfaces que não estão ao gerar nameservers resolv. conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="46124-532">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="46124-533">Enumere as interfaces de rede com nenhum endereço físico.</span><span class="sxs-lookup"><span data-stu-id="46124-533">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="46124-534">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="46124-534">[GH 2685]</span></span>
* <span data-ttu-id="46124-535">Correções de bugs adicionais e aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="46124-535">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="46124-536">Ferramentas do Linux disponíveis para desenvolvedores no Windows</span><span class="sxs-lookup"><span data-stu-id="46124-536">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="46124-537">Cadeia de ferramentas de linha de comando do Windows inclui bsdtar (tar) e o curl.</span><span class="sxs-lookup"><span data-stu-id="46124-537">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="46124-538">Leia [este blog](https://aka.ms/tarcurlwindows) para saber mais sobre a adição dessas duas novas ferramentas e ver como eles moldando a experiência do desenvolvedor no Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-538">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   `AF_UNIX` <span data-ttu-id="46124-539">está disponível no SDK Windows Insider (17061 +).</span><span class="sxs-lookup"><span data-stu-id="46124-539">is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="46124-540">Leia [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para saber mais sobre `AF_UNIX` e como os desenvolvedores no Windows podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="46124-540">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="46124-541">Console</span><span class="sxs-lookup"><span data-stu-id="46124-541">Console</span></span>
* <span data-ttu-id="46124-542">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-542">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-543">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-543">LTP Results:</span></span>
<span data-ttu-id="46124-544">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-544">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="46124-545">Compilação 17046</span><span class="sxs-lookup"><span data-stu-id="46124-545">Build 17046</span></span>

<span data-ttu-id="46124-546">Para Windows geral informações sobre compilação 17046, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="46124-546">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="46124-547">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-547">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-548">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-548">WSL</span></span>
- <span data-ttu-id="46124-549">Permitir que os processos sejam executados sem um terminal de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="46124-549">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="46124-550">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="46124-550">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="46124-551">Melhor suporte a CLONE_VFORK e CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="46124-551">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="46124-552">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="46124-552">[GH 1878, 2615]</span></span>
- <span data-ttu-id="46124-553">Ignore drivers de filtro TDI WSL operações de rede.</span><span class="sxs-lookup"><span data-stu-id="46124-553">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="46124-554">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="46124-554">[GH 1554]</span></span>
- <span data-ttu-id="46124-555">DrvFs cria links simbólicos do NT quando determinadas condições forem atendidas.</span><span class="sxs-lookup"><span data-stu-id="46124-555">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="46124-556">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="46124-556">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="46124-557">O destino do link deve ser relativo, não deve ultrapassar o quaisquer pontos de montagem ou links simbólicos e deve existir.</span><span class="sxs-lookup"><span data-stu-id="46124-557">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="46124-558">O usuário deve ter SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (Isso normalmente exige que você inicie wsl.exe com privilégios elevados), a menos que o modo de desenvolvedor está ativado.</span><span class="sxs-lookup"><span data-stu-id="46124-558">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="46124-559">Em outras situações, DrvFs ainda cria links simbólicos WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-559">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="46124-560">Permitir executando com privilégios elevados e sem privilégios elevados instâncias WSL simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="46124-560">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="46124-561">Suporte /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="46124-561">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="46124-562">Adicione wslpath para fazer WSL <> – conversões de caminho do Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-562">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="46124-563">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="46124-563">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="46124-564">Console</span><span class="sxs-lookup"><span data-stu-id="46124-564">Console</span></span>
- <span data-ttu-id="46124-565">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="46124-565">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-566">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-566">LTP Results:</span></span>
<span data-ttu-id="46124-567">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-567">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="46124-568">Build 17040</span><span class="sxs-lookup"><span data-stu-id="46124-568">Build 17040</span></span>

<span data-ttu-id="46124-569">Para Windows geral informações sobre compilação 17040, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="46124-569">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-570">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-570">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-571">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-571">WSL</span></span>
- <span data-ttu-id="46124-572">Não há correções desde 17035.</span><span class="sxs-lookup"><span data-stu-id="46124-572">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="46124-573">Console</span><span class="sxs-lookup"><span data-stu-id="46124-573">Console</span></span>
- <span data-ttu-id="46124-574">Não há correções desde 17035.</span><span class="sxs-lookup"><span data-stu-id="46124-574">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-575">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-575">LTP Results:</span></span>
<span data-ttu-id="46124-576">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-576">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="46124-577">Compilação 17035</span><span class="sxs-lookup"><span data-stu-id="46124-577">Build 17035</span></span>

<span data-ttu-id="46124-578">Para Windows geral informações sobre compilação 17035, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="46124-578">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-579">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-579">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-580">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-580">WSL</span></span>
- <span data-ttu-id="46124-581">Acessando arquivos em DrvFs pode falhar ocasionalmente EINVAL.</span><span class="sxs-lookup"><span data-stu-id="46124-581">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="46124-582">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="46124-582">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="46124-583">Console</span><span class="sxs-lookup"><span data-stu-id="46124-583">Console</span></span>
- <span data-ttu-id="46124-584">Alguma perda de cor ao inserir/excluir linhas no modo de VT.</span><span class="sxs-lookup"><span data-stu-id="46124-584">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-585">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-585">LTP Results:</span></span>
<span data-ttu-id="46124-586">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-586">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="46124-587">Build 17025</span><span class="sxs-lookup"><span data-stu-id="46124-587">Build 17025</span></span>

<span data-ttu-id="46124-588">Para Windows geral informações no build 17025, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="46124-588">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-589">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-589">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-590">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-590">WSL</span></span>
- <span data-ttu-id="46124-591">Inicie processos inicias em um novo grupo de processo de primeiro plano [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="46124-591">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="46124-592">Entrega SIGHUP corrige [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="46124-592">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="46124-593">Gere nome da ponte virtual padrão se não houver nenhuma [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="46124-593">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="46124-594">Implemente /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="46124-594">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="46124-595">Correções de pipe de stdout/stderr mais interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="46124-595">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="46124-596">Stub syncfs chamada do sistema.</span><span class="sxs-lookup"><span data-stu-id="46124-596">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="46124-597">Console</span><span class="sxs-lookup"><span data-stu-id="46124-597">Console</span></span>
- <span data-ttu-id="46124-598">Corrija a entrada tradução VT para consoles de terceiros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="46124-598">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-599">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-599">LTP Results:</span></span>
<span data-ttu-id="46124-600">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-600">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="46124-601">Compilação 17017</span><span class="sxs-lookup"><span data-stu-id="46124-601">Build 17017</span></span>

<span data-ttu-id="46124-602">Para Windows geral informações sobre compilação 17017, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="46124-602">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-603">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-603">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-604">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-604">WSL</span></span>
- <span data-ttu-id="46124-605">Ignore cabeçalhos de programa ELF vazios [GH 330].</span><span class="sxs-lookup"><span data-stu-id="46124-605">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="46124-606">Permitir LxssManager criar instâncias WSL para os usuários não interativo (ssh e agendada suporte de tarefa) [777 GH 1602].</span><span class="sxs-lookup"><span data-stu-id="46124-606">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="46124-607">Suporte WSL -> Win32 -> [GH 1228] de cenários WSL ("início").</span><span class="sxs-lookup"><span data-stu-id="46124-607">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="46124-608">Suporte limitado para a terminação de aplicativos de console, invocado por meio de interoperabilidade [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="46124-608">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="46124-609">Suporte a opções de montagem para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="46124-609">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="46124-610">Ptrace bloqueando a inicialização de filho [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="46124-610">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="46124-611">EPOLLET faltando alguns eventos [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="46124-611">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="46124-612">Retorne mais dados para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="46124-612">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="46124-613">Getdents com lseek fornece resultados incorretos.</span><span class="sxs-lookup"><span data-stu-id="46124-613">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="46124-614">Corrigi alguns travamentos de interoperabilidade do aplicativo do Win32, aguardando a entrada em um pipe que não tem mais nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="46124-614">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="46124-615">Suporte O_ASYNC para arquivos de tty/pty.</span><span class="sxs-lookup"><span data-stu-id="46124-615">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="46124-616">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-616">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46124-617">Console</span><span class="sxs-lookup"><span data-stu-id="46124-617">Console</span></span>
- <span data-ttu-id="46124-618">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-618">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-619">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-619">LTP Results:</span></span>
<span data-ttu-id="46124-620">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="46124-620">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="46124-621">Atualização do Fall Creators</span><span class="sxs-lookup"><span data-stu-id="46124-621">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="46124-622">Build 16288</span><span class="sxs-lookup"><span data-stu-id="46124-622">Build 16288</span></span>

<span data-ttu-id="46124-623">Para Windows geral informações sobre compilação 16288, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="46124-623">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-624">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-624">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-625">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-625">WSL</span></span>
- <span data-ttu-id="46124-626">Inicializar corretamente e relatar uid e gid modo de soquete para descritores de arquivo [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="46124-626">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="46124-627">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46124-628">Console</span><span class="sxs-lookup"><span data-stu-id="46124-628">Console</span></span>
- <span data-ttu-id="46124-629">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-630">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-630">LTP Results:</span></span>
<span data-ttu-id="46124-631">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="46124-631">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="46124-632">Compilação 16278</span><span class="sxs-lookup"><span data-stu-id="46124-632">Build 16278</span></span>

<span data-ttu-id="46124-633">Para Windows geral informações sobre compilação 162738, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="46124-633">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-634">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-634">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-635">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-635">WSL</span></span>
- <span data-ttu-id="46124-636">Cancelar explicitamente o mapeamento de exibições mapeadas de seções de backup em arquivo quando subdividir o estado de MM LX [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="46124-636">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="46124-637">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-637">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46124-638">Console</span><span class="sxs-lookup"><span data-stu-id="46124-638">Console</span></span>
- <span data-ttu-id="46124-639">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-639">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-640">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-640">LTP Results:</span></span>
<span data-ttu-id="46124-641">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="46124-641">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="46124-642">Compilação 16275</span><span class="sxs-lookup"><span data-stu-id="46124-642">Build 16275</span></span>

<span data-ttu-id="46124-643">Para Windows geral informações sobre compilação 162735, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="46124-643">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-644">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-645">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-645">WSL</span></span>
- <span data-ttu-id="46124-646">Nenhum WSL relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-646">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="46124-647">Console</span><span class="sxs-lookup"><span data-stu-id="46124-647">Console</span></span>
- <span data-ttu-id="46124-648">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-648">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-649">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-649">LTP Results:</span></span>
<span data-ttu-id="46124-650">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="46124-650">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="46124-651">Compilação 16273</span><span class="sxs-lookup"><span data-stu-id="46124-651">Build 16273</span></span>

<span data-ttu-id="46124-652">Para Windows geral informações sobre compilação 16273, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-652">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-653">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-653">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-654">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-654">WSL</span></span>
- <span data-ttu-id="46124-655">Corrigido um problema em que o DrvFs relatado, às vezes, o tipo de arquivo incorreto para diretórios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="46124-655">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="46124-656">Permitir a criação de soquetes NETLINK_KOBJECT_UEVENT desbloquear programas uevent que use [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="46124-656">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="46124-657">Adicionar suporte para conexão sem bloqueio [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="46124-657">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="46124-658">Implemente CLONE_FS clonar o sinalizador de chamada do sistema [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="46124-658">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="46124-659">Corrigir problemas em torno de não lidar com guias ou aspas corretamente na interoperabilidade de NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="46124-659">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="46124-660">Resolver o erro ao tentar iniciar novamente WSL instâncias [GH 651, 2095] o acesso negado</span><span class="sxs-lookup"><span data-stu-id="46124-660">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="46124-661">Implementar operações futex FUTEX_REQUEUE e FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="46124-661">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="46124-662">Corrija as permissões para vários arquivos SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="46124-662">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="46124-663">Corrigir Haskell travamento de pilha durante a instalação do [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="46124-663">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="46124-664">Implementar binfmt_misc "C" ' l'e 'P' sinalizadores [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="46124-664">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="46124-665">Adicionar /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="46124-665">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="46124-666">Adicionar suporte parcial para a chamada do sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="46124-666">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="46124-667">Criar um stub SO_REUSEPORT & adicionando suporte para SO_PASSCRED para soquetes netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="46124-667">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="46124-668">Retornar códigos de erro diferentes de RegisterDistribuiton se uma distribuição está instalado ou desinstalado.</span><span class="sxs-lookup"><span data-stu-id="46124-668">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="46124-669">Permitir cancelamento de registro de distribuições de WSL parcialmente instaladas por meio de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="46124-669">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="46124-670">Corrigir a suspensão de teste de soquete python de udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="46124-670">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="46124-671">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-671">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46124-672">Console</span><span class="sxs-lookup"><span data-stu-id="46124-672">Console</span></span>
- <span data-ttu-id="46124-673">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-673">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-674">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-674">LTP Results:</span></span>
<span data-ttu-id="46124-675">Total de testes: 1904</span><span class="sxs-lookup"><span data-stu-id="46124-675">Total Tests: 1904</span></span><br/>
<span data-ttu-id="46124-676">Testes ignorados do total: 209</span><span class="sxs-lookup"><span data-stu-id="46124-676">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="46124-677">Total de falhas: 229</span><span class="sxs-lookup"><span data-stu-id="46124-677">Total Failures: 229</span></span><br/>
[<span data-ttu-id="46124-678">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-678">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="46124-679">Compilação 16257</span><span class="sxs-lookup"><span data-stu-id="46124-679">Build 16257</span></span>

<span data-ttu-id="46124-680">Para Windows geral informações sobre compilação 16257, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-680">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-681">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-681">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-682">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-682">WSL</span></span>
- <span data-ttu-id="46124-683">Implementar a chamada do sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="46124-683">Implement prlimit64 system call</span></span>
- <span data-ttu-id="46124-684">Adicionar suporte para ulimit – n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="46124-684">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="46124-685">Stub MSG_MORE para soquetes TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="46124-685">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="46124-686">Corrigir o comportamento de vetor auxiliar AT_EXECFN inválido [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="46124-686">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="46124-687">Corrigir o comportamento de copiar/colar para console/tty e adicionar melhor buffer cheio tratamento [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="46124-687">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="46124-688">Defina AT_SECURE na auxiliar vetor para programas em set-user-ID e set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="46124-688">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="46124-689">Ponto de extremidade mestre pseudo-terminal não manipulando TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="46124-689">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="46124-690">Correção de lseek faz para retroceder diretórios em LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="46124-690">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="46124-691">/dev/ptmx trava depois de uso intenso [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="46124-691">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="46124-692">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-692">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46124-693">Console</span><span class="sxs-lookup"><span data-stu-id="46124-693">Console</span></span>
- <span data-ttu-id="46124-694">Correção para horizontal linhas/sublinhados em todos os lugares [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="46124-694">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="46124-695">Corrigir para processar pedido alterado NPM tornando mais difícil fechar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="46124-695">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="46124-696">Adicionado o novo esquema de cores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="46124-696">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-697">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-697">LTP Results:</span></span>
<span data-ttu-id="46124-698">Nenhuma alteração desde 16251</span><span class="sxs-lookup"><span data-stu-id="46124-698">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46124-699">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-699">Syscall Support</span></span>
<span data-ttu-id="46124-700">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-700">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-701">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-701">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="46124-702">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="46124-702">Known Issues</span></span>
#### [<a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a><span data-ttu-id="46124-703">Problema do GitHub 2392: Pastas do Windows não reconhecido pelo WSL...</span><span class="sxs-lookup"><span data-stu-id="46124-703">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="46124-704">No build 16257, o WSL tem problemas ao enumerar arquivos/pastas do Windows por meio de `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="46124-704">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="46124-705">Esse problema foi corrigido e devem ser liberado no build Insiders durante a semana começar 14/8/2017.</span><span class="sxs-lookup"><span data-stu-id="46124-705">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="46124-706">Compilação 16251</span><span class="sxs-lookup"><span data-stu-id="46124-706">Build 16251</span></span>

<span data-ttu-id="46124-707">Para Windows geral informações sobre compilação 16251, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-707">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-708">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-709">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-709">WSL</span></span>
- <span data-ttu-id="46124-710">Remover marca de versão beta do componente opcional do WSL, consulte [postagem de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="46124-710">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="46124-711">Inicializar corretamente o conjunto salvo uid e gid para set-user-ID e a ID do grupo de conjunto de binários em exec [GH 962 do MSExchangeTransport, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="46124-711">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="46124-712">Suporte adicionado para ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="46124-712">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="46124-713">Suporte adicionado para ptrace PTRACE_GETFPREGS e PTRACE_GETREGSET com NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="46124-713">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="46124-714">Corrigido ptrace parar em sinais ignorado</span><span class="sxs-lookup"><span data-stu-id="46124-714">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="46124-715">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-715">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46124-716">Console</span><span class="sxs-lookup"><span data-stu-id="46124-716">Console</span></span>
- <span data-ttu-id="46124-717">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-717">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-718">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-718">LTP Results:</span></span>
<span data-ttu-id="46124-719">Número de testes aprovados: 768</span><span class="sxs-lookup"><span data-stu-id="46124-719">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="46124-720">Número de testes com falha: 244</span><span class="sxs-lookup"><span data-stu-id="46124-720">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="46124-721">Número de testes ignorados: 96</span><span class="sxs-lookup"><span data-stu-id="46124-721">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="46124-722">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-722">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="46124-723">Compilação 16241</span><span class="sxs-lookup"><span data-stu-id="46124-723">Build 16241</span></span>

<span data-ttu-id="46124-724">Para Windows geral informações sobre compilação 16241, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-724">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-725">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-725">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46124-726">WSL</span><span class="sxs-lookup"><span data-stu-id="46124-726">WSL</span></span>
- <span data-ttu-id="46124-727">Nenhum WSL relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-727">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="46124-728">Console</span><span class="sxs-lookup"><span data-stu-id="46124-728">Console</span></span>
- <span data-ttu-id="46124-729">Correção para gerar o caractere incorreto para dez linhas de cruzamento, relatado originalmente [aqui](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="46124-729">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="46124-730">Correção para nenhum texto de saída que está sendo exibido na página de código 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="46124-730">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="46124-731">Não transfira as alterações feitas em valores RGB da cor de um para outras partes da paleta, alterar a seleção.</span><span class="sxs-lookup"><span data-stu-id="46124-731">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="46124-732">Isso fará a folha de propriedades de console muito mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="46124-732">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="46124-733">CTRL + S parece não funcionar corretamente</span><span class="sxs-lookup"><span data-stu-id="46124-733">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="46124-734">Não negrito /-Dim completamente ausentes de códigos de escape ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="46124-734">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="46124-735">Console corretamente não dá suporte a temas de cores Vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="46124-735">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="46124-736">Não é possível colar determinados caracteres [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="46124-736">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="46124-737">Redimensionamento refluxo de forma estranha interage com o redimensionamento de uma janela de bash quando coisas está na linha de comando/Editar [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="46124-737">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="46124-738">CTRL + L sair da tela suja [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="46124-738">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="46124-739">Bug de renderização do console ao exibir VT em HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="46124-739">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="46124-740">Caracteres Japansese pareçam estranhos com o caractere Unicode U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="46124-740">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="46124-741">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-741">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="46124-742">Build 16237</span><span class="sxs-lookup"><span data-stu-id="46124-742">Build 16237</span></span>

<span data-ttu-id="46124-743">Para Windows geral informações sobre compilação 16237, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-743">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-744">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-744">Fixed</span></span>
- <span data-ttu-id="46124-745">Use os atributos padrão para arquivos sem EAs no lxfs (raiz, raiz, 0000)</span><span class="sxs-lookup"><span data-stu-id="46124-745">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="46124-746">Adicionado suporte para as distribuições que usam atributos estendidos</span><span class="sxs-lookup"><span data-stu-id="46124-746">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="46124-747">Correção de enchimento de entradas retornadas pela getdents e getdents64</span><span class="sxs-lookup"><span data-stu-id="46124-747">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="46124-748">Corrigir a verificação de permissões para a chamada do sistema shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="46124-748">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="46124-749">Estado fixo epoll inicial incorreto para ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="46124-749">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="46124-750">Corrigir a leitura do DrvFs diret não retornando todas as entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="46124-750">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="46124-751">Corrigir LxFs leitura diret quando os arquivos estão desvinculado [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="46124-751">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="46124-752">Permitir que arquivos drvfs desvinculado ser reaberto por meio de procfs</span><span class="sxs-lookup"><span data-stu-id="46124-752">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="46124-753">Adicionada a substituição da chave de registro global para desabilitar os recursos WSL (interoperabilidade / montagem da unidade)</span><span class="sxs-lookup"><span data-stu-id="46124-753">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="46124-754">Correção de contagem incorreta de bloco em "estatística" para DrvFs (e LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="46124-754">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="46124-755">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-755">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="46124-756">Compilação 16232</span><span class="sxs-lookup"><span data-stu-id="46124-756">Build 16232</span></span>

<span data-ttu-id="46124-757">Para Windows geral informações sobre compilação 16232, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-757">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-758">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-758">Fixed</span></span>
- <span data-ttu-id="46124-759">Nenhum WSL relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="46124-759">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="46124-760">Compilação 16226</span><span class="sxs-lookup"><span data-stu-id="46124-760">Build 16226</span></span>

<span data-ttu-id="46124-761">Para Windows geral informações sobre compilação 16226, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-761">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-762">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-762">Fixed</span></span>
- <span data-ttu-id="46124-763">xattr relacionadas ao suporte de syscalls (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="46124-763">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="46124-764">suporte de xattr Security.capablity.</span><span class="sxs-lookup"><span data-stu-id="46124-764">security.capablity xattr support.</span></span>
- <span data-ttu-id="46124-765">Compatibilidade aprimorada com certos sistemas de arquivos e filtros, incluindo servidores SMB não MS.</span><span class="sxs-lookup"><span data-stu-id="46124-765">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="46124-766">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="46124-766">[GH #1952]</span></span>
- <span data-ttu-id="46124-767">Suporte aprimorado para espaços reservados do OneDrive, espaços reservados do GVFS e compacta OS arquivos compactados.</span><span class="sxs-lookup"><span data-stu-id="46124-767">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="46124-768">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-768">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="46124-769">Compilação 16215</span><span class="sxs-lookup"><span data-stu-id="46124-769">Build 16215</span></span>

<span data-ttu-id="46124-770">Para Windows geral informações sobre compilação 16215, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-770">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-771">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-771">Fixed</span></span>
- <span data-ttu-id="46124-772">WSL não exige o modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="46124-772">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="46124-773">Suporte a junções de diretório no drvfs.</span><span class="sxs-lookup"><span data-stu-id="46124-773">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="46124-774">Lidar com a desinstalação dos pacotes de appx de distribuição de WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-774">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="46124-775">Atualização procfs Mostrar privado e compartilhado mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="46124-775">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="46124-776">Adicione capacidade para wslconfig.exe limpar as distribuições que são parcialmente instaladas ou desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="46124-776">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="46124-777">Adicionado suporte para IP_MTU_DISCOVER para soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="46124-777">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="46124-778">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="46124-778">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="46124-779">Inferir a família de protocolo para as rotas para AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="46124-779">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="46124-780">Melhorias do dispositivo serial [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="46124-780">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="46124-781">Compilação 16199</span><span class="sxs-lookup"><span data-stu-id="46124-781">Build 16199</span></span>

<span data-ttu-id="46124-782">Para Windows geral informações sobre compilação 16199, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-782">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-783">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-783">Fixed</span></span>
- <span data-ttu-id="46124-784">Nenhum WSL relacionados a alterações nessas versões.</span><span class="sxs-lookup"><span data-stu-id="46124-784">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="46124-785">Compilação 16193</span><span class="sxs-lookup"><span data-stu-id="46124-785">Build 16193</span></span>

<span data-ttu-id="46124-786">Para Windows geral informações sobre compilação 16193, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-786">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-787">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-787">Fixed</span></span>
- <span data-ttu-id="46124-788">Condição de corrida entre o envio SIGCONT e um threadgroup encerrando [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="46124-788">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="46124-789">alterar dispositivos tty e pty para relatório FILE_DEVICE_NAMED_PIPE em vez de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="46124-789">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="46124-790">Correção SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="46124-790">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="46124-791">Movido DrvFs montagem para init daemon [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="46124-791">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="46124-792">Adicionado suporte em DrvFs para seguir links simbólicos do NT.</span><span class="sxs-lookup"><span data-stu-id="46124-792">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="46124-793">Compilação 16184</span><span class="sxs-lookup"><span data-stu-id="46124-793">Build 16184</span></span>

<span data-ttu-id="46124-794">Para Windows geral informações sobre compilação 16184, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-794">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-795">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-795">Fixed</span></span>
- <span data-ttu-id="46124-796">Removida a tarefa de manutenção de pacotes apt (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="46124-796">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="46124-797">Correção da saída não aparecendo de processos do Windows no Node. js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="46124-797">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="46124-798">Reduza os requisitos de alinhamento no lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="46124-798">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="46124-799">Corrigido o tratamento do sinalizador AT_EMPTY_PATH em um número de chamadas do sistema.</span><span class="sxs-lookup"><span data-stu-id="46124-799">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="46124-800">Corrigido um problema em que a exclusão DrvFs arquivos com identificadores abertos fará com que o arquivo a apresentar um comportamento indefinido [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="46124-800">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="46124-801">/ etc/hosts agora herdarão as entradas do arquivo de hosts do Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="46124-801">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="46124-802">Compilação 16179</span><span class="sxs-lookup"><span data-stu-id="46124-802">Build 16179</span></span>

<span data-ttu-id="46124-803">Para Windows geral informações sobre compilação 16179, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-803">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-804">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-804">Fixed</span></span>
- <span data-ttu-id="46124-805">Nenhuma alteração WSL desta semana.</span><span class="sxs-lookup"><span data-stu-id="46124-805">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="46124-806">Compilação 16176</span><span class="sxs-lookup"><span data-stu-id="46124-806">Build 16176</span></span>

<span data-ttu-id="46124-807">Para Windows geral informações sobre compilação 16176, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-807">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-808">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-808">Fixed</span></span>

- [<span data-ttu-id="46124-809">Suporte serial habilitado</span><span class="sxs-lookup"><span data-stu-id="46124-809">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="46124-810">Opção de soquete adicionada IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="46124-810">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="46124-811">Implementado função pwritev (ao carregar o arquivo para PHP/nginx-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="46124-811">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="46124-812">Adição de opções de soquete IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="46124-812">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="46124-813">Suporte para a opção de soquete IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="46124-813">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="46124-814">Opção de soquete _MTU IP (V6) adicionada para o nó de aplicativos, traceroute, dig, nslookup e host</span><span class="sxs-lookup"><span data-stu-id="46124-814">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="46124-815">Opção de soquete adicionada IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="46124-815">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="46124-816">Aprimoramentos do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="46124-816">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="46124-817">Permitir que a montagem de caminhos UNC</span><span class="sxs-lookup"><span data-stu-id="46124-817">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="46124-818">Habilitar o suporte CDFS em drvfs</span><span class="sxs-lookup"><span data-stu-id="46124-818">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="46124-819">Lidar corretamente com permissões de rede para sistemas de arquivos em drvfs</span><span class="sxs-lookup"><span data-stu-id="46124-819">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="46124-820">Adicionar suporte para unidades remotas a drvfs</span><span class="sxs-lookup"><span data-stu-id="46124-820">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="46124-821">Habilitar FAT dar suporte a drvfs</span><span class="sxs-lookup"><span data-stu-id="46124-821">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="46124-822">Aprimoramentos e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-822">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-823">Resultados LTP</span><span class="sxs-lookup"><span data-stu-id="46124-823">LTP Results</span></span>
<span data-ttu-id="46124-824">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="46124-824">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="46124-825">Compilação 16170</span><span class="sxs-lookup"><span data-stu-id="46124-825">Build 16170</span></span>

<span data-ttu-id="46124-826">Para Windows geral informações sobre compilação 16170, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-826">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="46124-827">Lançamos um novo [postagem de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutindo nossos esforços para testar o WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-827">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="46124-828">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-828">Fixed</span></span>

- <span data-ttu-id="46124-829">Soquete de suporte à opção IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="46124-829">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="46124-830">Adicione suporte para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="46124-830">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="46124-831">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="46124-831">[GH 1692]</span></span>
- <span data-ttu-id="46124-832">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-832">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-833">Resultados LTP</span><span class="sxs-lookup"><span data-stu-id="46124-833">LTP Results</span></span>
<span data-ttu-id="46124-834">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="46124-834">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="46124-835">Compilar 15046 para o Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="46124-835">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="46124-836">Há não mais WSL correções ou recursos planejados para inclusão na atualização para o Windows 10 para criadores.</span><span class="sxs-lookup"><span data-stu-id="46124-836">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="46124-837">Notas de versão do WSL serão retomada nas próximas semanas para adições de direcionamento a próxima atualização importante do Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-837">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="46124-838">Para Windows geral informações sobre compilação 15046 e Insider futuras versões visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-838">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="46124-839">Compilação 15042</span><span class="sxs-lookup"><span data-stu-id="46124-839">Build 15042</span></span>

<span data-ttu-id="46124-840">Para Windows geral informações sobre compilação 15042, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-840">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-841">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-841">Fixed</span></span>

- <span data-ttu-id="46124-842">Correção de um deadlock durante a remoção de um caminho que termina em ".."</span><span class="sxs-lookup"><span data-stu-id="46124-842">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="46124-843">Corrigido um problema em que FIONBIO não retornando 0 em caso de sucesso [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="46124-843">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="46124-844">Corrigido o problema com comprimento zero leituras de soquetes de datagrama inet</span><span class="sxs-lookup"><span data-stu-id="46124-844">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="46124-845">Corrigir um possível deadlock devido a condição de corrida na pesquisa de inode drvfs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="46124-845">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="46124-846">O suporte estendido para dados de auxiliares de soquete unix; SCM_CREDENTIALS e SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="46124-846">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="46124-847">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-847">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-848">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-848">LTP Results:</span></span>
<span data-ttu-id="46124-849">Número de aprovação no teste: 737</span><span class="sxs-lookup"><span data-stu-id="46124-849">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="46124-850">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="46124-850">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="46124-851">Compilação 15031</span><span class="sxs-lookup"><span data-stu-id="46124-851">Build 15031</span></span>

<span data-ttu-id="46124-852">Para Windows geral informações sobre compilação 15031, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-852">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-853">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-853">Fixed</span></span>

- <span data-ttu-id="46124-854">Corrigido um bug onde time(2) esporadicamente seria inadequados.</span><span class="sxs-lookup"><span data-stu-id="46124-854">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="46124-855">Corrigido e emitir onde \* SIGPROCMASK syscalls pode corromper a máscara de sinal.</span><span class="sxs-lookup"><span data-stu-id="46124-855">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="46124-856">Agora retorne comprimento de linha de comando completa na notificação de criação de processo WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-856">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="46124-857">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="46124-857">[GH 1632]</span></span>
- <span data-ttu-id="46124-858">WSL agora relata a saída de thread por meio de ptrace suspensões GDB.</span><span class="sxs-lookup"><span data-stu-id="46124-858">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="46124-859">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="46124-859">[GH 1196]</span></span>
- <span data-ttu-id="46124-860">Corrigido o bug onde ptys poderia ser interrompido após a pesado tmux e/s.</span><span class="sxs-lookup"><span data-stu-id="46124-860">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="46124-861">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="46124-861">[GH 1358]</span></span>
- <span data-ttu-id="46124-862">Validação de tempo limite fixo em várias chamadas do sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="46124-862">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="46124-863">Suporte EFD_SEMAPHORE eventfd adicionado [GH 452]</span><span class="sxs-lookup"><span data-stu-id="46124-863">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="46124-864">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-864">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-865">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-865">LTP Results:</span></span>
<span data-ttu-id="46124-866">Número de aprovação no teste: 737</span><span class="sxs-lookup"><span data-stu-id="46124-866">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="46124-867">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="46124-867">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="46124-868">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-868">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="46124-869">Compilação 15025</span><span class="sxs-lookup"><span data-stu-id="46124-869">Build 15025</span></span>

<span data-ttu-id="46124-870">Para Windows geral informações sobre compilação 15025, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-870">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-871">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-871">Fixed</span></span>

- <span data-ttu-id="46124-872">Correção de bug que grep quebrado 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="46124-872">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="46124-873">Sinalizador EFD_SEMAPHORE implementado para eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="46124-873">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="46124-874">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="46124-874">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="46124-875">Sinal controlado por suporte de e/s para soquetes de fluxo de unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="46124-875">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="46124-876">Suporte F_GETPIPE_SZ e F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="46124-876">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="46124-877">Implementar recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="46124-877">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="46124-878">Corrigido o bug onde epoll_wait() não estava esperando [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="46124-878">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="46124-879">Implement /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="46124-879">Implement /proc/version_signature</span></span>
- <span data-ttu-id="46124-880">Syscall Tee agora retorna falha se ambos os descritores de arquivo se referirem ao mesmo pipe</span><span class="sxs-lookup"><span data-stu-id="46124-880">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="46124-881">Implementado comportamento correto em SO_PEERCRED para soquetes do Unix</span><span class="sxs-lookup"><span data-stu-id="46124-881">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="46124-882">Manipulação de parâmetro inválido de syscall tkill fixa</span><span class="sxs-lookup"><span data-stu-id="46124-882">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="46124-883">Alterações para aumentar a preformace de drvfs</span><span class="sxs-lookup"><span data-stu-id="46124-883">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="46124-884">Correção secundária para o bloqueio de e/s do Ruby</span><span class="sxs-lookup"><span data-stu-id="46124-884">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="46124-885">Fixo recvmsg() retornando EINVAL para o sinalizador MSG_DONTWAIT para soquetes inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="46124-885">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="46124-886">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-886">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-887">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-887">LTP Results:</span></span>
<span data-ttu-id="46124-888">Número de aprovação no teste: 732</span><span class="sxs-lookup"><span data-stu-id="46124-888">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="46124-889">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="46124-889">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="46124-890">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-890">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="46124-891">Compilação 15019</span><span class="sxs-lookup"><span data-stu-id="46124-891">Build 15019</span></span>

<span data-ttu-id="46124-892">Para Windows geral informações sobre compilação 15019, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-892">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-893">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-893">Fixed</span></span>

- <span data-ttu-id="46124-894">Corrigido um bug que relatou incorretamente o uso da CPU em procfs para ferramentas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="46124-894">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="46124-895">Ao chamar Open () com O_TRUNC em uma existente arquivo inotify agora gera IN_MODIFY antes IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="46124-895">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="46124-896">Correções para getsockopt de soquete do unix SO_ERROR habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="46124-896">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="46124-897">Implementar /proc/sys/net/core/somaxconn para a linguagem GO</span><span class="sxs-lookup"><span data-stu-id="46124-897">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="46124-898">Tarefa de segundo plano de atualização de pacote de APT-get agora é executado oculta da exibição</span><span class="sxs-lookup"><span data-stu-id="46124-898">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="46124-899">Escopo claro para o localhost do ipv6 (Spring-Framework(Java) falha).</span><span class="sxs-lookup"><span data-stu-id="46124-899">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="46124-900">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-900">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-901">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-901">LTP Results:</span></span>
<span data-ttu-id="46124-902">Número de aprovação no teste: 714</span><span class="sxs-lookup"><span data-stu-id="46124-902">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="46124-903">Número de falha (com falha, ignorada, etc...): 249</span><span class="sxs-lookup"><span data-stu-id="46124-903">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="46124-904">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-904">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="46124-905">Compilação 15014</span><span class="sxs-lookup"><span data-stu-id="46124-905">Build 15014</span></span>

<span data-ttu-id="46124-906">Para Windows geral informações sobre compilação 15014, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="46124-906">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-907">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-907">Fixed</span></span>

- <span data-ttu-id="46124-908">CTRL + C agora funciona conforme o esperado</span><span class="sxs-lookup"><span data-stu-id="46124-908">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="46124-909">htop e ps auxw agora mostram correto utilização de recursos (GH #516)</span><span class="sxs-lookup"><span data-stu-id="46124-909">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="46124-910">Tradução básica de exceções de NT para sinais.</span><span class="sxs-lookup"><span data-stu-id="46124-910">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="46124-911">(#513 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-911">(GH #513)</span></span>
- <span data-ttu-id="46124-912">Agora fallocate falha com ENOSPC quando ficando sem espaço, em vez de EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="46124-912">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="46124-913">/Proc/sys/kernel/sem adicionado.</span><span class="sxs-lookup"><span data-stu-id="46124-913">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="46124-914">Chamadas do sistema semop e semtimedop implementadas</span><span class="sxs-lookup"><span data-stu-id="46124-914">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="46124-915">Erros de nslookup fixo com a opção de soquete IP_RECVTOS & IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="46124-915">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="46124-916">Suporte para opções de soquete IP_RECVTTL e IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="46124-916">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="46124-917">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-917">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-918">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-918">LTP Results:</span></span>
<span data-ttu-id="46124-919">Número de aprovação no teste: 709</span><span class="sxs-lookup"><span data-stu-id="46124-919">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="46124-920">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="46124-920">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="46124-921">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-921">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="46124-922">Resumo de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-922">Syscall Summary</span></span>
<span data-ttu-id="46124-923">Syscalls total: 384</span><span class="sxs-lookup"><span data-stu-id="46124-923">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="46124-924">Total implementado: 235</span><span class="sxs-lookup"><span data-stu-id="46124-924">Total Implemented: 235</span></span> </br>
<span data-ttu-id="46124-925">Total de fazer o stub: 22</span><span class="sxs-lookup"><span data-stu-id="46124-925">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="46124-926">Total de não implementado: 127</span><span class="sxs-lookup"><span data-stu-id="46124-926">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="46124-927">Análise detalhada</span><span class="sxs-lookup"><span data-stu-id="46124-927">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="46124-928">Build 15007</span><span class="sxs-lookup"><span data-stu-id="46124-928">Build 15007</span></span>

<span data-ttu-id="46124-929">Para Windows geral informações sobre compilação 15007, visite o [Blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="46124-929">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="46124-930">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="46124-930">Known Issue</span></span>

- <span data-ttu-id="46124-931">Há um bug conhecido no qual o console não reconhece algumas Ctrl + <key> entrada.</span><span class="sxs-lookup"><span data-stu-id="46124-931">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="46124-932">Isso inclui o comando ctrl-c, que agirá como um pressionamento de tecla "c" normal.</span><span class="sxs-lookup"><span data-stu-id="46124-932">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="46124-933">Solução alternativa: Mapear uma chave alternativa para Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="46124-933">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="46124-934">Por exemplo, para mapear Ctrl + K, Ctrl + c fazer: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="46124-934">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="46124-935">Esse mapeamento é por terminal e precisará ser feito *cada* bash do tempo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="46124-935">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="46124-936">Os usuários podem explorar a opção de incluir isso no seu</span><span class="sxs-lookup"><span data-stu-id="46124-936">Users can explore the option to include this in their</span></span> `.bashrc`

### <a name="fixed"></a><span data-ttu-id="46124-937">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-937">Fixed</span></span>

- <span data-ttu-id="46124-938">Corrigido o problema onde executando WSL consuma 100% de um núcleo de CPU</span><span class="sxs-lookup"><span data-stu-id="46124-938">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="46124-939">Opção IP_PKTINFO, IPV6_RECVPKTINFO agora tem suportada de soquete.</span><span class="sxs-lookup"><span data-stu-id="46124-939">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="46124-940">(GH #851 987)</span><span class="sxs-lookup"><span data-stu-id="46124-940">(GH #851, 987)</span></span>
- <span data-ttu-id="46124-941">Truncar o endereço físico de interface de rede para 16 bytes no lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="46124-941">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="46124-942">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-942">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-943">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-943">LTP Results:</span></span>
<span data-ttu-id="46124-944">Número de aprovação no teste: 709</span><span class="sxs-lookup"><span data-stu-id="46124-944">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="46124-945">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="46124-945">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="46124-946">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-946">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="46124-947">Build 15002</span><span class="sxs-lookup"><span data-stu-id="46124-947">Build 15002</span></span>

<span data-ttu-id="46124-948">Para Windows geral informações no build 15002, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-948">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="46124-949">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="46124-949">Known Issue</span></span>

<span data-ttu-id="46124-950">Dois problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="46124-950">Two known issues:</span></span>
- <span data-ttu-id="46124-951">Há um bug conhecido no qual o console não reconhece algumas Ctrl + <key> entrada.</span><span class="sxs-lookup"><span data-stu-id="46124-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="46124-952">Isso inclui o comando ctrl-c, que agirá como um pressionamento de tecla "c" normal.</span><span class="sxs-lookup"><span data-stu-id="46124-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="46124-953">Solução alternativa: Mapear uma chave alternativa para Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="46124-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="46124-954">Por exemplo, para mapear Ctrl + K, Ctrl + c fazer: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="46124-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="46124-955">Esse mapeamento é por terminal e precisará ser feito *cada* bash do tempo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="46124-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="46124-956">Os usuários podem explorar a opção de incluir isso no seu</span><span class="sxs-lookup"><span data-stu-id="46124-956">Users can explore the option to include this in their</span></span> `.bashrc`

- <span data-ttu-id="46124-957">Enquanto WSL está em execução, um thread de sistema consumirá 100% de um núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="46124-957">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="46124-958">A causa raiz foi resolvida e corrigida internamente.</span><span class="sxs-lookup"><span data-stu-id="46124-958">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="46124-959">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-959">Fixed</span></span>

- <span data-ttu-id="46124-960">Agora, todas as sessões de bash devem ser criadas no mesmo nível de permissão.</span><span class="sxs-lookup"><span data-stu-id="46124-960">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="46124-961">Tentativa de iniciar uma sessão em um nível diferente será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="46124-961">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="46124-962">Isso significa que os consoles de administrador e não-administrador não pode ser executado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="46124-962">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="46124-963">(#626 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-963">(GH #626)</span></span>
<br/>
- <span data-ttu-id="46124-964">Implementado as seguintes mensagens NETLINK_ROUTE (requer o administrador do Windows)</span><span class="sxs-lookup"><span data-stu-id="46124-964">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="46124-965">RTM_NEWADDR (dá suporte a `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="46124-965">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="46124-966">RTM_NEWROUTE (dá suporte a `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="46124-966">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="46124-967">RTM_DELADDR (dá suporte a `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="46124-967">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="46124-968">RTM_DELROUTE (supports `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="46124-968">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="46124-969">Tarefa agendada, verificação de pacotes atualizar não serão mais executados em uma conexão limitada (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="46124-969">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="46124-970">Corrigido o erro em que canalizar obtém isto é, paralisada bash - c "ls - alR /" | bash -c "gato" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="46124-970">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="46124-971">Opção de soquete TCP_KEEPCNT implementada (GH #843)</span><span class="sxs-lookup"><span data-stu-id="46124-971">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="46124-972">Opção de soquete IP_MTU_DISCOVER INET implementada (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="46124-972">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="46124-973">Removida a funcionalidade herdada para executar binários de NT de init com pesquisa de caminho do NT.</span><span class="sxs-lookup"><span data-stu-id="46124-973">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="46124-974">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="46124-974">(GH #1325)</span></span>
- <span data-ttu-id="46124-975">Corrigir o modo de desenvolvimento/kmsg para permitir o acesso de leitura do grupo / (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="46124-975">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="46124-976">/Proc/sys/kernel/random/uuid implementado (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="46124-976">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="46124-977">Corrigido o erro em que a hora de início do processo estava mostrando como ano 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="46124-977">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="46124-978">Variável de ambiente de termo padrão comutada para xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="46124-978">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="46124-979">Modificado da maneira que o processo de confirmação é calculada durante a bifurcação do processo.</span><span class="sxs-lookup"><span data-stu-id="46124-979">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="46124-980">(#1286 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-980">(GH #1286)</span></span>
- <span data-ttu-id="46124-981">/Proc/sys/vm/overcommit_memory implementado.</span><span class="sxs-lookup"><span data-stu-id="46124-981">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="46124-982">(#1286 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-982">(GH #1286)</span></span>
- <span data-ttu-id="46124-983">Arquivo /proc/net/route implementado (GH #69)</span><span class="sxs-lookup"><span data-stu-id="46124-983">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="46124-984">Correção de erro em que o nome do atalho foi incorretamente localizado (GH #696)</span><span class="sxs-lookup"><span data-stu-id="46124-984">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="46124-985">Elf fixa analisando a lógica que valida incorretamente os cabeçalhos do programa deve ser menor que (ou igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="46124-985">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="46124-986">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="46124-986">(GH #1048)</span></span>
- <span data-ttu-id="46124-987">Retorno de chamada statfs implementado para procfs, sysfs, cgroupfs e binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="46124-987">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="46124-988">Windows AptPackageIndexUpdate fixo que não será fechado (1184 de # GH, também são discutidas em GH #1193)</span><span class="sxs-lookup"><span data-stu-id="46124-988">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="46124-989">Personalidade ASLR adicionada suporte ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="46124-989">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="46124-990">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="46124-990">(GH #1148, 1128)</span></span>
- <span data-ttu-id="46124-991">PTRACE_GETSIGINFO aprimorada, SIGSEGV para rastreamentos de pilha do gdb adequado durante AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="46124-991">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="46124-992">ELF, não há mais de análise falha por patchelf binários.</span><span class="sxs-lookup"><span data-stu-id="46124-992">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="46124-993">(#471 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-993">(GH #471)</span></span>
- <span data-ttu-id="46124-994">VPN DNS propagadas para /etc/resolv.conf (GH #416 1350)</span><span class="sxs-lookup"><span data-stu-id="46124-994">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="46124-995">Feche o melhorias para TCP mais confiável para transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="46124-995">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="46124-996">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="46124-996">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="46124-997">Código de erro correto agora retornam quando há muitos arquivos abertos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="46124-997">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="46124-998">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="46124-998">(GH #1126, 2090)</span></span>
- <span data-ttu-id="46124-999">Auditoria do Windows agora relatórios de log de nome de imagem no processo de criar uma auditoria.</span><span class="sxs-lookup"><span data-stu-id="46124-999">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="46124-1000">Normalmente falham ao iniciar bash.exe de dentro de uma janela de bash</span><span class="sxs-lookup"><span data-stu-id="46124-1000">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="46124-1001">Mensagem de erro adicionado ao interoperabilidade não consegue acessar um diretório de trabalho em LxFs (ou seja, notepad.exe. bashrc)</span><span class="sxs-lookup"><span data-stu-id="46124-1001">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="46124-1002">Corrigido um problema em que o caminho do Windows foi truncado no WSL</span><span class="sxs-lookup"><span data-stu-id="46124-1002">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="46124-1003">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1003">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1004">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1004">LTP Results:</span></span>
<span data-ttu-id="46124-1005">Número de aprovação no teste: 690</span><span class="sxs-lookup"><span data-stu-id="46124-1005">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="46124-1006">Número de falha (com falha, ignorada, etc...): 274</span><span class="sxs-lookup"><span data-stu-id="46124-1006">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="46124-1007">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1007">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="46124-1008">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1008">Syscall Support</span></span>
<span data-ttu-id="46124-1009">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1009">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1010">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1010">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="46124-1011">Compilação 14986</span><span class="sxs-lookup"><span data-stu-id="46124-1011">Build 14986</span></span>

<span data-ttu-id="46124-1012">Para Windows geral informações sobre compilação 14986, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-1012">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1013">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1013">Fixed</span></span>

- <span data-ttu-id="46124-1014">Verificações de bugs fixas com Netlink e Pty IOCTLs</span><span class="sxs-lookup"><span data-stu-id="46124-1014">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="46124-1015">Versão do kernel agora relata 4.4.0-43 para manter a consistência com Xenial</span><span class="sxs-lookup"><span data-stu-id="46124-1015">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="46124-1016">Bash.exe agora inicia quando a entrada direcionada para ' nul:' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="46124-1016">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="46124-1017">IDs de thread agora é relatada corretamente no procfs (GH 967 de #)</span><span class="sxs-lookup"><span data-stu-id="46124-1017">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="46124-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Sinalizadores IN_ISDIR agora têm suportados no inotify_add_watch() (GH 1280 de #)</span><span class="sxs-lookup"><span data-stu-id="46124-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="46124-1019">Implemente timer_create e chamadas do sistema relacionados.</span><span class="sxs-lookup"><span data-stu-id="46124-1019">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="46124-1020">Isso habilita o suporte GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="46124-1020">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="46124-1021">Corrigido um problema em que o ping retornado um tempo de 0.000ms (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="46124-1021">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="46124-1022">Retorne o código de erro correta quando muitos arquivos são abertos.</span><span class="sxs-lookup"><span data-stu-id="46124-1022">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="46124-1023">Problema corrigido no WSL em que a solicitação Netlink para dados de interface de rede falharia com EINVAL se o endereço da interface hardware for 32-bytes (como a interface Teredo)</span><span class="sxs-lookup"><span data-stu-id="46124-1023">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="46124-1024">Observe que o utilitário Linux "ip" contém um bug em que ele falhará se WSL relata um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="46124-1024">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="46124-1025">Este é um bug no "ip", não WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1025">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="46124-1026">O "ip" utilitário embute o comprimento do buffer de cadeia de caracteres usado para imprimir o endereço de hardware, e esse buffer for muito pequeno para imprimir um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="46124-1026">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="46124-1027">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1027">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1028">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1028">LTP Results:</span></span>
<span data-ttu-id="46124-1029">Número de aprovação no teste: 669</span><span class="sxs-lookup"><span data-stu-id="46124-1029">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="46124-1030">Número de falha (com falha, ignorada, etc...): 258</span><span class="sxs-lookup"><span data-stu-id="46124-1030">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="46124-1031">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1031">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="46124-1032">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1032">Syscall Support</span></span>
<span data-ttu-id="46124-1033">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1033">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1034">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1034">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="46124-1035">Compilação 14971</span><span class="sxs-lookup"><span data-stu-id="46124-1035">Build 14971</span></span>

<span data-ttu-id="46124-1036">Para Windows geral informações sobre compilação 14971, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-1036">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1037">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1037">Fixed</span></span>

 - <span data-ttu-id="46124-1038">Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="46124-1038">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="46124-1039">As atualizações agendadas regularmente serão retomada na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="46124-1039">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1040">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1040">LTP Results:</span></span>
<span data-ttu-id="46124-1041">Inalterado desde 14965</span><span class="sxs-lookup"><span data-stu-id="46124-1041">Unchanged from 14965</span></span> </br>
<span data-ttu-id="46124-1042">Número de aprovação no teste: 664</span><span class="sxs-lookup"><span data-stu-id="46124-1042">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="46124-1043">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="46124-1043">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46124-1044">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1044">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="46124-1045">Compilação 14965</span><span class="sxs-lookup"><span data-stu-id="46124-1045">Build 14965</span></span>

<span data-ttu-id="46124-1046">Para Windows geral informações sobre compilação 14965, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-1046">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1047">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1047">Fixed</span></span>

- <span data-ttu-id="46124-1048">Suporte para Netlink soquetes do protocolo NETLINK_ROUTE RTM_GETLINK e RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="46124-1048">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="46124-1049">Habilita comandos de ifconfig e ip para enumeração de rede</span><span class="sxs-lookup"><span data-stu-id="46124-1049">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="46124-1050">Mais informações podem ser encontradas no nosso [postagem de blog de rede WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="46124-1050">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="46124-1051">/sbin agora está no caminho do usuário por padrão</span><span class="sxs-lookup"><span data-stu-id="46124-1051">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="46124-1052">Caminho de usuário NT agora anexado ao caminho WSL por padrão (ou seja, você pode agora digitar notepad.exe sem adicionar System32 para o caminho do Linux)</span><span class="sxs-lookup"><span data-stu-id="46124-1052">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="46124-1053">Suporte adicionado para /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="46124-1053">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="46124-1054">Binários do NT agora pode ser iniciados no WSL quando o diretório de trabalho atual contém caracteres não-ansi (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="46124-1054">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="46124-1055">Permitir desligamento em soquete de fluxo de unix desconectado.</span><span class="sxs-lookup"><span data-stu-id="46124-1055">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="46124-1056">Adicionado suporte para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="46124-1056">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="46124-1057">Suporte adicionado para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="46124-1057">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="46124-1058">Corrigido o erro em que canalizar obtém isto é, paralisada bash - c "ls - alR /" | bash -c "gato" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="46124-1058">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="46124-1059">Tratar solicitações para se conectar ao terminal atual.</span><span class="sxs-lookup"><span data-stu-id="46124-1059">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="46124-1060">Marcar /proc/.<pid>/oom_score_adj como gravável.</span><span class="sxs-lookup"><span data-stu-id="46124-1060">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="46124-1061">Adicione pasta /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="46124-1061">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="46124-1062">sched_setaffinity deverá retornar o número de máscara de bits de afinidade</span><span class="sxs-lookup"><span data-stu-id="46124-1062">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="46124-1063">Corrija a lógica de validação ELF que assume incorretamente os caminhos de interpretador devem ter menos de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="46124-1063">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="46124-1064">(#743 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-1064">(GH #743)</span></span>
- <span data-ttu-id="46124-1065">Descritores de arquivo aberto podem manter a janela do console aberta (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="46124-1065">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="46124-1066">Erro de Fixeed onde Rename () falhou com barra no nome de destino (GH #1008) à direita</span><span class="sxs-lookup"><span data-stu-id="46124-1066">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="46124-1067">Implementar /proc/net/dev arquivo</span><span class="sxs-lookup"><span data-stu-id="46124-1067">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="46124-1068">Fixo 0.000ms executa ping devido à resolução do timer.</span><span class="sxs-lookup"><span data-stu-id="46124-1068">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="46124-1069">/Proc/self/environ implementado (GH #730)</span><span class="sxs-lookup"><span data-stu-id="46124-1069">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="46124-1070">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1070">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1071">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1071">LTP Results:</span></span>
<span data-ttu-id="46124-1072">Número de aprovação no teste: 664</span><span class="sxs-lookup"><span data-stu-id="46124-1072">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="46124-1073">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="46124-1073">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46124-1074">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1074">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="46124-1075">Compilação 14959</span><span class="sxs-lookup"><span data-stu-id="46124-1075">Build 14959</span></span>

<span data-ttu-id="46124-1076">Para Windows geral informações sobre compilação 14959, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="46124-1076">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1077">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1077">Fixed</span></span>

- <span data-ttu-id="46124-1078">Notificação aprimorada do processo de Pico para Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-1078">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="46124-1079">Informações adicionais de [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="46124-1079">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="46124-1080">Maior estabilidade com a interoperabilidade do Windows</span><span class="sxs-lookup"><span data-stu-id="46124-1080">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="46124-1081">Correção de erro 0x80070057 ao iniciar bash.exe quando o Enterprise Data Protection (EDP) está habilitado</span><span class="sxs-lookup"><span data-stu-id="46124-1081">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="46124-1082">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1082">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1083">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1083">LTP Results:</span></span>
<span data-ttu-id="46124-1084">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="46124-1084">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46124-1085">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="46124-1085">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46124-1086">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1086">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="46124-1087">Compilação 14955</span><span class="sxs-lookup"><span data-stu-id="46124-1087">Build 14955</span></span>

<span data-ttu-id="46124-1088">Para Windows geral informações sobre compilação 14955, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="46124-1088">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1089">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1089">Fixed</span></span>

 - <span data-ttu-id="46124-1090">Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="46124-1090">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="46124-1091">As atualizações agendadas regularmente serão retomada na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="46124-1091">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1092">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1092">LTP Results:</span></span>
<span data-ttu-id="46124-1093">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="46124-1093">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46124-1094">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="46124-1094">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46124-1095">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1095">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="46124-1096">Compilação 14951</span><span class="sxs-lookup"><span data-stu-id="46124-1096">Build 14951</span></span>

<span data-ttu-id="46124-1097">Para Windows geral informações sobre compilação 14951, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-1097">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="46124-1098">Novo recurso: Windows / interoperabilidade do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="46124-1098">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="46124-1099">Binários do Windows agora podem ser chamados diretamente da linha de comando WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1099">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="46124-1100">Isso fornece aos usuários a capacidade de interagir com seu ambiente do Windows e o sistema de forma que não foi possível.</span><span class="sxs-lookup"><span data-stu-id="46124-1100">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="46124-1101">Como um exemplo rápido, é possível que os usuários executem os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="46124-1101">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="46124-1102">Mais informações podem ser encontradas em:</span><span class="sxs-lookup"><span data-stu-id="46124-1102">More information can be found at:</span></span>

- [<span data-ttu-id="46124-1103">Blog da equipe do WSL para interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="46124-1103">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="46124-1104">Documentação de interoperabilidade do MSDN</span><span class="sxs-lookup"><span data-stu-id="46124-1104">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="46124-1105">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1105">Fixed</span></span>

- <span data-ttu-id="46124-1106">Ubuntu 16.04 (Xenial) agora está instalado para todas as novas instâncias WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1106">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="46124-1107">Os usuários com as instâncias (confiáveis) 14.04 existentes não serão atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="46124-1107">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="46124-1108">Localidade definida durante a instalação agora é exibida.</span><span class="sxs-lookup"><span data-stu-id="46124-1108">Locale set during install is now displayed</span></span>
- <span data-ttu-id="46124-1109">Melhorias de terminal, incluindo o bug em que o redirecionamento de um processo WSL para um arquivo faz nem sempre funcionam</span><span class="sxs-lookup"><span data-stu-id="46124-1109">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="46124-1110">Tempo de vida do console deve ser vinculado ao tempo de vida de bash.exe</span><span class="sxs-lookup"><span data-stu-id="46124-1110">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="46124-1111">Tamanho da janela de console deve usar tamanho visível, o tamanho do buffer não</span><span class="sxs-lookup"><span data-stu-id="46124-1111">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="46124-1112">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1112">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1113">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1113">LTP Results:</span></span>
<span data-ttu-id="46124-1114">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="46124-1114">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46124-1115">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="46124-1115">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46124-1116">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1116">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="46124-1117">Compilação 14946</span><span class="sxs-lookup"><span data-stu-id="46124-1117">Build 14946</span></span>

<span data-ttu-id="46124-1118">Para Windows geral informações sobre compilação 14946, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="46124-1118">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1119">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1119">Fixed</span></span>

- <span data-ttu-id="46124-1120">Corrigido um problema que impediu a criação de contas de usuário do WSL para usuários com nomes de usuário do NT que contêm espaços ou aspas.</span><span class="sxs-lookup"><span data-stu-id="46124-1120">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="46124-1121">Alterar VolFs e DrvFs para retornar 0 para a contagem de links do diretório em stat</span><span class="sxs-lookup"><span data-stu-id="46124-1121">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="46124-1122">Suporte à opção de soquete IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="46124-1122">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="46124-1123">Limite a um único console loop de e/s por tty.</span><span class="sxs-lookup"><span data-stu-id="46124-1123">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="46124-1124">Exemplo: o comando a seguir é possível:</span><span class="sxs-lookup"><span data-stu-id="46124-1124">Example: the following command is possible:</span></span>
  - <span data-ttu-id="46124-1125">bash -c "dados echo" | bash - c "ssh user@example.com ' cat > foo '"</span><span class="sxs-lookup"><span data-stu-id="46124-1125">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="46124-1126">Substitua os espaços por guias no /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="46124-1126">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="46124-1127">DrvFs agora aparece no mountinfo com um nome que corresponde ao volume montado do Windows</span><span class="sxs-lookup"><span data-stu-id="46124-1127">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="46124-1128">/Home e raiz agora aparecem no mountinfo com nomes corretos</span><span class="sxs-lookup"><span data-stu-id="46124-1128">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="46124-1129">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1129">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1130">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1130">LTP Results:</span></span>
<span data-ttu-id="46124-1131">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="46124-1131">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46124-1132">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="46124-1132">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46124-1133">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1133">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="46124-1134">Compilação 14942</span><span class="sxs-lookup"><span data-stu-id="46124-1134">Build 14942</span></span>

<span data-ttu-id="46124-1135">Para Windows geral informações sobre compilação 14942, visite o [Blog Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="46124-1135">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1136">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1136">Fixed</span></span>

- <span data-ttu-id="46124-1137">Um número de verificações de bugs resolvidos, incluindo o "TENTATIVA de executar de /NOEXECUTE memória" rede falha que foi bloqueando SSH</span><span class="sxs-lookup"><span data-stu-id="46124-1137">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="46124-1138">o suporte para notificações geradas de aplicativos do Windows em DrvFs inotifiy está agora</span><span class="sxs-lookup"><span data-stu-id="46124-1138">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="46124-1139">Implemente TCP_KEEPIDLE e TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="46124-1139">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="46124-1140">(#695 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-1140">(GH #695)</span></span>
- <span data-ttu-id="46124-1141">Implementar a chamada do sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="46124-1141">Implement the pivot_root system call</span></span>
- <span data-ttu-id="46124-1142">Implementar a opção de soquete para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="46124-1142">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="46124-1143">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1143">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="46124-1144">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1144">LTP Results:</span></span>
<span data-ttu-id="46124-1145">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="46124-1145">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46124-1146">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="46124-1146">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46124-1147">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1147">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="46124-1148">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1148">Syscall Support</span></span>
<span data-ttu-id="46124-1149">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1149">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1150">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1150">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="46124-1151">Compilação 14936</span><span class="sxs-lookup"><span data-stu-id="46124-1151">Build 14936</span></span>

<span data-ttu-id="46124-1152">Para Windows geral informações sobre compilação 14936, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-1152">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="46124-1153">Observação: WSL instalará Ubuntu versão 16.04 (Xenial) em vez do Ubuntu 14.04 (confiável) em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="46124-1153">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="46124-1154">Essa alteração será aplicada para Insiders instalar novas instâncias (lxrun.exe /install ou primeira execução do bash.exe).</span><span class="sxs-lookup"><span data-stu-id="46124-1154">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="46124-1155">As instâncias existentes com e confiável não serão atualizadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="46124-1155">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="46124-1156">Os usuários podem atualizar suas imagens confiáveis para Xenial usando o comando de atualização de versão.</span><span class="sxs-lookup"><span data-stu-id="46124-1156">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="46124-1157">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="46124-1157">Known Issue</span></span>
<span data-ttu-id="46124-1158">WSL está enfrentando um problema com algumas implementações de soquete.</span><span class="sxs-lookup"><span data-stu-id="46124-1158">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="46124-1159">A verificação de erro se manifesta como uma falha com o erro "TENTATIVA de executar /NOEXECUTE memória INSUFICIENTE".</span><span class="sxs-lookup"><span data-stu-id="46124-1159">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="46124-1160">A manifestação mais comum desse problema é uma falha ao usar o ssh.</span><span class="sxs-lookup"><span data-stu-id="46124-1160">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="46124-1161">A causa raiz é fixo em compilações internas e será enviada para Insiders assim que possível.</span><span class="sxs-lookup"><span data-stu-id="46124-1161">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="46124-1162">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1162">Fixed</span></span>

- <span data-ttu-id="46124-1163">Implementado a chamada do sistema chroot</span><span class="sxs-lookup"><span data-stu-id="46124-1163">Implemented the chroot system call</span></span>
- <span data-ttu-id="46124-1164">Melhorias no inotify ~~incluindo suporte para notificações geradas de aplicativos do Windows em DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="46124-1164">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="46124-1165">Correção: Inotify dá suporte para alterações originadas a partir de aplicativos do Windows não está disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1165">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="46124-1166">Associação de IPv6 de soquete::<port n> agora dá suporte a IPV6_V6ONLY (GH #68, 157 #, #393, 460 #, #674, 740 #, #982, 996 #)</span><span class="sxs-lookup"><span data-stu-id="46124-1166">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="46124-1167">Comportamento WNOWAIT para waitid systemcall implementado (GH #638)</span><span class="sxs-lookup"><span data-stu-id="46124-1167">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="46124-1168">Suporte para opções de soquete IP IP_HDRINCL e IP_TTL</span><span class="sxs-lookup"><span data-stu-id="46124-1168">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="46124-1169">Read () de comprimento zero deve retornar imediatamente (GH #975)</span><span class="sxs-lookup"><span data-stu-id="46124-1169">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="46124-1170">Tratar corretamente os prefixos de nomes de arquivo e o nome do arquivo que não incluem um terminador nulo em um arquivo. tar.</span><span class="sxs-lookup"><span data-stu-id="46124-1170">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="46124-1171">suporte a epoll o /dev/null</span><span class="sxs-lookup"><span data-stu-id="46124-1171">epoll support for /dev/null</span></span>
- <span data-ttu-id="46124-1172">Corrigir a fonte de tempo /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="46124-1172">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="46124-1173">Bash -c agora capaz de redirecionar para um arquivo</span><span class="sxs-lookup"><span data-stu-id="46124-1173">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="46124-1174">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1174">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1175">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1175">LTP Results:</span></span>
<span data-ttu-id="46124-1176">Número de aprovação no teste: 664</span><span class="sxs-lookup"><span data-stu-id="46124-1176">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="46124-1177">Número de falha (com falha, ignorada, etc...): 264</span><span class="sxs-lookup"><span data-stu-id="46124-1177">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="46124-1178">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1178">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="46124-1179">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1179">Syscall Support</span></span>
<span data-ttu-id="46124-1180">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1180">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1181">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1181">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="46124-1182">Compilação 14931</span><span class="sxs-lookup"><span data-stu-id="46124-1182">Build 14931</span></span>

<span data-ttu-id="46124-1183">Para Windows geral informações sobre compilação 14931, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-1183">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1184">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1184">Fixed</span></span>

 - <span data-ttu-id="46124-1185">Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="46124-1185">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="46124-1186">As atualizações agendadas regularmente serão retomada na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="46124-1186">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="46124-1187">Compilação 14926</span><span class="sxs-lookup"><span data-stu-id="46124-1187">Build 14926</span></span>

<span data-ttu-id="46124-1188">Para Windows geral informações sobre compilação 14926, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-1188">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1189">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1189">Fixed</span></span>

- <span data-ttu-id="46124-1190">Ping agora funciona em consoles que não têm privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="46124-1190">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="46124-1191">Ping6 agora tem suportada, também sem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="46124-1191">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="46124-1192">Suporte de Inotify para arquivos modificados por meio de WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1192">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="46124-1193">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="46124-1193">(GH #216)</span></span>
  - <span data-ttu-id="46124-1194">Sinalizadores com suporte:</span><span class="sxs-lookup"><span data-stu-id="46124-1194">Flags supported:</span></span>
    - <span data-ttu-id="46124-1195">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="46124-1195">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="46124-1196">eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="46124-1196">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="46124-1197">atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="46124-1197">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="46124-1198">ler a saída: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="46124-1198">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="46124-1199">Problema conhecido: Modificar arquivos de aplicativos do Windows não gera nenhum evento</span><span class="sxs-lookup"><span data-stu-id="46124-1199">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="46124-1200">Soquete do UNIX agora dá suporte a SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="46124-1200">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46124-1201">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="46124-1201">LTP Results:</span></span>
<span data-ttu-id="46124-1202">Número de aprovação no teste: 651</span><span class="sxs-lookup"><span data-stu-id="46124-1202">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="46124-1203">Número de falha (com falha, ignorada, etc...): 258</span><span class="sxs-lookup"><span data-stu-id="46124-1203">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="46124-1204">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="46124-1204">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="46124-1205">Compilação 14915</span><span class="sxs-lookup"><span data-stu-id="46124-1205">Build 14915</span></span>

<span data-ttu-id="46124-1206">Para Windows geral informações sobre compilação 14915, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="46124-1206">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1207">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1207">Fixed</span></span>
-  <span data-ttu-id="46124-1208">Socketpair para soquetes de datagrama (GH #262) do unix</span><span class="sxs-lookup"><span data-stu-id="46124-1208">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="46124-1209">Suporte de soquete do UNIX para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="46124-1209">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="46124-1210">Suporte de soquete do UNIX para SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="46124-1210">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="46124-1211">Suporte de soquete do UNIX para SOCK_SEQPACKET (GH #758 546 #)</span><span class="sxs-lookup"><span data-stu-id="46124-1211">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="46124-1212">Adicionando suporte para envio de soquete de datagrama de unix, recebimento e desligamento</span><span class="sxs-lookup"><span data-stu-id="46124-1212">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="46124-1213">Corrija a verificação de erro devido à validação de parâmetro inválido mmap para endereços não fixos.</span><span class="sxs-lookup"><span data-stu-id="46124-1213">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="46124-1214">(#847 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-1214">(GH #847)</span></span>
- <span data-ttu-id="46124-1215">Suporte para suspender / retomar de estados de terminal</span><span class="sxs-lookup"><span data-stu-id="46124-1215">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="46124-1216">Suporte para TIOCPKT ioctl desbloquear o utilitário de tela (GH #774)</span><span class="sxs-lookup"><span data-stu-id="46124-1216">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="46124-1217">Problema conhecido: Teclas de função não operacionais</span><span class="sxs-lookup"><span data-stu-id="46124-1217">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="46124-1218">Corrigida uma corrida no TimerFd que poderia causar um membro liberado ReaderReady seja acessada por LxpTimerFdWorkerRoutine (GH #814)</span><span class="sxs-lookup"><span data-stu-id="46124-1218">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="46124-1219">Habilitar o suporte de chamada do sistema reinicializável para futex, sondagem e clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="46124-1219">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="46124-1220">Suporte de montagem de associação adicionado</span><span class="sxs-lookup"><span data-stu-id="46124-1220">Added bind mount support</span></span>
- <span data-ttu-id="46124-1221">remover o compartilhamento para oferecer suporte ao namespace de montagem</span><span class="sxs-lookup"><span data-stu-id="46124-1221">unshare for mount namespace support</span></span>
    - <span data-ttu-id="46124-1222">Problema conhecido: Ao criar um novo namespace de montagem com `unshare(CLONE_NEWNS)` diretório de trabalho atual continuará apontar para o namespace antigo</span><span class="sxs-lookup"><span data-stu-id="46124-1222">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="46124-1223">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="46124-1223">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="46124-1224">Compilação 14905</span><span class="sxs-lookup"><span data-stu-id="46124-1224">Build 14905</span></span>

<span data-ttu-id="46124-1225">Para Windows geral informações sobre compilação 14905, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-1225">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1226">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1226">Fixed</span></span>
- <span data-ttu-id="46124-1227">Sistema reinicializável chamadas agora são suportado (GH #349 GH #520)</span><span class="sxs-lookup"><span data-stu-id="46124-1227">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="46124-1228">Links simbólicos para diretórios terminando em / agora operacionais (GH #650)</span><span class="sxs-lookup"><span data-stu-id="46124-1228">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="46124-1229">Implementado ioctl RNDGETENTCNT para /dev/random</span><span class="sxs-lookup"><span data-stu-id="46124-1229">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="46124-1230">Implementado o /proc/. [pid] / monta /proc/. [pid] / mountinfo e /proc/. [pid] / mountstats arquivos</span><span class="sxs-lookup"><span data-stu-id="46124-1230">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="46124-1231">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1231">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="46124-1232">Compilação 14901</span><span class="sxs-lookup"><span data-stu-id="46124-1232">Build 14901</span></span>
<span data-ttu-id="46124-1233">Primeiro Insider build para a versão de atualização de aniversário do Windows 10 de postagem.</span><span class="sxs-lookup"><span data-stu-id="46124-1233">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="46124-1234">Para Windows geral informações sobre compilação 14901, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-1234">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1235">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1235">Fixed</span></span>
- <span data-ttu-id="46124-1236">Corrigido o problema de barra "/" à direita</span><span class="sxs-lookup"><span data-stu-id="46124-1236">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="46124-1237">Comandos como `$ mv a/c/ a/b/` agora funciona</span><span class="sxs-lookup"><span data-stu-id="46124-1237">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="46124-1238">Instalando agora solicita se Ubuntu localidade deve ser definida como localidade do Windows</span><span class="sxs-lookup"><span data-stu-id="46124-1238">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="46124-1239">Procfs suporte para a pasta de ns</span><span class="sxs-lookup"><span data-stu-id="46124-1239">Procfs support for ns folder</span></span>
- <span data-ttu-id="46124-1240">Adicionado a montagem e desmontagem para tmpfs, procfs e sistemas de arquivos sysfs</span><span class="sxs-lookup"><span data-stu-id="46124-1240">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="46124-1241">Corrigir mknod [arroba], assinatura ABI de 32 bits</span><span class="sxs-lookup"><span data-stu-id="46124-1241">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="46124-1242">Movido para o modelo de expedição de soquetes do UNIX</span><span class="sxs-lookup"><span data-stu-id="46124-1242">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="46124-1243">Tamanho do buffer de recebimento INET soquete definido usando o setsockopt deveria ser respeitado.</span><span class="sxs-lookup"><span data-stu-id="46124-1243">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="46124-1244">Sinalizador de mensagem de recebimento de soquete do unix MSG_CMSG_CLOEXEC implementar</span><span class="sxs-lookup"><span data-stu-id="46124-1244">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="46124-1245">Redirecionamento de pipe de stdin/stdout de processo do Linux (GH n º 2)</span><span class="sxs-lookup"><span data-stu-id="46124-1245">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="46124-1246">Permite que o pipe de comandos de bash - c no CMD.</span><span class="sxs-lookup"><span data-stu-id="46124-1246">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="46124-1247">Exemplo: > dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="46124-1247">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="46124-1248">Bash agora pode ser instalado em sistemas com vários arquivos de paginação (GH #538 358 #)</span><span class="sxs-lookup"><span data-stu-id="46124-1248">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="46124-1249">Tamanho do buffer de soquete INET padrão deve corresponder da configuração padrão do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="46124-1249">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="46124-1250">Alinhar syscalls xattr para listxattr</span><span class="sxs-lookup"><span data-stu-id="46124-1250">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="46124-1251">Retornar apenas as interfaces com um endereço IPv4 válido de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="46124-1251">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="46124-1252">Corrigir a ação padrão de sinal quando injetado por ptrace</span><span class="sxs-lookup"><span data-stu-id="46124-1252">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="46124-1253">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="46124-1253">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="46124-1254">Use os valores do registro de contexto de máquina ao restaurar o contexto no sigreturn</span><span class="sxs-lookup"><span data-stu-id="46124-1254">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="46124-1255">Isso resolve o problema em que o java e javac foram deslocado para alguns usuários</span><span class="sxs-lookup"><span data-stu-id="46124-1255">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="46124-1256">Implementar /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="46124-1256">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46124-1257">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1257">Syscall Support</span></span>
<span data-ttu-id="46124-1258">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1258">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1259">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1259">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="46124-1260">Compilar 14388 para atualização de aniversário do Windows 10</span><span class="sxs-lookup"><span data-stu-id="46124-1260">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="46124-1261">Para Windows geral informações sobre compilação 14388, visite o [Blog Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="46124-1261">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46124-1262">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1262">Fixed</span></span>
- <span data-ttu-id="46124-1263">Correções para se preparar para a atualização de aniversário do Windows 10 em 8/2</span><span class="sxs-lookup"><span data-stu-id="46124-1263">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="46124-1264">Para obter mais informações sobre como o WSL na atualização de aniversário podem ser encontradas em nossa [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="46124-1264">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="46124-1265">Compilação 14376</span><span class="sxs-lookup"><span data-stu-id="46124-1265">Build 14376</span></span>
<span data-ttu-id="46124-1266">Para Windows geral informações sobre compilação 14376, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="46124-1266">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46124-1267">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1267">Fixed</span></span>
- <span data-ttu-id="46124-1268">Removido algumas instâncias em que o apt-get trava (GH #493)</span><span class="sxs-lookup"><span data-stu-id="46124-1268">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="46124-1269">Corrigido um problema em que as montagens vazias não foram tratadas corretamente</span><span class="sxs-lookup"><span data-stu-id="46124-1269">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="46124-1270">Corrigido um problema em que ramdisks não foram montados corretamente</span><span class="sxs-lookup"><span data-stu-id="46124-1270">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="46124-1271">Aceitação de soquete do unix de alteração para dar suporte a sinalizadores (parcial GH #451)</span><span class="sxs-lookup"><span data-stu-id="46124-1271">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="46124-1272">Fixo de rede comuns relacionadas a tela azul</span><span class="sxs-lookup"><span data-stu-id="46124-1272">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="46124-1273">Corrigido o bluescreen ao acessar /proc/. [pid] / tarefa (GH #523)</span><span class="sxs-lookup"><span data-stu-id="46124-1273">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="46124-1274">Fixo alta utilização da CPU para alguns cenários pty (GH 488 #, #504)</span><span class="sxs-lookup"><span data-stu-id="46124-1274">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="46124-1275">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1275">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="46124-1276">Compilação 14371</span><span class="sxs-lookup"><span data-stu-id="46124-1276">Build 14371</span></span>
<span data-ttu-id="46124-1277">Para Windows geral informações sobre compilação 14371, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="46124-1277">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46124-1278">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1278">Fixed</span></span>
- <span data-ttu-id="46124-1279">Corrigida a corrida de medição de tempo com SIGCHLD e wait() ao usar ptrace</span><span class="sxs-lookup"><span data-stu-id="46124-1279">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="46124-1280">Corrigidos alguns comportamentos quando os caminhos têm à direita / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="46124-1280">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="46124-1281">Corrigido o problema com a renomeação/desvincular falhando devido a identificadores abertos para crianças</span><span class="sxs-lookup"><span data-stu-id="46124-1281">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="46124-1282">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1282">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="46124-1283">Compilação 14366</span><span class="sxs-lookup"><span data-stu-id="46124-1283">Build 14366</span></span>
<span data-ttu-id="46124-1284">Para Windows geral informações sobre compilação 14366, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="46124-1284">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46124-1285">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1285">Fixed</span></span>
- <span data-ttu-id="46124-1286">Corrigir na criação do arquivo por meio de links simbólicos</span><span class="sxs-lookup"><span data-stu-id="46124-1286">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="46124-1287">Adicionado listxattr para Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="46124-1287">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="46124-1288">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1288">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46124-1289">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1289">Syscall Support</span></span>
-   <span data-ttu-id="46124-1290">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1290">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1291">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1291">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="46124-1292">O build 14361</span><span class="sxs-lookup"><span data-stu-id="46124-1292">Build 14361</span></span>
<span data-ttu-id="46124-1293">Para Windows geral informações no build 14361, visite o [Blog Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="46124-1293">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46124-1294">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1294">Fixed</span></span>
- <span data-ttu-id="46124-1295">DrvFs agora diferencia maiusculas de minúsculas quando em execução no Bash no Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-1295">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="46124-1296">Os usuários case.txt de maio e caso. Unidades de TXT no seu c/dev/emcpowera1</span><span class="sxs-lookup"><span data-stu-id="46124-1296">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="46124-1297">Somente há suporte para a diferenciação de maiusculas dentro do Bash no Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-1297">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="46124-1298">Quando fora do NTFS Bash relatará corretamente os arquivos, mas um comportamento inesperado pode ocorrer a interação com os arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="46124-1298">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="46124-1299">A raiz de cada volume (ou seja, /mnt/c) não diferencia maiusculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="46124-1299">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="46124-1300">Para obter mais informações sobre como tratar esses arquivos no Windows podem ser encontradas [aqui](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="46124-1300">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="46124-1301">Aperfeiçoou pty / tty suporte.</span><span class="sxs-lookup"><span data-stu-id="46124-1301">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="46124-1302">Aplicativos como TMUX agora tem suporte (GH n º 40)</span><span class="sxs-lookup"><span data-stu-id="46124-1302">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="46124-1303">Problema de instalação fixa em que contas de usuário criadas nem sempre</span><span class="sxs-lookup"><span data-stu-id="46124-1303">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="46124-1304">Estrutura de arg de linha de comando, permitindo a lista de argumentos muitíssimo otimizada.</span><span class="sxs-lookup"><span data-stu-id="46124-1304">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="46124-1305">(#153 GH)</span><span class="sxs-lookup"><span data-stu-id="46124-1305">(GH #153)</span></span>
- <span data-ttu-id="46124-1306">Arquivos de read_only agora capaz de excluir e chmod de DrvFs</span><span class="sxs-lookup"><span data-stu-id="46124-1306">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="46124-1307">Corrigidos alguns casos onde a terminal trava na desconexão (GH n º 43)</span><span class="sxs-lookup"><span data-stu-id="46124-1307">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="46124-1308">chmod e alterar o proprietário agora funcionam em dispositivos de tty</span><span class="sxs-lookup"><span data-stu-id="46124-1308">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="46124-1309">Permitir a conexão para 0.0.0.0 e:: como localhost (GH 388)</span><span class="sxs-lookup"><span data-stu-id="46124-1309">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="46124-1310">Sendmsg/recvmsg agora lidar com um comprimento do vetor de e/s de > 1 (parcial GH #376)</span><span class="sxs-lookup"><span data-stu-id="46124-1310">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="46124-1311">Os usuários podem agora recusá-la do arquivo de hosts gerada automaticamente (GH #398)</span><span class="sxs-lookup"><span data-stu-id="46124-1311">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="46124-1312">A correspondência automática de localidade do Linux para a localidade do NT durante a instalação (GH #11)</span><span class="sxs-lookup"><span data-stu-id="46124-1312">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="46124-1313">Adicionado o arquivo /proc/sys/vm/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="46124-1313">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="46124-1314">strace agora é encerrado corretamente</span><span class="sxs-lookup"><span data-stu-id="46124-1314">strace now exits correctly</span></span>
- <span data-ttu-id="46124-1315">Permitir que os pipes para ser reaberto por meio de /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="46124-1315">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="46124-1316">Ocultar diretórios sob %LOCALAPPDATA%\lxss de DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="46124-1316">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="46124-1317">Melhor tratamento de bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="46124-1317">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="46124-1318">Comandos como "bash ~ ls - c" agora tem suporte (GH #467)</span><span class="sxs-lookup"><span data-stu-id="46124-1318">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="46124-1319">Soquetes agora notificar epoll leitura disponível durante o desligamento (GH #271)</span><span class="sxs-lookup"><span data-stu-id="46124-1319">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="46124-1320">lxrun / desinstalação faz um trabalho melhor de excluir os arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="46124-1320">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="46124-1321">Corrigido ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="46124-1321">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="46124-1322">Suporte aprimorado para x11 aplicativos como xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="46124-1322">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="46124-1323">Atualizado o tamanho de pilha do thread inicial para corresponder à configuração do Ubuntu padrão e informar o tamanho corretamente para o syscall get_rlimit (GH 172 #, #258)</span><span class="sxs-lookup"><span data-stu-id="46124-1323">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="46124-1324">Relatórios de nomes de imagem de processo de pico (por exemplo, para fazer auditoria) aprimorados</span><span class="sxs-lookup"><span data-stu-id="46124-1324">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="46124-1325">/Proc/mountinfo implementado para o comando df</span><span class="sxs-lookup"><span data-stu-id="46124-1325">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="46124-1326">Correção de código de erro de symlink para o nome do filho.</span><span class="sxs-lookup"><span data-stu-id="46124-1326">Fixed symlink error code for child name .</span></span> <span data-ttu-id="46124-1327">e...</span><span class="sxs-lookup"><span data-stu-id="46124-1327">and ..</span></span>
- <span data-ttu-id="46124-1328">Melhorias e correções de bug de aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1328">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46124-1329">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1329">Syscall Support</span></span>
<span data-ttu-id="46124-1330">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1330">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1331">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1331">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="46124-1332">Build 14352</span><span class="sxs-lookup"><span data-stu-id="46124-1332">Build 14352</span></span>
<span data-ttu-id="46124-1333">Para Windows geral informações no build 14352, visite o [Blog Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="46124-1333">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46124-1334">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1334">Fixed</span></span>
- <span data-ttu-id="46124-1335">Correção do problema em que grandes arquivos não foram baixados / criados corretamente.</span><span class="sxs-lookup"><span data-stu-id="46124-1335">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="46124-1336">Isso deve desbloquear npm e outros cenários (GH n º 3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="46124-1336">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="46124-1337">Removido algumas instâncias onde soquetes de suspensão</span><span class="sxs-lookup"><span data-stu-id="46124-1337">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="46124-1338">Corrigidos alguns erros ptrace</span><span class="sxs-lookup"><span data-stu-id="46124-1338">Corrected some ptrace errors</span></span>
- <span data-ttu-id="46124-1339">Corrigido o problema com o WSL, permitindo que mais de 255 caracteres de nomes de arquivo</span><span class="sxs-lookup"><span data-stu-id="46124-1339">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="46124-1340">Suporte aprimorado para caracteres estendidos</span><span class="sxs-lookup"><span data-stu-id="46124-1340">Improved support for non-English characters</span></span>
- <span data-ttu-id="46124-1341">Adicionar dados de fuso horário atual do Windows e definir como padrão</span><span class="sxs-lookup"><span data-stu-id="46124-1341">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="46124-1342">Do id exclusiva do dispositivo para cada ponto de montagem (fix jre – GH n º 49)</span><span class="sxs-lookup"><span data-stu-id="46124-1342">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="46124-1343">Corrigir problema com caminhos que contenham "."</span><span class="sxs-lookup"><span data-stu-id="46124-1343">Correct issue with paths containing “.”</span></span> <span data-ttu-id="46124-1344">e ".."</span><span class="sxs-lookup"><span data-stu-id="46124-1344">and “..”</span></span>
- <span data-ttu-id="46124-1345">Adicionado suporte Fifo (GH #71)</span><span class="sxs-lookup"><span data-stu-id="46124-1345">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="46124-1346">Formato atualizado do resolv. conf para corresponder ao formato nativo do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="46124-1346">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="46124-1347">Uma limpeza procfs</span><span class="sxs-lookup"><span data-stu-id="46124-1347">Some procfs cleanup</span></span>
- <span data-ttu-id="46124-1348">Ping habilitado para consoles do administrador (GH n º 18)</span><span class="sxs-lookup"><span data-stu-id="46124-1348">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46124-1349">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1349">Syscall Support</span></span>
<span data-ttu-id="46124-1350">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1351">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="46124-1352">Compilação 14342</span><span class="sxs-lookup"><span data-stu-id="46124-1352">Build 14342</span></span>
<span data-ttu-id="46124-1353">Para Windows geral informações sobre compilação 14342 a [Blog Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="46124-1353">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="46124-1354">Informações sobre VolFs e DriveFs podem ser encontradas na [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="46124-1354">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46124-1355">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1355">Fixed</span></span>
- <span data-ttu-id="46124-1356">Corrigido o problema de instalação quando o usuário do Windows tinha caracteres Unicode no nome de usuário</span><span class="sxs-lookup"><span data-stu-id="46124-1356">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="46124-1357">A solução alternativa udev de atualização de apt-get nas perguntas Frequentes agora é fornecida por padrão na primeira execução</span><span class="sxs-lookup"><span data-stu-id="46124-1357">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="46124-1358">Habilitada a links simbólicos no DriveFs (/mnt/<drive>) diretórios</span><span class="sxs-lookup"><span data-stu-id="46124-1358">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="46124-1359">Links simbólicos agora funcionam entre DriveFs e VolFs</span><span class="sxs-lookup"><span data-stu-id="46124-1359">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="46124-1360">Caminho de nível superior endereçado ao problema de análise: ls. / / agora funcionará conforme o esperado</span><span class="sxs-lookup"><span data-stu-id="46124-1360">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="46124-1361">instalar o NPM em DriveFs e as opções -g agora estão trabalhando</span><span class="sxs-lookup"><span data-stu-id="46124-1361">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="46124-1362">Problema corrigido, impedindo que o servidor PHP iniciando</span><span class="sxs-lookup"><span data-stu-id="46124-1362">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="46124-1363">Valores de ambiente padrão atualizado, como $PATH para corresponder mais próximos Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="46124-1363">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="46124-1364">Adicionada uma tarefa de manutenção semanal no Windows para atualizar o cache de pacotes apt</span><span class="sxs-lookup"><span data-stu-id="46124-1364">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="46124-1365">Corrigido um problema com a validação de cabeçalho ELF, WSL agora dá suporte a todas as opções de Melkor</span><span class="sxs-lookup"><span data-stu-id="46124-1365">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="46124-1366">Shell zsh é funcional</span><span class="sxs-lookup"><span data-stu-id="46124-1366">Zsh shell is functional</span></span>
- <span data-ttu-id="46124-1367">Agora há suporte para os binários pré-compilados do Go</span><span class="sxs-lookup"><span data-stu-id="46124-1367">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="46124-1368">Avisar sobre Bash.exe executado pela primeira vez agora está localizado corretamente</span><span class="sxs-lookup"><span data-stu-id="46124-1368">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="46124-1369">/proc/meminfo agora retorna informações corretas</span><span class="sxs-lookup"><span data-stu-id="46124-1369">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="46124-1370">Soquetes agora têm suportados no VFS</span><span class="sxs-lookup"><span data-stu-id="46124-1370">Sockets now supported in VFS</span></span>
- <span data-ttu-id="46124-1371">/dev agora montado como tempfs</span><span class="sxs-lookup"><span data-stu-id="46124-1371">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="46124-1372">PEPS agora tem suportada</span><span class="sxs-lookup"><span data-stu-id="46124-1372">Fifo now supported</span></span>
- <span data-ttu-id="46124-1373">Sistemas de vários núcleos agora mostrando corretamente em/proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="46124-1373">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="46124-1374">Melhorias adicionais e mensagens de erro de download durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="46124-1374">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="46124-1375">Syscall melhorias e correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="46124-1375">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="46124-1376">Syscall com suporte a lista abaixo.</span><span class="sxs-lookup"><span data-stu-id="46124-1376">Supported syscall list below.</span></span>
- <span data-ttu-id="46124-1377">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1377">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="46124-1378">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="46124-1378">Known Issues</span></span>
- <span data-ttu-id="46124-1379">Não Resolvendo '.. '</span><span class="sxs-lookup"><span data-stu-id="46124-1379">Not resolving ‘..’</span></span> <span data-ttu-id="46124-1380">corretamente em DriveFs em alguns casos</span><span class="sxs-lookup"><span data-stu-id="46124-1380">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46124-1381">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1381">Syscall Support</span></span>
<span data-ttu-id="46124-1382">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1382">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46124-1383">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1383">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="46124-1384">Compilação 14332</span><span class="sxs-lookup"><span data-stu-id="46124-1384">Build 14332</span></span>

<span data-ttu-id="46124-1385">Para Windows geral informações sobre compilação 14332, visite o [Blog Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="46124-1385">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="46124-1386">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1386">Fixed</span></span>
- <span data-ttu-id="46124-1387">Melhor geração de resolv. conf, incluindo a priorizar as entradas DNS</span><span class="sxs-lookup"><span data-stu-id="46124-1387">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="46124-1388">Problema com a movimentação de arquivos e diretórios entre /mnt e não- / mnt unidades</span><span class="sxs-lookup"><span data-stu-id="46124-1388">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="46124-1389">Os arquivos tar agora podem ser criados com links simbólicos</span><span class="sxs-lookup"><span data-stu-id="46124-1389">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="46124-1390">Diretório de /run/lock padrão adicionados na criação da instância</span><span class="sxs-lookup"><span data-stu-id="46124-1390">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="46124-1391">Atualizar o /dev/null para retornar informações de stat adequada</span><span class="sxs-lookup"><span data-stu-id="46124-1391">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="46124-1392">Erros adicionais durante o download durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="46124-1392">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="46124-1393">Syscall melhorias e correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="46124-1393">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="46124-1394">Syscall com suporte a lista abaixo.</span><span class="sxs-lookup"><span data-stu-id="46124-1394">Supported syscall list below.</span></span>
- <span data-ttu-id="46124-1395">Melhorias e correções de bug de aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1395">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46124-1396">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1396">Syscall Support</span></span>
<span data-ttu-id="46124-1397">Abaixo está a nova syscall que tem alguma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1397">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="46124-1398">O syscall nesta lista tem suporte pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1398">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="46124-1399">Build 14328</span><span class="sxs-lookup"><span data-stu-id="46124-1399">Build 14328</span></span>

<span data-ttu-id="46124-1400">Para Windows geral informações sobre compilação 14332, visite o [Blog Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="46124-1400">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="46124-1401">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="46124-1401">New Features</span></span>
* <span data-ttu-id="46124-1402">Agora dão suporte a usuários do Linux.</span><span class="sxs-lookup"><span data-stu-id="46124-1402">Now support Linux users.</span></span>  <span data-ttu-id="46124-1403">Instalação do Bash no Ubuntu no Windows solicitará que para a criação de um usuário do Linux.</span><span class="sxs-lookup"><span data-stu-id="46124-1403">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="46124-1404">Para obter mais informações, visite https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="46124-1404">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="46124-1405">Nome do host agora está definido para o nome do computador Windows, não há mais @localhost</span><span class="sxs-lookup"><span data-stu-id="46124-1405">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="46124-1406">Para obter mais informações sobre build 14328, visite: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="46124-1406">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="46124-1407">Fixo</span><span class="sxs-lookup"><span data-stu-id="46124-1407">Fixed</span></span>
* <span data-ttu-id="46124-1408">Melhorias de symlink para /mnt/ não<drive> arquivos</span><span class="sxs-lookup"><span data-stu-id="46124-1408">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="46124-1409">instalação de NPM agora funciona</span><span class="sxs-lookup"><span data-stu-id="46124-1409">npm install now works</span></span>
    * <span data-ttu-id="46124-1410">JDK / jre agora pode ser instalado usando as instruções encontradas [aqui](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="46124-1410">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="46124-1411">problema conhecido: links simbólicos não funcionam para o Windows monta.</span><span class="sxs-lookup"><span data-stu-id="46124-1411">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="46124-1412">Funcionalidade estará disponível em uma compilação posterior</span><span class="sxs-lookup"><span data-stu-id="46124-1412">Functionality will be available in a later build</span></span>
* <span data-ttu-id="46124-1413">parte superior e htop agora exibem</span><span class="sxs-lookup"><span data-stu-id="46124-1413">top and htop now display</span></span>
* <span data-ttu-id="46124-1414">Mensagens de erro adicionais para algumas falhas de instalação</span><span class="sxs-lookup"><span data-stu-id="46124-1414">Additional error messages for some install failures</span></span>
* <span data-ttu-id="46124-1415">Syscall melhorias e correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="46124-1415">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="46124-1416">Syscall com suporte a lista abaixo.</span><span class="sxs-lookup"><span data-stu-id="46124-1416">Supported syscall list below.</span></span>
* <span data-ttu-id="46124-1417">Melhorias e correções de bug de aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="46124-1417">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46124-1418">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="46124-1418">Syscall Support</span></span>
<span data-ttu-id="46124-1419">Abaixo está uma lista de syscalls com alguma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="46124-1419">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="46124-1420">Syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="46124-1420">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
