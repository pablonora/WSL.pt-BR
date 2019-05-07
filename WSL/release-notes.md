---
title: Notas de versão do subsistema do Windows para Linux
description: Notas de versão para o subsistema Windows para Linux.  Atualizada semanalmente.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 2567e68ca0e9897a7b7bc7315760b81ff4923c1a
ms.sourcegitcommit: 8c74868b8d8ff0106e15e4bce5e8337642883ec1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2019
ms.locfileid: "64988259"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="9e1a8-105">Notas de versão do subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="9e1a8-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18890"></a><span data-ttu-id="9e1a8-106">Compilação 18890</span><span class="sxs-lookup"><span data-stu-id="9e1a8-106">Build 18890</span></span>
<span data-ttu-id="9e1a8-107">Para Windows geral informações sobre compilação 18890, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-107">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-108">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-108">WSL</span></span>
* <span data-ttu-id="9e1a8-109">Vazamento de soquete sem bloqueio [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-109">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="9e1a8-110">Entrada EOF para o terminal pode bloquear as leituras subsequentes [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-110">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="9e1a8-111">Atualize resolv. conf cabeçalho para se referir a wsl.conf [discutidos GH 3928]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-111">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="9e1a8-112">Um deadlock no código de exclusão epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-112">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="9e1a8-113">Lidar com espaços em argumentos para-- importar e – exportar [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-113">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="9e1a8-114">Estendendo mmap arquivos não funciona corretamente [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-114">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="9e1a8-115">Corrigir o problema com o ARM64 \\acesso de $ wsl não está funcionando corretamente</span><span class="sxs-lookup"><span data-stu-id="9e1a8-115">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="9e1a8-116">Adicionar um ícone padrão melhor wsl.exe</span><span class="sxs-lookup"><span data-stu-id="9e1a8-116">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="9e1a8-117">Compilação 18342</span><span class="sxs-lookup"><span data-stu-id="9e1a8-117">Build 18342</span></span>
<span data-ttu-id="9e1a8-118">Para Windows geral informações sobre compilação 18342, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-118">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-119">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-119">WSL</span></span>
* <span data-ttu-id="9e1a8-120">Adicionamos a capacidade dos usuários acessar os arquivos do Linux em uma distribuição WSL do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-120">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="9e1a8-121">Esses arquivos podem ser acessados por meio da linha de comando e também aplicativos do Windows, como o Explorador de arquivos, VSCode, etc. podem interagir com esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-121">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="9e1a8-122">Acessar seus arquivos, navegando até \\ \\$ wsl\\< distro_name >, ou ver uma lista de execução de distribuições, navegando até \\ \\$ wsl</span><span class="sxs-lookup"><span data-stu-id="9e1a8-122">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="9e1a8-123">Adicionar marcas de informações adicionais de CPU e corrigir os valores de Cpus_allowed [ lista] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-123">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="9e1a8-124">Suporte a execução de thread não líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-124">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="9e1a8-125">Tratar falhas de atualização de configuração como não-fatais [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-125">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="9e1a8-126">Atualizar binfmt para lidar adequadamente com deslocamentos [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-126">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="9e1a8-127">Habilitar o mapeamento unidades de rede para planejar 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-127">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="9e1a8-128">Suporte ao Windows -> Linux e tradução de caminho do Windows para montagens -> do Linux</span><span class="sxs-lookup"><span data-stu-id="9e1a8-128">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="9e1a8-129">Criar seções somente leitura para mapeamentos em arquivos abertos somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e1a8-129">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="9e1a8-130">Compilação 18334</span><span class="sxs-lookup"><span data-stu-id="9e1a8-130">Build 18334</span></span>
<span data-ttu-id="9e1a8-131">Para Windows geral informações sobre compilação 18334, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-131">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-132">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-132">WSL</span></span>
* <span data-ttu-id="9e1a8-133">Reestruturação da maneira que a zona de tempo do Windows é mapeada para um fuso horário do Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-133">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="9e1a8-134">Corrigir vazamentos de memória e adicionar novas funções de conversão de cadeia de caracteres [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-134">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="9e1a8-135">SIGCONT em um threadgroup sem threads é não operacional [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-135">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="9e1a8-136">Exibir corretamente os descritores de arquivo de soquete e epoll em /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="9e1a8-136">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="9e1a8-137">Compilação 18305</span><span class="sxs-lookup"><span data-stu-id="9e1a8-137">Build 18305</span></span>
<span data-ttu-id="9e1a8-138">Para Windows geral informações sobre compilação 18305, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-138">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-139">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-139">WSL</span></span>
* <span data-ttu-id="9e1a8-140">pthreads perder o acesso aos arquivos quando o thread primário é encerrado [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-140">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="9e1a8-141">TIOCSCTTY deve ignorar o parâmetro "force", a menos que seja necessário [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-141">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="9e1a8-142">aprimoramentos de linha de comando wsl.exe e adição de importação / exportação de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-142">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="9e1a8-143">Compilação 18277</span><span class="sxs-lookup"><span data-stu-id="9e1a8-143">Build 18277</span></span>
<span data-ttu-id="9e1a8-144">Para Windows geral informações sobre compilação 18277, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-144">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-145">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-145">WSL</span></span>
* <span data-ttu-id="9e1a8-146">Corrigir o erro "nenhuma interface deste tipo suportada" apresentado na compilação 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-146">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="9e1a8-147">Ignorar o sinalizador de MNT_FORCE unmount syscall [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-147">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="9e1a8-148">Alternar a interoperabilidade do WSL para usar a API oficial do CreatePseudoConsole</span><span class="sxs-lookup"><span data-stu-id="9e1a8-148">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="9e1a8-149">Não manter nenhum valor de tempo limite quando FUTEX_WAIT é reiniciado</span><span class="sxs-lookup"><span data-stu-id="9e1a8-149">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="9e1a8-150">Compilação 18272</span><span class="sxs-lookup"><span data-stu-id="9e1a8-150">Build 18272</span></span>
<span data-ttu-id="9e1a8-151">Para Windows geral informações sobre compilação 18272, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-151">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-152">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-152">WSL</span></span>
* <span data-ttu-id="9e1a8-153">**AVISO:** Há um problema nesta compilação que faz o WSL inoperável.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-153">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="9e1a8-154">Ao tentar iniciar sua distribuição, você verá um erro "Nenhuma interface deste tipo suportada".</span><span class="sxs-lookup"><span data-stu-id="9e1a8-154">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="9e1a8-155">O problema foi corrigido e estará no build Insider rápido da próxima semana.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-155">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="9e1a8-156">Se você tiver instalado essa compilação, você pode reverter para a compilação anterior do Windows usando "Ir para a versão anterior do Windows 10" nas configurações -> atualização de & segurança -> Recovery.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-156">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="9e1a8-157">Compilação 18267</span><span class="sxs-lookup"><span data-stu-id="9e1a8-157">Build 18267</span></span>
<span data-ttu-id="9e1a8-158">Para Windows geral informações sobre compilação 18267, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-158">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-159">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-159">WSL</span></span>
* <span data-ttu-id="9e1a8-160">Corrija o problema em que o processo zumbi não pode ser reaped e permanecerão enfileirados indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-160">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="9e1a8-161">WslRegisterDistribution trava se a mensagem de erro excede o tamanho máximo [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-161">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="9e1a8-162">Permitir fsync bem-sucedido para arquivos somente leitura em DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-162">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="9e1a8-163">Certifique-se de que pastas /bin e /sbin existem antes de criar links simbólicos dentro de [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-163">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="9e1a8-164">Adicionado um mecanismo de tempo limite de encerramento de instância para instâncias WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-164">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="9e1a8-165">Atualmente, o limite é definido como 15 segundos, que significa que a instância será encerrada 15 segundos após o último processo WSL é encerrado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-165">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="9e1a8-166">Para encerrar uma distribuição imediatamente, use:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-166">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="9e1a8-167">Compilar 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-167">Build 17763 (1809)</span></span>
<span data-ttu-id="9e1a8-168">Para Windows geral informações sobre compilação 17763, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-168">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-169">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-169">WSL</span></span>
* <span data-ttu-id="9e1a8-170">Verificação de permissão de syscall SetPriority muito restrita para alterar a prioridade do thread mesmo [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-170">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="9e1a8-171">Certifique-se de que o tempo de interrupção não polarizada é usado para o tempo de inicialização para evitar o retorno de valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-171">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="9e1a8-172">Tratar links simbólicos no interpretador WSL binfmt [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-172">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="9e1a8-173">Melhor tratamento de limpeza de descritor de arquivo threadgroup líder.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-173">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="9e1a8-174">Alternar WSL usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter de kernel para evitar estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-174">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="9e1a8-175">Ptrace conexão pode fazer com que o valor de retorno incorreto de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-175">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="9e1a8-176">Correção relacionada AF_UNIX vários problemas [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-176">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="9e1a8-177">Correção do problema que poderia causar a interoperabilidade do WSL falhar se o diretório de trabalho atual é menor que 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-177">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="9e1a8-178">Evitar um atraso de segundo, as conexões de loopback às portas não existente [GH 3286] com falha</span><span class="sxs-lookup"><span data-stu-id="9e1a8-178">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="9e1a8-179">Adicionar arquivo de stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-179">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="9e1a8-180">Informações mais precisas do escopo de IPV6.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-180">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="9e1a8-181">Suporte PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-181">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="9e1a8-182">Sistema de arquivos do pipe limpando inadvertidamente o evento de borda disparada epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-182">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="9e1a8-183">Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-183">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="9e1a8-184">Melhor suporte de zumbi [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-184">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="9e1a8-185">Adicionar entradas de wsl.conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-185">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="9e1a8-186">Correção para getsockname nem sempre retornar o tipo de família do soquete UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-186">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="9e1a8-187">Adicionar suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-187">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="9e1a8-188">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-188">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="9e1a8-189">Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-189">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="9e1a8-190">Corrigir o problema na pasta raiz [GH 3304] de verificação de permissão</span><span class="sxs-lookup"><span data-stu-id="9e1a8-190">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="9e1a8-191">Suporte limitado para TTY teclado ioctls KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-191">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="9e1a8-192">Aplicativos de interface do usuário do Windows devem ser executado mesmo quando iniciado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-192">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="9e1a8-193">Adicione a opção wsl -u ou --usuário [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-193">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="9e1a8-194">Corrigir problemas de inicialização WSL inicialização rápida está habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-194">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="9e1a8-195">Soquetes do UNIX precisam manter credenciais de par desconectada [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-195">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="9e1a8-196">Soquetes do Unix sem-bloqueio apresentando indefinidamente EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-196">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="9e1a8-197">Caso = off, é os novo drvfs padrão [2937 de GH, 3212, 3328] do tipo de montagem</span><span class="sxs-lookup"><span data-stu-id="9e1a8-197">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="9e1a8-198">Ver [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-198">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="9e1a8-199">Adicionar wslconfig / encerrar para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-199">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="9e1a8-200">Corrigi o problema com o contexto de shell WSL entradas de menu que não tratar corretamente os caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-200">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="9e1a8-201">Expor diferenciação por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="9e1a8-201">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="9e1a8-202">ARM64: Emule as operações de manutenção do cache.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-202">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="9e1a8-203">Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-203">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="9e1a8-204">DrvFs: unescape apenas caracteres no intervalo particular que correspondem ao caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-204">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="9e1a8-205">Corrigir o erro off-by-one na validação de comprimento ELF analisador interpretador [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-205">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="9e1a8-206">Temporizadores WSL absolutos com um tempo no passado não disparam [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-206">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="9e1a8-207">Certifique-se recentemente de arquivos esparsos criados estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-207">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="9e1a8-208">Atomicamente Crie diretórios diferencia maiusculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-208">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="9e1a8-209">Foi corrigido um problema adicional em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-209">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="9e1a8-210">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-210">[GH 2712]</span></span>
* <span data-ttu-id="9e1a8-211">WSL fixa inicie falha quando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-211">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="9e1a8-212">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-212">[GH 3020]</span></span>
* <span data-ttu-id="9e1a8-213">Adicione menu de contexto do explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-213">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="9e1a8-214">Para usar, mantenha a tecla shift e clique com botão direito quando estiver em uma janela do explorer.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-214">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="9e1a8-215">Corrigir o comportamento de não bloqueio de soquete Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-215">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="9e1a8-216">Correção de travamento comando NETLINK conforme relatado na 2026 GH.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-216">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="9e1a8-217">Adicione suporte para sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-217">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="9e1a8-218">Corrigi o problema com eventos de inotify não causam truncamento [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-218">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="9e1a8-219">Adicione--opção de exec para wsl.exe invocar um binário único sem um shell.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-219">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="9e1a8-220">Adicione--opção de distribuição para wsl.exe selecionar uma distribuição específica.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-220">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="9e1a8-221">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-221">Limited support for dmesg.</span></span> <span data-ttu-id="9e1a8-222">Aplicativos agora podem fazer dmesg.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-222">Applications can now log to dmesg.</span></span> <span data-ttu-id="9e1a8-223">Driver WSL registra informações limitadas dmesg.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-223">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="9e1a8-224">No futuro, isso pode ser estendido para executar outro informações/diagnóstico do driver.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-224">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="9e1a8-225">Observação: dmesg é suportado atualmente por meio de `/dev/kmsg` interface de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-225">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="9e1a8-226">`syslog` ainda não há suporte para a interface de syscall.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-226">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="9e1a8-227">E, portanto, algumas da `dmesg` opções de linha de comando como `-S`, `-C` não funcionam.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-227">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="9e1a8-228">Alterar gid padrão e o modo de dispositivos seriais para corresponder nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-228">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="9e1a8-229">DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-229">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="9e1a8-230">Observação: DrvFs tem algumas limitações no nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-230">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="9e1a8-231">Alguns caracteres (como '/', ':' e '\*') não são permitido e estendidos nomes de atributo não diferenciam maiusculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-231">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="9e1a8-232">Compilação 18252 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-232">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="9e1a8-233">Para Windows geral informações sobre compilação 18252, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-233">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-234">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-234">WSL</span></span>
* <span data-ttu-id="9e1a8-235">Mova os binários de init e bsdtar fora lxssmanager dll e em uma pasta de ferramentas separadas</span><span class="sxs-lookup"><span data-stu-id="9e1a8-235">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="9e1a8-236">Corrigir a corrida em torno de fechar o descritor de arquivo ao usar CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="9e1a8-236">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="9e1a8-237">Lidar com campos opcionais no /proc/pid/mountinfo ao traduzir DrvFs caminhos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-237">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="9e1a8-238">Permitir mknod DrvFs seja bem-sucedida sem suporte de metadados para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="9e1a8-238">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="9e1a8-239">Arquivos somente leitura criados em DrvFs devem ter o atributo somente leitura definido [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-239">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="9e1a8-240">Adicionar /sbin/mount.drvfs auxiliar para lidar com a montagem de DrvFs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-240">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="9e1a8-241">Use DrvFs renomeação POSIX.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-241">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="9e1a8-242">Permita a tradução de caminho em volumes sem um GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-242">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="9e1a8-243">Compilar 17738 (rápida)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-243">Build 17738 (Fast)</span></span>
<span data-ttu-id="9e1a8-244">Para Windows geral informações sobre compilação 17738, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-244">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-245">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-245">WSL</span></span>
* <span data-ttu-id="9e1a8-246">Verificação de permissão de syscall SetPriority muito restrita para alterar a prioridade do thread mesmo [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-246">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="9e1a8-247">Certifique-se de que o tempo de interrupção não polarizada é usado para o tempo de inicialização para evitar o retorno de valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-247">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="9e1a8-248">Tratar links simbólicos no interpretador WSL binfmt [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-248">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="9e1a8-249">Melhor tratamento de limpeza de descritor de arquivo threadgroup líder.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-249">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="9e1a8-250">Compilar 17728 (rápida)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-250">Build 17728 (Fast)</span></span>
<span data-ttu-id="9e1a8-251">Para Windows geral informações sobre compilação 17728, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-251">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-252">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-252">WSL</span></span>
* <span data-ttu-id="9e1a8-253">Alternar WSL usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter de kernel para evitar estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-253">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="9e1a8-254">Ptrace conexão pode fazer com que o valor de retorno incorreto de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-254">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="9e1a8-255">Correção de a que um número de AF_UNIX relacionadas problemas [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-255">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="9e1a8-256">Correção do problema que poderia causar a interoperabilidade do WSL falhar se o diretório de trabalho atual é menor que 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-256">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="9e1a8-257">Compilação 18204 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-257">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="9e1a8-258">Para Windows geral informações sobre compilação 18204, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-258">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-259">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-259">WSL</span></span>
* <span data-ttu-id="9e1a8-260">Redirecionar inadvertenly de sistema de arquivos, limpando o evento de borda disparada epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-260">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="9e1a8-261">Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-261">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="9e1a8-262">Compilar 17723 (rápida)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-262">Build 17723 (Fast)</span></span>
<span data-ttu-id="9e1a8-263">Para Windows geral informações sobre compilação 17723, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-263">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-264">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-264">WSL</span></span>
* <span data-ttu-id="9e1a8-265">Evitar um atraso de segundo, as conexões de loopback às portas não existente [GH 3286] com falha</span><span class="sxs-lookup"><span data-stu-id="9e1a8-265">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="9e1a8-266">Adicionar arquivo de stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-266">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="9e1a8-267">Informações mais precisas do escopo de IPV6.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-267">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="9e1a8-268">Suporte PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-268">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="9e1a8-269">Redirecionar inadvertenly de sistema de arquivos, limpando o evento de borda disparada epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="9e1a8-270">Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="9e1a8-271">Compilação 17713</span><span class="sxs-lookup"><span data-stu-id="9e1a8-271">Build 17713</span></span>
<span data-ttu-id="9e1a8-272">Para Windows geral informações sobre compilação 17713, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-272">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-273">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-273">WSL</span></span>
* <span data-ttu-id="9e1a8-274">Melhor suporte de zumbi [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-274">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="9e1a8-275">Adicionar entradas de wsl.conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-275">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="9e1a8-276">Correção para getsockname nem sempre retornar o tipo de família do soquete UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-276">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="9e1a8-277">Adicionar suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-277">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="9e1a8-278">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-278">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="9e1a8-279">Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-279">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="9e1a8-280">Corrigir o problema na pasta raiz [GH 3304] de verificação de permissão</span><span class="sxs-lookup"><span data-stu-id="9e1a8-280">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="9e1a8-281">Suporte limitado para TTY teclado ioctls KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-281">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="9e1a8-282">Aplicativos de interface do usuário do Windows devem ser executado mesmo quando iniciado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-282">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="9e1a8-283">Compilação 17704</span><span class="sxs-lookup"><span data-stu-id="9e1a8-283">Build 17704</span></span>
<span data-ttu-id="9e1a8-284">Para Windows geral informações sobre compilação 17704, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-284">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-285">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-285">WSL</span></span>
* <span data-ttu-id="9e1a8-286">Adicione a opção wsl -u ou --usuário [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-286">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="9e1a8-287">Corrigir problemas de inicialização WSL inicialização rápida está habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-287">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="9e1a8-288">Soquetes do UNIX precisam manter credenciais de par desconectada [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-288">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="9e1a8-289">Soquetes do Unix sem-bloqueio apresentando indefinidamente EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-289">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="9e1a8-290">Caso = off, é os novo drvfs padrão [2937 de GH, 3212, 3328] do tipo de montagem</span><span class="sxs-lookup"><span data-stu-id="9e1a8-290">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="9e1a8-291">Ver [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-291">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="9e1a8-292">Adicionar wslconfig / encerrar para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-292">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="9e1a8-293">Build 17692</span><span class="sxs-lookup"><span data-stu-id="9e1a8-293">Build 17692</span></span>
<span data-ttu-id="9e1a8-294">Para Windows geral informações sobre compilação 17692, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-294">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-295">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-295">WSL</span></span>
* <span data-ttu-id="9e1a8-296">Corrigi o problema com o contexto de shell WSL entradas de menu que não tratar corretamente os caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-296">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="9e1a8-297">Expor diferenciação por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="9e1a8-297">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="9e1a8-298">ARM64: Emule as operações de manutenção do cache.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-298">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="9e1a8-299">Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-299">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="9e1a8-300">DrvFs: unescape apenas caracteres no intervalo particular que correspondem ao caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-300">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="9e1a8-301">Build 17686</span><span class="sxs-lookup"><span data-stu-id="9e1a8-301">Build 17686</span></span>
<span data-ttu-id="9e1a8-302">Para Windows geral informações sobre compilação 17686, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-302">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-303">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-303">WSL</span></span>
* <span data-ttu-id="9e1a8-304">Corrigir o erro off-by-one na validação de comprimento ELF analisador interpretador [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-304">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="9e1a8-305">Temporizadores WSL absolutos com um tempo no passado não disparam [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-305">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="9e1a8-306">Certifique-se recentemente de arquivos esparsos criados estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-306">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="9e1a8-307">Atomicamente Crie diretórios diferencia maiusculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-307">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="9e1a8-308">Compilação 17677</span><span class="sxs-lookup"><span data-stu-id="9e1a8-308">Build 17677</span></span>
<span data-ttu-id="9e1a8-309">Para Windows geral informações sobre compilação 17677, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-309">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-310">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-310">WSL</span></span>
* <span data-ttu-id="9e1a8-311">Foi corrigido um problema adicional em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-311">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="9e1a8-312">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-312">[GH 2712]</span></span>
* <span data-ttu-id="9e1a8-313">WSL fixa inicie falha quando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-313">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="9e1a8-314">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-314">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="9e1a8-315">Compilação 17666</span><span class="sxs-lookup"><span data-stu-id="9e1a8-315">Build 17666</span></span>
<span data-ttu-id="9e1a8-316">Para Windows geral informações sobre compilação 17666, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-316">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-317">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-317">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="9e1a8-318">AVISO: Há um problema, impedindo que o WSL seja executado em alguns chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-318">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="9e1a8-319">Uma correção está pronto e fazendo seu caminho para o branch de Build do Insider.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-319">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="9e1a8-320">Adicione menu de contexto do explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-320">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="9e1a8-321">Para usar shift espera e o botão direito do mouse quando estiver em uma janela do explorer.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-321">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="9e1a8-322">Corrigir o comportamento de não bloqueio de soquete unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-322">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="9e1a8-323">Correção de travamento comando NETLINK conforme relatado na 2026 GH.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-323">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="9e1a8-324">Adicione suporte para sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-324">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="9e1a8-325">Corrigi o problema com eventos de inotify não causam truncamento [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-325">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="9e1a8-326">Adicione--opção de exec para wsl.exe invocar um binário único sem um shell.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-326">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="9e1a8-327">Adicione--opção de distribuição para wsl.exe selecionar uma distribuição específica.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-327">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="9e1a8-328">Compilação 17655 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-328">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="9e1a8-329">Para Windows geral informações sobre compilação 17655, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-329">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-330">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-330">WSL</span></span>
* <span data-ttu-id="9e1a8-331">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-331">Limited support for dmesg.</span></span> <span data-ttu-id="9e1a8-332">Aplicativos agora podem fazer dmesg.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-332">Applications can now log to dmesg.</span></span> <span data-ttu-id="9e1a8-333">Driver WSL registra informações limitadas dmesg.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-333">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="9e1a8-334">No futuro, isso pode ser estendido para executar outro informações/diagnóstico do driver.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-334">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="9e1a8-335">Observação: dmesg é suportado atualmente por meio de `/dev/kmsg` interface de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-335">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="9e1a8-336">`syslog` ainda não há suporte para a interface sycall.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-336">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="9e1a8-337">E, portanto, algumas da `dmesg` opções de linha de comando como `-S`, `-C` não funcionam.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-337">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="9e1a8-338">Corrigido um problema em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-338">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="9e1a8-339">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-339">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="9e1a8-340">Compilação 17639 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-340">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="9e1a8-341">Para Windows geral informações sobre compilação 17639, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-341">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-342">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-342">WSL</span></span>
* <span data-ttu-id="9e1a8-343">Alterar gid padrão e o modo de dispositivos seriais para corresponder nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-343">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="9e1a8-344">DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-344">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="9e1a8-345">Observação: DrvFs tem algumas limitações no nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-345">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="9e1a8-346">Em particular, alguns caracteres (como '/', ':' e '\*') não são permitido e estendidos nomes de atributo não diferenciam maiusculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-346">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="9e1a8-347">Compilar 17133 (rápida)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-347">Build 17133 (Fast)</span></span>
<span data-ttu-id="9e1a8-348">Para Windows geral informações sobre compilação 17133, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-348">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-349">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-349">WSL</span></span>
* <span data-ttu-id="9e1a8-350">Correção de suspensão no WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-350">Fix for hang in WSL.</span></span> <span data-ttu-id="9e1a8-351">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-351">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="9e1a8-352">Compilar 17128 (rápida)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-352">Build 17128 (Fast)</span></span>
<span data-ttu-id="9e1a8-353">Para Windows geral informações sobre compilação 17128, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-353">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-354">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-354">WSL</span></span>
* <span data-ttu-id="9e1a8-355">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9e1a8-355">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="9e1a8-356">Compilação 17627 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-356">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="9e1a8-357">Para Windows geral informações sobre compilação 17627, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-357">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-358">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-358">WSL</span></span>
* <span data-ttu-id="9e1a8-359">Adicione suporte para as operações de reconhecimento de pi futex.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-359">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="9e1a8-360">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-360">[GH 1006]</span></span>
    * <span data-ttu-id="9e1a8-361">Observe que as prioridades não são atualmente suporte para o recurso WSL portanto, há limitações, mas o uso padrão deve ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-361">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="9e1a8-362">Suporte ao firewall do Windows para processos WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-362">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="9e1a8-363">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-363">[GH 1852]</span></span>
    * <span data-ttu-id="9e1a8-364">Por exemplo, para permitir que o WSL python processar para escutar em qualquer porta, use o cmd do Windows com privilégios elevados: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="9e1a8-364">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="9e1a8-365">Para obter detalhes adicionais sobre como adicionar regras de firewall, consulte [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-365">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="9e1a8-366">Respeite o shell padrão do usuário ao usar wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-366">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="9e1a8-367">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-367">[GH 2372]</span></span>
* <span data-ttu-id="9e1a8-368">Relatar todas as interfaces de rede ethernet.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-368">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="9e1a8-369">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-369">[GH 2996]</span></span>
* <span data-ttu-id="9e1a8-370">Uma melhor manipulação do arquivo /etc/passwd corrompido.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-370">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="9e1a8-371">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-371">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-372">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-372">Console</span></span>
* <span data-ttu-id="9e1a8-373">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-373">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-374">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-374">LTP Results:</span></span>
<span data-ttu-id="9e1a8-375">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-375">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="9e1a8-376">Compilação 17618 (Ignorar em frente)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-376">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="9e1a8-377">Para Windows geral informações sobre compilação 17618, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-377">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-378">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-378">WSL</span></span>
* <span data-ttu-id="9e1a8-379">Introduzir pseudoconsole funcionalidades para interoperabilidade do NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-379">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="9e1a8-380">O mecanismo de instalação herdada (lxrun.exe) foi preterido.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-380">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="9e1a8-381">O mecanismo com suporte para a instalação de distribuições é por meio do Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-381">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-382">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-382">Console</span></span>
* <span data-ttu-id="9e1a8-383">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-383">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-384">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-384">LTP Results:</span></span>
<span data-ttu-id="9e1a8-385">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-385">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="9e1a8-386">Build 17110</span><span class="sxs-lookup"><span data-stu-id="9e1a8-386">Build 17110</span></span>
<span data-ttu-id="9e1a8-387">Para Windows geral informações sobre compilação 17110, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-387">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-388">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-388">WSL</span></span>
* <span data-ttu-id="9e1a8-389">Permitir /init ser encerrado de Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-389">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="9e1a8-390">DrvFs agora usa por diretório diferenciar maiusculas de minúsculas por padrão (equivalente a "caso = dir" opção de montagem).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-390">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="9e1a8-391">Usando "caso = force" (o comportamento antigo) requer a definição de uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-391">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="9e1a8-392">Execute o seguinte comando para habilitar "caso = force" Se você precisar usá-lo: reg adicionar HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="9e1a8-392">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="9e1a8-393">Se você tiver criados com o WSL na versão mais antiga do Windows que precisam ser diferencia maiusculas de minúsculas de diretórios existentes, use fsutil.exe para marcá-los em maiusculas e minúsculas: fsutil.exe arquivo setcasesensitiveinfo <path> habilitar</span><span class="sxs-lookup"><span data-stu-id="9e1a8-393">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="9e1a8-394">Cadeias de caracteres retornadas de syscall o uname terminadas com NULL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-394">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-395">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-395">Console</span></span>
* <span data-ttu-id="9e1a8-396">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-396">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-397">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-397">LTP Results:</span></span>
<span data-ttu-id="9e1a8-398">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-398">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="9e1a8-399">Compilação 17107</span><span class="sxs-lookup"><span data-stu-id="9e1a8-399">Build 17107</span></span>
<span data-ttu-id="9e1a8-400">Para Windows geral informações sobre compilação 17107, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-400">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-401">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-401">WSL</span></span>
* <span data-ttu-id="9e1a8-402">Suporte a TCSETSF e TCSETSW em pontos de extremidade mestre pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-402">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="9e1a8-403">Iniciar os processos simultâneos de interoperabilidade pode resultar em EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-403">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="9e1a8-404">Corrigi PTRACE_ATTACH para mostrar o status de rastreamento apropriado no /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-404">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="9e1a8-405">Corrida de correção em que os processos de curta duração clonados com os CLEARTID SETTID sinalizadores e pode ser fechado sem limpar o endereço TID.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-405">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="9e1a8-406">Exiba uma mensagem ao atualizar os diretórios de sistema de arquivos do Linux, ao mover de uma compilação de pré-17093.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-406">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="9e1a8-407">Para obter mais detalhes sobre as alterações do sistema de 17093 arquivo, consulte as notas de versão para [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-407">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-408">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-408">Console</span></span>
* <span data-ttu-id="9e1a8-409">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-409">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-410">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-410">LTP Results:</span></span>
<span data-ttu-id="9e1a8-411">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-411">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="9e1a8-412">Compilação 17101</span><span class="sxs-lookup"><span data-stu-id="9e1a8-412">Build 17101</span></span>
<span data-ttu-id="9e1a8-413">Para Windows geral informações sobre compilação 17101, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-413">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-414">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-414">WSL</span></span>
* <span data-ttu-id="9e1a8-415">Suporte para signalfd.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-415">Support for signalfd.</span></span> <span data-ttu-id="9e1a8-416">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-416">[GH 129]</span></span>
* <span data-ttu-id="9e1a8-417">Suporte a nomes de arquivo que contém caracteres inválidos de NTFS, codificá-los como caracteres de Unicode particulares.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-417">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="9e1a8-418">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-418">[GH 1514]</span></span>
* <span data-ttu-id="9e1a8-419">Montagem automática usarão somente leitura quando não há suporte para gravação.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-419">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="9e1a8-420">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-420">[GH 2603]</span></span>
* <span data-ttu-id="9e1a8-421">Permitir a colagem dos pares substitutos de Unicode (como caracteres emoji).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-421">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="9e1a8-422">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-422">[GH 2765]</span></span>
* <span data-ttu-id="9e1a8-423">Arquivos pseudo /proc e /sys devem retornar leitura e gravação pronto para de select, sondagem, epoll, et al. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-423">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="9e1a8-424">Corrija o problema que poderia fazer com que o serviço entrar em loop infinito quando o registro foi violado ou corrompido.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-424">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="9e1a8-425">Corrija as mensagens netlink para trabalhar com a versão mais recente (upstream 4.14) iproute2.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-425">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-426">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-426">Console</span></span>
* <span data-ttu-id="9e1a8-427">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-427">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-428">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-428">LTP Results:</span></span>
<span data-ttu-id="9e1a8-429">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-429">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="9e1a8-430">Compilação 17093</span><span class="sxs-lookup"><span data-stu-id="9e1a8-430">Build 17093</span></span>
<span data-ttu-id="9e1a8-431">Para Windows geral informações sobre compilação 17093, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-431">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="9e1a8-432">Importante:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-432">Important:</span></span>
<span data-ttu-id="9e1a8-433">Ao iniciar o WSL pela primeira vez após a atualização para esta compilação, ele precisará executar algum trabalho atualizando os diretórios de sistema de arquivos do Linux.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-433">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="9e1a8-434">Isso pode levar vários minutos, portanto, pode parecer WSL iniciam lentamente.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-434">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="9e1a8-435">Isso deve ocorrer apenas uma vez para cada distribuição têm instalado da loja.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-435">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="9e1a8-436">Suporte aprimorado de maiusculas e minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-436">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="9e1a8-437">DrvFs agora dá suporte a diferenciação de maiusculas por diretório.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-437">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="9e1a8-438">Isso é um novo sinalizador que pode ser definido em diretórios para indicar que todas as operações nesses diretórios devem ser tratadas como diferencia maiusculas de minúsculas, que permite que até mesmo aplicativos Windows corretamente abrir arquivos que diferem somente maiusculas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-438">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="9e1a8-439">DrvFs possui novas opções de montagem, controlando a diferenciação de maiusculas em uma base por diretório</span><span class="sxs-lookup"><span data-stu-id="9e1a8-439">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="9e1a8-440">Caso = força: todos os diretórios são tratados como diferencia maiusculas de minúsculas (exceto para a raiz da unidade).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-440">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="9e1a8-441">Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-441">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="9e1a8-442">Esse é o comportamento herdado, exceto para marcar os novos diretórios diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-442">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="9e1a8-443">Caso = dir: somente diretórios com o sinalizador de diferenciação de maiusculas por diretório diferenciam maiusculas e minúsculas; outros diretórios diferenciam maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-443">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="9e1a8-444">Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-444">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="9e1a8-445">Caso = desativado: somente diretórios com o sinalizador de diferenciação de maiusculas por diretório diferenciam maiusculas e minúsculas; outros diretórios diferenciam maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-445">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="9e1a8-446">Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-446">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="9e1a8-447">Observação: diretórios criados pelo WSL em versões anteriores não têm esse sinalizador definido, portanto, não será tratada como diferencia maiusculas de minúsculas se você usar o "caso = dir" opção.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-447">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="9e1a8-448">Uma maneira de definir esse sinalizador nos diretórios existentes em breve.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-448">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="9e1a8-449">Exemplo de montagem com as seguintes opções (para as unidades existentes, você deve primeiro desmontar antes de montar com opções diferentes): sudo mount -t drvfs c: mnt/c -o caso = dir</span><span class="sxs-lookup"><span data-stu-id="9e1a8-449">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="9e1a8-450">Por enquanto, caso = força ainda é a opção padrão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-450">For now, case=force is still the default option.</span></span> <span data-ttu-id="9e1a8-451">Isso será alterado para caso = dir no futuro.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-451">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="9e1a8-452">Agora você pode usar barras "/" em caminhos do Windows ao montar DrvFs, por exemplo: -t drvfs //server/share /mnt/share de montagem sudo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-452">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="9e1a8-453">Agora, o WSL processa o arquivo /etc/fstab durante a inicialização de instância [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-453">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="9e1a8-454">Isso é feito antes de montar automaticamente DrvFs unidades; todas as unidades que já foram montadas por fstab serão não remontadas automaticamente, permitindo que você altere o ponto de montagem para unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-454">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="9e1a8-455">Esse comportamento pode ser desativado usando wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-455">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="9e1a8-456">Os arquivos de montagem, mountinfo e mountstats no /proc corretamente escapar caracteres especiais como barras invertidas e de espaços [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-456">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="9e1a8-457">Arquivos especiais criados com DrvFs como links simbólicos do WSL, ou fifos e soquetes quando os metadados estiverem habilitados, agora podem ser copiados e movidos do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-457">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="9e1a8-458">WSL é mais configurável com wsl.conf</span><span class="sxs-lookup"><span data-stu-id="9e1a8-458">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="9e1a8-459">Adicionamos um método para que você configure automaticamente algumas funcionalidades em WSL que será aplicada sempre que iniciar o subsistema.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-459">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="9e1a8-460">Isso inclui opções de montagem automática e a configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-460">This includes automount options and network configuration.</span></span> <span data-ttu-id="9e1a8-461">Saiba mais sobre isso em nossa postagem de blog em: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="9e1a8-461">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="9e1a8-462">AF_UNIX permite conexões de soquete entre processos do Linux no WSL e processos nativos do Windows</span><span class="sxs-lookup"><span data-stu-id="9e1a8-462">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="9e1a8-463">Aplicativos WSL e o Windows agora podem se comunicar entre si em soquetes do Unix.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-463">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="9e1a8-464">Imagine que você deseja executar um serviço no Windows e torná-lo disponível para aplicativos do Windows e WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-464">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="9e1a8-465">Agora, que é possível com soquetes do Unix.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-465">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="9e1a8-466">Leia mais em nosso blog postagem em https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="9e1a8-466">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-467">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-467">WSL</span></span>
* <span data-ttu-id="9e1a8-468">Suporte mmap() com MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-468">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="9e1a8-469">Suporte CLONE_PTRACE e CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-469">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="9e1a8-470">Lidar com sinal de encerramento não SIGCHLD em clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-470">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="9e1a8-471">/Proc/sys/fs/inotify/max_user_instances de stub e /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-471">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="9e1a8-472">Erro ao carregar os binários do ELF que contêm cabeçalhos de carga com deslocamentos diferente de zero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-472">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="9e1a8-473">Zerar à direita de bytes de página ao carregar imagens.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-473">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="9e1a8-474">Reduzir casos em que execve silenciosamente encerra o processo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-474">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-475">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-475">Console</span></span>
* <span data-ttu-id="9e1a8-476">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-476">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-477">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-477">LTP Results:</span></span>
<span data-ttu-id="9e1a8-478">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-478">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="9e1a8-479">Build 17083</span><span class="sxs-lookup"><span data-stu-id="9e1a8-479">Build 17083</span></span>
<span data-ttu-id="9e1a8-480">Para Windows geral informações sobre compilação 17083, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-480">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-481">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-481">WSL</span></span>
* <span data-ttu-id="9e1a8-482">Fixa de verificação de bugs relacionada a epoll [2798 de GH, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-482">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="9e1a8-483">Fixos travamentos quando desativar ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-483">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="9e1a8-484">Certifique-se de operações mmap aparecem atômica [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-484">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-485">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-485">Console</span></span>
* <span data-ttu-id="9e1a8-486">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-487">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-487">LTP Results:</span></span>
<span data-ttu-id="9e1a8-488">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-488">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="9e1a8-489">Build 17074</span><span class="sxs-lookup"><span data-stu-id="9e1a8-489">Build 17074</span></span>
<span data-ttu-id="9e1a8-490">Para Windows geral informações sobre compilação 17074, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-490">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-491">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-491">WSL</span></span>
* <span data-ttu-id="9e1a8-492">Formato de armazenamento fixa de metadados DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-492">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="9e1a8-493">**Importante:** Metadados de DrvFs criado antes desta compilação serão exibidos incorretamente ou não.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-493">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="9e1a8-494">Para corrigir arquivos afetados, use chmod e alterar o proprietário para reaplicar os metadados.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-494">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="9e1a8-495">Correção do problema com vários sinais e syscalls reinicializável.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-495">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-496">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-496">Console</span></span>
* <span data-ttu-id="9e1a8-497">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-497">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-498">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-498">LTP Results:</span></span>
<span data-ttu-id="9e1a8-499">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-499">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="9e1a8-500">Build 17063</span><span class="sxs-lookup"><span data-stu-id="9e1a8-500">Build 17063</span></span>
<span data-ttu-id="9e1a8-501">Para Windows geral informações sobre compilação 17063, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-501">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9e1a8-502">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-502">WSL</span></span>
* <span data-ttu-id="9e1a8-503">DrvFs dá suporte a metadados adicionais de Linux.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-503">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="9e1a8-504">Isso permite definir o proprietário e o modo de arquivos usando chmod/alterar o proprietário e também a criação de arquivos especiais, como fifos, soquetes do unix e arquivos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-504">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="9e1a8-505">Isso está desabilitado por padrão por enquanto, pois é ainda experimental.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-505">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="9e1a8-506">**Observação:**  Corrigimos um bug no formato de metadados usado pelo DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-506">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="9e1a8-507">Enquanto trabalha metadados nessa compilação para experimentação, os builds futuros não corretamente lerá metadados criados por essa compilação.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-507">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="9e1a8-508">Talvez você precise atualizar manualmente o proprietário de arquivos modificados e dispositivos com uma ID de dispositivo personalizada precisa ser recriada.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-508">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="9e1a8-509">Para habilitar a montagem DrvFs com a opção de metadados (para habilitá-lo em uma montagem existente, você deve primeiro desmontá-la):</span><span class="sxs-lookup"><span data-stu-id="9e1a8-509">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="9e1a8-510">Permissões de Linux são adicionadas como metadados adicionais no arquivo; elas não afetam as permissões do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-510">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="9e1a8-511">Lembre-se de que a edição de um arquivo usando um editor do Windows pode remover os metadados.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-511">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="9e1a8-512">Nesse caso, o arquivo será revertido para suas permissões padrão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-512">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="9e1a8-513">Opções de montagem adicionado para DrvFs para controlar arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-513">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="9e1a8-514">UID: a ID de usuário usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-514">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="9e1a8-515">GID: a ID do grupo usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-515">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="9e1a8-516">umask: uma máscara de permissões para excluir todos os arquivos e diretórios de octal.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-516">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="9e1a8-517">fmask: uma máscara de permissões para excluir todos os arquivos regulares de octal.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-517">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="9e1a8-518">dmask: uma máscara de permissões para excluir para todos os diretórios de octal.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-518">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="9e1a8-519">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="9e1a8-519">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="9e1a8-520">Combine com a opção de metadados para especificar as permissões padrão de arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-520">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="9e1a8-521">Introduzida uma nova variável de ambiente, `WSLENV`, para configurar como as variáveis de ambiente fluam entre WSL e Win32.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-521">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="9e1a8-522">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="9e1a8-522">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="9e1a8-523">`WSLENV` é uma lista delimitada por dois-pontos das variáveis de ambiente que pode ser incluído ao iniciar processos WSL do Win32 ou Win32 do WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-523">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="9e1a8-524">Cada variável pode ser sufixado com uma barra invertida seguida por sinalizadores para especificar como ele é convertido.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-524">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="9e1a8-525">p: O valor é um caminho que deve ser traduzido entre os caminhos de Win32 e WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-525">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="9e1a8-526">l: O valor é uma lista de caminhos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-526">l: The value is a list of paths.</span></span> <span data-ttu-id="9e1a8-527">Em WSL, é uma lista delimitada por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-527">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="9e1a8-528">No Win32, é uma lista delimitada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-528">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="9e1a8-529">u: O valor só deve ser incluído ao invocar o WSL do Win32</span><span class="sxs-lookup"><span data-stu-id="9e1a8-529">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="9e1a8-530">gravação: O valor só deve ser incluído ao invocar Win32 de WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-530">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="9e1a8-531">Você pode definir `WSLENV` em. bashrc ou no ambiente do Windows personalizado para o usuário.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-531">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="9e1a8-532">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-532">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="9e1a8-533">links simbólicos de drvfs relatam o tamanho correto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-533">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="9e1a8-534">leitura/gravação funciona para tamanhos de e/s muito grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-534">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="9e1a8-535">waitpid funciona com IDs (GH 2534) do grupo de processo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-535">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="9e1a8-536">desempenho significativamente aprimorado mmap para regiões de reserva grande; melhora o desempenho de ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-536">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="9e1a8-537">dá suporte a personalidade para READ_IMPLIES_EXEC; corrige maxima e clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-537">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="9e1a8-538">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-538">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="9e1a8-539">correções de falhas de página no modo; de excesso de alocação correções sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-539">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="9e1a8-540">Clone dá suporte a mais combinações de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="9e1a8-540">clone supports more flags combinations</span></span>
* <span data-ttu-id="9e1a8-541">Suporte a select/epoll de arquivos epoll (anteriormente não operacional).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-541">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="9e1a8-542">Notificar ptrace de syscalls não implementada.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-542">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="9e1a8-543">Ignorar as interfaces que não estão ao gerar nameservers resolv. conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-543">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="9e1a8-544">Enumere as interfaces de rede com nenhum endereço físico.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-544">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="9e1a8-545">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-545">[GH 2685]</span></span>
* <span data-ttu-id="9e1a8-546">Correções de bugs adicionais e aprimoramentos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-546">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="9e1a8-547">Ferramentas do Linux disponíveis para desenvolvedores no Windows</span><span class="sxs-lookup"><span data-stu-id="9e1a8-547">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="9e1a8-548">Cadeia de ferramentas de linha de comando do Windows inclui bsdtar (tar) e o curl.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-548">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="9e1a8-549">Leia [este blog](https://aka.ms/tarcurlwindows) para saber mais sobre a adição dessas duas novas ferramentas e ver como eles moldando a experiência do desenvolvedor no Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-549">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="9e1a8-550">`AF_UNIX` está disponível no SDK Windows Insider (17061 +).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-550">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="9e1a8-551">Leia [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para saber mais sobre `AF_UNIX` e como os desenvolvedores no Windows podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-551">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="9e1a8-552">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-552">Console</span></span>
* <span data-ttu-id="9e1a8-553">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-553">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-554">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-554">LTP Results:</span></span>
<span data-ttu-id="9e1a8-555">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-555">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="9e1a8-556">Compilação 17046</span><span class="sxs-lookup"><span data-stu-id="9e1a8-556">Build 17046</span></span>

<span data-ttu-id="9e1a8-557">Para Windows geral informações sobre compilação 17046, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-557">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="9e1a8-558">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-558">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-559">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-559">WSL</span></span>
- <span data-ttu-id="9e1a8-560">Permitir que os processos sejam executados sem um terminal de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-560">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="9e1a8-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="9e1a8-562">Melhor suporte a CLONE_VFORK e CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-562">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="9e1a8-563">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-563">[GH 1878, 2615]</span></span>
- <span data-ttu-id="9e1a8-564">Ignore drivers de filtro TDI WSL operações de rede.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-564">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="9e1a8-565">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-565">[GH 1554]</span></span>
- <span data-ttu-id="9e1a8-566">DrvFs cria links simbólicos do NT quando determinadas condições forem atendidas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-566">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="9e1a8-567">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-567">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="9e1a8-568">O destino do link deve ser relativo, não deve ultrapassar o quaisquer pontos de montagem ou links simbólicos e deve existir.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-568">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="9e1a8-569">O usuário deve ter SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (Isso normalmente exige que você inicie wsl.exe com privilégios elevados), a menos que o modo de desenvolvedor está ativado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-569">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="9e1a8-570">Em outras situações, DrvFs ainda cria links simbólicos WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-570">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="9e1a8-571">Permitir executando com privilégios elevados e sem privilégios elevados instâncias WSL simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-571">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="9e1a8-572">Suporte /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="9e1a8-572">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="9e1a8-573">Adicione wslpath para fazer WSL <> – conversões de caminho do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-573">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="9e1a8-574">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-574">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="9e1a8-575">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-575">Console</span></span>
- <span data-ttu-id="9e1a8-576">Não há correções.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-576">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-577">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-577">LTP Results:</span></span>
<span data-ttu-id="9e1a8-578">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-578">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="9e1a8-579">Build 17040</span><span class="sxs-lookup"><span data-stu-id="9e1a8-579">Build 17040</span></span>

<span data-ttu-id="9e1a8-580">Para Windows geral informações sobre compilação 17040, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-580">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-581">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-581">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-582">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-582">WSL</span></span>
- <span data-ttu-id="9e1a8-583">Não há correções desde 17035.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-583">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-584">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-584">Console</span></span>
- <span data-ttu-id="9e1a8-585">Não há correções desde 17035.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-585">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-586">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-586">LTP Results:</span></span>
<span data-ttu-id="9e1a8-587">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-587">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="9e1a8-588">Compilação 17035</span><span class="sxs-lookup"><span data-stu-id="9e1a8-588">Build 17035</span></span>

<span data-ttu-id="9e1a8-589">Para Windows geral informações sobre compilação 17035, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-589">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-590">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-591">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-591">WSL</span></span>
- <span data-ttu-id="9e1a8-592">Acessando arquivos em DrvFs pode falhar ocasionalmente EINVAL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-592">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="9e1a8-593">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-593">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-594">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-594">Console</span></span>
- <span data-ttu-id="9e1a8-595">Alguma perda de cor ao inserir/excluir linhas no modo de VT.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-595">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-596">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-596">LTP Results:</span></span>
<span data-ttu-id="9e1a8-597">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-597">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="9e1a8-598">Build 17025</span><span class="sxs-lookup"><span data-stu-id="9e1a8-598">Build 17025</span></span>

<span data-ttu-id="9e1a8-599">Para Windows geral informações no build 17025, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-599">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-600">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-600">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-601">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-601">WSL</span></span>
- <span data-ttu-id="9e1a8-602">Inicie processos inicias em um novo grupo de processo de primeiro plano [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-602">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="9e1a8-603">Entrega SIGHUP corrige [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-603">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="9e1a8-604">Gere nome da ponte virtual padrão se não houver nenhuma [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-604">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="9e1a8-605">Implemente /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-605">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="9e1a8-606">Correções de pipe de stdout/stderr mais interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-606">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="9e1a8-607">Stub syncfs chamada do sistema.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-607">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-608">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-608">Console</span></span>
- <span data-ttu-id="9e1a8-609">Corrija a entrada tradução VT para consoles de terceiros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-609">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-610">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-610">LTP Results:</span></span>
<span data-ttu-id="9e1a8-611">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-611">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="9e1a8-612">Compilação 17017</span><span class="sxs-lookup"><span data-stu-id="9e1a8-612">Build 17017</span></span>

<span data-ttu-id="9e1a8-613">Para Windows geral informações sobre compilação 17017, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-613">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-614">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-614">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-615">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-615">WSL</span></span>
- <span data-ttu-id="9e1a8-616">Ignore cabeçalhos de programa ELF vazios [GH 330].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-616">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="9e1a8-617">Permitir LxssManager criar instâncias WSL para os usuários não interativo (ssh e agendada suporte de tarefa) [777 GH 1602].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-617">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="9e1a8-618">Suporte WSL -> Win32 -> [GH 1228] de cenários WSL ("início").</span><span class="sxs-lookup"><span data-stu-id="9e1a8-618">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="9e1a8-619">Suporte limitado para a terminação de aplicativos de console, invocado por meio de interoperabilidade [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-619">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="9e1a8-620">Suporte a opções de montagem para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-620">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="9e1a8-621">Ptrace bloqueando a inicialização de filho [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-621">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="9e1a8-622">EPOLLET faltando alguns eventos [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-622">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="9e1a8-623">Retorne mais dados para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-623">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="9e1a8-624">Getdents com lseek fornece resultados incorretos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-624">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="9e1a8-625">Corrigi alguns travamentos de interoperabilidade do aplicativo do Win32, aguardando a entrada em um pipe que não tem mais nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-625">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="9e1a8-626">Suporte O_ASYNC para arquivos de tty/pty.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-626">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="9e1a8-627">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-628">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-628">Console</span></span>
- <span data-ttu-id="9e1a8-629">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-630">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-630">LTP Results:</span></span>
<span data-ttu-id="9e1a8-631">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-631">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="9e1a8-632">Atualização do Fall Creators</span><span class="sxs-lookup"><span data-stu-id="9e1a8-632">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="9e1a8-633">Build 16288</span><span class="sxs-lookup"><span data-stu-id="9e1a8-633">Build 16288</span></span>

<span data-ttu-id="9e1a8-634">Para Windows geral informações sobre compilação 16288, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-634">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-635">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-635">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-636">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-636">WSL</span></span>
- <span data-ttu-id="9e1a8-637">Inicializar corretamente e relatar uid e gid modo de soquete para descritores de arquivo [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-637">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="9e1a8-638">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-638">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-639">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-639">Console</span></span>
- <span data-ttu-id="9e1a8-640">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-640">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-641">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-641">LTP Results:</span></span>
<span data-ttu-id="9e1a8-642">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="9e1a8-642">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="9e1a8-643">Compilação 16278</span><span class="sxs-lookup"><span data-stu-id="9e1a8-643">Build 16278</span></span>

<span data-ttu-id="9e1a8-644">Para Windows geral informações sobre compilação 162738, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-644">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-645">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-645">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-646">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-646">WSL</span></span>
- <span data-ttu-id="9e1a8-647">Cancelar explicitamente o mapeamento de exibições mapeadas de seções de backup em arquivo quando subdividir o estado de MM LX [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-647">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="9e1a8-648">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-648">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-649">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-649">Console</span></span>
- <span data-ttu-id="9e1a8-650">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-650">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-651">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-651">LTP Results:</span></span>
<span data-ttu-id="9e1a8-652">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="9e1a8-652">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="9e1a8-653">Compilação 16275</span><span class="sxs-lookup"><span data-stu-id="9e1a8-653">Build 16275</span></span>

<span data-ttu-id="9e1a8-654">Para Windows geral informações sobre compilação 162735, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-654">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-655">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-655">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-656">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-656">WSL</span></span>
- <span data-ttu-id="9e1a8-657">Nenhum WSL relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-657">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-658">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-658">Console</span></span>
- <span data-ttu-id="9e1a8-659">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-660">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-660">LTP Results:</span></span>
<span data-ttu-id="9e1a8-661">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="9e1a8-661">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="9e1a8-662">Compilação 16273</span><span class="sxs-lookup"><span data-stu-id="9e1a8-662">Build 16273</span></span>

<span data-ttu-id="9e1a8-663">Para Windows geral informações sobre compilação 16273, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-663">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-664">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-665">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-665">WSL</span></span>
- <span data-ttu-id="9e1a8-666">Corrigido um problema em que o DrvFs relatado, às vezes, o tipo de arquivo incorreto para diretórios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-666">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="9e1a8-667">Permitir a criação de soquetes NETLINK_KOBJECT_UEVENT desbloquear programas uevent que use [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-667">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="9e1a8-668">Adicionar suporte para conexão sem bloqueio [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-668">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="9e1a8-669">Implemente CLONE_FS clonar o sinalizador de chamada do sistema [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-669">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="9e1a8-670">Corrigir problemas em torno de não lidar com guias ou aspas corretamente na interoperabilidade de NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-670">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="9e1a8-671">Resolver o erro ao tentar iniciar novamente WSL instâncias [GH 651, 2095] o acesso negado</span><span class="sxs-lookup"><span data-stu-id="9e1a8-671">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="9e1a8-672">Implementar operações futex FUTEX_REQUEUE e FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-672">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="9e1a8-673">Corrija as permissões para vários arquivos SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-673">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="9e1a8-674">Corrigir Haskell travamento de pilha durante a instalação do [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-674">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="9e1a8-675">Implementar binfmt_misc "C" ' l'e 'P' sinalizadores [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-675">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="9e1a8-676">Adicionar /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-676">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="9e1a8-677">Adicionar suporte parcial para a chamada do sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-677">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="9e1a8-678">Criar um stub SO_REUSEPORT & adicionando suporte para SO_PASSCRED para soquetes netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-678">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="9e1a8-679">Retornar códigos de erro diferentes de RegisterDistribuiton se uma distribuição está instalado ou desinstalado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-679">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="9e1a8-680">Permitir cancelamento de registro de distribuições de WSL parcialmente instaladas por meio de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="9e1a8-680">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="9e1a8-681">Corrigir a suspensão de teste de soquete python de udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="9e1a8-681">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="9e1a8-682">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-682">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-683">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-683">Console</span></span>
- <span data-ttu-id="9e1a8-684">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-684">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-685">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-685">LTP Results:</span></span>
<span data-ttu-id="9e1a8-686">Total de testes: 1904</span><span class="sxs-lookup"><span data-stu-id="9e1a8-686">Total Tests: 1904</span></span><br/>
<span data-ttu-id="9e1a8-687">Testes ignorados do total: 209</span><span class="sxs-lookup"><span data-stu-id="9e1a8-687">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="9e1a8-688">Total de falhas: 229</span><span class="sxs-lookup"><span data-stu-id="9e1a8-688">Total Failures: 229</span></span><br/>
[<span data-ttu-id="9e1a8-689">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-689">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="9e1a8-690">Build 16257</span><span class="sxs-lookup"><span data-stu-id="9e1a8-690">Build 16257</span></span>

<span data-ttu-id="9e1a8-691">Para Windows geral informações sobre compilação 16257, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-691">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-692">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-692">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-693">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-693">WSL</span></span>
- <span data-ttu-id="9e1a8-694">Implementar a chamada do sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="9e1a8-694">Implement prlimit64 system call</span></span>
- <span data-ttu-id="9e1a8-695">Adicionar suporte para ulimit – n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-695">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="9e1a8-696">Stub MSG_MORE para soquetes TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-696">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="9e1a8-697">Corrigir o comportamento de vetor auxiliar AT_EXECFN inválido [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-697">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="9e1a8-698">Corrigir o comportamento de copiar/colar para console/tty e adicionar melhor buffer cheio tratamento [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-698">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="9e1a8-699">Defina AT_SECURE na auxiliar vetor para programas em set-user-ID e set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-699">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="9e1a8-700">Ponto de extremidade mestre pseudo-terminal não manipulando TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-700">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="9e1a8-701">Correção de lseek faz para retroceder diretórios em LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-701">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="9e1a8-702">/dev/ptmx trava depois de uso intenso [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-702">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="9e1a8-703">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-703">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-704">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-704">Console</span></span>
- <span data-ttu-id="9e1a8-705">Correção para horizontal linhas/sublinhados em todos os lugares [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-705">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="9e1a8-706">Corrigir para processar pedido alterado NPM tornando mais difícil fechar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-706">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="9e1a8-707">Adicionado o novo esquema de cores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="9e1a8-707">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-708">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-708">LTP Results:</span></span>
<span data-ttu-id="9e1a8-709">Nenhuma alteração desde 16251</span><span class="sxs-lookup"><span data-stu-id="9e1a8-709">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-710">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-710">Syscall Support</span></span>
<span data-ttu-id="9e1a8-711">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-711">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-712">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-712">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="9e1a8-713">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-713">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="9e1a8-714">Problema do GitHub 2392: Pastas do Windows não reconhecido pelo WSL...</span><span class="sxs-lookup"><span data-stu-id="9e1a8-714">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="9e1a8-715">No build 16257, o WSL tem problemas ao enumerar arquivos/pastas do Windows por meio de `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-715">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="9e1a8-716">Esse problema foi corrigido e devem ser liberado no build Insiders durante a semana começar 14/8/2017.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-716">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="9e1a8-717">Compilação 16251</span><span class="sxs-lookup"><span data-stu-id="9e1a8-717">Build 16251</span></span>

<span data-ttu-id="9e1a8-718">Para Windows geral informações sobre compilação 16251, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-718">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-719">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-719">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-720">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-720">WSL</span></span>
- <span data-ttu-id="9e1a8-721">Remover marca de versão beta do componente opcional do WSL, consulte [postagem de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-721">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="9e1a8-722">Inicializar corretamente o conjunto salvo uid e gid para set-user-ID e a ID do grupo de conjunto de binários em exec [GH 962 do MSExchangeTransport, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-722">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="9e1a8-723">Suporte adicionado para ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-723">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="9e1a8-724">Suporte adicionado para ptrace PTRACE_GETFPREGS e PTRACE_GETREGSET com NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-724">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="9e1a8-725">Corrigido ptrace parar em sinais ignorado</span><span class="sxs-lookup"><span data-stu-id="9e1a8-725">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="9e1a8-726">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-726">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-727">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-727">Console</span></span>
- <span data-ttu-id="9e1a8-728">Nenhum Console relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-728">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-729">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-729">LTP Results:</span></span>
<span data-ttu-id="9e1a8-730">Número de testes aprovados: 768</span><span class="sxs-lookup"><span data-stu-id="9e1a8-730">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="9e1a8-731">Número de testes com falha: 244</span><span class="sxs-lookup"><span data-stu-id="9e1a8-731">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="9e1a8-732">Número de testes ignorados: 96</span><span class="sxs-lookup"><span data-stu-id="9e1a8-732">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="9e1a8-733">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-733">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="9e1a8-734">Compilação 16241</span><span class="sxs-lookup"><span data-stu-id="9e1a8-734">Build 16241</span></span>

<span data-ttu-id="9e1a8-735">Para Windows geral informações sobre compilação 16241, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-735">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-736">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-736">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9e1a8-737">WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-737">WSL</span></span>
- <span data-ttu-id="9e1a8-738">Nenhum WSL relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-738">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="9e1a8-739">Console</span><span class="sxs-lookup"><span data-stu-id="9e1a8-739">Console</span></span>
- <span data-ttu-id="9e1a8-740">Correção para gerar o caractere incorreto para dez linhas de cruzamento, relatado originalmente [aqui](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-740">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="9e1a8-741">Correção para nenhum texto de saída que está sendo exibido na página de código 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-741">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="9e1a8-742">Não transfira as alterações feitas em valores RGB da cor de um para outras partes da paleta, alterar a seleção.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-742">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="9e1a8-743">Isso fará a folha de propriedades de console muito mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-743">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="9e1a8-744">CTRL + S parece não funcionar corretamente</span><span class="sxs-lookup"><span data-stu-id="9e1a8-744">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="9e1a8-745">Não negrito /-Dim completamente ausentes de códigos de escape ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-745">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="9e1a8-746">Console corretamente não dá suporte a temas de cores Vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-746">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="9e1a8-747">Não é possível colar determinados caracteres [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-747">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="9e1a8-748">Redimensionamento refluxo de forma estranha interage com o redimensionamento de uma janela de bash quando coisas está na linha de comando/Editar [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-748">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="9e1a8-749">CTRL + L sair da tela suja [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-749">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="9e1a8-750">Bug de renderização do console ao exibir VT em HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-750">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="9e1a8-751">Caracteres Japansese pareçam estranhos com o caractere Unicode U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-751">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="9e1a8-752">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-752">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="9e1a8-753">Build 16237</span><span class="sxs-lookup"><span data-stu-id="9e1a8-753">Build 16237</span></span>

<span data-ttu-id="9e1a8-754">Para Windows geral informações sobre compilação 16237, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-754">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-755">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-755">Fixed</span></span>
- <span data-ttu-id="9e1a8-756">Use os atributos padrão para arquivos sem EAs no lxfs (raiz, raiz, 0000)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-756">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="9e1a8-757">Adicionado suporte para as distribuições que usam atributos estendidos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-757">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="9e1a8-758">Correção de enchimento de entradas retornadas pela getdents e getdents64</span><span class="sxs-lookup"><span data-stu-id="9e1a8-758">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="9e1a8-759">Corrigir a verificação de permissões para a chamada do sistema shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-759">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="9e1a8-760">Estado fixo epoll inicial incorreto para ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-760">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="9e1a8-761">Corrigir a leitura do DrvFs diret não retornando todas as entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-761">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="9e1a8-762">Corrigir LxFs leitura diret quando os arquivos estão desvinculado [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-762">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="9e1a8-763">Permitir que arquivos drvfs desvinculado ser reaberto por meio de procfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-763">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="9e1a8-764">Adicionada a substituição da chave de registro global para desabilitar os recursos WSL (interoperabilidade / montagem da unidade)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-764">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="9e1a8-765">Correção de contagem incorreta de bloco em "estatística" para DrvFs (e LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-765">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="9e1a8-766">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-766">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="9e1a8-767">Compilação 16232</span><span class="sxs-lookup"><span data-stu-id="9e1a8-767">Build 16232</span></span>

<span data-ttu-id="9e1a8-768">Para Windows geral informações sobre compilação 16232, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-768">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-769">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-769">Fixed</span></span>
- <span data-ttu-id="9e1a8-770">Nenhum WSL relacionados a alterações nesta versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-770">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="9e1a8-771">Compilação 16226</span><span class="sxs-lookup"><span data-stu-id="9e1a8-771">Build 16226</span></span>

<span data-ttu-id="9e1a8-772">Para Windows geral informações sobre compilação 16226, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-772">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-773">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-773">Fixed</span></span>
- <span data-ttu-id="9e1a8-774">xattr relacionadas ao suporte de syscalls (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-774">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="9e1a8-775">suporte de xattr Security.capablity.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-775">security.capablity xattr support.</span></span>
- <span data-ttu-id="9e1a8-776">Compatibilidade aprimorada com certos sistemas de arquivos e filtros, incluindo servidores SMB não MS.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-776">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="9e1a8-777">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-777">[GH #1952]</span></span>
- <span data-ttu-id="9e1a8-778">Suporte aprimorado para espaços reservados do OneDrive, espaços reservados do GVFS e compacta OS arquivos compactados.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-778">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="9e1a8-779">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-779">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="9e1a8-780">Compilação 16215</span><span class="sxs-lookup"><span data-stu-id="9e1a8-780">Build 16215</span></span>

<span data-ttu-id="9e1a8-781">Para Windows geral informações sobre compilação 16215, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-781">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-782">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-782">Fixed</span></span>
- <span data-ttu-id="9e1a8-783">WSL não exige o modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-783">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="9e1a8-784">Suporte a junções de diretório no drvfs.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-784">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="9e1a8-785">Lidar com a desinstalação dos pacotes de appx de distribuição de WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-785">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="9e1a8-786">Atualização procfs Mostrar privado e compartilhado mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-786">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="9e1a8-787">Adicione capacidade para wslconfig.exe limpar as distribuições que são parcialmente instaladas ou desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-787">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="9e1a8-788">Adicionado suporte para IP_MTU_DISCOVER para soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-788">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="9e1a8-789">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-789">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="9e1a8-790">Inferir a família de protocolo para as rotas para AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-790">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="9e1a8-791">Melhorias do dispositivo serial [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="9e1a8-791">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="9e1a8-792">Compilação 16199</span><span class="sxs-lookup"><span data-stu-id="9e1a8-792">Build 16199</span></span>

<span data-ttu-id="9e1a8-793">Para Windows geral informações sobre compilação 16199, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-793">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-794">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-794">Fixed</span></span>
- <span data-ttu-id="9e1a8-795">Nenhum WSL relacionados a alterações nessas versões.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-795">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="9e1a8-796">Compilação 16193</span><span class="sxs-lookup"><span data-stu-id="9e1a8-796">Build 16193</span></span>

<span data-ttu-id="9e1a8-797">Para Windows geral informações sobre compilação 16193, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-797">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-798">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-798">Fixed</span></span>
- <span data-ttu-id="9e1a8-799">Condição de corrida entre o envio SIGCONT e um threadgroup encerrando [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-799">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="9e1a8-800">alterar dispositivos tty e pty para relatório FILE_DEVICE_NAMED_PIPE em vez de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-800">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="9e1a8-801">Correção SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="9e1a8-801">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="9e1a8-802">Movido DrvFs montagem para init daemon [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-802">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="9e1a8-803">Adicionado suporte em DrvFs para seguir links simbólicos do NT.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-803">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="9e1a8-804">Compilação 16184</span><span class="sxs-lookup"><span data-stu-id="9e1a8-804">Build 16184</span></span>

<span data-ttu-id="9e1a8-805">Para Windows geral informações sobre compilação 16184, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-805">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-806">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-806">Fixed</span></span>
- <span data-ttu-id="9e1a8-807">Removida a tarefa de manutenção de pacotes apt (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-807">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="9e1a8-808">Correção da saída não aparecendo de processos do Windows no Node. js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-808">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="9e1a8-809">Reduza os requisitos de alinhamento no lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-809">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="9e1a8-810">Corrigido o tratamento do sinalizador AT_EMPTY_PATH em um número de chamadas do sistema.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-810">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="9e1a8-811">Corrigido um problema em que a exclusão DrvFs arquivos com identificadores abertos fará com que o arquivo a apresentar um comportamento indefinido [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-811">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="9e1a8-812">/ etc/hosts agora herdarão as entradas do arquivo de hosts do Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-812">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="9e1a8-813">Compilação 16179</span><span class="sxs-lookup"><span data-stu-id="9e1a8-813">Build 16179</span></span>

<span data-ttu-id="9e1a8-814">Para Windows geral informações sobre compilação 16179, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-814">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-815">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-815">Fixed</span></span>
- <span data-ttu-id="9e1a8-816">Nenhuma alteração WSL desta semana.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-816">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="9e1a8-817">Compilação 16176</span><span class="sxs-lookup"><span data-stu-id="9e1a8-817">Build 16176</span></span>

<span data-ttu-id="9e1a8-818">Para Windows geral informações sobre compilação 16176, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-818">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-819">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-819">Fixed</span></span>

- [<span data-ttu-id="9e1a8-820">Suporte serial habilitado</span><span class="sxs-lookup"><span data-stu-id="9e1a8-820">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="9e1a8-821">Opção de soquete adicionada IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-821">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="9e1a8-822">Implementado função pwritev (ao carregar o arquivo para PHP/nginx-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-822">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="9e1a8-823">Adição de opções de soquete IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-823">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="9e1a8-824">Suporte para a opção de soquete IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-824">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="9e1a8-825">Opção de soquete _MTU IP (V6) adicionada para o nó de aplicativos, traceroute, dig, nslookup e host</span><span class="sxs-lookup"><span data-stu-id="9e1a8-825">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="9e1a8-826">Opção de soquete adicionada IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="9e1a8-826">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="9e1a8-827">Aprimoramentos do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-827">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="9e1a8-828">Permitir que a montagem de caminhos UNC</span><span class="sxs-lookup"><span data-stu-id="9e1a8-828">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="9e1a8-829">Habilitar o suporte CDFS em drvfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-829">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="9e1a8-830">Lidar corretamente com permissões de rede para sistemas de arquivos em drvfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-830">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="9e1a8-831">Adicionar suporte para unidades remotas a drvfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-831">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="9e1a8-832">Habilitar FAT dar suporte a drvfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-832">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="9e1a8-833">Aprimoramentos e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-833">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-834">Resultados LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-834">LTP Results</span></span>
<span data-ttu-id="9e1a8-835">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="9e1a8-835">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="9e1a8-836">Compilação 16170</span><span class="sxs-lookup"><span data-stu-id="9e1a8-836">Build 16170</span></span>

<span data-ttu-id="9e1a8-837">Para Windows geral informações sobre compilação 16170, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-837">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="9e1a8-838">Lançamos um novo [postagem de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutindo nossos esforços para testar o WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-838">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="9e1a8-839">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-839">Fixed</span></span>

- <span data-ttu-id="9e1a8-840">Soquete de suporte à opção IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-840">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="9e1a8-841">Adicione suporte para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-841">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="9e1a8-842">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-842">[GH 1692]</span></span>
- <span data-ttu-id="9e1a8-843">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-843">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-844">Resultados LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-844">LTP Results</span></span>
<span data-ttu-id="9e1a8-845">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="9e1a8-845">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="9e1a8-846">Compilar 15046 para o Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="9e1a8-846">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="9e1a8-847">Há não mais WSL correções ou recursos planejados para inclusão na atualização para o Windows 10 para criadores.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-847">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="9e1a8-848">Notas de versão do WSL serão retomada nas próximas semanas para adições de direcionamento a próxima atualização importante do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-848">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="9e1a8-849">Para Windows geral informações sobre compilação 15046 e Insider futuras versões visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-849">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="9e1a8-850">Compilação 15042</span><span class="sxs-lookup"><span data-stu-id="9e1a8-850">Build 15042</span></span>

<span data-ttu-id="9e1a8-851">Para Windows geral informações sobre compilação 15042, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-851">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-852">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-852">Fixed</span></span>

- <span data-ttu-id="9e1a8-853">Correção de um deadlock durante a remoção de um caminho que termina em ".."</span><span class="sxs-lookup"><span data-stu-id="9e1a8-853">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="9e1a8-854">Corrigido um problema em que FIONBIO não retornando 0 em caso de sucesso [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-854">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="9e1a8-855">Corrigido o problema com comprimento zero leituras de soquetes de datagrama inet</span><span class="sxs-lookup"><span data-stu-id="9e1a8-855">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="9e1a8-856">Corrigir um possível deadlock devido a condição de corrida na pesquisa de inode drvfs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-856">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="9e1a8-857">O suporte estendido para dados de auxiliares de soquete unix; SCM_CREDENTIALS e SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-857">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="9e1a8-858">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-858">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-859">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-859">LTP Results:</span></span>
<span data-ttu-id="9e1a8-860">Número de aprovação no teste: 737</span><span class="sxs-lookup"><span data-stu-id="9e1a8-860">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="9e1a8-861">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="9e1a8-861">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="9e1a8-862">Compilação 15031</span><span class="sxs-lookup"><span data-stu-id="9e1a8-862">Build 15031</span></span>

<span data-ttu-id="9e1a8-863">Para Windows geral informações sobre compilação 15031, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-863">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-864">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-864">Fixed</span></span>

- <span data-ttu-id="9e1a8-865">Corrigido um bug onde time(2) esporadicamente seria inadequados.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-865">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="9e1a8-866">Corrigido e emitir onde \* SIGPROCMASK syscalls pode corromper a máscara de sinal.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-866">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="9e1a8-867">Agora retorne comprimento de linha de comando completa na notificação de criação de processo WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-867">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="9e1a8-868">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-868">[GH 1632]</span></span>
- <span data-ttu-id="9e1a8-869">WSL agora relata a saída de thread por meio de ptrace suspensões GDB.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-869">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="9e1a8-870">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-870">[GH 1196]</span></span>
- <span data-ttu-id="9e1a8-871">Corrigido o bug onde ptys poderia ser interrompido após a pesado tmux e/s.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-871">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="9e1a8-872">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-872">[GH 1358]</span></span>
- <span data-ttu-id="9e1a8-873">Validação de tempo limite fixo em várias chamadas do sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-873">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="9e1a8-874">Suporte EFD_SEMAPHORE eventfd adicionado [GH 452]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-874">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="9e1a8-875">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-875">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-876">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-876">LTP Results:</span></span>
<span data-ttu-id="9e1a8-877">Número de aprovação no teste: 737</span><span class="sxs-lookup"><span data-stu-id="9e1a8-877">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="9e1a8-878">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="9e1a8-878">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="9e1a8-879">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-879">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="9e1a8-880">Compilação 15025</span><span class="sxs-lookup"><span data-stu-id="9e1a8-880">Build 15025</span></span>

<span data-ttu-id="9e1a8-881">Para Windows geral informações sobre compilação 15025, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-881">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-882">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-882">Fixed</span></span>

- <span data-ttu-id="9e1a8-883">Correção de bug que grep quebrado 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-883">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="9e1a8-884">Sinalizador EFD_SEMAPHORE implementado para eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-884">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="9e1a8-885">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-885">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="9e1a8-886">Sinal controlado por suporte de e/s para soquetes de fluxo de unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-886">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="9e1a8-887">Suporte F_GETPIPE_SZ e F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-887">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="9e1a8-888">Implementar recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-888">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="9e1a8-889">Corrigido o bug onde epoll_wait() não estava esperando [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-889">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="9e1a8-890">Implement /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="9e1a8-890">Implement /proc/version_signature</span></span>
- <span data-ttu-id="9e1a8-891">Syscall Tee agora retorna falha se ambos os descritores de arquivo se referirem ao mesmo pipe</span><span class="sxs-lookup"><span data-stu-id="9e1a8-891">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="9e1a8-892">Implementado comportamento correto em SO_PEERCRED para soquetes do Unix</span><span class="sxs-lookup"><span data-stu-id="9e1a8-892">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="9e1a8-893">Manipulação de parâmetro inválido de syscall tkill fixa</span><span class="sxs-lookup"><span data-stu-id="9e1a8-893">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="9e1a8-894">Alterações para aumentar a preformace de drvfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-894">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="9e1a8-895">Correção secundária para o bloqueio de e/s do Ruby</span><span class="sxs-lookup"><span data-stu-id="9e1a8-895">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="9e1a8-896">Fixo recvmsg() retornando EINVAL para o sinalizador MSG_DONTWAIT para soquetes inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-896">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="9e1a8-897">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-897">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-898">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-898">LTP Results:</span></span>
<span data-ttu-id="9e1a8-899">Número de aprovação no teste: 732</span><span class="sxs-lookup"><span data-stu-id="9e1a8-899">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="9e1a8-900">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="9e1a8-900">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="9e1a8-901">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-901">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="9e1a8-902">Compilação 15019</span><span class="sxs-lookup"><span data-stu-id="9e1a8-902">Build 15019</span></span>

<span data-ttu-id="9e1a8-903">Para Windows geral informações sobre compilação 15019, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-903">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-904">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-904">Fixed</span></span>

- <span data-ttu-id="9e1a8-905">Corrigido um bug que relatou incorretamente o uso da CPU em procfs para ferramentas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-905">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="9e1a8-906">Ao chamar Open () com O_TRUNC em uma existente arquivo inotify agora gera IN_MODIFY antes IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="9e1a8-906">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="9e1a8-907">Correções para getsockopt de soquete do unix SO_ERROR habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="9e1a8-907">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="9e1a8-908">Implementar /proc/sys/net/core/somaxconn para a linguagem GO</span><span class="sxs-lookup"><span data-stu-id="9e1a8-908">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="9e1a8-909">Tarefa de segundo plano de atualização de pacote de APT-get agora é executado oculta da exibição</span><span class="sxs-lookup"><span data-stu-id="9e1a8-909">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="9e1a8-910">Escopo claro para o localhost do ipv6 (Spring-Framework(Java) falha).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-910">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="9e1a8-911">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-911">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-912">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-912">LTP Results:</span></span>
<span data-ttu-id="9e1a8-913">Número de aprovação no teste: 714</span><span class="sxs-lookup"><span data-stu-id="9e1a8-913">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="9e1a8-914">Número de falha (com falha, ignorada, etc...): 249</span><span class="sxs-lookup"><span data-stu-id="9e1a8-914">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="9e1a8-915">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-915">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="9e1a8-916">Compilação 15014</span><span class="sxs-lookup"><span data-stu-id="9e1a8-916">Build 15014</span></span>

<span data-ttu-id="9e1a8-917">Para Windows geral informações sobre compilação 15014, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-917">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-918">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-918">Fixed</span></span>

- <span data-ttu-id="9e1a8-919">CTRL + C agora funciona conforme o esperado</span><span class="sxs-lookup"><span data-stu-id="9e1a8-919">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="9e1a8-920">htop e ps auxw agora mostram correto utilização de recursos (GH #516)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-920">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="9e1a8-921">Tradução básica de exceções de NT para sinais.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-921">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="9e1a8-922">(#513 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-922">(GH #513)</span></span>
- <span data-ttu-id="9e1a8-923">Agora fallocate falha com ENOSPC quando ficando sem espaço, em vez de EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-923">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="9e1a8-924">/Proc/sys/kernel/sem adicionado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-924">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="9e1a8-925">Chamadas do sistema semop e semtimedop implementadas</span><span class="sxs-lookup"><span data-stu-id="9e1a8-925">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="9e1a8-926">Erros de nslookup fixo com a opção de soquete IP_RECVTOS & IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-926">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="9e1a8-927">Suporte para opções de soquete IP_RECVTTL e IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="9e1a8-927">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="9e1a8-928">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-928">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-929">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-929">LTP Results:</span></span>
<span data-ttu-id="9e1a8-930">Número de aprovação no teste: 709</span><span class="sxs-lookup"><span data-stu-id="9e1a8-930">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="9e1a8-931">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="9e1a8-931">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="9e1a8-932">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-932">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="9e1a8-933">Resumo de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-933">Syscall Summary</span></span>
<span data-ttu-id="9e1a8-934">Syscalls total: 384</span><span class="sxs-lookup"><span data-stu-id="9e1a8-934">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="9e1a8-935">Total implementado: 235</span><span class="sxs-lookup"><span data-stu-id="9e1a8-935">Total Implemented: 235</span></span> </br>
<span data-ttu-id="9e1a8-936">Total de fazer o stub: 22</span><span class="sxs-lookup"><span data-stu-id="9e1a8-936">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="9e1a8-937">Total de não implementado: 127</span><span class="sxs-lookup"><span data-stu-id="9e1a8-937">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="9e1a8-938">Análise detalhada</span><span class="sxs-lookup"><span data-stu-id="9e1a8-938">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="9e1a8-939">Build 15007</span><span class="sxs-lookup"><span data-stu-id="9e1a8-939">Build 15007</span></span>

<span data-ttu-id="9e1a8-940">Para Windows geral informações sobre compilação 15007, visite o [Blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-940">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="9e1a8-941">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="9e1a8-941">Known Issue</span></span>

- <span data-ttu-id="9e1a8-942">Há um bug conhecido no qual o console não reconhece algumas Ctrl + <key> entrada.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-942">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="9e1a8-943">Isso inclui o comando ctrl-c, que agirá como um pressionamento de tecla "c" normal.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-943">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="9e1a8-944">Solução alternativa: Mapear uma chave alternativa para Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-944">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="9e1a8-945">Por exemplo, para mapear Ctrl + K, Ctrl + c fazer: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-945">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="9e1a8-946">Esse mapeamento é por terminal e precisará ser feito *cada* bash do tempo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-946">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="9e1a8-947">Os usuários podem explorar a opção de incluir isso no seu `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="9e1a8-947">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="9e1a8-948">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-948">Fixed</span></span>

- <span data-ttu-id="9e1a8-949">Corrigido o problema onde executando WSL consuma 100% de um núcleo de CPU</span><span class="sxs-lookup"><span data-stu-id="9e1a8-949">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="9e1a8-950">Opção IP_PKTINFO, IPV6_RECVPKTINFO agora tem suportada de soquete.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-950">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="9e1a8-951">(GH #851 987)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-951">(GH #851, 987)</span></span>
- <span data-ttu-id="9e1a8-952">Truncar o endereço físico de interface de rede para 16 bytes no lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-952">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="9e1a8-953">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-953">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-954">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-954">LTP Results:</span></span>
<span data-ttu-id="9e1a8-955">Número de aprovação no teste: 709</span><span class="sxs-lookup"><span data-stu-id="9e1a8-955">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="9e1a8-956">Número de falha (com falha, ignorada, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="9e1a8-956">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="9e1a8-957">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-957">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="9e1a8-958">Build 15002</span><span class="sxs-lookup"><span data-stu-id="9e1a8-958">Build 15002</span></span>

<span data-ttu-id="9e1a8-959">Para Windows geral informações no build 15002, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-959">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="9e1a8-960">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="9e1a8-960">Known Issue</span></span>

<span data-ttu-id="9e1a8-961">Dois problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-961">Two known issues:</span></span>
- <span data-ttu-id="9e1a8-962">Há um bug conhecido no qual o console não reconhece algumas Ctrl + <key> entrada.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-962">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="9e1a8-963">Isso inclui o comando ctrl-c, que agirá como um pressionamento de tecla "c" normal.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-963">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="9e1a8-964">Solução alternativa: Mapear uma chave alternativa para Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-964">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="9e1a8-965">Por exemplo, para mapear Ctrl + K, Ctrl + c fazer: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-965">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="9e1a8-966">Esse mapeamento é por terminal e precisará ser feito *cada* bash do tempo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-966">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="9e1a8-967">Os usuários podem explorar a opção de incluir isso no seu `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="9e1a8-967">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="9e1a8-968">Enquanto WSL está em execução, um thread de sistema consumirá 100% de um núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-968">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="9e1a8-969">A causa raiz foi resolvida e corrigida internamente.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-969">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="9e1a8-970">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-970">Fixed</span></span>

- <span data-ttu-id="9e1a8-971">Agora, todas as sessões de bash devem ser criadas no mesmo nível de permissão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-971">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="9e1a8-972">Tentativa de iniciar uma sessão em um nível diferente será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-972">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="9e1a8-973">Isso significa que os consoles de administrador e não-administrador não pode ser executado ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-973">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="9e1a8-974">(#626 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-974">(GH #626)</span></span>
<br/>
- <span data-ttu-id="9e1a8-975">Implementado as seguintes mensagens NETLINK_ROUTE (requer o administrador do Windows)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-975">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="9e1a8-976">RTM_NEWADDR (dá suporte a `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-976">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="9e1a8-977">RTM_NEWROUTE (dá suporte a `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-977">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="9e1a8-978">RTM_DELADDR (dá suporte a `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-978">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="9e1a8-979">RTM_DELROUTE (supports `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-979">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="9e1a8-980">Tarefa agendada, verificação de pacotes atualizar não serão mais executados em uma conexão limitada (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-980">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="9e1a8-981">Corrigido o erro em que canalizar obtém isto é, paralisada bash - c "ls - alR /" | bash -c "gato" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-981">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="9e1a8-982">Opção de soquete TCP_KEEPCNT implementada (GH #843)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-982">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="9e1a8-983">Opção de soquete IP_MTU_DISCOVER INET implementada (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-983">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="9e1a8-984">Removida a funcionalidade herdada para executar binários de NT de init com pesquisa de caminho do NT.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-984">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="9e1a8-985">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-985">(GH #1325)</span></span>
- <span data-ttu-id="9e1a8-986">Corrigir o modo de desenvolvimento/kmsg para permitir o acesso de leitura do grupo / (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-986">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="9e1a8-987">/Proc/sys/kernel/random/uuid implementado (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-987">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="9e1a8-988">Corrigido o erro em que a hora de início do processo estava mostrando como ano 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-988">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="9e1a8-989">Variável de ambiente de termo padrão comutada para xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-989">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="9e1a8-990">Modificado da maneira que o processo de confirmação é calculada durante a bifurcação do processo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-990">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="9e1a8-991">(#1286 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-991">(GH #1286)</span></span>
- <span data-ttu-id="9e1a8-992">/Proc/sys/vm/overcommit_memory implementado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-992">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="9e1a8-993">(#1286 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-993">(GH #1286)</span></span>
- <span data-ttu-id="9e1a8-994">Arquivo /proc/net/route implementado (GH #69)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-994">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="9e1a8-995">Correção de erro em que o nome do atalho foi incorretamente localizado (GH #696)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-995">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="9e1a8-996">Elf fixa analisando a lógica que valida incorretamente os cabeçalhos do programa deve ser menor que (ou igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-996">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="9e1a8-997">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-997">(GH #1048)</span></span>
- <span data-ttu-id="9e1a8-998">Retorno de chamada statfs implementado para procfs, sysfs, cgroupfs e binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-998">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="9e1a8-999">Windows AptPackageIndexUpdate fixo que não será fechado (1184 de # GH, também são discutidas em GH #1193)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-999">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="9e1a8-1000">Personalidade ASLR adicionada suporte ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1000">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="9e1a8-1001">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1001">(GH #1148, 1128)</span></span>
- <span data-ttu-id="9e1a8-1002">PTRACE_GETSIGINFO aprimorada, SIGSEGV para rastreamentos de pilha do gdb adequado durante AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1002">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="9e1a8-1003">ELF, não há mais de análise falha por patchelf binários.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1003">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="9e1a8-1004">(#471 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1004">(GH #471)</span></span>
- <span data-ttu-id="9e1a8-1005">VPN DNS propagadas para /etc/resolv.conf (GH #416 1350)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1005">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="9e1a8-1006">Feche o melhorias para TCP mais confiável para transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1006">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="9e1a8-1007">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1007">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="9e1a8-1008">Código de erro correto agora retornam quando há muitos arquivos abertos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1008">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="9e1a8-1009">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1009">(GH #1126, 2090)</span></span>
- <span data-ttu-id="9e1a8-1010">Auditoria do Windows agora relatórios de log de nome de imagem no processo de criar uma auditoria.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1010">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="9e1a8-1011">Normalmente falham ao iniciar bash.exe de dentro de uma janela de bash</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1011">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="9e1a8-1012">Mensagem de erro adicionado ao interoperabilidade não consegue acessar um diretório de trabalho em LxFs (ou seja, notepad.exe. bashrc)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1012">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="9e1a8-1013">Corrigido um problema em que o caminho do Windows foi truncado no WSL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1013">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="9e1a8-1014">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1014">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1015">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1015">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1016">Número de aprovação no teste: 690</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1016">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="9e1a8-1017">Número de falha (com falha, ignorada, etc...): 274</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1017">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="9e1a8-1018">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1018">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1019">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1019">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1020">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1020">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1021">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1021">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="9e1a8-1022">Compilação 14986</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1022">Build 14986</span></span>

<span data-ttu-id="9e1a8-1023">Para Windows geral informações sobre compilação 14986, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1023">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1024">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1024">Fixed</span></span>

- <span data-ttu-id="9e1a8-1025">Verificações de bugs fixas com Netlink e Pty IOCTLs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1025">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="9e1a8-1026">Versão do kernel agora relata 4.4.0-43 para manter a consistência com Xenial</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1026">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="9e1a8-1027">Bash.exe agora inicia quando a entrada direcionada para ' nul:' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1027">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="9e1a8-1028">IDs de thread agora é relatada corretamente no procfs (GH 967 de #)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1028">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="9e1a8-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Sinalizadores IN_ISDIR agora têm suportados no inotify_add_watch() (GH 1280 de #)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="9e1a8-1030">Implemente timer_create e chamadas do sistema relacionados.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1030">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="9e1a8-1031">Isso habilita o suporte GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1031">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="9e1a8-1032">Corrigido um problema em que o ping retornado um tempo de 0.000ms (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1032">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="9e1a8-1033">Retorne o código de erro correta quando muitos arquivos são abertos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1033">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="9e1a8-1034">Problema corrigido no WSL em que a solicitação Netlink para dados de interface de rede falharia com EINVAL se o endereço da interface hardware for 32-bytes (como a interface Teredo)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1034">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="9e1a8-1035">Observe que o utilitário Linux "ip" contém um bug em que ele falhará se WSL relata um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1035">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="9e1a8-1036">Este é um bug no "ip", não WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1036">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="9e1a8-1037">O "ip" utilitário embute o comprimento do buffer de cadeia de caracteres usado para imprimir o endereço de hardware, e esse buffer for muito pequeno para imprimir um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1037">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="9e1a8-1038">Melhorias e correções adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1038">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1039">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1039">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1040">Número de aprovação no teste: 669</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1040">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="9e1a8-1041">Número de falha (com falha, ignorada, etc...): 258</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1041">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="9e1a8-1042">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1042">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1043">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1043">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1044">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1044">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1045">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1045">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="9e1a8-1046">Compilação 14971</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1046">Build 14971</span></span>

<span data-ttu-id="9e1a8-1047">Para Windows geral informações sobre compilação 14971, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1047">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1048">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1048">Fixed</span></span>

 - <span data-ttu-id="9e1a8-1049">Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1049">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="9e1a8-1050">As atualizações agendadas regularmente serão retomada na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1050">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1051">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1051">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1052">Inalterado desde 14965</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1052">Unchanged from 14965</span></span> </br>
<span data-ttu-id="9e1a8-1053">Número de aprovação no teste: 664</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1053">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="9e1a8-1054">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1054">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9e1a8-1055">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1055">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="9e1a8-1056">Compilação 14965</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1056">Build 14965</span></span>

<span data-ttu-id="9e1a8-1057">Para Windows geral informações sobre compilação 14965, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1057">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1058">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1058">Fixed</span></span>

- <span data-ttu-id="9e1a8-1059">Suporte para Netlink soquetes do protocolo NETLINK_ROUTE RTM_GETLINK e RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1059">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="9e1a8-1060">Habilita comandos de ifconfig e ip para enumeração de rede</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1060">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="9e1a8-1061">Mais informações podem ser encontradas no nosso [postagem de blog de rede WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1061">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="9e1a8-1062">/sbin agora está no caminho do usuário por padrão</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1062">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="9e1a8-1063">Caminho de usuário NT agora anexado ao caminho WSL por padrão (ou seja, você pode agora digitar notepad.exe sem adicionar System32 para o caminho do Linux)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1063">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="9e1a8-1064">Suporte adicionado para /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1064">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="9e1a8-1065">Binários do NT agora pode ser iniciados no WSL quando o diretório de trabalho atual contém caracteres não-ansi (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1065">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="9e1a8-1066">Permitir desligamento em soquete de fluxo de unix desconectado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1066">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="9e1a8-1067">Adicionado suporte para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1067">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="9e1a8-1068">Suporte adicionado para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1068">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="9e1a8-1069">Corrigido o erro em que canalizar obtém isto é, paralisada bash - c "ls - alR /" | bash -c "gato" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1069">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="9e1a8-1070">Tratar solicitações para se conectar ao terminal atual.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1070">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="9e1a8-1071">Marcar /proc/.<pid>/oom_score_adj como gravável.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1071">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="9e1a8-1072">Adicione pasta /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1072">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="9e1a8-1073">sched_setaffinity deverá retornar o número de máscara de bits de afinidade</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1073">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="9e1a8-1074">Corrija a lógica de validação ELF que assume incorretamente os caminhos de interpretador devem ter menos de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1074">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="9e1a8-1075">(#743 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1075">(GH #743)</span></span>
- <span data-ttu-id="9e1a8-1076">Descritores de arquivo aberto podem manter a janela do console aberta (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1076">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="9e1a8-1077">Erro de Fixeed onde Rename () falhou com barra no nome de destino (GH #1008) à direita</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1077">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="9e1a8-1078">Implementar /proc/net/dev arquivo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1078">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="9e1a8-1079">Fixo 0.000ms executa ping devido à resolução do timer.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1079">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="9e1a8-1080">/Proc/self/environ implementado (GH #730)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1080">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="9e1a8-1081">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1081">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1082">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1082">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1083">Número de aprovação no teste: 664</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1083">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="9e1a8-1084">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1084">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9e1a8-1085">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1085">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="9e1a8-1086">Compilação 14959</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1086">Build 14959</span></span>

<span data-ttu-id="9e1a8-1087">Para Windows geral informações sobre compilação 14959, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1087">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1088">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1088">Fixed</span></span>

- <span data-ttu-id="9e1a8-1089">Notificação aprimorada do processo de Pico para Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1089">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="9e1a8-1090">Informações adicionais de [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1090">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="9e1a8-1091">Maior estabilidade com a interoperabilidade do Windows</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1091">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="9e1a8-1092">Correção de erro 0x80070057 ao iniciar bash.exe quando o Enterprise Data Protection (EDP) está habilitado</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1092">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="9e1a8-1093">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1093">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1094">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1094">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1095">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1095">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9e1a8-1096">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1096">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9e1a8-1097">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1097">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="9e1a8-1098">Compilação 14955</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1098">Build 14955</span></span>

<span data-ttu-id="9e1a8-1099">Para Windows geral informações sobre compilação 14955, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1099">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1100">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1100">Fixed</span></span>

 - <span data-ttu-id="9e1a8-1101">Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1101">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="9e1a8-1102">As atualizações agendadas regularmente serão retomada na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1102">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1103">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1103">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1104">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9e1a8-1105">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9e1a8-1106">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="9e1a8-1107">Compilação 14951</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1107">Build 14951</span></span>

<span data-ttu-id="9e1a8-1108">Para Windows geral informações sobre compilação 14951, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1108">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="9e1a8-1109">Novo recurso: Windows / interoperabilidade do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1109">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="9e1a8-1110">Binários do Windows agora podem ser chamados diretamente da linha de comando WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1110">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="9e1a8-1111">Isso fornece aos usuários a capacidade de interagir com seu ambiente do Windows e o sistema de forma que não foi possível.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1111">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="9e1a8-1112">Como um exemplo rápido, é possível que os usuários executem os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1112">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="9e1a8-1113">Mais informações podem ser encontradas em:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1113">More information can be found at:</span></span>

- [<span data-ttu-id="9e1a8-1114">Blog da equipe do WSL para interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1114">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="9e1a8-1115">Documentação de interoperabilidade do MSDN</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1115">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1116">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1116">Fixed</span></span>

- <span data-ttu-id="9e1a8-1117">Ubuntu 16.04 (Xenial) agora está instalado para todas as novas instâncias WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1117">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="9e1a8-1118">Os usuários com as instâncias (confiáveis) 14.04 existentes não serão atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1118">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="9e1a8-1119">Localidade definida durante a instalação agora é exibida.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1119">Locale set during install is now displayed</span></span>
- <span data-ttu-id="9e1a8-1120">Melhorias de terminal, incluindo o bug em que o redirecionamento de um processo WSL para um arquivo faz nem sempre funcionam</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1120">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="9e1a8-1121">Tempo de vida do console deve ser vinculado ao tempo de vida de bash.exe</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1121">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="9e1a8-1122">Tamanho da janela de console deve usar tamanho visível, o tamanho do buffer não</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1122">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="9e1a8-1123">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1123">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1124">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1124">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1125">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1125">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9e1a8-1126">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1126">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9e1a8-1127">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1127">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="9e1a8-1128">Compilação 14946</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1128">Build 14946</span></span>

<span data-ttu-id="9e1a8-1129">Para Windows geral informações sobre compilação 14946, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1129">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1130">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1130">Fixed</span></span>

- <span data-ttu-id="9e1a8-1131">Corrigido um problema que impediu a criação de contas de usuário do WSL para usuários com nomes de usuário do NT que contêm espaços ou aspas.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1131">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="9e1a8-1132">Alterar VolFs e DrvFs para retornar 0 para a contagem de links do diretório em stat</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1132">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="9e1a8-1133">Suporte à opção de soquete IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1133">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="9e1a8-1134">Limite a um único console loop de e/s por tty.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1134">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="9e1a8-1135">Exemplo: o comando a seguir é possível:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1135">Example: the following command is possible:</span></span>
  - <span data-ttu-id="9e1a8-1136">bash -c "dados echo" | bash - c "ssh user@example.com ' cat > foo '"</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="9e1a8-1137">Substitua os espaços por guias no /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1137">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="9e1a8-1138">DrvFs agora aparece no mountinfo com um nome que corresponde ao volume montado do Windows</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1138">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="9e1a8-1139">/Home e raiz agora aparecem no mountinfo com nomes corretos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1139">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="9e1a8-1140">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1140">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1141">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1141">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1142">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1142">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9e1a8-1143">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1143">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9e1a8-1144">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1144">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="9e1a8-1145">Compilação 14942</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1145">Build 14942</span></span>

<span data-ttu-id="9e1a8-1146">Para Windows geral informações sobre compilação 14942, visite o [Blog Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1146">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1147">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1147">Fixed</span></span>

- <span data-ttu-id="9e1a8-1148">Um número de verificações de bugs resolvidos, incluindo o "TENTATIVA de executar de /NOEXECUTE memória" rede falha que foi bloqueando SSH</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1148">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="9e1a8-1149">o suporte para notificações geradas de aplicativos do Windows em DrvFs inotifiy está agora</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1149">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="9e1a8-1150">Implemente TCP_KEEPIDLE e TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1150">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="9e1a8-1151">(#695 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1151">(GH #695)</span></span>
- <span data-ttu-id="9e1a8-1152">Implementar a chamada do sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1152">Implement the pivot_root system call</span></span>
- <span data-ttu-id="9e1a8-1153">Implementar a opção de soquete para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1153">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="9e1a8-1154">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1154">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1155">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1155">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1156">Número de aprovação no teste: 665</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1156">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9e1a8-1157">Número de falha (com falha, ignorada, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9e1a8-1158">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1159">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1159">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1160">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1160">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1161">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1161">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="9e1a8-1162">Compilação 14936</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1162">Build 14936</span></span>

<span data-ttu-id="9e1a8-1163">Para Windows geral informações sobre compilação 14936, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1163">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="9e1a8-1164">Observação: WSL instalará Ubuntu versão 16.04 (Xenial) em vez do Ubuntu 14.04 (confiável) em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1164">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="9e1a8-1165">Essa alteração será aplicada para Insiders instalar novas instâncias (lxrun.exe /install ou primeira execução do bash.exe).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1165">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="9e1a8-1166">As instâncias existentes com e confiável não serão atualizadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1166">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="9e1a8-1167">Os usuários podem atualizar suas imagens confiáveis para Xenial usando o comando de atualização de versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1167">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="9e1a8-1168">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1168">Known Issue</span></span>
<span data-ttu-id="9e1a8-1169">WSL está enfrentando um problema com algumas implementações de soquete.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1169">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="9e1a8-1170">A verificação de erro se manifesta como uma falha com o erro "TENTATIVA de executar /NOEXECUTE memória INSUFICIENTE".</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1170">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="9e1a8-1171">A manifestação mais comum desse problema é uma falha ao usar o ssh.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1171">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="9e1a8-1172">A causa raiz é fixo em compilações internas e será enviada para Insiders assim que possível.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1172">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1173">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1173">Fixed</span></span>

- <span data-ttu-id="9e1a8-1174">Implementado a chamada do sistema chroot</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1174">Implemented the chroot system call</span></span>
- <span data-ttu-id="9e1a8-1175">Melhorias no inotify ~~incluindo suporte para notificações geradas de aplicativos do Windows em DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1175">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="9e1a8-1176">Correção: Inotify dá suporte para alterações originadas a partir de aplicativos do Windows não está disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1176">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="9e1a8-1177">Associação de IPv6 de soquete::<port n> agora dá suporte a IPV6_V6ONLY (GH #68, 157 #, #393, 460 #, #674, 740 #, #982, 996 #)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1177">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="9e1a8-1178">Comportamento WNOWAIT para waitid systemcall implementado (GH #638)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1178">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="9e1a8-1179">Suporte para opções de soquete IP IP_HDRINCL e IP_TTL</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1179">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="9e1a8-1180">Read () de comprimento zero deve retornar imediatamente (GH #975)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1180">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="9e1a8-1181">Tratar corretamente os prefixos de nomes de arquivo e o nome do arquivo que não incluem um terminador nulo em um arquivo. tar.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1181">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="9e1a8-1182">suporte a epoll o /dev/null</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1182">epoll support for /dev/null</span></span>
- <span data-ttu-id="9e1a8-1183">Corrigir a fonte de tempo /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1183">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="9e1a8-1184">Bash -c agora capaz de redirecionar para um arquivo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1184">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="9e1a8-1185">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1185">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1186">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1186">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1187">Número de aprovação no teste: 664</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1187">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="9e1a8-1188">Número de falha (com falha, ignorada, etc...): 264</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1188">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="9e1a8-1189">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1189">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1190">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1190">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1191">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1191">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1192">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1192">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="9e1a8-1193">Compilação 14931</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1193">Build 14931</span></span>

<span data-ttu-id="9e1a8-1194">Para Windows geral informações sobre compilação 14931, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1194">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1195">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1195">Fixed</span></span>

 - <span data-ttu-id="9e1a8-1196">Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1196">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="9e1a8-1197">As atualizações agendadas regularmente serão retomada na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1197">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="9e1a8-1198">Compilação 14926</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1198">Build 14926</span></span>

<span data-ttu-id="9e1a8-1199">Para Windows geral informações sobre compilação 14926, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1199">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1200">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1200">Fixed</span></span>

- <span data-ttu-id="9e1a8-1201">Ping agora funciona em consoles que não têm privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1201">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="9e1a8-1202">Ping6 agora tem suportada, também sem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1202">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="9e1a8-1203">Suporte de Inotify para arquivos modificados por meio de WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1203">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="9e1a8-1204">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1204">(GH #216)</span></span>
  - <span data-ttu-id="9e1a8-1205">Sinalizadores com suporte:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1205">Flags supported:</span></span>
    - <span data-ttu-id="9e1a8-1206">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1206">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="9e1a8-1207">eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1207">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="9e1a8-1208">atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1208">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="9e1a8-1209">ler a saída: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1209">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="9e1a8-1210">Problema conhecido: Modificar arquivos de aplicativos do Windows não gera nenhum evento</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1210">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="9e1a8-1211">Soquete do UNIX agora dá suporte a SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1211">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9e1a8-1212">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1212">LTP Results:</span></span>
<span data-ttu-id="9e1a8-1213">Número de aprovação no teste: 651</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1213">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="9e1a8-1214">Número de falha (com falha, ignorada, etc...): 258</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1214">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="9e1a8-1215">Logs de execução de teste LTP</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1215">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="9e1a8-1216">Compilação 14915</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1216">Build 14915</span></span>

<span data-ttu-id="9e1a8-1217">Para Windows geral informações sobre compilação 14915, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1217">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1218">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1218">Fixed</span></span>
-  <span data-ttu-id="9e1a8-1219">Socketpair para soquetes de datagrama (GH #262) do unix</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1219">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="9e1a8-1220">Suporte de soquete do UNIX para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1220">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="9e1a8-1221">Suporte de soquete do UNIX para SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1221">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="9e1a8-1222">Suporte de soquete do UNIX para SOCK_SEQPACKET (GH #758 546 #)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1222">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="9e1a8-1223">Adicionando suporte para envio de soquete de datagrama de unix, recebimento e desligamento</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1223">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="9e1a8-1224">Corrija a verificação de erro devido à validação de parâmetro inválido mmap para endereços não fixos.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1224">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="9e1a8-1225">(#847 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1225">(GH #847)</span></span>
- <span data-ttu-id="9e1a8-1226">Suporte para suspender / retomar de estados de terminal</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1226">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="9e1a8-1227">Suporte para TIOCPKT ioctl desbloquear o utilitário de tela (GH #774)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1227">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="9e1a8-1228">Problema conhecido: Teclas de função não operacionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1228">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="9e1a8-1229">Corrigida uma corrida no TimerFd que poderia causar um membro liberado ReaderReady seja acessada por LxpTimerFdWorkerRoutine (GH #814)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1229">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="9e1a8-1230">Habilitar o suporte de chamada do sistema reinicializável para futex, sondagem e clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1230">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="9e1a8-1231">Suporte de montagem de associação adicionado</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1231">Added bind mount support</span></span>
- <span data-ttu-id="9e1a8-1232">remover o compartilhamento para oferecer suporte ao namespace de montagem</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1232">unshare for mount namespace support</span></span>
    - <span data-ttu-id="9e1a8-1233">Problema conhecido: Ao criar um novo namespace de montagem com `unshare(CLONE_NEWNS)` diretório de trabalho atual continuará apontar para o namespace antigo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1233">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="9e1a8-1234">Outros aperfeiçoamentos e correções de bugs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1234">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="9e1a8-1235">Compilação 14905</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1235">Build 14905</span></span>

<span data-ttu-id="9e1a8-1236">Para Windows geral informações sobre compilação 14905, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1236">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1237">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1237">Fixed</span></span>
- <span data-ttu-id="9e1a8-1238">Sistema reinicializável chamadas agora são suportado (GH #349 GH #520)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1238">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="9e1a8-1239">Links simbólicos para diretórios terminando em / agora operacionais (GH #650)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1239">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="9e1a8-1240">Implementado ioctl RNDGETENTCNT para /dev/random</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1240">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="9e1a8-1241">Implementado o /proc/. [pid] / monta /proc/. [pid] / mountinfo e /proc/. [pid] / mountstats arquivos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1241">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="9e1a8-1242">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1242">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="9e1a8-1243">Compilação 14901</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1243">Build 14901</span></span>
<span data-ttu-id="9e1a8-1244">Primeiro Insider build para a versão de atualização de aniversário do Windows 10 de postagem.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1244">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="9e1a8-1245">Para Windows geral informações sobre compilação 14901, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1245">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1246">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1246">Fixed</span></span>
- <span data-ttu-id="9e1a8-1247">Corrigido o problema de barra "/" à direita</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1247">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="9e1a8-1248">Comandos como `$ mv a/c/ a/b/` agora funciona</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1248">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="9e1a8-1249">Instalando agora solicita se Ubuntu localidade deve ser definida como localidade do Windows</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1249">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="9e1a8-1250">Procfs suporte para a pasta de ns</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1250">Procfs support for ns folder</span></span>
- <span data-ttu-id="9e1a8-1251">Adicionado a montagem e desmontagem para tmpfs, procfs e sistemas de arquivos sysfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1251">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="9e1a8-1252">Corrigir mknod [arroba], assinatura ABI de 32 bits</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1252">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="9e1a8-1253">Movido para o modelo de expedição de soquetes do UNIX</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1253">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="9e1a8-1254">Tamanho do buffer de recebimento INET soquete definido usando o setsockopt deveria ser respeitado.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1254">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="9e1a8-1255">Sinalizador de mensagem de recebimento de soquete do unix MSG_CMSG_CLOEXEC implementar</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1255">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="9e1a8-1256">Redirecionamento de pipe de stdin/stdout de processo do Linux (GH n º 2)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1256">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="9e1a8-1257">Permite que o pipe de comandos de bash - c no CMD.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1257">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="9e1a8-1258">Exemplo: > dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1258">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="9e1a8-1259">Bash agora pode ser instalado em sistemas com vários arquivos de paginação (GH #538 358 #)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1259">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="9e1a8-1260">Tamanho do buffer de soquete INET padrão deve corresponder da configuração padrão do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1260">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="9e1a8-1261">Alinhar syscalls xattr para listxattr</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1261">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="9e1a8-1262">Retornar apenas as interfaces com um endereço IPv4 válido de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1262">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="9e1a8-1263">Corrigir a ação padrão de sinal quando injetado por ptrace</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1263">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="9e1a8-1264">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1264">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="9e1a8-1265">Use os valores do registro de contexto de máquina ao restaurar o contexto no sigreturn</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1265">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="9e1a8-1266">Isso resolve o problema em que o java e javac foram deslocado para alguns usuários</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1266">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="9e1a8-1267">Implementar /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1267">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1268">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1268">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1269">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1269">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1270">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1270">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="9e1a8-1271">Compilar 14388 para atualização de aniversário do Windows 10</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1271">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="9e1a8-1272">Para Windows geral informações sobre compilação 14388, visite o [Blog Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1272">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1273">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1273">Fixed</span></span>
- <span data-ttu-id="9e1a8-1274">Correções para se preparar para a atualização de aniversário do Windows 10 em 8/2</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1274">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="9e1a8-1275">Para obter mais informações sobre como o WSL na atualização de aniversário podem ser encontradas em nossa [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1275">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="9e1a8-1276">Compilação 14376</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1276">Build 14376</span></span>
<span data-ttu-id="9e1a8-1277">Para Windows geral informações sobre compilação 14376, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1277">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1278">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1278">Fixed</span></span>
- <span data-ttu-id="9e1a8-1279">Removido algumas instâncias em que o apt-get trava (GH #493)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1279">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="9e1a8-1280">Corrigido um problema em que as montagens vazias não foram tratadas corretamente</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1280">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="9e1a8-1281">Corrigido um problema em que ramdisks não foram montados corretamente</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1281">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="9e1a8-1282">Aceitação de soquete do unix de alteração para dar suporte a sinalizadores (parcial GH #451)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1282">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="9e1a8-1283">Fixo de rede comuns relacionadas a tela azul</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1283">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="9e1a8-1284">Corrigido o bluescreen ao acessar /proc/. [pid] / tarefa (GH #523)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1284">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="9e1a8-1285">Fixo alta utilização da CPU para alguns cenários pty (GH 488 #, #504)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1285">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="9e1a8-1286">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1286">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="9e1a8-1287">Compilação 14371</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1287">Build 14371</span></span>
<span data-ttu-id="9e1a8-1288">Para Windows geral informações sobre compilação 14371, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1288">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1289">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1289">Fixed</span></span>
- <span data-ttu-id="9e1a8-1290">Corrigida a corrida de medição de tempo com SIGCHLD e wait() ao usar ptrace</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1290">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="9e1a8-1291">Corrigidos alguns comportamentos quando os caminhos têm à direita / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1291">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="9e1a8-1292">Corrigido o problema com a renomeação/desvincular falhando devido a identificadores abertos para crianças</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1292">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="9e1a8-1293">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1293">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="9e1a8-1294">Compilação 14366</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1294">Build 14366</span></span>
<span data-ttu-id="9e1a8-1295">Para Windows geral informações sobre compilação 14366, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1295">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1296">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1296">Fixed</span></span>
- <span data-ttu-id="9e1a8-1297">Corrigir na criação do arquivo por meio de links simbólicos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1297">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="9e1a8-1298">Adicionado listxattr para Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1298">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="9e1a8-1299">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1299">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1300">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1300">Syscall Support</span></span>
-   <span data-ttu-id="9e1a8-1301">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1301">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1302">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1302">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="9e1a8-1303">O build 14361</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1303">Build 14361</span></span>
<span data-ttu-id="9e1a8-1304">Para Windows geral informações no build 14361, visite o [Blog Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1304">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1305">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1305">Fixed</span></span>
- <span data-ttu-id="9e1a8-1306">DrvFs agora diferencia maiusculas de minúsculas quando em execução no Bash no Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1306">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="9e1a8-1307">Os usuários case.txt de maio e caso. Unidades de TXT no seu c/dev/emcpowera1</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1307">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="9e1a8-1308">Somente há suporte para a diferenciação de maiusculas dentro do Bash no Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1308">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="9e1a8-1309">Quando fora do NTFS Bash relatará corretamente os arquivos, mas um comportamento inesperado pode ocorrer a interação com os arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1309">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="9e1a8-1310">A raiz de cada volume (ou seja, /mnt/c) não diferencia maiusculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1310">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="9e1a8-1311">Para obter mais informações sobre como tratar esses arquivos no Windows podem ser encontradas [aqui](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1311">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="9e1a8-1312">Aperfeiçoou pty / tty suporte.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1312">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="9e1a8-1313">Aplicativos como TMUX agora tem suporte (GH n º 40)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1313">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="9e1a8-1314">Problema de instalação fixa em que contas de usuário criadas nem sempre</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1314">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="9e1a8-1315">Estrutura de arg de linha de comando, permitindo a lista de argumentos muitíssimo otimizada.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1315">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="9e1a8-1316">(#153 GH)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1316">(GH #153)</span></span>
- <span data-ttu-id="9e1a8-1317">Arquivos de read_only agora capaz de excluir e chmod de DrvFs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1317">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="9e1a8-1318">Corrigidos alguns casos onde a terminal trava na desconexão (GH n º 43)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1318">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="9e1a8-1319">chmod e alterar o proprietário agora funcionam em dispositivos de tty</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1319">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="9e1a8-1320">Permitir a conexão para 0.0.0.0 e:: como localhost (GH 388)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1320">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="9e1a8-1321">Sendmsg/recvmsg agora lidar com um comprimento do vetor de e/s de > 1 (parcial GH #376)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1321">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="9e1a8-1322">Os usuários podem agora recusá-la do arquivo de hosts gerada automaticamente (GH #398)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1322">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="9e1a8-1323">A correspondência automática de localidade do Linux para a localidade do NT durante a instalação (GH #11)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1323">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="9e1a8-1324">Adicionado o arquivo /proc/sys/vm/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1324">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="9e1a8-1325">strace agora é encerrado corretamente</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1325">strace now exits correctly</span></span>
- <span data-ttu-id="9e1a8-1326">Permitir que os pipes para ser reaberto por meio de /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1326">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="9e1a8-1327">Ocultar diretórios sob %LOCALAPPDATA%\lxss de DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1327">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="9e1a8-1328">Melhor tratamento de bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1328">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="9e1a8-1329">Comandos como "bash ~ ls - c" agora tem suporte (GH #467)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1329">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="9e1a8-1330">Soquetes agora notificar epoll leitura disponível durante o desligamento (GH #271)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1330">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="9e1a8-1331">lxrun / desinstalação faz um trabalho melhor de excluir os arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1331">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="9e1a8-1332">Corrigido ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1332">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="9e1a8-1333">Suporte aprimorado para x11 aplicativos como xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1333">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="9e1a8-1334">Atualizado o tamanho de pilha do thread inicial para corresponder à configuração do Ubuntu padrão e informar o tamanho corretamente para o syscall get_rlimit (GH 172 #, #258)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1334">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="9e1a8-1335">Relatórios de nomes de imagem de processo de pico (por exemplo, para fazer auditoria) aprimorados</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1335">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="9e1a8-1336">/Proc/mountinfo implementado para o comando df</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1336">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="9e1a8-1337">Correção de código de erro de symlink para o nome do filho.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1337">Fixed symlink error code for child name .</span></span> <span data-ttu-id="9e1a8-1338">e...</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1338">and ..</span></span>
- <span data-ttu-id="9e1a8-1339">Melhorias e correções de bug de aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1339">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1340">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1340">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1341">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1341">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1342">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1342">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="9e1a8-1343">Build 14352</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1343">Build 14352</span></span>
<span data-ttu-id="9e1a8-1344">Para Windows geral informações no build 14352, visite o [Blog Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1344">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1345">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1345">Fixed</span></span>
- <span data-ttu-id="9e1a8-1346">Correção do problema em que grandes arquivos não foram baixados / criados corretamente.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1346">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="9e1a8-1347">Isso deve desbloquear npm e outros cenários (GH n º 3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1347">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="9e1a8-1348">Removido algumas instâncias onde soquetes de suspensão</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1348">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="9e1a8-1349">Corrigidos alguns erros ptrace</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1349">Corrected some ptrace errors</span></span>
- <span data-ttu-id="9e1a8-1350">Corrigido o problema com o WSL, permitindo que mais de 255 caracteres de nomes de arquivo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1350">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="9e1a8-1351">Suporte aprimorado para caracteres estendidos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1351">Improved support for non-English characters</span></span>
- <span data-ttu-id="9e1a8-1352">Adicionar dados de fuso horário atual do Windows e definir como padrão</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1352">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="9e1a8-1353">Do id exclusiva do dispositivo para cada ponto de montagem (fix jre – GH n º 49)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1353">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="9e1a8-1354">Corrigir problema com caminhos que contenham "."</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1354">Correct issue with paths containing “.”</span></span> <span data-ttu-id="9e1a8-1355">e ".."</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1355">and “..”</span></span>
- <span data-ttu-id="9e1a8-1356">Adicionado suporte Fifo (GH #71)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1356">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="9e1a8-1357">Formato atualizado do resolv. conf para corresponder ao formato nativo do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1357">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="9e1a8-1358">Uma limpeza procfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1358">Some procfs cleanup</span></span>
- <span data-ttu-id="9e1a8-1359">Ping habilitado para consoles do administrador (GH n º 18)</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1359">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1360">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1360">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1361">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1361">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1362">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1362">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="9e1a8-1363">Compilação 14342</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1363">Build 14342</span></span>
<span data-ttu-id="9e1a8-1364">Para Windows geral informações sobre compilação 14342 a [Blog Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1364">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="9e1a8-1365">Informações sobre VolFs e DriveFs podem ser encontradas na [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1365">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1366">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1366">Fixed</span></span>
- <span data-ttu-id="9e1a8-1367">Corrigido o problema de instalação quando o usuário do Windows tinha caracteres Unicode no nome de usuário</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1367">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="9e1a8-1368">A solução alternativa udev de atualização de apt-get nas perguntas Frequentes agora é fornecida por padrão na primeira execução</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1368">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="9e1a8-1369">Habilitada a links simbólicos no DriveFs (/mnt/<drive>) diretórios</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1369">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="9e1a8-1370">Links simbólicos agora funcionam entre DriveFs e VolFs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1370">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="9e1a8-1371">Caminho de nível superior endereçado ao problema de análise: ls. / / agora funcionará conforme o esperado</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1371">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="9e1a8-1372">instalar o NPM em DriveFs e as opções -g agora estão trabalhando</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1372">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="9e1a8-1373">Problema corrigido, impedindo que o servidor PHP iniciando</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1373">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="9e1a8-1374">Valores de ambiente padrão atualizado, como $PATH para corresponder mais próximos Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1374">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="9e1a8-1375">Adicionada uma tarefa de manutenção semanal no Windows para atualizar o cache de pacotes apt</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1375">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="9e1a8-1376">Corrigido um problema com a validação de cabeçalho ELF, WSL agora dá suporte a todas as opções de Melkor</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1376">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="9e1a8-1377">Shell zsh é funcional</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1377">Zsh shell is functional</span></span>
- <span data-ttu-id="9e1a8-1378">Agora há suporte para os binários pré-compilados do Go</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1378">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="9e1a8-1379">Avisar sobre Bash.exe executado pela primeira vez agora está localizado corretamente</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1379">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="9e1a8-1380">/proc/meminfo agora retorna informações corretas</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1380">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="9e1a8-1381">Soquetes agora têm suportados no VFS</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1381">Sockets now supported in VFS</span></span>
- <span data-ttu-id="9e1a8-1382">/dev agora montado como tempfs</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1382">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="9e1a8-1383">PEPS agora tem suportada</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1383">Fifo now supported</span></span>
- <span data-ttu-id="9e1a8-1384">Sistemas de vários núcleos agora mostrando corretamente em/proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1384">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="9e1a8-1385">Melhorias adicionais e mensagens de erro de download durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1385">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="9e1a8-1386">Syscall melhorias e correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1386">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="9e1a8-1387">Syscall com suporte a lista abaixo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1387">Supported syscall list below.</span></span>
- <span data-ttu-id="9e1a8-1388">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1388">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="9e1a8-1389">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1389">Known Issues</span></span>
- <span data-ttu-id="9e1a8-1390">Não Resolvendo '.. '</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1390">Not resolving ‘..’</span></span> <span data-ttu-id="9e1a8-1391">corretamente em DriveFs em alguns casos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1391">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1392">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1392">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1393">Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1393">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1394">Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1394">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="9e1a8-1395">Compilação 14332</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1395">Build 14332</span></span>

<span data-ttu-id="9e1a8-1396">Para Windows geral informações sobre compilação 14332, visite o [Blog Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1396">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="9e1a8-1397">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1397">Fixed</span></span>
- <span data-ttu-id="9e1a8-1398">Melhor geração de resolv. conf, incluindo a priorizar as entradas DNS</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1398">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="9e1a8-1399">Problema com a movimentação de arquivos e diretórios entre /mnt e não- / mnt unidades</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1399">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="9e1a8-1400">Os arquivos tar agora podem ser criados com links simbólicos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1400">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="9e1a8-1401">Diretório de /run/lock padrão adicionados na criação da instância</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1401">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="9e1a8-1402">Atualizar o /dev/null para retornar informações de stat adequada</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1402">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="9e1a8-1403">Erros adicionais durante o download durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1403">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="9e1a8-1404">Syscall melhorias e correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1404">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="9e1a8-1405">Syscall com suporte a lista abaixo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1405">Supported syscall list below.</span></span>
- <span data-ttu-id="9e1a8-1406">Melhorias e correções de bug de aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1406">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1407">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1407">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1408">Abaixo está a nova syscall que tem alguma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1408">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="9e1a8-1409">O syscall nesta lista tem suporte pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1409">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="9e1a8-1410">Build 14328</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1410">Build 14328</span></span>

<span data-ttu-id="9e1a8-1411">Para Windows geral informações sobre compilação 14332, visite o [Blog Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1411">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="9e1a8-1412">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1412">New Features</span></span>
* <span data-ttu-id="9e1a8-1413">Agora dão suporte a usuários do Linux.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1413">Now support Linux users.</span></span>  <span data-ttu-id="9e1a8-1414">Instalação do Bash no Ubuntu no Windows solicitará que para a criação de um usuário do Linux.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1414">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="9e1a8-1415">Para obter mais informações, visite https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1415">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="9e1a8-1416">Nome do host agora está definido para o nome do computador Windows, não há mais @localhost</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1416">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="9e1a8-1417">Para obter mais informações sobre build 14328, visite: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1417">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="9e1a8-1418">Fixo</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1418">Fixed</span></span>
* <span data-ttu-id="9e1a8-1419">Melhorias de symlink para /mnt/ não<drive> arquivos</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1419">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="9e1a8-1420">instalação de NPM agora funciona</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1420">npm install now works</span></span>
    * <span data-ttu-id="9e1a8-1421">JDK / jre agora pode ser instalado usando as instruções encontradas [aqui](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1421">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="9e1a8-1422">problema conhecido: links simbólicos não funcionam para o Windows monta.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1422">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="9e1a8-1423">Funcionalidade estará disponível em uma compilação posterior</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1423">Functionality will be available in a later build</span></span>
* <span data-ttu-id="9e1a8-1424">parte superior e htop agora exibem</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1424">top and htop now display</span></span>
* <span data-ttu-id="9e1a8-1425">Mensagens de erro adicionais para algumas falhas de instalação</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1425">Additional error messages for some install failures</span></span>
* <span data-ttu-id="9e1a8-1426">Syscall melhorias e correções de bugs.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1426">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="9e1a8-1427">Syscall com suporte a lista abaixo.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1427">Supported syscall list below.</span></span>
* <span data-ttu-id="9e1a8-1428">Melhorias e correções de bug de aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1428">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9e1a8-1429">Suporte de syscall</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1429">Syscall Support</span></span>
<span data-ttu-id="9e1a8-1430">Abaixo está uma lista de syscalls com alguma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1430">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="9e1a8-1431">Syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9e1a8-1431">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
