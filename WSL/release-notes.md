---
title: Notas de versão do subsistema Windows para Linux
description: Notas de versão do subsistema Windows para Linux.  Atualizado semanalmente.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: e2d9d5fc70c173e9b516ab7af01599b623b40b39
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67042428"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="eebc2-105">Notas de versão do subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="eebc2-105">Release Notes for Windows Subsystem for Linux</span></span>


## <a name="build-18917"></a><span data-ttu-id="eebc2-106">Build 18917</span><span class="sxs-lookup"><span data-stu-id="eebc2-106">Build 18917</span></span>
<span data-ttu-id="eebc2-107">Para obter informações gerais do Windows sobre o Build 18917 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-107">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-108">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-108">WSL</span></span>
* <span data-ttu-id="eebc2-109">WSL 2 já está disponível!</span><span class="sxs-lookup"><span data-stu-id="eebc2-109">WSL 2 is now available!</span></span> <span data-ttu-id="eebc2-110">Consulte o [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="eebc2-110">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="eebc2-111">Corrigir uma regressão em que a inicialização de processos do Windows via symlinks não funcionou corretamente [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="eebc2-111">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="eebc2-112">Adicione WSL. exe--List--Verbose, WSL. exe--List--Quiet e WSL. exe--Import--opções de versão a WSL. exe</span><span class="sxs-lookup"><span data-stu-id="eebc2-112">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="eebc2-113">Adicionar WSL. exe--opção de desligamento</span><span class="sxs-lookup"><span data-stu-id="eebc2-113">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="eebc2-114">Plano 9: Permitir que a abertura de um diretório para gravação seja realizada com sucesso</span><span class="sxs-lookup"><span data-stu-id="eebc2-114">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="eebc2-115">Build 18890</span><span class="sxs-lookup"><span data-stu-id="eebc2-115">Build 18890</span></span>
<span data-ttu-id="eebc2-116">Para obter informações gerais do Windows sobre o Build 18890 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-116">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-117">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-117">WSL</span></span>
* <span data-ttu-id="eebc2-118">Vazamento de soquete sem bloqueio [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="eebc2-118">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="eebc2-119">A entrada de EOF para o terminal pode bloquear leituras subsequentes [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="eebc2-119">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="eebc2-120">Atualize o cabeçalho de resolução. conf para fazer referência a WSL. conf [discutido no GH 3928]</span><span class="sxs-lookup"><span data-stu-id="eebc2-120">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="eebc2-121">Deadlock no código de exclusão de epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="eebc2-121">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="eebc2-122">Manipular espaços em argumentos para--Import e – export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="eebc2-122">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="eebc2-123">A extensão de arquivos mmap não funciona corretamente [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="eebc2-123">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="eebc2-124">Correção do problema com \\o ARM64 WSL $ Access não funcionar corretamente</span><span class="sxs-lookup"><span data-stu-id="eebc2-124">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="eebc2-125">Adicionar melhor ícone padrão para WSL. exe</span><span class="sxs-lookup"><span data-stu-id="eebc2-125">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="eebc2-126">Build 18342</span><span class="sxs-lookup"><span data-stu-id="eebc2-126">Build 18342</span></span>
<span data-ttu-id="eebc2-127">Para obter informações gerais do Windows sobre o Build 18342 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-127">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-128">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-128">WSL</span></span>
* <span data-ttu-id="eebc2-129">Adicionamos a capacidade para os usuários acessarem arquivos do Linux em um WSL distribuição do Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-129">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="eebc2-130">Esses arquivos podem ser acessados por meio da linha de comando, e também aplicativos do Windows, como explorador de arquivos, VSCode, etc. podem interagir com esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-130">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="eebc2-131">Acesse seus arquivos navegando \\até \\WSL\\$ < distro_name > ou consulte uma lista de distribuições em execução navegando \\até \\WSL $</span><span class="sxs-lookup"><span data-stu-id="eebc2-131">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="eebc2-132">Adicionar marcas de informações de CPU adicionais e corrigir os valores de Cpus_allowed [_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="eebc2-132">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="eebc2-133">Suporte a exec de thread não líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="eebc2-133">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="eebc2-134">Tratar falhas de atualização de configuração como não fatal [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="eebc2-134">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="eebc2-135">Atualizar binfmt para lidar corretamente com os deslocamentos [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="eebc2-135">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="eebc2-136">Habilitar o mapeamento de unidades de rede para o plano 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="eebc2-136">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="eebc2-137">Suporte para Windows-> Linux e Linux-> Tradução de caminho do Windows para montagens de associação</span><span class="sxs-lookup"><span data-stu-id="eebc2-137">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="eebc2-138">Criar seções somente leitura para mapeamentos em arquivos abertos somente leitura</span><span class="sxs-lookup"><span data-stu-id="eebc2-138">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="eebc2-139">Build 18334</span><span class="sxs-lookup"><span data-stu-id="eebc2-139">Build 18334</span></span>
<span data-ttu-id="eebc2-140">Para obter informações gerais do Windows sobre o Build 18334 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-140">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-141">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-141">WSL</span></span>
* <span data-ttu-id="eebc2-142">Reprojetar a maneira como o fuso horário do Windows é mapeado para um fuso horário do Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="eebc2-142">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="eebc2-143">Corrigir vazamentos de memória e adicionar novas funções de conversão de cadeia de caracteres [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="eebc2-143">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="eebc2-144">SIGCONT em um thread sem threads é um não operacional [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="eebc2-144">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="eebc2-145">Exibir corretamente os descritores de arquivo de soquete e epoll no/proc/Self/FD</span><span class="sxs-lookup"><span data-stu-id="eebc2-145">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="eebc2-146">Build 18305</span><span class="sxs-lookup"><span data-stu-id="eebc2-146">Build 18305</span></span>
<span data-ttu-id="eebc2-147">Para obter informações gerais do Windows sobre o Build 18305 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-147">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-148">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-148">WSL</span></span>
* <span data-ttu-id="eebc2-149">pthreads perder o acesso a arquivos quando o thread primário sair [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="eebc2-149">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="eebc2-150">TIOCSCTTY deve ignorar o parâmetro "Force", a menos que seja necessário [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="eebc2-150">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="eebc2-151">melhorias na linha de comando do WSL. exe e adição de funcionalidade de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="eebc2-151">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="eebc2-152">Build 18277</span><span class="sxs-lookup"><span data-stu-id="eebc2-152">Build 18277</span></span>
<span data-ttu-id="eebc2-153">Para obter informações gerais do Windows sobre o Build 18277 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-153">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-154">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-154">WSL</span></span>
* <span data-ttu-id="eebc2-155">Corrigir o erro "não há suporte para essa interface" introduzido na compilação 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="eebc2-155">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="eebc2-156">Ignorar o sinalizador MNT_FORCE para o syscall umount [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="eebc2-156">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="eebc2-157">Alternar a interoperabilidade WSL para usar a API CreatePseudoConsole oficial</span><span class="sxs-lookup"><span data-stu-id="eebc2-157">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="eebc2-158">Manter nenhum valor de tempo limite durante a reinicialização de FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="eebc2-158">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="eebc2-159">Build 18272</span><span class="sxs-lookup"><span data-stu-id="eebc2-159">Build 18272</span></span>
<span data-ttu-id="eebc2-160">Para obter informações gerais do Windows sobre o Build 18272 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-160">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-161">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-161">WSL</span></span>
* <span data-ttu-id="eebc2-162">**ALERTA** Há um problema nessa compilação que torna o WSL inoperante.</span><span class="sxs-lookup"><span data-stu-id="eebc2-162">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="eebc2-163">Ao tentar iniciar sua distribuição, você verá um erro "nenhuma interface com suporte".</span><span class="sxs-lookup"><span data-stu-id="eebc2-163">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="eebc2-164">O problema foi corrigido e estará na compilação rápida do insider da próxima semana.</span><span class="sxs-lookup"><span data-stu-id="eebc2-164">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="eebc2-165">Se você tiver instalado essa compilação, poderá reverter para a compilação anterior do Windows usando "voltar para a versão anterior do Windows 10" em Settings-> Update & Security-> Recovery.</span><span class="sxs-lookup"><span data-stu-id="eebc2-165">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="eebc2-166">Build 18267</span><span class="sxs-lookup"><span data-stu-id="eebc2-166">Build 18267</span></span>
<span data-ttu-id="eebc2-167">Para obter informações gerais do Windows sobre o Build 18267 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-167">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-168">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-168">WSL</span></span>
* <span data-ttu-id="eebc2-169">Correção do problema em que o processo zumbi pode não ser aproveitado e permanecer indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="eebc2-169">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="eebc2-170">WslRegisterDistribution paralisa se a mensagem de erro exceder o comprimento máximo [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="eebc2-170">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="eebc2-171">Permitir que o fsync tenha sucesso para arquivos somente leitura no DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="eebc2-171">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="eebc2-172">Verifique se os diretórios/bin e/sbin existem antes de criar symlinks dentro de [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="eebc2-172">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="eebc2-173">Adicionou um mecanismo de tempo limite de encerramento de instância para instâncias de WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-173">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="eebc2-174">O tempo limite é definido atualmente como 15 segundos, o que significa que a instância será encerrada 15 segundos após o último processo de WSL sair.</span><span class="sxs-lookup"><span data-stu-id="eebc2-174">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="eebc2-175">Para encerrar uma distribuição imediatamente, use:</span><span class="sxs-lookup"><span data-stu-id="eebc2-175">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="eebc2-176">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="eebc2-176">Build 17763 (1809)</span></span>
<span data-ttu-id="eebc2-177">Para obter informações gerais do Windows sobre o Build 17763 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-177">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-178">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-178">WSL</span></span>
* <span data-ttu-id="eebc2-179">Verificação de permissão syscall setanteriority muito estrita para alterar a mesma prioridade de thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="eebc2-179">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="eebc2-180">Verifique se o tempo de interrupção não polarizado é usado para o tempo de inicialização para evitar retornar valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="eebc2-180">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="eebc2-181">Tratar symlinks no intérprete WSL binfmt [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="eebc2-181">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="eebc2-182">Melhor manipulação da limpeza do descritor de arquivo de líder do grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="eebc2-182">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="eebc2-183">Alterne WSL para usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter para evitar o estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="eebc2-183">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="eebc2-184">A anexação ptrace pode causar um valor de retorno insatisfatório de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="eebc2-184">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="eebc2-185">Corrigir vários problemas relacionados ao AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="eebc2-185">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="eebc2-186">Correção do problema que poderia causar falha de interoperabilidade WSL se o diretório de trabalho atual tiver menos de 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="eebc2-186">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="eebc2-187">Evite um segundo atraso na falha de conexões de loopback para portas inexistentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="eebc2-187">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="eebc2-188">Adicionar arquivo stub/proc/sys/FS/File-Max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="eebc2-188">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="eebc2-189">Informações mais precisas sobre o escopo do IPV6.</span><span class="sxs-lookup"><span data-stu-id="eebc2-189">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="eebc2-190">Suporte do PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="eebc2-190">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="eebc2-191">O sistema de arquivos de pipe inadvertidamente limpa o evento epoll disparado por borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="eebc2-191">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="eebc2-192">O executável do Win32 iniciado via NTFS symlink não respeita o symlink Name [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="eebc2-192">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="eebc2-193">Suporte ao zumbi melhorado [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="eebc2-193">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="eebc2-194">Adicionar entradas WSL. conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="eebc2-194">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="eebc2-195">Correção para getsockname nem sempre retornando tipo de família de soquetes UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="eebc2-195">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="eebc2-196">Adicionar suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="eebc2-196">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="eebc2-197">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="eebc2-197">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="eebc2-198">Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="eebc2-198">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="eebc2-199">Corrigir o problema de verificação de permissão na pasta raiz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="eebc2-199">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="eebc2-200">Suporte limitado para os IOCTLs de teclado TTY KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="eebc2-200">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="eebc2-201">Os aplicativos da interface do usuário do Windows devem ser executados mesmo quando iniciados em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="eebc2-201">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="eebc2-202">Adicionar a opção WSL-u ou--User [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="eebc2-202">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="eebc2-203">Corrigir problemas de inicialização do WSL quando a inicialização rápida estiver habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="eebc2-203">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="eebc2-204">Os soquetes UNIX precisam reter as credenciais de pares desconectados [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="eebc2-204">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="eebc2-205">Soquetes UNIX sem bloqueio com falha indefinidamente com EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="eebc2-205">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="eebc2-206">Case = off é o novo tipo de montagem de drvfs padrão [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="eebc2-206">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="eebc2-207">Consulte o [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="eebc2-207">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="eebc2-208">Adicione wslconfig/Terminate para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="eebc2-208">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="eebc2-209">Corrija o problema com as entradas do menu de contexto do Shell WSL que não manipulam corretamente caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="eebc2-209">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="eebc2-210">Expor a diferenciação de maiúsculas e minúsculas por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="eebc2-210">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="eebc2-211">ARM64 Emular operações de manutenção de cache.</span><span class="sxs-lookup"><span data-stu-id="eebc2-211">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="eebc2-212">Resolver o [problema dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="eebc2-212">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="eebc2-213">DrvFs: apenas caracteres de escape de saída no intervalo privado que correspondem a um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="eebc2-213">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="eebc2-214">Corrigir erro off-by-One na validação de comprimento do interpretador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="eebc2-214">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="eebc2-215">WSL timers absolutos com um tempo no passado não são disparados [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="eebc2-215">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="eebc2-216">Verifique se os pontos de nova análise criados recentemente estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="eebc2-216">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="eebc2-217">Crie de forma atômica diretórios que diferenciam maiúsculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-217">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="eebc2-218">Correção de um problema adicional em que operações multi-threaded podiam retornar ENOENT mesmo que o arquivo exista.</span><span class="sxs-lookup"><span data-stu-id="eebc2-218">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="eebc2-219">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="eebc2-219">[GH 2712]</span></span>
* <span data-ttu-id="eebc2-220">Correção da falha de inicialização do WSL quando o UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-220">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="eebc2-221">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="eebc2-221">[GH 3020]</span></span>
* <span data-ttu-id="eebc2-222">Adicione o menu de contexto do Explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="eebc2-222">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="eebc2-223">Para usar, mantenha Shift e clique com o botão direito do mouse quando estiver em uma janela do Explorer.</span><span class="sxs-lookup"><span data-stu-id="eebc2-223">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="eebc2-224">Corrigir comportamento de não bloqueio de soquete do UNIX [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="eebc2-224">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="eebc2-225">Corrija o comando do NetLink suspenso conforme relatado no GH 2026.</span><span class="sxs-lookup"><span data-stu-id="eebc2-225">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="eebc2-226">Adicionar suporte para os sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="eebc2-226">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="eebc2-227">Correção do problema com truncamento não causando eventos INotifyPropertyChanged [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="eebc2-227">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="eebc2-228">Adicione a opção--exec para WSL. exe para invocar um único binário sem um shell.</span><span class="sxs-lookup"><span data-stu-id="eebc2-228">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="eebc2-229">Adicionar--opção de distribuição para WSL. exe para selecionar um distribuição específico.</span><span class="sxs-lookup"><span data-stu-id="eebc2-229">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="eebc2-230">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="eebc2-230">Limited support for dmesg.</span></span> <span data-ttu-id="eebc2-231">Os aplicativos agora podem fazer logon no dmesg.</span><span class="sxs-lookup"><span data-stu-id="eebc2-231">Applications can now log to dmesg.</span></span> <span data-ttu-id="eebc2-232">O driver WSL registra informações limitadas no dmesg.</span><span class="sxs-lookup"><span data-stu-id="eebc2-232">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="eebc2-233">No futuro, isso pode ser estendido para transportar outras informações/diagnósticos do driver.</span><span class="sxs-lookup"><span data-stu-id="eebc2-233">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="eebc2-234">Observação: no momento, há suporte para `/dev/kmsg` dmesg por meio da interface do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-234">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="eebc2-235">`syslog`Ainda não há suporte para a interface syscall.</span><span class="sxs-lookup"><span data-stu-id="eebc2-235">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="eebc2-236">E, portanto, algumas das opções `dmesg` `-S`de linha de comando, como `-C` , não funcionam.</span><span class="sxs-lookup"><span data-stu-id="eebc2-236">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="eebc2-237">Alterar o GID e o modo padrão de dispositivos seriais para corresponder ao nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="eebc2-237">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="eebc2-238">O DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-238">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="eebc2-239">Observação: DrvFs tem algumas limitações sobre o nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-239">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="eebc2-240">Alguns caracteres (como '/', ': ' e '\*') não são permitidos e os nomes de atributos estendidos não diferenciam maiúsculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="eebc2-240">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="eebc2-241">Build 18252 (pular para a frente)</span><span class="sxs-lookup"><span data-stu-id="eebc2-241">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="eebc2-242">Para obter informações gerais do Windows sobre o Build 18252 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-242">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-243">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-243">WSL</span></span>
* <span data-ttu-id="eebc2-244">Mover os binários init e bsdtar para fora do lxssmanager dll e para uma pasta de ferramentas separada</span><span class="sxs-lookup"><span data-stu-id="eebc2-244">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="eebc2-245">Corrigir a corrida ao fechar o descritor de arquivo ao usar o CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="eebc2-245">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="eebc2-246">Manipular campos opcionais no/proc/pid/mountinfo ao traduzir caminhos de DrvFs</span><span class="sxs-lookup"><span data-stu-id="eebc2-246">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="eebc2-247">Permitir que DrvFs mknod tenha sucesso sem suporte de metadados para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="eebc2-247">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="eebc2-248">Os arquivos ReadOnly criados em DrvFs devem ter o atributo ReadOnly definido [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="eebc2-248">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="eebc2-249">Adicionar o auxiliar/sbin/mount.drvfs para lidar com a montagem de DrvFs</span><span class="sxs-lookup"><span data-stu-id="eebc2-249">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="eebc2-250">Use renomeação POSIX em DrvFs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-250">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="eebc2-251">Permitir tradução de caminho em volumes sem um GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="eebc2-251">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="eebc2-252">Build 17738 (rápido)</span><span class="sxs-lookup"><span data-stu-id="eebc2-252">Build 17738 (Fast)</span></span>
<span data-ttu-id="eebc2-253">Para obter informações gerais do Windows sobre o Build 17738 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-253">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-254">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-254">WSL</span></span>
* <span data-ttu-id="eebc2-255">Verificação de permissão syscall setanteriority muito estrita para alterar a mesma prioridade de thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="eebc2-255">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="eebc2-256">Verifique se o tempo de interrupção não polarizado é usado para o tempo de inicialização para evitar retornar valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="eebc2-256">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="eebc2-257">Tratar symlinks no intérprete WSL binfmt [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="eebc2-257">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="eebc2-258">Melhor manipulação da limpeza do descritor de arquivo de líder do grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="eebc2-258">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="eebc2-259">Build 17728 (rápido)</span><span class="sxs-lookup"><span data-stu-id="eebc2-259">Build 17728 (Fast)</span></span>
<span data-ttu-id="eebc2-260">Para obter informações gerais do Windows sobre o Build 17728 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-260">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-261">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-261">WSL</span></span>
* <span data-ttu-id="eebc2-262">Alterne WSL para usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter para evitar o estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="eebc2-262">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="eebc2-263">A anexação ptrace pode causar um valor de retorno insatisfatório de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="eebc2-263">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="eebc2-264">Corrigir vários problemas relacionados ao AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="eebc2-264">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="eebc2-265">Correção do problema que poderia causar falha de interoperabilidade WSL se o diretório de trabalho atual tiver menos de 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="eebc2-265">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="eebc2-266">Build 18204 (pular para a frente)</span><span class="sxs-lookup"><span data-stu-id="eebc2-266">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="eebc2-267">Para obter informações gerais do Windows sobre o Build 18204 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-267">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-268">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-268">WSL</span></span>
* <span data-ttu-id="eebc2-269">Inadvertenly do sistema de arquivos de pipe limpando o evento epoll disparado por borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="eebc2-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="eebc2-270">O executável do Win32 iniciado via NTFS symlink não respeita o symlink Name [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="eebc2-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="eebc2-271">Build 17723 (rápido)</span><span class="sxs-lookup"><span data-stu-id="eebc2-271">Build 17723 (Fast)</span></span>
<span data-ttu-id="eebc2-272">Para obter informações gerais do Windows sobre o Build 17723 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-272">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-273">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-273">WSL</span></span>
* <span data-ttu-id="eebc2-274">Evite um segundo atraso na falha de conexões de loopback para portas inexistentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="eebc2-274">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="eebc2-275">Adicionar arquivo stub/proc/sys/FS/File-Max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="eebc2-275">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="eebc2-276">Informações mais precisas sobre o escopo do IPV6.</span><span class="sxs-lookup"><span data-stu-id="eebc2-276">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="eebc2-277">Suporte do PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="eebc2-277">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="eebc2-278">Inadvertenly do sistema de arquivos de pipe limpando o evento epoll disparado por borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="eebc2-278">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="eebc2-279">O executável do Win32 iniciado via NTFS symlink não respeita o symlink Name [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="eebc2-279">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="eebc2-280">Build 17713</span><span class="sxs-lookup"><span data-stu-id="eebc2-280">Build 17713</span></span>
<span data-ttu-id="eebc2-281">Para obter informações gerais do Windows sobre o Build 17713 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-281">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-282">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-282">WSL</span></span>
* <span data-ttu-id="eebc2-283">Suporte ao zumbi melhorado [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="eebc2-283">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="eebc2-284">Adicionar entradas WSL. conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="eebc2-284">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="eebc2-285">Correção para getsockname nem sempre retornando tipo de família de soquetes UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="eebc2-285">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="eebc2-286">Adicionar suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="eebc2-286">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="eebc2-287">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="eebc2-287">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="eebc2-288">Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="eebc2-288">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="eebc2-289">Corrigir o problema de verificação de permissão na pasta raiz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="eebc2-289">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="eebc2-290">Suporte limitado para os IOCTLs de teclado TTY KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="eebc2-290">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="eebc2-291">Os aplicativos da interface do usuário do Windows devem ser executados mesmo quando iniciados em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="eebc2-291">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="eebc2-292">Build 17704</span><span class="sxs-lookup"><span data-stu-id="eebc2-292">Build 17704</span></span>
<span data-ttu-id="eebc2-293">Para obter informações gerais do Windows sobre o Build 17704 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-293">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-294">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-294">WSL</span></span>
* <span data-ttu-id="eebc2-295">Adicionar a opção WSL-u ou--User [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="eebc2-295">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="eebc2-296">Corrigir problemas de inicialização do WSL quando a inicialização rápida estiver habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="eebc2-296">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="eebc2-297">Os soquetes UNIX precisam reter as credenciais de pares desconectados [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="eebc2-297">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="eebc2-298">Soquetes UNIX sem bloqueio com falha indefinidamente com EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="eebc2-298">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="eebc2-299">Case = off é o novo tipo de montagem de drvfs padrão [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="eebc2-299">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="eebc2-300">Consulte o [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="eebc2-300">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="eebc2-301">Adicione wslconfig/Terminate para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="eebc2-301">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="eebc2-302">Build 17692</span><span class="sxs-lookup"><span data-stu-id="eebc2-302">Build 17692</span></span>
<span data-ttu-id="eebc2-303">Para obter informações gerais do Windows sobre o Build 17692 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="eebc2-303">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-304">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-304">WSL</span></span>
* <span data-ttu-id="eebc2-305">Corrija o problema com as entradas do menu de contexto do Shell WSL que não manipulam corretamente caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="eebc2-305">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="eebc2-306">Expor a diferenciação de maiúsculas e minúsculas por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="eebc2-306">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="eebc2-307">ARM64 Emular operações de manutenção de cache.</span><span class="sxs-lookup"><span data-stu-id="eebc2-307">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="eebc2-308">Resolver o [problema dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="eebc2-308">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="eebc2-309">DrvFs: apenas caracteres de escape de saída no intervalo privado que correspondem a um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="eebc2-309">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="eebc2-310">Build 17686</span><span class="sxs-lookup"><span data-stu-id="eebc2-310">Build 17686</span></span>
<span data-ttu-id="eebc2-311">Para obter informações gerais do Windows sobre o Build 17686 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="eebc2-311">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-312">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-312">WSL</span></span>
* <span data-ttu-id="eebc2-313">Corrigir erro off-by-One na validação de comprimento do interpretador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="eebc2-313">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="eebc2-314">WSL timers absolutos com um tempo no passado não são disparados [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="eebc2-314">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="eebc2-315">Verifique se os pontos de nova análise criados recentemente estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="eebc2-315">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="eebc2-316">Crie de forma atômica diretórios que diferenciam maiúsculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-316">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="eebc2-317">Build 17677</span><span class="sxs-lookup"><span data-stu-id="eebc2-317">Build 17677</span></span>
<span data-ttu-id="eebc2-318">Para obter informações gerais do Windows sobre o Build 17677 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-318">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-319">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-319">WSL</span></span>
* <span data-ttu-id="eebc2-320">Correção de um problema adicional em que operações multi-threaded podiam retornar ENOENT mesmo que o arquivo exista.</span><span class="sxs-lookup"><span data-stu-id="eebc2-320">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="eebc2-321">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="eebc2-321">[GH 2712]</span></span>
* <span data-ttu-id="eebc2-322">Correção da falha de inicialização do WSL quando o UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-322">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="eebc2-323">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="eebc2-323">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="eebc2-324">Build 17666</span><span class="sxs-lookup"><span data-stu-id="eebc2-324">Build 17666</span></span>
<span data-ttu-id="eebc2-325">Para obter informações gerais do Windows sobre o Build 17666 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-325">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-326">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-326">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="eebc2-327">AVISO: Há um problema que impede a execução do WSL em alguns chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="eebc2-327">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="eebc2-328">Uma correção está pronta e preparando-se para o Branch do insider Build.</span><span class="sxs-lookup"><span data-stu-id="eebc2-328">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="eebc2-329">Adicione o menu de contexto do Explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="eebc2-329">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="eebc2-330">Para usar manter pressionada e clicar com o botão direito do mouse quando estiver em uma janela do Explorer.</span><span class="sxs-lookup"><span data-stu-id="eebc2-330">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="eebc2-331">Corrigir comportamento de não bloqueio de soquete do UNIX [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="eebc2-331">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="eebc2-332">Corrija o comando do NetLink suspenso conforme relatado no GH 2026.</span><span class="sxs-lookup"><span data-stu-id="eebc2-332">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="eebc2-333">Adicionar suporte para os sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="eebc2-333">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="eebc2-334">Correção do problema com truncamento não causando eventos INotifyPropertyChanged [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="eebc2-334">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="eebc2-335">Adicione a opção--exec para WSL. exe para invocar um único binário sem um shell.</span><span class="sxs-lookup"><span data-stu-id="eebc2-335">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="eebc2-336">Adicionar--opção de distribuição para WSL. exe para selecionar um distribuição específico.</span><span class="sxs-lookup"><span data-stu-id="eebc2-336">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="eebc2-337">Build 17655 (pular para a frente)</span><span class="sxs-lookup"><span data-stu-id="eebc2-337">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="eebc2-338">Para obter informações gerais do Windows sobre o Build 17655 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-338">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-339">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-339">WSL</span></span>
* <span data-ttu-id="eebc2-340">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="eebc2-340">Limited support for dmesg.</span></span> <span data-ttu-id="eebc2-341">Os aplicativos agora podem fazer logon no dmesg.</span><span class="sxs-lookup"><span data-stu-id="eebc2-341">Applications can now log to dmesg.</span></span> <span data-ttu-id="eebc2-342">O driver WSL registra informações limitadas no dmesg.</span><span class="sxs-lookup"><span data-stu-id="eebc2-342">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="eebc2-343">No futuro, isso pode ser estendido para transportar outras informações/diagnósticos do driver.</span><span class="sxs-lookup"><span data-stu-id="eebc2-343">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="eebc2-344">Observação: no momento, há suporte para `/dev/kmsg` dmesg por meio da interface do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-344">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="eebc2-345">`syslog`Ainda não há suporte para a interface sycall.</span><span class="sxs-lookup"><span data-stu-id="eebc2-345">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="eebc2-346">E, portanto, algumas das opções `dmesg` `-S`de linha de comando, como `-C` , não funcionam.</span><span class="sxs-lookup"><span data-stu-id="eebc2-346">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="eebc2-347">Correção de um problema em que as operações multi-threaded podiam retornar ENOENT, mesmo que o arquivo exista.</span><span class="sxs-lookup"><span data-stu-id="eebc2-347">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="eebc2-348">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="eebc2-348">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="eebc2-349">Build 17639 (pular para a frente)</span><span class="sxs-lookup"><span data-stu-id="eebc2-349">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="eebc2-350">Para obter informações gerais do Windows sobre o Build 17639 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-350">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-351">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-351">WSL</span></span>
* <span data-ttu-id="eebc2-352">Alterar o GID e o modo padrão de dispositivos seriais para corresponder ao nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="eebc2-352">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="eebc2-353">O DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-353">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="eebc2-354">Observação: DrvFs tem algumas limitações sobre o nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-354">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="eebc2-355">Em particular, alguns caracteres (como '/', ': ' e '\*') não são permitidos, e os nomes de atributos estendidos não diferenciam maiúsculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="eebc2-355">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="eebc2-356">Build 17133 (rápido)</span><span class="sxs-lookup"><span data-stu-id="eebc2-356">Build 17133 (Fast)</span></span>
<span data-ttu-id="eebc2-357">Para obter informações gerais do Windows sobre o Build 17133 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-357">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-358">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-358">WSL</span></span>
* <span data-ttu-id="eebc2-359">Correção para o travamento no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-359">Fix for hang in WSL.</span></span> <span data-ttu-id="eebc2-360">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="eebc2-360">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="eebc2-361">Build 17128 (rápido)</span><span class="sxs-lookup"><span data-stu-id="eebc2-361">Build 17128 (Fast)</span></span>
<span data-ttu-id="eebc2-362">Para obter informações gerais do Windows sobre o Build 17128 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-362">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-363">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-363">WSL</span></span>
* <span data-ttu-id="eebc2-364">Nenhum</span><span class="sxs-lookup"><span data-stu-id="eebc2-364">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="eebc2-365">Build 17627 (pular para a frente)</span><span class="sxs-lookup"><span data-stu-id="eebc2-365">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="eebc2-366">Para obter informações gerais do Windows sobre o Build 17627 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-366">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-367">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-367">WSL</span></span>
* <span data-ttu-id="eebc2-368">Adicione suporte para as operações que reconhecem o Futex PI.</span><span class="sxs-lookup"><span data-stu-id="eebc2-368">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="eebc2-369">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="eebc2-369">[GH 1006]</span></span>
    * <span data-ttu-id="eebc2-370">Observe que as prioridades não são atualmente um recurso WSL com suporte para que haja limitações, mas o uso padrão deve ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-370">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="eebc2-371">Suporte do firewall do Windows para processos WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-371">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="eebc2-372">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="eebc2-372">[GH 1852]</span></span>
    * <span data-ttu-id="eebc2-373">Por exemplo, para permitir que o processo Python WSL escute em qualquer porta, use o cmd do Windows com privilégios elevados:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="eebc2-373">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="eebc2-374">Para obter detalhes adicionais sobre como adicionar regras de firewall, consulte [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="eebc2-374">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="eebc2-375">Respeitar o shell padrão do usuário ao usar WSL. exe.</span><span class="sxs-lookup"><span data-stu-id="eebc2-375">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="eebc2-376">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="eebc2-376">[GH 2372]</span></span>
* <span data-ttu-id="eebc2-377">Relatar todas as interfaces de rede como Ethernet.</span><span class="sxs-lookup"><span data-stu-id="eebc2-377">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="eebc2-378">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="eebc2-378">[GH 2996]</span></span>
* <span data-ttu-id="eebc2-379">Melhor manipulação do arquivo/etc/passwd corrompido.</span><span class="sxs-lookup"><span data-stu-id="eebc2-379">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="eebc2-380">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="eebc2-380">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-381">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-381">Console</span></span>
* <span data-ttu-id="eebc2-382">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-382">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-383">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-383">LTP Results:</span></span>
<span data-ttu-id="eebc2-384">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-384">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="eebc2-385">Build 17618 (pular para a frente)</span><span class="sxs-lookup"><span data-stu-id="eebc2-385">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="eebc2-386">Para obter informações gerais do Windows sobre o Build 17618 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-386">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-387">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-387">WSL</span></span>
* <span data-ttu-id="eebc2-388">Introduza a funcionalidade pseudoconsole para NT Interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="eebc2-388">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="eebc2-389">O mecanismo de instalação herdado (lxrun. exe) foi preterido.</span><span class="sxs-lookup"><span data-stu-id="eebc2-389">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="eebc2-390">O mecanismo com suporte para a instalação de distribuições é por meio do Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="eebc2-390">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-391">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-391">Console</span></span>
* <span data-ttu-id="eebc2-392">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-392">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-393">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-393">LTP Results:</span></span>
<span data-ttu-id="eebc2-394">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-394">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="eebc2-395">Build 17110</span><span class="sxs-lookup"><span data-stu-id="eebc2-395">Build 17110</span></span>
<span data-ttu-id="eebc2-396">Para obter informações gerais do Windows sobre o Build 17110 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-396">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-397">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-397">WSL</span></span>
* <span data-ttu-id="eebc2-398">Permitir que/init seja encerrado do Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="eebc2-398">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="eebc2-399">O DrvFs agora usa a diferenciação de maiúsculas e minúsculas por diretório por padrão (equivalente à opção de montagem "Case = dir").</span><span class="sxs-lookup"><span data-stu-id="eebc2-399">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="eebc2-400">Usar "Case = Force" (o comportamento antigo) requer a definição de uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="eebc2-400">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="eebc2-401">Execute o seguinte comando para habilitar "Case = Force" se você precisar usá-lo: reg Add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="eebc2-401">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="eebc2-402">Se você tiver diretórios existentes criados com WSL na versão anterior do Windows que precisam diferenciar maiúsculas de minúsculas, use fsutil. exe para marcá-los como diferenciação de maiúsculas e minúsculas: fsutil. exe file setcasesensitiveinfo <path> Enable</span><span class="sxs-lookup"><span data-stu-id="eebc2-402">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="eebc2-403">Cadeias de caracteres de término nulas retornadas da syscall uname.</span><span class="sxs-lookup"><span data-stu-id="eebc2-403">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-404">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-404">Console</span></span>
* <span data-ttu-id="eebc2-405">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-405">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-406">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-406">LTP Results:</span></span>
<span data-ttu-id="eebc2-407">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-407">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="eebc2-408">Build 17107</span><span class="sxs-lookup"><span data-stu-id="eebc2-408">Build 17107</span></span>
<span data-ttu-id="eebc2-409">Para obter informações gerais do Windows sobre o Build 17107 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-409">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-410">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-410">WSL</span></span>
* <span data-ttu-id="eebc2-411">Suporte a TCSETSF e TCSETSW nos pontos de extremidade mestre PTY [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="eebc2-411">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="eebc2-412">Iniciar processos de interoperabilidade simultâneas pode resultar em EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="eebc2-412">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="eebc2-413">Corrija PTRACE_ATTACH para mostrar o status de rastreamento adequado em/proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="eebc2-413">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="eebc2-414">Corrija a corrida em que os processos de curta duração clonados com os sinalizadores CLEARTID e dsvid podem sair sem limpar o endereço de TID.</span><span class="sxs-lookup"><span data-stu-id="eebc2-414">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="eebc2-415">Exiba uma mensagem ao atualizar os diretórios do sistema de arquivos do Linux ao mudar de uma compilação anterior à 17093.</span><span class="sxs-lookup"><span data-stu-id="eebc2-415">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="eebc2-416">Para obter mais detalhes sobre as alterações do sistema de arquivos 17093, consulte as notas de versão para [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="eebc2-416">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-417">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-417">Console</span></span>
* <span data-ttu-id="eebc2-418">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-418">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-419">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-419">LTP Results:</span></span>
<span data-ttu-id="eebc2-420">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-420">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="eebc2-421">Build 17101</span><span class="sxs-lookup"><span data-stu-id="eebc2-421">Build 17101</span></span>
<span data-ttu-id="eebc2-422">Para obter informações gerais do Windows sobre o Build 17101 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-422">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-423">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-423">WSL</span></span>
* <span data-ttu-id="eebc2-424">Suporte para signalfd.</span><span class="sxs-lookup"><span data-stu-id="eebc2-424">Support for signalfd.</span></span> <span data-ttu-id="eebc2-425">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="eebc2-425">[GH 129]</span></span>
* <span data-ttu-id="eebc2-426">Suporte a nomes de arquivos que contêm caracteres NTFS ilegais codificando-os como caracteres Unicode privados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-426">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="eebc2-427">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="eebc2-427">[GH 1514]</span></span>
* <span data-ttu-id="eebc2-428">A montagem automática fará fallback para somente leitura quando não houver suporte para gravação.</span><span class="sxs-lookup"><span data-stu-id="eebc2-428">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="eebc2-429">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="eebc2-429">[GH 2603]</span></span>
* <span data-ttu-id="eebc2-430">Permitir colagem de pares substitutos Unicode (como caracteres de Emoji).</span><span class="sxs-lookup"><span data-stu-id="eebc2-430">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="eebc2-431">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="eebc2-431">[GH 2765]</span></span>
* <span data-ttu-id="eebc2-432">Pseudo-arquivos em/proc e/sys devem retornar leitura e gravação prontos de Select, votação, epoll, et al. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="eebc2-432">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="eebc2-433">Correção do problema que pode fazer com que o serviço entre em loop infinito quando o registro foi adulterado ou está corrompido.</span><span class="sxs-lookup"><span data-stu-id="eebc2-433">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="eebc2-434">Corrija as mensagens do NetLink para trabalhar com a versão mais recente (upstream 4,14) do iproute2.</span><span class="sxs-lookup"><span data-stu-id="eebc2-434">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-435">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-435">Console</span></span>
* <span data-ttu-id="eebc2-436">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-436">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-437">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-437">LTP Results:</span></span>
<span data-ttu-id="eebc2-438">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-438">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="eebc2-439">Build 17093</span><span class="sxs-lookup"><span data-stu-id="eebc2-439">Build 17093</span></span>
<span data-ttu-id="eebc2-440">Para obter informações gerais do Windows sobre o Build 17093 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-440">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="eebc2-441">Importante:</span><span class="sxs-lookup"><span data-stu-id="eebc2-441">Important:</span></span>
<span data-ttu-id="eebc2-442">Ao iniciar o WSL pela primeira vez após a atualização para essa compilação, ele precisa executar algum trabalho atualizando os diretórios do sistema de arquivos do Linux.</span><span class="sxs-lookup"><span data-stu-id="eebc2-442">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="eebc2-443">Isso pode levar até vários minutos, então WSL pode parecer ser iniciado lentamente.</span><span class="sxs-lookup"><span data-stu-id="eebc2-443">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="eebc2-444">Isso só deve ocorrer uma vez para cada distribuição instalada por meio da loja.</span><span class="sxs-lookup"><span data-stu-id="eebc2-444">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="eebc2-445">Suporte de distinção de maiúsculas e minúsculas aprimorado no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-445">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="eebc2-446">O DrvFs agora dá suporte à distinção de maiúsculas e minúsculas por diretório.</span><span class="sxs-lookup"><span data-stu-id="eebc2-446">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="eebc2-447">Esse é um novo sinalizador que pode ser definido em diretórios para indicar que todas as operações nesses diretórios devem ser tratadas como diferenciando maiúsculas de minúsculas, o que permite até que os aplicativos do Windows Abram corretamente arquivos que diferem apenas por maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-447">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="eebc2-448">DrvFs tem novas opções de montagem que controlam a diferenciação de maiúsculas e minúsculas em uma base por diretório</span><span class="sxs-lookup"><span data-stu-id="eebc2-448">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="eebc2-449">Case = Force: todos os diretórios são tratados como diferenciando maiúsculas de minúsculas (exceto para a raiz da unidade).</span><span class="sxs-lookup"><span data-stu-id="eebc2-449">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="eebc2-450">Os novos diretórios criados com WSL são marcados como diferenciando maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-450">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="eebc2-451">Esse é o comportamento herdado, exceto para marcar novos diretórios como diferenciar maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-451">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="eebc2-452">Case = dir: somente os diretórios com o sinalizador de sensibilidade de caso por diretório são tratados como diferenciando maiúsculas de minúsculas; outros diretórios não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-452">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="eebc2-453">Os novos diretórios criados com WSL são marcados como diferenciando maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-453">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="eebc2-454">Case = off: somente os diretórios com o sinalizador de sensibilidade de caso por diretório são tratados como diferenciando maiúsculas de minúsculas; outros diretórios não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-454">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="eebc2-455">Os novos diretórios criados com WSL são marcados como não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-455">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="eebc2-456">Observação: os diretórios criados por WSL em versões anteriores não têm esse sinalizador definido, portanto, não serão tratados como diferenciação de maiúsculas e minúsculas se você usar a opção "Case = dir".</span><span class="sxs-lookup"><span data-stu-id="eebc2-456">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="eebc2-457">Uma maneira de definir esse sinalizador em diretórios existentes estará disponível em breve.</span><span class="sxs-lookup"><span data-stu-id="eebc2-457">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="eebc2-458">Exemplo de montagem com essas opções (para unidades existentes, você deve primeiro desmontar antes de poder montar com opções diferentes): sudo mount-t drvfs C:/mnt/c-o case = dir</span><span class="sxs-lookup"><span data-stu-id="eebc2-458">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="eebc2-459">Por enquanto, Case = Force ainda é a opção padrão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-459">For now, case=force is still the default option.</span></span> <span data-ttu-id="eebc2-460">Isso será alterado para Case = dir no futuro.</span><span class="sxs-lookup"><span data-stu-id="eebc2-460">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="eebc2-461">Agora você pode usar barras invertidas em caminhos do Windows ao montar DrvFs, por exemplo: sudo mount-t DrvFs//Server/share/mnt/share</span><span class="sxs-lookup"><span data-stu-id="eebc2-461">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="eebc2-462">WSL agora processa o arquivo/etc/fstab durante o início da instância [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="eebc2-462">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="eebc2-463">Isso é feito antes da montagem automática de unidades de DrvFs; todas as unidades que já foram montadas pelo fstab não serão remontadas automaticamente, permitindo que você altere o ponto de montagem de unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-463">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="eebc2-464">Esse comportamento pode ser desativado usando WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="eebc2-464">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="eebc2-465">Os arquivos Mount, mountinfo e mountstats no/proc escapar corretamente caracteres especiais, como barras invertidas e espaços [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="eebc2-465">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="eebc2-466">Arquivos especiais criados com DrvFs, como links simbólicos do WSL, ou FIFOs e soquetes quando os metadados estão habilitados, agora podem ser copiados e movidos do Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-466">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="eebc2-467">WSL é mais configurável com WSL. conf</span><span class="sxs-lookup"><span data-stu-id="eebc2-467">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="eebc2-468">Adicionamos um método para configurar automaticamente determinadas funcionalidades no WSL que serão aplicadas toda vez que você iniciar o subsistema.</span><span class="sxs-lookup"><span data-stu-id="eebc2-468">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="eebc2-469">Isso inclui opções de montagem automática e configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="eebc2-469">This includes automount options and network configuration.</span></span> <span data-ttu-id="eebc2-470">Saiba mais sobre isso em nossa postagem no blog em: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="eebc2-470">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="eebc2-471">AF_UNIX permite conexões de soquete entre processos do Linux em processos nativos do WSL e do Windows</span><span class="sxs-lookup"><span data-stu-id="eebc2-471">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="eebc2-472">Os aplicativos WSL e Windows agora podem se comunicar entre si por meio de soquetes UNIX.</span><span class="sxs-lookup"><span data-stu-id="eebc2-472">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="eebc2-473">Imagine que você deseja executar um serviço no Windows e disponibilizá-lo para aplicativos do Windows e do WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-473">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="eebc2-474">Agora, isso é possível com os soquetes do UNIX.</span><span class="sxs-lookup"><span data-stu-id="eebc2-474">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="eebc2-475">Leia mais em nossa postagem no blog em https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="eebc2-475">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-476">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-476">WSL</span></span>
* <span data-ttu-id="eebc2-477">Suporte a mmap () com MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="eebc2-477">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="eebc2-478">Suporte a CLONE_PTRACE e CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="eebc2-478">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="eebc2-479">Manipular o sinal de encerramento não SIGCHLD no clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="eebc2-479">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="eebc2-480">Stub/proc/sys/FS/inotify/max_user_instances e/proc/sys/FS/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="eebc2-480">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="eebc2-481">Erro ao carregar binários ELF que contêm cabeçalhos de carga com deslocamentos diferentes de zero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="eebc2-481">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="eebc2-482">Zero os bytes de página à direita ao carregar imagens.</span><span class="sxs-lookup"><span data-stu-id="eebc2-482">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="eebc2-483">Reduzir os casos em que o execve encerra o processo silenciosamente</span><span class="sxs-lookup"><span data-stu-id="eebc2-483">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-484">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-484">Console</span></span>
* <span data-ttu-id="eebc2-485">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-486">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-486">LTP Results:</span></span>
<span data-ttu-id="eebc2-487">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-487">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="eebc2-488">Build 17083</span><span class="sxs-lookup"><span data-stu-id="eebc2-488">Build 17083</span></span>
<span data-ttu-id="eebc2-489">Para obter informações gerais do Windows sobre o Build 17083 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-489">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-490">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-490">WSL</span></span>
* <span data-ttu-id="eebc2-491">Correção de verificação relacionada a epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="eebc2-491">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="eebc2-492">Correção de travamentos ao desativar ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="eebc2-492">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="eebc2-493">Garantir que as operações mmap apareçam atômicas [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="eebc2-493">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-494">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-494">Console</span></span>
* <span data-ttu-id="eebc2-495">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-496">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-496">LTP Results:</span></span>
<span data-ttu-id="eebc2-497">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-497">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="eebc2-498">Build 17074</span><span class="sxs-lookup"><span data-stu-id="eebc2-498">Build 17074</span></span>
<span data-ttu-id="eebc2-499">Para obter informações gerais do Windows sobre o Build 17074 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-499">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-500">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-500">WSL</span></span>
* <span data-ttu-id="eebc2-501">Formato de armazenamento fixo de metadados DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="eebc2-501">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="eebc2-502">**Importante:** Os metadados DrvFs criados antes dessa compilação serão exibidos incorretamente ou não.</span><span class="sxs-lookup"><span data-stu-id="eebc2-502">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="eebc2-503">Para corrigir os arquivos afetados, use chmod e aldelet para aplicar novamente os metadados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-503">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="eebc2-504">Corrigido o problema com vários sinais e syscalls reiniciável.</span><span class="sxs-lookup"><span data-stu-id="eebc2-504">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-505">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-505">Console</span></span>
* <span data-ttu-id="eebc2-506">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-506">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-507">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-507">LTP Results:</span></span>
<span data-ttu-id="eebc2-508">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-508">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="eebc2-509">Build 17063</span><span class="sxs-lookup"><span data-stu-id="eebc2-509">Build 17063</span></span>
<span data-ttu-id="eebc2-510">Para obter informações gerais do Windows sobre o Build 17063 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-510">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="eebc2-511">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-511">WSL</span></span>
* <span data-ttu-id="eebc2-512">O DrvFs dá suporte a metadados adicionais do Linux.</span><span class="sxs-lookup"><span data-stu-id="eebc2-512">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="eebc2-513">Isso permite definir o proprietário e o modo de arquivos usando chmod/alownerion e também a criação de arquivos especiais, como FIFOs, soquetes UNIX e arquivos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-513">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="eebc2-514">Isso é desabilitado por padrão por enquanto, pois ainda é experimental.</span><span class="sxs-lookup"><span data-stu-id="eebc2-514">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="eebc2-515">**Observação:**  Corrigimos um bug no formato de metadados usado pelo DrvFs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-515">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="eebc2-516">Embora os metadados funcionem nesse Build para experimentação, as compilações futuras não lêem corretamente os metadados criados por essa compilação.</span><span class="sxs-lookup"><span data-stu-id="eebc2-516">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="eebc2-517">Talvez seja necessário atualizar manualmente o proprietário para arquivos modificados e os dispositivos com uma ID de dispositivo personalizada precisarão ser recriados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-517">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="eebc2-518">Para habilitar, monte DrvFs com a opção de metadados (para habilitá-lo em uma montagem existente, você deve primeiro desmontá-lo):</span><span class="sxs-lookup"><span data-stu-id="eebc2-518">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="eebc2-519">As permissões do Linux são adicionadas como metadados adicionais ao arquivo; Eles não afetam as permissões do Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-519">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="eebc2-520">Lembre-se de que a edição de um arquivo usando um editor do Windows pode remover os metadados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-520">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="eebc2-521">Nesse caso, o arquivo será revertido para suas permissões padrão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-521">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="eebc2-522">Adição de opções de montagem a DrvFs para controlar arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-522">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="eebc2-523">UID: a ID de usuário usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-523">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="eebc2-524">GID: a ID do grupo usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-524">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="eebc2-525">umask: uma máscara octal de permissões a serem excluídas para todos os arquivos e diretórios.</span><span class="sxs-lookup"><span data-stu-id="eebc2-525">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="eebc2-526">fMask: uma máscara octal de permissões a serem excluídas para todos os arquivos regulares.</span><span class="sxs-lookup"><span data-stu-id="eebc2-526">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="eebc2-527">dmask: uma máscara octal de permissões a serem excluídas para todos os diretórios.</span><span class="sxs-lookup"><span data-stu-id="eebc2-527">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="eebc2-528">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="eebc2-528">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="eebc2-529">Combine com a opção de metadados para especificar permissões padrão para arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-529">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="eebc2-530">Introduziu uma nova variável de `WSLENV`ambiente,, para configurar como as variáveis de ambiente fluem entre WSL e Win32.</span><span class="sxs-lookup"><span data-stu-id="eebc2-530">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="eebc2-531">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="eebc2-531">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="eebc2-532">`WSLENV`é uma lista delimitada por dois-pontos de variáveis de ambiente que pode ser incluída ao iniciar processos de WSL de processos Win32 ou Win32 de WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-532">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="eebc2-533">Cada variável pode ser sufixada com uma barra seguida por sinalizadores para especificar como ela é traduzida.</span><span class="sxs-lookup"><span data-stu-id="eebc2-533">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="eebc2-534">DTI O valor é um caminho que deve ser convertido entre caminhos WSL e caminhos Win32.</span><span class="sxs-lookup"><span data-stu-id="eebc2-534">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="eebc2-535">debug O valor é uma lista de caminhos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-535">l: The value is a list of paths.</span></span> <span data-ttu-id="eebc2-536">No WSL, é uma lista delimitada por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-536">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="eebc2-537">No Win32, é uma lista delimitada por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="eebc2-537">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="eebc2-538">t O valor só deve ser incluído ao invocar WSL do Win32</span><span class="sxs-lookup"><span data-stu-id="eebc2-538">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="eebc2-539">Mostrar O valor só deve ser incluído ao invocar o Win32 de WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-539">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="eebc2-540">Você pode definir `WSLENV` em. bashrc ou no ambiente personalizado do Windows para seu usuário.</span><span class="sxs-lookup"><span data-stu-id="eebc2-540">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="eebc2-541">montagens de drvfs preserva corretamente os carimbos de data/hora do tar, CP-p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="eebc2-541">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="eebc2-542">drvfs symlinks relate o tamanho correto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="eebc2-542">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="eebc2-543">leitura/gravação funciona para tamanhos de e/s muito grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="eebc2-543">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="eebc2-544">waitpid trabalha com IDs de grupo de processos (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="eebc2-544">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="eebc2-545">desempenho de mmap significativamente melhorado para grandes regiões de reserva; melhora o desempenho do GHC (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="eebc2-545">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="eebc2-546">suporte a personalidades para READ_IMPLIES_EXEC; corrige máximo e CLISP (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="eebc2-546">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="eebc2-547">MProtect dá suporte a PROT_GROWSDOWN; Corrige CLISP (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="eebc2-547">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="eebc2-548">correções de falhas de página no modo de excesso de confirmação; corrige SBCL (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="eebc2-548">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="eebc2-549">o clone dá suporte a mais combinações de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="eebc2-549">clone supports more flags combinations</span></span>
* <span data-ttu-id="eebc2-550">Suporte Select/epoll de arquivos epoll (anteriormente um não op).</span><span class="sxs-lookup"><span data-stu-id="eebc2-550">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="eebc2-551">Notificar ptrace de syscalls não implementados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-551">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="eebc2-552">Ignorar interfaces que não estão em funcionamento ao gerar nomes de resolução. conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="eebc2-552">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="eebc2-553">Enumere as interfaces de rede sem endereço físico.</span><span class="sxs-lookup"><span data-stu-id="eebc2-553">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="eebc2-554">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="eebc2-554">[GH 2685]</span></span>
* <span data-ttu-id="eebc2-555">Correções e aprimoramentos de bugs adicionais.</span><span class="sxs-lookup"><span data-stu-id="eebc2-555">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="eebc2-556">Ferramentas do Linux disponíveis para desenvolvedores no Windows</span><span class="sxs-lookup"><span data-stu-id="eebc2-556">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="eebc2-557">A linha de comando do Windows ferramentas inclui bsdtar (tar) e ondulação.</span><span class="sxs-lookup"><span data-stu-id="eebc2-557">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="eebc2-558">Leia [este blog](https://aka.ms/tarcurlwindows) para saber mais sobre a adição dessas duas novas ferramentas e veja como elas estão moldando a experiência do desenvolvedor no Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-558">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="eebc2-559">`AF_UNIX`está disponível no SDK do Windows Insider (17061 +).</span><span class="sxs-lookup"><span data-stu-id="eebc2-559">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="eebc2-560">Leia [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para saber mais sobre `AF_UNIX` como os desenvolvedores do Windows podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-560">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="eebc2-561">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-561">Console</span></span>
* <span data-ttu-id="eebc2-562">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-562">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-563">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-563">LTP Results:</span></span>
<span data-ttu-id="eebc2-564">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-564">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="eebc2-565">Build 17046</span><span class="sxs-lookup"><span data-stu-id="eebc2-565">Build 17046</span></span>

<span data-ttu-id="eebc2-566">Para obter informações gerais do Windows sobre o Build 17046 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="eebc2-566">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="eebc2-567">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-567">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-568">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-568">WSL</span></span>
- <span data-ttu-id="eebc2-569">Permitir que processos sejam executados sem um terminal ativo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-569">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="eebc2-570">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="eebc2-570">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="eebc2-571">Melhor suporte a CLONE_VFORK e CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="eebc2-571">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="eebc2-572">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="eebc2-572">[GH 1878, 2615]</span></span>
- <span data-ttu-id="eebc2-573">Ignorar drivers de filtro de TDI para operações de rede WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-573">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="eebc2-574">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="eebc2-574">[GH 1554]</span></span>
- <span data-ttu-id="eebc2-575">DrvFs cria NT symlinks quando determinadas condições são atendidas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-575">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="eebc2-576">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="eebc2-576">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="eebc2-577">O destino do link deve ser relativo, não deve cruzar nenhum ponto de montagem ou symlinks e deve existir.</span><span class="sxs-lookup"><span data-stu-id="eebc2-577">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="eebc2-578">O usuário deve ter SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (isso normalmente requer que você inicie o WSL. exe com privilégios elevados), a menos que o modo de desenvolvedor esteja ativado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-578">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="eebc2-579">Em todas as outras situações, o DrvFs ainda cria WSL symlinks.</span><span class="sxs-lookup"><span data-stu-id="eebc2-579">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="eebc2-580">Permitir a execução de instâncias de WSL elevadas e não elevadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="eebc2-580">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="eebc2-581">Suporte a/proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="eebc2-581">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="eebc2-582">Adicione wslpath ao WSL <-> conversões de caminho do Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-582">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="eebc2-583">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="eebc2-583">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="eebc2-584">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-584">Console</span></span>
- <span data-ttu-id="eebc2-585">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="eebc2-585">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-586">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-586">LTP Results:</span></span>
<span data-ttu-id="eebc2-587">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-587">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="eebc2-588">Build 17040</span><span class="sxs-lookup"><span data-stu-id="eebc2-588">Build 17040</span></span>

<span data-ttu-id="eebc2-589">Para obter informações gerais do Windows sobre o Build 17040 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="eebc2-589">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-590">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-591">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-591">WSL</span></span>
- <span data-ttu-id="eebc2-592">Nenhuma correção desde 17035.</span><span class="sxs-lookup"><span data-stu-id="eebc2-592">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-593">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-593">Console</span></span>
- <span data-ttu-id="eebc2-594">Nenhuma correção desde 17035.</span><span class="sxs-lookup"><span data-stu-id="eebc2-594">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-595">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-595">LTP Results:</span></span>
<span data-ttu-id="eebc2-596">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-596">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="eebc2-597">Build 17035</span><span class="sxs-lookup"><span data-stu-id="eebc2-597">Build 17035</span></span>

<span data-ttu-id="eebc2-598">Para obter informações gerais do Windows sobre o Build 17035 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="eebc2-598">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-599">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-599">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-600">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-600">WSL</span></span>
- <span data-ttu-id="eebc2-601">O acesso a arquivos em DrvFs pode ocasionalmente falhar com EINVAL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-601">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="eebc2-602">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="eebc2-602">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-603">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-603">Console</span></span>
- <span data-ttu-id="eebc2-604">Alguma perda de cor ao inserir/excluir linhas no modo VT.</span><span class="sxs-lookup"><span data-stu-id="eebc2-604">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-605">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-605">LTP Results:</span></span>
<span data-ttu-id="eebc2-606">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-606">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="eebc2-607">Build 17025</span><span class="sxs-lookup"><span data-stu-id="eebc2-607">Build 17025</span></span>

<span data-ttu-id="eebc2-608">Para obter informações gerais do Windows sobre o Build 17025 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="eebc2-608">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-609">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-609">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-610">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-610">WSL</span></span>
- <span data-ttu-id="eebc2-611">Inicie os processos iniciais em um novo grupo de processo de primeiro plano [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="eebc2-611">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="eebc2-612">Correções de entrega SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="eebc2-612">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="eebc2-613">Gere o nome de ponte virtual padrão se nenhum for fornecido [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="eebc2-613">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="eebc2-614">Implemente/proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="eebc2-614">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="eebc2-615">Mais correções de pipe stdout/stderr de interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="eebc2-615">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="eebc2-616">Chamada do sistema syncfs de stub.</span><span class="sxs-lookup"><span data-stu-id="eebc2-616">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-617">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-617">Console</span></span>
- <span data-ttu-id="eebc2-618">Corrigir a conversão de VT de entrada para consoles de terceiros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="eebc2-618">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-619">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-619">LTP Results:</span></span>
<span data-ttu-id="eebc2-620">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-620">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="eebc2-621">Build 17017</span><span class="sxs-lookup"><span data-stu-id="eebc2-621">Build 17017</span></span>

<span data-ttu-id="eebc2-622">Para obter informações gerais do Windows sobre o Build 17017 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="eebc2-622">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-623">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-623">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-624">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-624">WSL</span></span>
- <span data-ttu-id="eebc2-625">Ignorar cabeçalhos de programa ELF vazios [GH 330].</span><span class="sxs-lookup"><span data-stu-id="eebc2-625">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="eebc2-626">Permitir que o LxssManager Crie instâncias WSL para usuários não interativos (SSH e suporte a tarefas agendadas) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="eebc2-626">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="eebc2-627">Suporte ao WSL-> Win32-> os cenários de WSL ("criação") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="eebc2-627">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="eebc2-628">Suporte limitado para encerramento de aplicativos de console invocados via Interop [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="eebc2-628">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="eebc2-629">Suporte a opções de montagem para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="eebc2-629">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="eebc2-630">Ptrace bloqueando a inicialização do filho [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="eebc2-630">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="eebc2-631">EPOLLET faltam alguns eventos [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="eebc2-631">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="eebc2-632">Retornar mais dados para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="eebc2-632">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="eebc2-633">Getolgas com lseek fornece resultados incorretos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-633">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="eebc2-634">Corrija algumas travas do aplicativo de interoperabilidade Win32, aguardando a entrada em um pipe que não tenha mais dados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-634">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="eebc2-635">Suporte a O_ASYNC para arquivos TTY/PTY.</span><span class="sxs-lookup"><span data-stu-id="eebc2-635">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="eebc2-636">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-636">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-637">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-637">Console</span></span>
- <span data-ttu-id="eebc2-638">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-638">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-639">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-639">LTP Results:</span></span>
<span data-ttu-id="eebc2-640">Teste em andamento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-640">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="eebc2-641">Atualização do Fall Creators</span><span class="sxs-lookup"><span data-stu-id="eebc2-641">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="eebc2-642">Build 16288</span><span class="sxs-lookup"><span data-stu-id="eebc2-642">Build 16288</span></span>

<span data-ttu-id="eebc2-643">Para obter informações gerais do Windows sobre o Build 16288 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-643">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-644">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-645">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-645">WSL</span></span>
- <span data-ttu-id="eebc2-646">Inicializar corretamente e reportar UID, GID e modo para descritores de arquivo de soquete [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="eebc2-646">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="eebc2-647">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-647">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-648">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-648">Console</span></span>
- <span data-ttu-id="eebc2-649">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-649">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-650">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-650">LTP Results:</span></span>
<span data-ttu-id="eebc2-651">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="eebc2-651">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="eebc2-652">Build 16278</span><span class="sxs-lookup"><span data-stu-id="eebc2-652">Build 16278</span></span>

<span data-ttu-id="eebc2-653">Para obter informações gerais do Windows sobre o Build 162738 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-653">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-654">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-654">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-655">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-655">WSL</span></span>
- <span data-ttu-id="eebc2-656">Desmapear explicitamente exibições mapeadas de seções com backup de arquivo ao dividir o estado LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="eebc2-656">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="eebc2-657">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-657">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-658">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-658">Console</span></span>
- <span data-ttu-id="eebc2-659">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-660">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-660">LTP Results:</span></span>
<span data-ttu-id="eebc2-661">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="eebc2-661">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="eebc2-662">Build 16275</span><span class="sxs-lookup"><span data-stu-id="eebc2-662">Build 16275</span></span>

<span data-ttu-id="eebc2-663">Para obter informações gerais do Windows sobre o Build 162735 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-663">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-664">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-665">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-665">WSL</span></span>
- <span data-ttu-id="eebc2-666">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-666">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-667">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-667">Console</span></span>
- <span data-ttu-id="eebc2-668">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-668">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-669">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-669">LTP Results:</span></span>
<span data-ttu-id="eebc2-670">Nenhuma alteração desde 16273</span><span class="sxs-lookup"><span data-stu-id="eebc2-670">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="eebc2-671">Build 16273</span><span class="sxs-lookup"><span data-stu-id="eebc2-671">Build 16273</span></span>

<span data-ttu-id="eebc2-672">Para obter informações gerais do Windows sobre o Build 16273 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-672">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-673">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-673">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-674">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-674">WSL</span></span>
- <span data-ttu-id="eebc2-675">Corrigido um problema em que DrvFs às vezes relatou o tipo de arquivo errado para diretórios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="eebc2-675">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="eebc2-676">Permitir a criação de soquetes NETLINK_KOBJECT_UEVENT para desbloquear programas que usam UEVENT [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="eebc2-676">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="eebc2-677">Adicionar suporte para conexão sem bloqueio [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="eebc2-677">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="eebc2-678">Implementar o sinalizador de chamada do sistema clone CLONE_FS [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="eebc2-678">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="eebc2-679">Corrigir problemas em relação a não lidar com guias ou aspas corretamente no NT Interop [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="eebc2-679">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="eebc2-680">Resolver erro de acesso negado ao tentar iniciar novamente instâncias de WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="eebc2-680">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="eebc2-681">Implementar operações Futex FUTEX_REQUEUE e FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="eebc2-681">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="eebc2-682">Corrigir permissões para vários arquivos SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="eebc2-682">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="eebc2-683">Corrigir o travamento da pilha do Haskell durante a instalação [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="eebc2-683">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="eebc2-684">Implementar sinalizadores ' C ' ' O ' e ' P ' do binfmt_misc [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="eebc2-684">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="eebc2-685">Adicionar/proc/sys/kernel/SHMMAX/shmmni &/threads-Max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="eebc2-685">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="eebc2-686">Adicionar suporte parcial para chamada do sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="eebc2-686">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="eebc2-687">SO_REUSEPORT de stub & Adicionar suporte para SO_PASSCRED para soquetes NetLink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="eebc2-687">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="eebc2-688">Retornar códigos de erro diferentes de RegisterDistribuiton se uma distribuição estiver sendo instalada ou desinstalado no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-688">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="eebc2-689">Permitir o cancelamento de registro de distribuições de WSL parcialmente instaladas por meio de wslconfig. exe</span><span class="sxs-lookup"><span data-stu-id="eebc2-689">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="eebc2-690">Corrigir o travamento do teste de soquete Python do UDP:: MSG_PEEK</span><span class="sxs-lookup"><span data-stu-id="eebc2-690">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="eebc2-691">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-691">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-692">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-692">Console</span></span>
- <span data-ttu-id="eebc2-693">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-693">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-694">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-694">LTP Results:</span></span>
<span data-ttu-id="eebc2-695">Total de testes: 1904</span><span class="sxs-lookup"><span data-stu-id="eebc2-695">Total Tests: 1904</span></span><br/>
<span data-ttu-id="eebc2-696">Total de testes ignorados: 209</span><span class="sxs-lookup"><span data-stu-id="eebc2-696">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="eebc2-697">Total de falhas: 229</span><span class="sxs-lookup"><span data-stu-id="eebc2-697">Total Failures: 229</span></span><br/>
[<span data-ttu-id="eebc2-698">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-698">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="eebc2-699">Build 16257</span><span class="sxs-lookup"><span data-stu-id="eebc2-699">Build 16257</span></span>

<span data-ttu-id="eebc2-700">Para obter informações gerais do Windows sobre o Build 16257 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-700">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-701">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-701">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-702">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-702">WSL</span></span>
- <span data-ttu-id="eebc2-703">Implementar chamada do sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="eebc2-703">Implement prlimit64 system call</span></span>
- <span data-ttu-id="eebc2-704">Adicionar suporte para ulimit-n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="eebc2-704">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="eebc2-705">MSG_MORE de stub para Soquetes TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="eebc2-705">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="eebc2-706">Corrigir comportamento de vetor auxiliar AT_EXECFN inválido [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="eebc2-706">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="eebc2-707">Corrigir comportamento de copiar/colar para console/TTY e adicionar melhor manipulação de buffer completo [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="eebc2-707">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="eebc2-708">Definir AT_SECURE em vetor auxiliar para programas Set-User-ID e Set-Group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="eebc2-708">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="eebc2-709">Psuedo-ponto de extremidade do terminal mestre não tratando TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="eebc2-709">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="eebc2-710">Corrigir o lseek faz para rebobinar diretórios no LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="eebc2-710">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="eebc2-711">/dev/ptmx trava após uso intenso [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="eebc2-711">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="eebc2-712">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-712">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-713">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-713">Console</span></span>
- <span data-ttu-id="eebc2-714">Correção para linhas horizontais/sublinhados em todos os lugares [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="eebc2-714">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="eebc2-715">Correção para a ordem de processo alterada, tornando o NPM mais difícil de fechar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="eebc2-715">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="eebc2-716">Adicionou nosso novo esquema de cores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="eebc2-716">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-717">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-717">LTP Results:</span></span>
<span data-ttu-id="eebc2-718">Nenhuma alteração desde 16251</span><span class="sxs-lookup"><span data-stu-id="eebc2-718">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-719">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-719">Syscall Support</span></span>
<span data-ttu-id="eebc2-720">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-720">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-721">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-721">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="eebc2-722">Problemas Conhecidos</span><span class="sxs-lookup"><span data-stu-id="eebc2-722">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="eebc2-723">Problema do GitHub 2392: Pastas do Windows não reconhecidas pelo WSL...</span><span class="sxs-lookup"><span data-stu-id="eebc2-723">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="eebc2-724">No Build 16257, WSL tem problemas ao enumerar arquivos/pastas do Windows `/mnt/c/...`via.</span><span class="sxs-lookup"><span data-stu-id="eebc2-724">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="eebc2-725">Esse problema foi corrigido e deve ser liberado na criação de insiders durante a semana, começando em 8/14/2017.</span><span class="sxs-lookup"><span data-stu-id="eebc2-725">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="eebc2-726">Build 16251</span><span class="sxs-lookup"><span data-stu-id="eebc2-726">Build 16251</span></span>

<span data-ttu-id="eebc2-727">Para obter informações gerais do Windows sobre o Build 16251 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-727">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-728">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-728">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-729">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-729">WSL</span></span>
- <span data-ttu-id="eebc2-730">Remova a marca beta do componente opcional WSL, confira postagem no [blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="eebc2-730">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="eebc2-731">Inicializar corretamente UID e GID salvos para os binários Set-User-ID e Set-Group-ID em exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="eebc2-731">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="eebc2-732">Adicionado suporte para ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="eebc2-732">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="eebc2-733">Adicionado suporte para ptrace PTRACE_GETFPREGS e PTRACE_GETREGSET com NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="eebc2-733">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="eebc2-734">Correção de ptrace para parar em sinais ignorados</span><span class="sxs-lookup"><span data-stu-id="eebc2-734">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="eebc2-735">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-735">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-736">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-736">Console</span></span>
- <span data-ttu-id="eebc2-737">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-737">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-738">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-738">LTP Results:</span></span>
<span data-ttu-id="eebc2-739">Número de testes de passagem: 768</span><span class="sxs-lookup"><span data-stu-id="eebc2-739">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="eebc2-740">Número de testes com falha: 244</span><span class="sxs-lookup"><span data-stu-id="eebc2-740">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="eebc2-741">Número de testes ignorados: 96</span><span class="sxs-lookup"><span data-stu-id="eebc2-741">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="eebc2-742">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-742">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="eebc2-743">Build 16241</span><span class="sxs-lookup"><span data-stu-id="eebc2-743">Build 16241</span></span>

<span data-ttu-id="eebc2-744">Para obter informações gerais do Windows sobre o Build 16241 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-744">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-745">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-745">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="eebc2-746">WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-746">WSL</span></span>
- <span data-ttu-id="eebc2-747">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-747">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="eebc2-748">Console</span><span class="sxs-lookup"><span data-stu-id="eebc2-748">Console</span></span>
- <span data-ttu-id="eebc2-749">Correção para a saída do caractere errado para as linhas de cruzamento DEC, originalmente relatadas [aqui](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="eebc2-749">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="eebc2-750">Correção para nenhum texto de saída exibido na página de código 65001 (UTF8)</span><span class="sxs-lookup"><span data-stu-id="eebc2-750">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="eebc2-751">Não transfira as alterações feitas aos valores RGB de uma cor para outras partes da paleta na alteração de seleção.</span><span class="sxs-lookup"><span data-stu-id="eebc2-751">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="eebc2-752">Isso tornará a planilha de propriedades do console muito mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="eebc2-752">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="eebc2-753">CTRL + S parece não funcionar corretamente</span><span class="sxs-lookup"><span data-stu-id="eebc2-753">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="eebc2-754">Sem negrito/Dim totalmente ausente dos códigos de escape ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="eebc2-754">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="eebc2-755">O console não dá suporte corretamente a temas de cor do vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="eebc2-755">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="eebc2-756">Não é possível colar determinados caracteres [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="eebc2-756">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="eebc2-757">O redimensionamento de refluxo interage de acordo com o redimensionamento de uma janela bash quando as coisas estão na linha de comando/edição [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="eebc2-757">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="eebc2-758">CTRL-L deixa a tela suja [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="eebc2-758">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="eebc2-759">Bug de renderização do console ao exibir VT em HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="eebc2-759">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="eebc2-760">Japansese caracteres parecem estranhos com o caractere Unicode U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="eebc2-760">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="eebc2-761">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-761">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="eebc2-762">Build 16237</span><span class="sxs-lookup"><span data-stu-id="eebc2-762">Build 16237</span></span>

<span data-ttu-id="eebc2-763">Para obter informações gerais do Windows sobre o Build 16237 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-763">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-764">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-764">Fixed</span></span>
- <span data-ttu-id="eebc2-765">Usar atributos padrão para arquivos sem EAs em lxfs (raiz, raiz, 0000)</span><span class="sxs-lookup"><span data-stu-id="eebc2-765">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="eebc2-766">Suporte adicionado para distribuições que usam atributos estendidos</span><span class="sxs-lookup"><span data-stu-id="eebc2-766">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="eebc2-767">Corrigir o preenchimento das entradas retornadas por getolgas e getdents64</span><span class="sxs-lookup"><span data-stu-id="eebc2-767">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="eebc2-768">Corrigir a verificação de permissões para a chamada do sistema shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="eebc2-768">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="eebc2-769">Corrigido o estado de epoll inicial incorreto para ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="eebc2-769">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="eebc2-770">Corrigir DrvFs readdir não retornando todas as entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="eebc2-770">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="eebc2-771">Corrigir LxFs readdir quando os arquivos estiverem desvinculados [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="eebc2-771">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="eebc2-772">Permitir que arquivos drvfs não vinculados sejam reabertos por meio do procfs</span><span class="sxs-lookup"><span data-stu-id="eebc2-772">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="eebc2-773">Substituição da chave do registro global adicionada para desabilitar os recursos do WSL (Interop/montagem de unidade)</span><span class="sxs-lookup"><span data-stu-id="eebc2-773">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="eebc2-774">Corrigir a contagem de blocos incorretos em "stat" para DrvFs (e LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="eebc2-774">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="eebc2-775">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-775">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="eebc2-776">Build 16232</span><span class="sxs-lookup"><span data-stu-id="eebc2-776">Build 16232</span></span>

<span data-ttu-id="eebc2-777">Para obter informações gerais do Windows sobre o Build 16232 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-777">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-778">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-778">Fixed</span></span>
- <span data-ttu-id="eebc2-779">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-779">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="eebc2-780">Build 16226</span><span class="sxs-lookup"><span data-stu-id="eebc2-780">Build 16226</span></span>

<span data-ttu-id="eebc2-781">Para obter informações gerais do Windows sobre o Build 16226 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-781">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-782">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-782">Fixed</span></span>
- <span data-ttu-id="eebc2-783">suporte de syscalls relacionado a xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="eebc2-783">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="eebc2-784">Security. capablity xattr support.</span><span class="sxs-lookup"><span data-stu-id="eebc2-784">security.capablity xattr support.</span></span>
- <span data-ttu-id="eebc2-785">Compatibilidade aprimorada com determinados sistemas de arquivos e filtros, incluindo servidores SMB não MS.</span><span class="sxs-lookup"><span data-stu-id="eebc2-785">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="eebc2-786">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="eebc2-786">[GH #1952]</span></span>
- <span data-ttu-id="eebc2-787">Suporte aprimorado para espaços reservados do OneDrive, espaços reservados do GVFS e arquivos compactados do sistema operacional compactado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-787">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="eebc2-788">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-788">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="eebc2-789">Build 16215</span><span class="sxs-lookup"><span data-stu-id="eebc2-789">Build 16215</span></span>

<span data-ttu-id="eebc2-790">Para obter informações gerais do Windows sobre o Build 16215 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-790">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-791">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-791">Fixed</span></span>
- <span data-ttu-id="eebc2-792">O WSL não exige mais o modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="eebc2-792">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="eebc2-793">Suporte a junções de diretório em drvfs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-793">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="eebc2-794">Manipule a desinstalação de pacotes Appx de distribuição de WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-794">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="eebc2-795">Atualize procfs para mostrar mapeamentos privados e compartilhados.</span><span class="sxs-lookup"><span data-stu-id="eebc2-795">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="eebc2-796">Adicione capacidade de wslconfig. exe para limpar distribuições parcialmente instaladas ou desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-796">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="eebc2-797">Adicionado suporte para IP_MTU_DISCOVER para Soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="eebc2-797">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="eebc2-798">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="eebc2-798">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="eebc2-799">Inferir a família de protocolos para rotas para AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="eebc2-799">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="eebc2-800">Aprimoramentos de dispositivo serial [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="eebc2-800">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="eebc2-801">Build 16199</span><span class="sxs-lookup"><span data-stu-id="eebc2-801">Build 16199</span></span>

<span data-ttu-id="eebc2-802">Para obter informações gerais do Windows sobre o Build 16199 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-802">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-803">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-803">Fixed</span></span>
- <span data-ttu-id="eebc2-804">Nenhuma alteração relacionada ao WSL nessas versões.</span><span class="sxs-lookup"><span data-stu-id="eebc2-804">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="eebc2-805">Build 16193</span><span class="sxs-lookup"><span data-stu-id="eebc2-805">Build 16193</span></span>

<span data-ttu-id="eebc2-806">Para obter informações gerais do Windows sobre o Build 16193 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-806">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-807">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-807">Fixed</span></span>
- <span data-ttu-id="eebc2-808">Condição de corrida entre o envio de SIGCONT e um encerramento de um @ GH 1973]</span><span class="sxs-lookup"><span data-stu-id="eebc2-808">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="eebc2-809">alterar dispositivos tty e PTY para relatar FILE_DEVICE_NAMED_PIPE em vez de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="eebc2-809">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="eebc2-810">Correção de SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="eebc2-810">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="eebc2-811">A montagem do DrvFs foi movida para o daemon init [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="eebc2-811">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="eebc2-812">Adicionado suporte em DrvFs para os seguintes NT symlinks.</span><span class="sxs-lookup"><span data-stu-id="eebc2-812">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="eebc2-813">Build 16184</span><span class="sxs-lookup"><span data-stu-id="eebc2-813">Build 16184</span></span>

<span data-ttu-id="eebc2-814">Para obter informações gerais do Windows sobre o Build 16184 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-814">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-815">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-815">Fixed</span></span>
- <span data-ttu-id="eebc2-816">Tarefa de manutenção do pacote apt removida (lxrun. exe/update)</span><span class="sxs-lookup"><span data-stu-id="eebc2-816">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="eebc2-817">A saída corrigida não aparece nos processos do Windows no node. js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="eebc2-817">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="eebc2-818">Relaxar os requisitos de alinhamento no lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="eebc2-818">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="eebc2-819">Manipulação fixa do sinalizador AT_EMPTY_PATH em um número de chamadas do sistema.</span><span class="sxs-lookup"><span data-stu-id="eebc2-819">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="eebc2-820">Correção do problema em que a exclusão de arquivos DrvFs com identificadores abertos fará com que o arquivo apresente comportamento indefinido [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="eebc2-820">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="eebc2-821">o/etc/hosts agora herdará entradas do arquivo hosts do Windows (%WINDIR%\System32\Drivers\Etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="eebc2-821">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="eebc2-822">Build 16179</span><span class="sxs-lookup"><span data-stu-id="eebc2-822">Build 16179</span></span>

<span data-ttu-id="eebc2-823">Para obter informações gerais do Windows sobre o Build 16179 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-823">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-824">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-824">Fixed</span></span>
- <span data-ttu-id="eebc2-825">Nenhuma alteração de WSL desta semana.</span><span class="sxs-lookup"><span data-stu-id="eebc2-825">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="eebc2-826">Build 16176</span><span class="sxs-lookup"><span data-stu-id="eebc2-826">Build 16176</span></span>

<span data-ttu-id="eebc2-827">Para obter informações gerais do Windows sobre o Build 16176 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-827">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-828">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-828">Fixed</span></span>

- [<span data-ttu-id="eebc2-829">Suporte serial habilitado</span><span class="sxs-lookup"><span data-stu-id="eebc2-829">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="eebc2-830">Opção de soquete IP adicionada IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="eebc2-830">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="eebc2-831">Função pwritev implementada (ao carregar o arquivo para Nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="eebc2-831">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="eebc2-832">Opções de soquete IP adicionadas IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="eebc2-832">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="eebc2-833">Suporte para a opção socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="eebc2-833">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="eebc2-834">Adição de IP (V6) _MTU Socket Option para aplicativos nó, traceroute, busca, Nslookup, host</span><span class="sxs-lookup"><span data-stu-id="eebc2-834">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="eebc2-835">Opção de soquete IP adicionada IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="eebc2-835">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="eebc2-836">Aprimoramentos do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="eebc2-836">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="eebc2-837">Permitir a montagem de caminhos UNC</span><span class="sxs-lookup"><span data-stu-id="eebc2-837">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="eebc2-838">Habilitar o suporte CDFS no drvfs</span><span class="sxs-lookup"><span data-stu-id="eebc2-838">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="eebc2-839">Manipular corretamente as permissões para sistemas de arquivos de rede no drvfs</span><span class="sxs-lookup"><span data-stu-id="eebc2-839">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="eebc2-840">Adicionar suporte para unidades remotas ao drvfs</span><span class="sxs-lookup"><span data-stu-id="eebc2-840">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="eebc2-841">Habilitar o suporte a FAT no drvfs</span><span class="sxs-lookup"><span data-stu-id="eebc2-841">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="eebc2-842">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-842">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-843">Resultados do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-843">LTP Results</span></span>
<span data-ttu-id="eebc2-844">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="eebc2-844">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="eebc2-845">Build 16170</span><span class="sxs-lookup"><span data-stu-id="eebc2-845">Build 16170</span></span>

<span data-ttu-id="eebc2-846">Para obter informações gerais do Windows sobre o Build 16170 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-846">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="eebc2-847">Lançamos uma nova [postagem de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutindo nossos esforços para testar o WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-847">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="eebc2-848">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-848">Fixed</span></span>

- <span data-ttu-id="eebc2-849">Opção de soquete de suporte IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="eebc2-849">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="eebc2-850">Adicione suporte para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="eebc2-850">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="eebc2-851">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="eebc2-851">[GH 1692]</span></span>
- <span data-ttu-id="eebc2-852">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-852">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-853">Resultados do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-853">LTP Results</span></span>
<span data-ttu-id="eebc2-854">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="eebc2-854">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="eebc2-855">Compilar o 15046 para a atualização do Windows 10 para criadores</span><span class="sxs-lookup"><span data-stu-id="eebc2-855">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="eebc2-856">Não há mais correções WSL ou recursos planejados para inclusão na atualização de criadores para o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="eebc2-856">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="eebc2-857">As notas de versão do WSL serão retomadas nas próximas semanas para as adições direcionadas ao próximo Windows Update principal.</span><span class="sxs-lookup"><span data-stu-id="eebc2-857">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="eebc2-858">Para obter informações gerais do Windows sobre o Build 15046 e futuras versões do Insider, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-858">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="eebc2-859">Build 15042</span><span class="sxs-lookup"><span data-stu-id="eebc2-859">Build 15042</span></span>

<span data-ttu-id="eebc2-860">Para obter informações gerais do Windows sobre o Build 15042 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-860">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-861">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-861">Fixed</span></span>

- <span data-ttu-id="eebc2-862">Correção de um deadlock ao remover um caminho que termina em ".."</span><span class="sxs-lookup"><span data-stu-id="eebc2-862">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="eebc2-863">Corrigido um problema em que FIONBIO não retornava 0 no êxito [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="eebc2-863">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="eebc2-864">Correção do problema com leituras de comprimento zero de soquetes de datagrama inet</span><span class="sxs-lookup"><span data-stu-id="eebc2-864">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="eebc2-865">Corrigir um possível deadlock devido à condição de corrida na pesquisa de inode de drvfs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="eebc2-865">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="eebc2-866">Suporte estendido para dados complementares de soquete UNIX; SCM_CREDENTIALS e SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="eebc2-866">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="eebc2-867">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-867">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-868">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-868">LTP Results:</span></span>
<span data-ttu-id="eebc2-869">Número de testes aprovados: 737</span><span class="sxs-lookup"><span data-stu-id="eebc2-869">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="eebc2-870">Número de não aprovados (com falha, ignorado, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="eebc2-870">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="eebc2-871">Build 15031</span><span class="sxs-lookup"><span data-stu-id="eebc2-871">Build 15031</span></span>

<span data-ttu-id="eebc2-872">Para obter informações gerais do Windows sobre o Build 15031 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-872">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-873">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-873">Fixed</span></span>

- <span data-ttu-id="eebc2-874">Corrigido um bug em que o tempo (2) se comportaria esporadicamente.</span><span class="sxs-lookup"><span data-stu-id="eebc2-874">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="eebc2-875">Corrigido e problema em que \* SIGPROCMASK syscalls poderia corromper a máscara de sinal.</span><span class="sxs-lookup"><span data-stu-id="eebc2-875">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="eebc2-876">Agora, retorne o comprimento de linha de comando completo na notificação de criação de processo WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-876">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="eebc2-877">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="eebc2-877">[GH 1632]</span></span>
- <span data-ttu-id="eebc2-878">WSL agora relata a saída do thread por meio do ptrace para travas do GDB.</span><span class="sxs-lookup"><span data-stu-id="eebc2-878">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="eebc2-879">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="eebc2-879">[GH 1196]</span></span>
- <span data-ttu-id="eebc2-880">Corrigido o bug em que PTYs seria interrompido depois de tmux de e/s pesada.</span><span class="sxs-lookup"><span data-stu-id="eebc2-880">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="eebc2-881">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="eebc2-881">[GH 1358]</span></span>
- <span data-ttu-id="eebc2-882">Correção da validação de tempo limite em muitas chamadas do sistema (Futex, SEMTIMEDOP, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="eebc2-882">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="eebc2-883">Adicionado suporte eventfd EFD_SEMAPHORE [GH 452]</span><span class="sxs-lookup"><span data-stu-id="eebc2-883">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="eebc2-884">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-884">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-885">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-885">LTP Results:</span></span>
<span data-ttu-id="eebc2-886">Número de testes aprovados: 737</span><span class="sxs-lookup"><span data-stu-id="eebc2-886">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="eebc2-887">Número de não aprovados (com falha, ignorado, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="eebc2-887">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="eebc2-888">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-888">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="eebc2-889">Build 15025</span><span class="sxs-lookup"><span data-stu-id="eebc2-889">Build 15025</span></span>

<span data-ttu-id="eebc2-890">Para obter informações gerais do Windows sobre o Build 15025 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-890">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-891">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-891">Fixed</span></span>

- <span data-ttu-id="eebc2-892">Correção para o bug que quebrou o grep 2,27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="eebc2-892">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="eebc2-893">Sinalizador EFD_SEMAPHORE implementado para syscall eventfd2 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="eebc2-893">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="eebc2-894">Implementado/proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="eebc2-894">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="eebc2-895">Suporte de e/s controlado por sinal para soquetes de fluxo do UNIX [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="eebc2-895">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="eebc2-896">Suporte a F_GETPIPE_SZ e F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="eebc2-896">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="eebc2-897">Implementar syscall recvmmsg () [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="eebc2-897">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="eebc2-898">Corrigido o bug em que epoll_wait () não estava aguardando [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="eebc2-898">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="eebc2-899">Implementar/proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="eebc2-899">Implement /proc/version_signature</span></span>
- <span data-ttu-id="eebc2-900">O syscall de hoje retorna uma falha se os dois descritores de arquivo se referirem ao mesmo pipe</span><span class="sxs-lookup"><span data-stu-id="eebc2-900">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="eebc2-901">Implementação do comportamento correto para SO_PEERCRED para soquetes UNIX</span><span class="sxs-lookup"><span data-stu-id="eebc2-901">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="eebc2-902">Manipulação de parâmetro inválida de syscall tkill corrigida</span><span class="sxs-lookup"><span data-stu-id="eebc2-902">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="eebc2-903">Alterações para aumentar o preformace de drvfs</span><span class="sxs-lookup"><span data-stu-id="eebc2-903">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="eebc2-904">Correção secundária para bloqueio de e/s Ruby</span><span class="sxs-lookup"><span data-stu-id="eebc2-904">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="eebc2-905">Corrigido recvmsg () retornando EINVAL para o sinalizador MSG_DONTWAIT para os soquetes inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="eebc2-905">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="eebc2-906">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-906">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-907">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-907">LTP Results:</span></span>
<span data-ttu-id="eebc2-908">Número de testes aprovados: 732</span><span class="sxs-lookup"><span data-stu-id="eebc2-908">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="eebc2-909">Número de não aprovados (com falha, ignorado, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="eebc2-909">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="eebc2-910">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-910">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="eebc2-911">Build 15019</span><span class="sxs-lookup"><span data-stu-id="eebc2-911">Build 15019</span></span>

<span data-ttu-id="eebc2-912">Para obter informações gerais do Windows sobre o Build 15019 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-912">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-913">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-913">Fixed</span></span>

- <span data-ttu-id="eebc2-914">Correção do bug que reportou incorretamente o uso da CPU em procfs para ferramentas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="eebc2-914">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="eebc2-915">Ao chamar Open () com O_TRUNC em um arquivo existente, INotifyPropertyChanged agora gera IN_MODIFY antes de IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="eebc2-915">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="eebc2-916">Correções para SO_ERROR de soquetes UNIX getsockopt para habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="eebc2-916">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="eebc2-917">Implementar o/proc/sys/net/Core/SOMAXCONN para o idioma GO</span><span class="sxs-lookup"><span data-stu-id="eebc2-917">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="eebc2-918">Apt-obter tarefa de histórico de atualização de pacote agora é executada oculta da exibição</span><span class="sxs-lookup"><span data-stu-id="eebc2-918">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="eebc2-919">Limpar escopo do localhost IPv6 (falha de Spring-Framework (Java)).</span><span class="sxs-lookup"><span data-stu-id="eebc2-919">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="eebc2-920">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-920">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-921">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-921">LTP Results:</span></span>
<span data-ttu-id="eebc2-922">Número de testes aprovados: 714</span><span class="sxs-lookup"><span data-stu-id="eebc2-922">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="eebc2-923">Número de não aprovados (com falha, ignorado, etc...): 249</span><span class="sxs-lookup"><span data-stu-id="eebc2-923">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="eebc2-924">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-924">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="eebc2-925">Build 15014</span><span class="sxs-lookup"><span data-stu-id="eebc2-925">Build 15014</span></span>

<span data-ttu-id="eebc2-926">Para obter informações gerais do Windows sobre o Build 15014 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="eebc2-926">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-927">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-927">Fixed</span></span>

- <span data-ttu-id="eebc2-928">CTRL + C agora funciona conforme o esperado</span><span class="sxs-lookup"><span data-stu-id="eebc2-928">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="eebc2-929">htop e PS auxw agora mostram a utilização de recursos correta (GH #516)</span><span class="sxs-lookup"><span data-stu-id="eebc2-929">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="eebc2-930">Tradução básica de exceções NT para sinais.</span><span class="sxs-lookup"><span data-stu-id="eebc2-930">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="eebc2-931">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="eebc2-931">(GH #513)</span></span>
- <span data-ttu-id="eebc2-932">fallocate agora falha com ENOSPC ao ficar sem espaço em vez de EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="eebc2-932">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="eebc2-933">/Proc/sys/kernel/sem. adicionados</span><span class="sxs-lookup"><span data-stu-id="eebc2-933">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="eebc2-934">Implementadas chamadas do sistema semop e SEMTIMEDOP</span><span class="sxs-lookup"><span data-stu-id="eebc2-934">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="eebc2-935">Correção de erros nslookup com IP_RECVTOS & IPV6_RECVTCLASS Socket Option (GH 69)</span><span class="sxs-lookup"><span data-stu-id="eebc2-935">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="eebc2-936">Suporte para opções de soquete IP_RECVTTL e IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="eebc2-936">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="eebc2-937">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-937">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-938">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-938">LTP Results:</span></span>
<span data-ttu-id="eebc2-939">Número de testes aprovados: 709</span><span class="sxs-lookup"><span data-stu-id="eebc2-939">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="eebc2-940">Número de não aprovados (com falha, ignorado, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="eebc2-940">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="eebc2-941">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-941">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="eebc2-942">Resumo de syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-942">Syscall Summary</span></span>
<span data-ttu-id="eebc2-943">Total de syscalls: 384</span><span class="sxs-lookup"><span data-stu-id="eebc2-943">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="eebc2-944">Total implementado: 235</span><span class="sxs-lookup"><span data-stu-id="eebc2-944">Total Implemented: 235</span></span> </br>
<span data-ttu-id="eebc2-945">Total de fragmentado: 22</span><span class="sxs-lookup"><span data-stu-id="eebc2-945">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="eebc2-946">Total não implementado: 127</span><span class="sxs-lookup"><span data-stu-id="eebc2-946">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="eebc2-947">Detalhamento detalhado</span><span class="sxs-lookup"><span data-stu-id="eebc2-947">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="eebc2-948">Build 15007</span><span class="sxs-lookup"><span data-stu-id="eebc2-948">Build 15007</span></span>

<span data-ttu-id="eebc2-949">Para obter informações gerais do Windows sobre o Build 15007 visite o [blog do Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="eebc2-949">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="eebc2-950">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="eebc2-950">Known Issue</span></span>

- <span data-ttu-id="eebc2-951">Há um bug conhecido em que o console não reconhece algumas entradas CTRL + <key> .</span><span class="sxs-lookup"><span data-stu-id="eebc2-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="eebc2-952">Isso inclui o comando CTRL-c que atuará como um pressionamento normal de ' C'.</span><span class="sxs-lookup"><span data-stu-id="eebc2-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="eebc2-953">Solução alternativa: Mapeie uma chave alternativa para CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="eebc2-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="eebc2-954">Por exemplo, para mapear CTRL + K para CTRL + C, `stty intr \^k`faça o:.</span><span class="sxs-lookup"><span data-stu-id="eebc2-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="eebc2-955">Esse mapeamento é por terminal e terá que ser feito *toda* vez que o bash for iniciado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="eebc2-956">Os usuários podem explorar a opção para incluí-lo em seus`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="eebc2-956">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="eebc2-957">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-957">Fixed</span></span>

- <span data-ttu-id="eebc2-958">Correção do problema em que a execução do WSL consumiria 100% de um núcleo de CPU</span><span class="sxs-lookup"><span data-stu-id="eebc2-958">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="eebc2-959">A opção de soquete IP_PKTINFO, IPV6_RECVPKTINFO agora tem suporte.</span><span class="sxs-lookup"><span data-stu-id="eebc2-959">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="eebc2-960">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="eebc2-960">(GH #851, 987)</span></span>
- <span data-ttu-id="eebc2-961">Truncar o endereço físico da interface de rede para 16 bytes em lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="eebc2-961">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="eebc2-962">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-962">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-963">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-963">LTP Results:</span></span>
<span data-ttu-id="eebc2-964">Número de testes aprovados: 709</span><span class="sxs-lookup"><span data-stu-id="eebc2-964">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="eebc2-965">Número de não aprovados (com falha, ignorado, etc...): 255</span><span class="sxs-lookup"><span data-stu-id="eebc2-965">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="eebc2-966">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-966">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="eebc2-967">Build 15002</span><span class="sxs-lookup"><span data-stu-id="eebc2-967">Build 15002</span></span>

<span data-ttu-id="eebc2-968">Para obter informações gerais do Windows sobre o Build 15002 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-968">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="eebc2-969">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="eebc2-969">Known Issue</span></span>

<span data-ttu-id="eebc2-970">Dois problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="eebc2-970">Two known issues:</span></span>
- <span data-ttu-id="eebc2-971">Há um bug conhecido em que o console não reconhece algumas entradas CTRL + <key> .</span><span class="sxs-lookup"><span data-stu-id="eebc2-971">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="eebc2-972">Isso inclui o comando CTRL-c que atuará como um pressionamento normal de ' C'.</span><span class="sxs-lookup"><span data-stu-id="eebc2-972">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="eebc2-973">Solução alternativa: Mapeie uma chave alternativa para CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="eebc2-973">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="eebc2-974">Por exemplo, para mapear CTRL + K para CTRL + C, `stty intr \^k`faça o:.</span><span class="sxs-lookup"><span data-stu-id="eebc2-974">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="eebc2-975">Esse mapeamento é por terminal e terá que ser feito *toda* vez que o bash for iniciado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-975">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="eebc2-976">Os usuários podem explorar a opção para incluí-lo em seus`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="eebc2-976">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="eebc2-977">Enquanto o WSL estiver executando um thread do sistema, consumirá 100% de um núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="eebc2-977">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="eebc2-978">A causa raiz foi resolvida e corrigida internamente.</span><span class="sxs-lookup"><span data-stu-id="eebc2-978">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="eebc2-979">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-979">Fixed</span></span>

- <span data-ttu-id="eebc2-980">Todas as sessões de bash agora devem ser criadas no mesmo nível de permissão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-980">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="eebc2-981">A tentativa de iniciar uma sessão em um nível diferente será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="eebc2-981">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="eebc2-982">Isso significa que os consoles admin e não admin não podem ser executados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-982">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="eebc2-983">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="eebc2-983">(GH #626)</span></span>
<br/>
- <span data-ttu-id="eebc2-984">Implementadas as seguintes mensagens NETLINK_ROUTEs (requer administrador do Windows)</span><span class="sxs-lookup"><span data-stu-id="eebc2-984">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="eebc2-985">RTM_NEWADDR (dá `ip addr add`suporte)</span><span class="sxs-lookup"><span data-stu-id="eebc2-985">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="eebc2-986">RTM_NEWROUTE (dá `ip route add`suporte)</span><span class="sxs-lookup"><span data-stu-id="eebc2-986">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="eebc2-987">RTM_DELADDR (dá `ip addr del`suporte)</span><span class="sxs-lookup"><span data-stu-id="eebc2-987">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="eebc2-988">RTM_DELROUTE (dá `ip route del`suporte)</span><span class="sxs-lookup"><span data-stu-id="eebc2-988">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="eebc2-989">A verificação de tarefa agendada dos pacotes a serem atualizados não será mais executada em uma conexão limitada (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="eebc2-989">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="eebc2-990">Corrigido o erro em que a tubulação fica presa, ou seja, bash-c "ls-alR/" | bash-c "Cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="eebc2-990">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="eebc2-991">Opção TCP_KEEPCNT Socket implementada (GH #843)</span><span class="sxs-lookup"><span data-stu-id="eebc2-991">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="eebc2-992">Opção de soquete IP_MTU_DISCOVER INET implementada (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="eebc2-992">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="eebc2-993">Funcionalidade herdada removida para executar binários NT a partir de init com a pesquisa de NT Path.</span><span class="sxs-lookup"><span data-stu-id="eebc2-993">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="eebc2-994">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="eebc2-994">(GH #1325)</span></span>
- <span data-ttu-id="eebc2-995">Corrigir o modo de/dev/kmsg para permitir acesso de leitura/grupo (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="eebc2-995">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="eebc2-996">Implementado/proc/sys/kernel/Random/UUID (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="eebc2-996">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="eebc2-997">Erro corrigido em que a hora de início do processo foi mostrada como ano 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="eebc2-997">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="eebc2-998">Variável de ambiente de termo padrão alternada para xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="eebc2-998">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="eebc2-999">Modificou a maneira como a confirmação de processamento é calculada durante o processo Fork.</span><span class="sxs-lookup"><span data-stu-id="eebc2-999">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="eebc2-1000">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1000">(GH #1286)</span></span>
- <span data-ttu-id="eebc2-1001">/Proc/sys/VM/overcommit_memory. implementados</span><span class="sxs-lookup"><span data-stu-id="eebc2-1001">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="eebc2-1002">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1002">(GH #1286)</span></span>
- <span data-ttu-id="eebc2-1003">Arquivo/proc/net/Route implementado (GH #69)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1003">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="eebc2-1004">Corrigido o erro em que o nome do atalho foi localizado incorretamente (GH #696)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1004">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="eebc2-1005">A lógica de análise Elf fixa que está validando incorretamente os cabeçalhos de programa deve ser menor que (ou igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1005">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="eebc2-1006">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1006">(GH #1048)</span></span>
- <span data-ttu-id="eebc2-1007">Implementado o retorno de chamada statfs para procfs, sysfs, cgroupfs e binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1007">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="eebc2-1008">Correção das janelas AptPackageIndexUpdate que não serão fechadas (GH #1184, também discutidas em GH #1193)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1008">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="eebc2-1009">Adicionado suporte de ADDR_NO_RANDOMIZE de personalidade de ASLR.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1009">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="eebc2-1010">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1010">(GH #1148, 1128)</span></span>
- <span data-ttu-id="eebc2-1011">Melhoria de PTRACE_GETSIGINFO, SIGSEGV, para rastreamentos de pilha gdb apropriados durante o AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1011">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="eebc2-1012">A análise de Elf não falha mais para binários patchelf.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1012">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="eebc2-1013">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1013">(GH #471)</span></span>
- <span data-ttu-id="eebc2-1014">DNS de VPN propagado para/etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1014">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="eebc2-1015">Melhorias no TCP Close para transferência de dados mais confiável.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1015">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="eebc2-1016">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1016">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="eebc2-1017">Agora, retorne o código de erro correto quando muitos arquivos estiverem abertos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1017">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="eebc2-1018">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1018">(GH #1126, 2090)</span></span>
- <span data-ttu-id="eebc2-1019">O log de auditoria do Windows agora relata o nome da imagem em processar criar auditoria.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1019">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="eebc2-1020">Agora, falha normalmente ao iniciar bash. exe de dentro de uma janela de bash</span><span class="sxs-lookup"><span data-stu-id="eebc2-1020">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="eebc2-1021">Mensagem de erro adicionada quando a interoperabilidade não consegue acessar um diretório de trabalho em LxFs (ou seja, notepad. exe. bashrc)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1021">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="eebc2-1022">Corrigido o problema em que o caminho do Windows foi truncado em WSL</span><span class="sxs-lookup"><span data-stu-id="eebc2-1022">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="eebc2-1023">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1023">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1024">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1024">LTP Results:</span></span>
<span data-ttu-id="eebc2-1025">Número de testes aprovados: 690</span><span class="sxs-lookup"><span data-stu-id="eebc2-1025">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="eebc2-1026">Número de não aprovados (com falha, ignorado, etc...): 274</span><span class="sxs-lookup"><span data-stu-id="eebc2-1026">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="eebc2-1027">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1027">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1028">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1028">Syscall Support</span></span>
<span data-ttu-id="eebc2-1029">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1029">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1030">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1030">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="eebc2-1031">Build 14986</span><span class="sxs-lookup"><span data-stu-id="eebc2-1031">Build 14986</span></span>

<span data-ttu-id="eebc2-1032">Para obter informações gerais do Windows sobre o Build 14986 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1032">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1033">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1033">Fixed</span></span>

- <span data-ttu-id="eebc2-1034">Correção de bugchecks com NetLink e PTY IOCTLs</span><span class="sxs-lookup"><span data-stu-id="eebc2-1034">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="eebc2-1035">A versão do kernel agora relata 4.4.0-43 para consistência com Xenial</span><span class="sxs-lookup"><span data-stu-id="eebc2-1035">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="eebc2-1036">O bash. exe agora é iniciado quando a entrada é direcionada para ' nul: ' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1036">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="eebc2-1037">IDs de thread agora relatadas corretamente em procfs (GH #967)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1037">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="eebc2-1038">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Sinalizadores IN_ISDIR agora têm suporte em inotify_add_watch () (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1038">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="eebc2-1039">Implemente timer_create e chamadas de sistema relacionadas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1039">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="eebc2-1040">Isso habilita o suporte a GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1040">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="eebc2-1041">Corrigido o problema em que o ping retornou um tempo de 0.000 MS (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1041">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="eebc2-1042">Retorne o código de erro correto quando muitos arquivos forem abertos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1042">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="eebc2-1043">Correção do problema em WSL em que a solicitação do NetLink para dados da interface de rede falharia com EINVAL se o endereço de hardware da interface for 32-bytes (como a interface teredo)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1043">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="eebc2-1044">Observe que o utilitário "IP" do Linux contém um bug em que ele falhará se WSL relatar um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1044">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="eebc2-1045">Esse é um bug em "IP", não WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1045">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="eebc2-1046">O utilitário "IP" codifica o tamanho do buffer de cadeia de caracteres usado para imprimir o endereço de hardware e esse buffer é muito pequeno para imprimir um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1046">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="eebc2-1047">Correções e aprimoramentos adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1047">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1048">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1048">LTP Results:</span></span>
<span data-ttu-id="eebc2-1049">Número de testes aprovados: 669</span><span class="sxs-lookup"><span data-stu-id="eebc2-1049">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="eebc2-1050">Número de não aprovados (com falha, ignorado, etc...): 258</span><span class="sxs-lookup"><span data-stu-id="eebc2-1050">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="eebc2-1051">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1051">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1052">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1052">Syscall Support</span></span>
<span data-ttu-id="eebc2-1053">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1053">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1054">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1054">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="eebc2-1055">Build 14971</span><span class="sxs-lookup"><span data-stu-id="eebc2-1055">Build 14971</span></span>

<span data-ttu-id="eebc2-1056">Para obter informações gerais do Windows sobre o Build 14971 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1056">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1057">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1057">Fixed</span></span>

 - <span data-ttu-id="eebc2-1058">Devido a circunstâncias além do nosso controle, não há atualizações nessa compilação para o subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1058">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="eebc2-1059">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1059">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1060">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1060">LTP Results:</span></span>
<span data-ttu-id="eebc2-1061">Não alterado de 14965</span><span class="sxs-lookup"><span data-stu-id="eebc2-1061">Unchanged from 14965</span></span> </br>
<span data-ttu-id="eebc2-1062">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="eebc2-1062">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="eebc2-1063">Número de não aprovados (com falha, ignorado, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="eebc2-1063">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="eebc2-1064">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1064">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="eebc2-1065">Build 14965</span><span class="sxs-lookup"><span data-stu-id="eebc2-1065">Build 14965</span></span>

<span data-ttu-id="eebc2-1066">Para obter informações gerais do Windows sobre o Build 14965 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1066">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1067">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1067">Fixed</span></span>

- <span data-ttu-id="eebc2-1068">Suporte para RTM_GETLINK e RTM_GETADDR do protocolo NetLink Sockets NETLINK_ROUTE (GH #468)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1068">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="eebc2-1069">Habilita os comandos ifconfig e IP para enumeração de rede</span><span class="sxs-lookup"><span data-stu-id="eebc2-1069">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="eebc2-1070">Mais informações podem ser encontradas em nossa [postagem no blog de rede WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1070">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="eebc2-1071">/sbin agora está no caminho do usuário por padrão</span><span class="sxs-lookup"><span data-stu-id="eebc2-1071">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="eebc2-1072">O caminho de usuário do NT agora é acrescentado ao caminho WSL por padrão (ou seja, agora você pode digitar notepad. exe sem adicionar system32 ao caminho do Linux)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1072">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="eebc2-1073">Adicionado suporte para/proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="eebc2-1073">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="eebc2-1074">Os binários do NT agora podem ser iniciados em WSL quando o diretório de trabalho atual contém caracteres não-ANSI (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1074">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="eebc2-1075">Permitir desligamento no soquete de fluxo UNIX desconectado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1075">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="eebc2-1076">Adicionado suporte para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1076">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="eebc2-1077">Adicionado suporte para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="eebc2-1077">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="eebc2-1078">Corrigido o erro em que a tubulação fica presa, ou seja, bash-c "ls-alR/" | bash-c "Cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1078">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="eebc2-1079">Manipule solicitações para se conectar ao terminal atual.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1079">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="eebc2-1080">Marque/proc/<pid>/oom_score_adj como gravável.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1080">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="eebc2-1081">Adicione a pasta/sys/FS/CGroup.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1081">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="eebc2-1082">sched_setaffinity deve retornar o número de máscara de bits de afinidade</span><span class="sxs-lookup"><span data-stu-id="eebc2-1082">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="eebc2-1083">Corrigir a lógica de validação ELF que pressupõe incorretamente que os caminhos do intérprete devem ter menos de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1083">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="eebc2-1084">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1084">(GH #743)</span></span>
- <span data-ttu-id="eebc2-1085">Abrir descritores de arquivo podem manter a janela do console aberta (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1085">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="eebc2-1086">Erro de Fixeed em que renomear () falhou com barra à direita no nome de destino (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1086">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="eebc2-1087">Implementar arquivo/proc/net/dev</span><span class="sxs-lookup"><span data-stu-id="eebc2-1087">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="eebc2-1088">Correção de pings 0.000 MS devido à resolução do timer.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1088">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="eebc2-1089">Implementado/proc/Self/Environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1089">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="eebc2-1090">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1090">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1091">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1091">LTP Results:</span></span>
<span data-ttu-id="eebc2-1092">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="eebc2-1092">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="eebc2-1093">Número de não aprovados (com falha, ignorado, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="eebc2-1093">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="eebc2-1094">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1094">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="eebc2-1095">Build 14959</span><span class="sxs-lookup"><span data-stu-id="eebc2-1095">Build 14959</span></span>

<span data-ttu-id="eebc2-1096">Para obter informações gerais do Windows sobre o Build 14959 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1096">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1097">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1097">Fixed</span></span>

- <span data-ttu-id="eebc2-1098">Notificação de processo RsFilter aprimorada para Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1098">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="eebc2-1099">Informações adicionais encontradas no [blog do WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1099">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="eebc2-1100">Estabilidade aprimorada com a interoperabilidade do Windows</span><span class="sxs-lookup"><span data-stu-id="eebc2-1100">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="eebc2-1101">Corrigido o erro 0x80070057 ao iniciar o bash. exe quando a proteção de dados empresariais (EDP) estiver habilitada</span><span class="sxs-lookup"><span data-stu-id="eebc2-1101">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="eebc2-1102">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1102">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1103">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1103">LTP Results:</span></span>
<span data-ttu-id="eebc2-1104">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="eebc2-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="eebc2-1105">Número de não aprovados (com falha, ignorado, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="eebc2-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="eebc2-1106">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="eebc2-1107">Build 14955</span><span class="sxs-lookup"><span data-stu-id="eebc2-1107">Build 14955</span></span>

<span data-ttu-id="eebc2-1108">Para obter informações gerais do Windows sobre o Build 14955 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1108">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1109">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1109">Fixed</span></span>

 - <span data-ttu-id="eebc2-1110">Devido a circunstâncias além do nosso controle, não há atualizações nessa compilação para o subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1110">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="eebc2-1111">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1111">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1112">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1112">LTP Results:</span></span>
<span data-ttu-id="eebc2-1113">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="eebc2-1113">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="eebc2-1114">Número de não aprovados (com falha, ignorado, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="eebc2-1114">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="eebc2-1115">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1115">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="eebc2-1116">Build 14951</span><span class="sxs-lookup"><span data-stu-id="eebc2-1116">Build 14951</span></span>

<span data-ttu-id="eebc2-1117">Para obter informações gerais do Windows sobre o Build 14951 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1117">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="eebc2-1118">Novo recurso: Interoperabilidade do Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="eebc2-1118">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="eebc2-1119">Os binários do Windows agora podem ser chamados diretamente da linha de comando WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1119">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="eebc2-1120">Isso dá aos usuários a capacidade de interagir com o ambiente e o sistema do Windows de uma maneira que não foi possível.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1120">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="eebc2-1121">Como um exemplo rápido, agora é possível que os usuários executem os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1121">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="eebc2-1122">Mais informações podem ser encontradas em:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1122">More information can be found at:</span></span>

- [<span data-ttu-id="eebc2-1123">Blog da equipe do WSL para interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="eebc2-1123">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="eebc2-1124">Documentação do MSDN Interop</span><span class="sxs-lookup"><span data-stu-id="eebc2-1124">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="eebc2-1125">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1125">Fixed</span></span>

- <span data-ttu-id="eebc2-1126">O Ubuntu 16, 4 (Xenial) agora está instalado para todas as novas instâncias de WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1126">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="eebc2-1127">Os usuários com instâncias 14, 4 (confiáveis) existentes não serão atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1127">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="eebc2-1128">A localidade definida durante a instalação agora é exibida</span><span class="sxs-lookup"><span data-stu-id="eebc2-1128">Locale set during install is now displayed</span></span>
- <span data-ttu-id="eebc2-1129">Melhorias de terminal, incluindo bugs em que o redirecionamento de um processo WSL para um arquivo nem sempre funciona</span><span class="sxs-lookup"><span data-stu-id="eebc2-1129">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="eebc2-1130">O tempo de vida do console deve estar vinculado ao tempo de vida do bash. exe</span><span class="sxs-lookup"><span data-stu-id="eebc2-1130">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="eebc2-1131">O tamanho da janela do console deve usar tamanho visível, não tamanho do buffer</span><span class="sxs-lookup"><span data-stu-id="eebc2-1131">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="eebc2-1132">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1132">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1133">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1133">LTP Results:</span></span>
<span data-ttu-id="eebc2-1134">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="eebc2-1134">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="eebc2-1135">Número de não aprovados (com falha, ignorado, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="eebc2-1135">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="eebc2-1136">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1136">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="eebc2-1137">Build 14946</span><span class="sxs-lookup"><span data-stu-id="eebc2-1137">Build 14946</span></span>

<span data-ttu-id="eebc2-1138">Para obter informações gerais do Windows sobre o Build 14946 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1138">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1139">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1139">Fixed</span></span>

- <span data-ttu-id="eebc2-1140">Correção de um problema que impedia a criação de contas de usuário WSL para usuários com NT Names que contenham espaços ou aspas.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1140">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="eebc2-1141">Altere VolFs e DrvFs para retornar 0 para a contagem de links do diretório em stat</span><span class="sxs-lookup"><span data-stu-id="eebc2-1141">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="eebc2-1142">Suporte à opção de soquete IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1142">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="eebc2-1143">Limite para um loop de e/s de console único por TTY.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1143">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="eebc2-1144">Exemplo: o seguinte comando é possível:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1144">Example: the following command is possible:</span></span>
  - <span data-ttu-id="eebc2-1145">bash-c "ecoar dados" | bash-c "ssh user@example.com " Cat > foo. txt ' "</span><span class="sxs-lookup"><span data-stu-id="eebc2-1145">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="eebc2-1146">substituir espaços por tabulações em/proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1146">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="eebc2-1147">DrvFs agora aparece em mountinfo com um nome que corresponde ao volume montado do Windows</span><span class="sxs-lookup"><span data-stu-id="eebc2-1147">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="eebc2-1148">/Home e/root agora aparecem em mountinfo com nomes corretos</span><span class="sxs-lookup"><span data-stu-id="eebc2-1148">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="eebc2-1149">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1149">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1150">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1150">LTP Results:</span></span>
<span data-ttu-id="eebc2-1151">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="eebc2-1151">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="eebc2-1152">Número de não aprovados (com falha, ignorado, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="eebc2-1152">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="eebc2-1153">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1153">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="eebc2-1154">Build 14942</span><span class="sxs-lookup"><span data-stu-id="eebc2-1154">Build 14942</span></span>

<span data-ttu-id="eebc2-1155">Para obter informações gerais do Windows sobre o Build 14942 visite o [blog do Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1155">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1156">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1156">Fixed</span></span>

- <span data-ttu-id="eebc2-1157">Vários bugchecks endereçados, incluindo a falha de rede "tentativa de executar a memória noexecute" que estava bloqueando o SSH</span><span class="sxs-lookup"><span data-stu-id="eebc2-1157">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="eebc2-1158">o suporte do inotifiy para notificações geradas de aplicativos do Windows no DrvFs agora está em</span><span class="sxs-lookup"><span data-stu-id="eebc2-1158">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="eebc2-1159">Implemente TCP_KEEPIDLE e TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1159">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="eebc2-1160">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1160">(GH #695)</span></span>
- <span data-ttu-id="eebc2-1161">Implementar a chamada do sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="eebc2-1161">Implement the pivot_root system call</span></span>
- <span data-ttu-id="eebc2-1162">Implementar opção de soquete para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="eebc2-1162">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="eebc2-1163">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1163">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="eebc2-1164">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1164">LTP Results:</span></span>
<span data-ttu-id="eebc2-1165">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="eebc2-1165">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="eebc2-1166">Número de não aprovados (com falha, ignorado, etc...): 263</span><span class="sxs-lookup"><span data-stu-id="eebc2-1166">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="eebc2-1167">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1167">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1168">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1168">Syscall Support</span></span>
<span data-ttu-id="eebc2-1169">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1169">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1170">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1170">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="eebc2-1171">Build 14936</span><span class="sxs-lookup"><span data-stu-id="eebc2-1171">Build 14936</span></span>

<span data-ttu-id="eebc2-1172">Para obter informações gerais do Windows sobre o Build 14936 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1172">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="eebc2-1173">Observação: O WSL instalará o Ubuntu versão 16, 4 (Xenial) em vez do Ubuntu 14, 4 (trusty) em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1173">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="eebc2-1174">Essa alteração se aplicará a pessoas que instalam novas instâncias (lxrun. exe/install ou a primeira execução de bash. exe).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1174">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="eebc2-1175">As instâncias existentes com confiança não serão atualizadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1175">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="eebc2-1176">Os usuários podem atualizar sua imagem de confiança para Xenial usando o comando do-Release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1176">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="eebc2-1177">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="eebc2-1177">Known Issue</span></span>
<span data-ttu-id="eebc2-1178">WSL está enfrentando um problema com algumas implementações de soquete.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1178">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="eebc2-1179">A verificação de bugs se manifesta como uma falha com o erro "tentativa de execução de noexecute MEMORY".</span><span class="sxs-lookup"><span data-stu-id="eebc2-1179">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="eebc2-1180">A manifestação mais comum desse problema é uma falha ao usar SSH.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1180">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="eebc2-1181">A causa raiz é corrigida em compilações internas e será enviada por push para pessoas da primeira oportunidade.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1181">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="eebc2-1182">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1182">Fixed</span></span>

- <span data-ttu-id="eebc2-1183">Implementada a chamada do sistema chroot</span><span class="sxs-lookup"><span data-stu-id="eebc2-1183">Implemented the chroot system call</span></span>
- <span data-ttu-id="eebc2-1184">Melhorias no INotifyPropertyChanged, ~~incluindo suporte para notificações geradas de aplicativos do Windows no DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="eebc2-1184">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="eebc2-1185">Correção O suporte do INotifyPropertyChanged para alterações provenientes de aplicativos do Windows não estão disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1185">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="eebc2-1186">Associação de soquete a IPv6:<port n> : agora dá suporte a IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1186">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="eebc2-1187">Comportamento de WNOWAIT para waitid systemcall implementado (GH #638)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1187">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="eebc2-1188">Suporte para opções de soquete de IP IP_HDRINCL e IP_TTL</span><span class="sxs-lookup"><span data-stu-id="eebc2-1188">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="eebc2-1189">Leitura de comprimento zero () deve retornar imediatamente (GH #975)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1189">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="eebc2-1190">Manipule corretamente nomes de arquivos e prefixos de nome de arquivo que não incluem um terminador nulo em um arquivo. tar.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1190">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="eebc2-1191">suporte do epoll para/dev/null</span><span class="sxs-lookup"><span data-stu-id="eebc2-1191">epoll support for /dev/null</span></span>
- <span data-ttu-id="eebc2-1192">Corrigir a origem do tempo de/dev/Alarm</span><span class="sxs-lookup"><span data-stu-id="eebc2-1192">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="eebc2-1193">Bash-c agora é capaz de redirecionar para um arquivo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1193">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="eebc2-1194">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1194">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1195">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1195">LTP Results:</span></span>
<span data-ttu-id="eebc2-1196">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="eebc2-1196">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="eebc2-1197">Número de não aprovados (com falha, ignorado, etc...): 264</span><span class="sxs-lookup"><span data-stu-id="eebc2-1197">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="eebc2-1198">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1198">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1199">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1199">Syscall Support</span></span>
<span data-ttu-id="eebc2-1200">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1200">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1201">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1201">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="eebc2-1202">Build 14931</span><span class="sxs-lookup"><span data-stu-id="eebc2-1202">Build 14931</span></span>

<span data-ttu-id="eebc2-1203">Para obter informações gerais do Windows sobre o Build 14931 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1203">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1204">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1204">Fixed</span></span>

 - <span data-ttu-id="eebc2-1205">Devido a circunstâncias além do nosso controle, não há atualizações nessa compilação para o subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1205">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="eebc2-1206">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1206">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="eebc2-1207">Build 14926</span><span class="sxs-lookup"><span data-stu-id="eebc2-1207">Build 14926</span></span>

<span data-ttu-id="eebc2-1208">Para obter informações gerais do Windows sobre o Build 14926 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1208">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1209">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1209">Fixed</span></span>

- <span data-ttu-id="eebc2-1210">O ping agora funciona em consoles que não têm privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="eebc2-1210">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="eebc2-1211">O Ping6 agora tem suporte, também sem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="eebc2-1211">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="eebc2-1212">Suporte a INotifyPropertyChanged para arquivos modificados por meio de WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1212">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="eebc2-1213">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1213">(GH #216)</span></span>
  - <span data-ttu-id="eebc2-1214">Sinalizadores com suporte:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1214">Flags supported:</span></span>
    - <span data-ttu-id="eebc2-1215">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="eebc2-1215">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="eebc2-1216">eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="eebc2-1216">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="eebc2-1217">atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="eebc2-1217">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="eebc2-1218">ler saída: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="eebc2-1218">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="eebc2-1219">Problema conhecido: Modificar arquivos de aplicativos do Windows não gera eventos</span><span class="sxs-lookup"><span data-stu-id="eebc2-1219">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="eebc2-1220">O soquete UNIX agora dá suporte a SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="eebc2-1220">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="eebc2-1221">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="eebc2-1221">LTP Results:</span></span>
<span data-ttu-id="eebc2-1222">Número de testes aprovados: 651</span><span class="sxs-lookup"><span data-stu-id="eebc2-1222">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="eebc2-1223">Número de não aprovados (com falha, ignorado, etc...): 258</span><span class="sxs-lookup"><span data-stu-id="eebc2-1223">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="eebc2-1224">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="eebc2-1224">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="eebc2-1225">Build 14915</span><span class="sxs-lookup"><span data-stu-id="eebc2-1225">Build 14915</span></span>

<span data-ttu-id="eebc2-1226">Para obter informações gerais do Windows sobre o Build 14915 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1226">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1227">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1227">Fixed</span></span>
-  <span data-ttu-id="eebc2-1228">Socketpair para soquetes de datagramas UNIX (GH #262)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1228">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="eebc2-1229">Suporte a soquetes UNIX para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="eebc2-1229">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="eebc2-1230">Suporte a soquetes UNIX para SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1230">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="eebc2-1231">Suporte a soquetes UNIX para SOCK_SEQPACKET (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1231">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="eebc2-1232">Adição de suporte para envio, recebimento e desligamento de soquete de datagrama UNIX</span><span class="sxs-lookup"><span data-stu-id="eebc2-1232">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="eebc2-1233">Correção de verificação devido à validação de parâmetro mmap inválida para endereços não fixos.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1233">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="eebc2-1234">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1234">(GH #847)</span></span>
- <span data-ttu-id="eebc2-1235">Suporte para Suspensão/retomada de Estados de terminal</span><span class="sxs-lookup"><span data-stu-id="eebc2-1235">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="eebc2-1236">Suporte para TIOCPKT IOCTL para desbloquear o utilitário de tela (GH #774)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1236">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="eebc2-1237">Problema conhecido: Teclas de função não operacionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1237">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="eebc2-1238">Correção de uma corrida em TimerFd que poderia fazer com que um membro livre ' ReaderReady ' fosse acessado pelo LxpTimerFdWorkerRoutine (GH #814)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1238">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="eebc2-1239">Habilitar suporte à chamada do sistema reiniciável para Futex, pesquisa e clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="eebc2-1239">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="eebc2-1240">Adicionado suporte à montagem de associação</span><span class="sxs-lookup"><span data-stu-id="eebc2-1240">Added bind mount support</span></span>
- <span data-ttu-id="eebc2-1241">descompartilhar para suporte de namespace de montagem</span><span class="sxs-lookup"><span data-stu-id="eebc2-1241">unshare for mount namespace support</span></span>
    - <span data-ttu-id="eebc2-1242">Problema conhecido: Ao criar um novo namespace de montagem `unshare(CLONE_NEWNS)` com o diretório de trabalho atual, ele continuará a apontar para o namespace antigo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1242">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="eebc2-1243">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1243">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="eebc2-1244">Build 14905</span><span class="sxs-lookup"><span data-stu-id="eebc2-1244">Build 14905</span></span>

<span data-ttu-id="eebc2-1245">Para obter informações gerais do Windows sobre o Build 14905 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1245">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1246">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1246">Fixed</span></span>
- <span data-ttu-id="eebc2-1247">Agora há suporte para chamadas reiniciáveis do sistema (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1247">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="eebc2-1248">Symlinks para diretórios que terminam em/agora operacional (GH #650)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1248">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="eebc2-1249">RNDGETENTCNT IOCTL implementado para/dev/random</span><span class="sxs-lookup"><span data-stu-id="eebc2-1249">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="eebc2-1250">Implementou os arquivos/proc/[pid]/mounts,/proc/[pid]/mountinfo e/proc/[pid]/mountstats</span><span class="sxs-lookup"><span data-stu-id="eebc2-1250">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="eebc2-1251">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1251">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="eebc2-1252">Build 14901</span><span class="sxs-lookup"><span data-stu-id="eebc2-1252">Build 14901</span></span>
<span data-ttu-id="eebc2-1253">Primeira compilação do insider Build para a versão de atualização de aniversário do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1253">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="eebc2-1254">Para obter informações gerais do Windows sobre o Build 14901 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1254">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1255">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1255">Fixed</span></span>
- <span data-ttu-id="eebc2-1256">Problema de barra à direita fixa</span><span class="sxs-lookup"><span data-stu-id="eebc2-1256">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="eebc2-1257">Comandos como `$ mv a/c/ a/b/` agora funcionam</span><span class="sxs-lookup"><span data-stu-id="eebc2-1257">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="eebc2-1258">Instalar agora solicita se a localidade do Ubuntu deve ser definida como localidade do Windows</span><span class="sxs-lookup"><span data-stu-id="eebc2-1258">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="eebc2-1259">Suporte do procfs para a pasta NS</span><span class="sxs-lookup"><span data-stu-id="eebc2-1259">Procfs support for ns folder</span></span>
- <span data-ttu-id="eebc2-1260">Adição de montagem e desmontagem para sistemas de arquivos tmpfs, procfs e sysfs</span><span class="sxs-lookup"><span data-stu-id="eebc2-1260">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="eebc2-1261">Corrigir mknod [at] assinatura da ABI de 32 bits</span><span class="sxs-lookup"><span data-stu-id="eebc2-1261">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="eebc2-1262">Soquetes UNIX movidos para o modelo de expedição</span><span class="sxs-lookup"><span data-stu-id="eebc2-1262">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="eebc2-1263">O tamanho do buffer de recebimento de soquete INET usando o setsockopt deve ser respeitado</span><span class="sxs-lookup"><span data-stu-id="eebc2-1263">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="eebc2-1264">Implementar sinalizador de mensagem de recebimento de soquete do UNIX MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="eebc2-1264">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="eebc2-1265">Processo Linux de redirecionamento de pipe STDIN/STDOUT (GH #2)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1265">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="eebc2-1266">Permite a tubulação de comandos bash-c no CMD.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1266">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="eebc2-1267">Exemplo: > dir | bash-c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="eebc2-1267">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="eebc2-1268">O bash agora pode ser instalado em sistemas com vários Pagefiles (GH #538, #358)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1268">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="eebc2-1269">O tamanho do buffer do soquete INET padrão deve corresponder ao da configuração padrão do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="eebc2-1269">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="eebc2-1270">Alinhar xattr syscalls ao listxattr</span><span class="sxs-lookup"><span data-stu-id="eebc2-1270">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="eebc2-1271">Retornar apenas interfaces com um endereço IPv4 válido de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="eebc2-1271">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="eebc2-1272">Corrigir a ação padrão de sinal quando injetada por ptrace</span><span class="sxs-lookup"><span data-stu-id="eebc2-1272">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="eebc2-1273">implementar/proc/sys/VM/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="eebc2-1273">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="eebc2-1274">Use os valores de registro de contexto do computador ao restaurar o contexto em sigreturn</span><span class="sxs-lookup"><span data-stu-id="eebc2-1274">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="eebc2-1275">Isso resolve o problema em que o Java e o javac estavam suspensos para alguns usuários</span><span class="sxs-lookup"><span data-stu-id="eebc2-1275">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="eebc2-1276">Implementar/proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="eebc2-1276">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1277">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1277">Syscall Support</span></span>
<span data-ttu-id="eebc2-1278">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1278">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1279">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1279">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="eebc2-1280">Compilar 14388 para atualização de aniversário do Windows 10</span><span class="sxs-lookup"><span data-stu-id="eebc2-1280">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="eebc2-1281">Para obter informações gerais do Windows sobre o Build 14388 visite o [blog do Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1281">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="eebc2-1282">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1282">Fixed</span></span>
- <span data-ttu-id="eebc2-1283">Correções para se preparar para a atualização de aniversário do Windows 10 em 8/2</span><span class="sxs-lookup"><span data-stu-id="eebc2-1283">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="eebc2-1284">Mais informações sobre WSL na atualização de aniversário podem ser encontradas em nosso [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1284">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="eebc2-1285">Build 14376</span><span class="sxs-lookup"><span data-stu-id="eebc2-1285">Build 14376</span></span>
<span data-ttu-id="eebc2-1286">Para obter informações gerais do Windows sobre o Build 14376 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1286">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="eebc2-1287">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1287">Fixed</span></span>
- <span data-ttu-id="eebc2-1288">Removidas algumas instâncias em que apt-get paralisa (GH #493)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1288">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="eebc2-1289">Corrigido um problema em que as montagens vazias não foram manipuladas corretamente</span><span class="sxs-lookup"><span data-stu-id="eebc2-1289">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="eebc2-1290">Corrigido um problema em que os ramdisks não foram montados corretamente</span><span class="sxs-lookup"><span data-stu-id="eebc2-1290">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="eebc2-1291">Alterar a aceitação de soquete do UNIX para os sinalizadores de suporte (GH parcial #451)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1291">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="eebc2-1292">Correção de bluescreen relacionado à rede comum</span><span class="sxs-lookup"><span data-stu-id="eebc2-1292">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="eebc2-1293">Bluescreen corrigido ao acessar/proc/[pid]/Task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1293">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="eebc2-1294">Correção da utilização alta da CPU para alguns cenários de PTY (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1294">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="eebc2-1295">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1295">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="eebc2-1296">Build 14371</span><span class="sxs-lookup"><span data-stu-id="eebc2-1296">Build 14371</span></span>
<span data-ttu-id="eebc2-1297">Para obter informações gerais do Windows sobre o Build 14371 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1297">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="eebc2-1298">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1298">Fixed</span></span>
- <span data-ttu-id="eebc2-1299">Correção da corrida de tempo com SIGCHLD e Wait () ao usar ptrace</span><span class="sxs-lookup"><span data-stu-id="eebc2-1299">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="eebc2-1300">Corrigido algum comportamento quando os caminhos têm um #432 (GH) à direita</span><span class="sxs-lookup"><span data-stu-id="eebc2-1300">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="eebc2-1301">Corrigido o problema com a falha de renomeação/desvinculação devido a identificadores abertos para filhos</span><span class="sxs-lookup"><span data-stu-id="eebc2-1301">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="eebc2-1302">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1302">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="eebc2-1303">Build 14366</span><span class="sxs-lookup"><span data-stu-id="eebc2-1303">Build 14366</span></span>
<span data-ttu-id="eebc2-1304">Para obter informações gerais do Windows sobre o Build 14366 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1304">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="eebc2-1305">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1305">Fixed</span></span>
- <span data-ttu-id="eebc2-1306">Correção na criação de arquivo por meio de symlinks</span><span class="sxs-lookup"><span data-stu-id="eebc2-1306">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="eebc2-1307">Adicionado listxattr para Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1307">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="eebc2-1308">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1308">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1309">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1309">Syscall Support</span></span>
-   <span data-ttu-id="eebc2-1310">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1310">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1311">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1311">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="eebc2-1312">Build 14361</span><span class="sxs-lookup"><span data-stu-id="eebc2-1312">Build 14361</span></span>
<span data-ttu-id="eebc2-1313">Para obter informações gerais do Windows sobre o Build 14361 visite o [blog do Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1313">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="eebc2-1314">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1314">Fixed</span></span>
- <span data-ttu-id="eebc2-1315">O DrvFs agora diferencia maiúsculas de minúsculas quando executado no bash no Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1315">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="eebc2-1316">Os usuários podem Case. txt e maiúsculas e minúsculas. TXT em suas unidades/mnt/c</span><span class="sxs-lookup"><span data-stu-id="eebc2-1316">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="eebc2-1317">A diferenciação de maiúsculas e minúsculas só tem suporte no bash no Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1317">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="eebc2-1318">Quando fora do bash, o NTFS relatará os arquivos corretamente, mas o comportamento inesperado poderá ocorrer interagindo com os arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1318">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="eebc2-1319">A raiz de cada volume (ou seja,/mnt/c) não diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="eebc2-1319">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="eebc2-1320">Mais informações sobre como lidar com esses arquivos no Windows podem ser encontradas [aqui](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1320">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="eebc2-1321">Suporte de PTY/TTY muito aprimorado.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1321">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="eebc2-1322">Aplicativos como TMUX agora com suporte (GH #40)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1322">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="eebc2-1323">Problema de instalação corrigido em que as contas de usuário não são sempre criadas</span><span class="sxs-lookup"><span data-stu-id="eebc2-1323">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="eebc2-1324">Estrutura de ARG de linha de comando otimizada que permite a lista de argumentos extremamente longo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1324">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="eebc2-1325">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1325">(GH #153)</span></span>
- <span data-ttu-id="eebc2-1326">Agora é possível excluir e alread_onlyr arquivos do DrvFs</span><span class="sxs-lookup"><span data-stu-id="eebc2-1326">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="eebc2-1327">Correção de algumas instâncias em que o terminal trava na desconexão (GH #43)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1327">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="eebc2-1328">o chmod e o proprietário agora funcionam em dispositivos tty</span><span class="sxs-lookup"><span data-stu-id="eebc2-1328">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="eebc2-1329">Permitir conexão a 0.0.0.0 e:: as localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1329">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="eebc2-1330">Sendmsg/recvmsg agora lida com um comprimento de vetor de e/s de > 1 (Partial GH #376)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1330">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="eebc2-1331">Os usuários agora podem recusar o arquivo de hosts gerados automaticamente (GH #398)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1331">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="eebc2-1332">Corresponder automaticamente a localidade do Linux à localidade do NT durante a instalação (GH #11)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1332">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="eebc2-1333">Adicionado o arquivo/proc/sys/VM/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1333">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="eebc2-1334">strace agora é encerrado corretamente</span><span class="sxs-lookup"><span data-stu-id="eebc2-1334">strace now exits correctly</span></span>
- <span data-ttu-id="eebc2-1335">Permitir que os pipes sejam reabertos por meio de/proc/Self/FD (GH #222)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1335">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="eebc2-1336">Ocultar diretórios em%LOCALAPPDATA%\lxss de DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1336">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="eebc2-1337">Melhor manipulação do bash. exe ~.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1337">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="eebc2-1338">Comandos como "bash ~-c ls" agora têm suporte (GH #467)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1338">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="eebc2-1339">Os soquetes agora notificam epoll leitura disponíveis durante o desligamento (GH #271)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1339">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="eebc2-1340">lxrun/Uninstall realiza um trabalho melhor de exclusão dos arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="eebc2-1340">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="eebc2-1341">PS-f corrigida (GH #246)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1341">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="eebc2-1342">Suporte aprimorado para aplicativos X11, como xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1342">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="eebc2-1343">Tamanho da pilha de thread inicial atualizado para corresponder à configuração padrão do Ubuntu e relatando o tamanho corretamente para o syscall get_rlimit (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1343">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="eebc2-1344">Relatório aprimorado de nomes de imagem de processo RsFilter (por exemplo, para auditoria)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1344">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="eebc2-1345">Implementado o/proc/mountinfo para o comando df</span><span class="sxs-lookup"><span data-stu-id="eebc2-1345">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="eebc2-1346">O código de erro symlink foi corrigido para o nome filho.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1346">Fixed symlink error code for child name .</span></span> <span data-ttu-id="eebc2-1347">e..</span><span class="sxs-lookup"><span data-stu-id="eebc2-1347">and ..</span></span>
- <span data-ttu-id="eebc2-1348">Aprimoramentos bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1348">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1349">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1349">Syscall Support</span></span>
<span data-ttu-id="eebc2-1350">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1351">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="eebc2-1352">Build 14352</span><span class="sxs-lookup"><span data-stu-id="eebc2-1352">Build 14352</span></span>
<span data-ttu-id="eebc2-1353">Para obter informações gerais do Windows sobre o Build 14352 visite o [blog do Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1353">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1354">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1354">Fixed</span></span>
- <span data-ttu-id="eebc2-1355">Correção do problema em que arquivos grandes não foram baixados/criados corretamente.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1355">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="eebc2-1356">Isso deve desbloquear NPM e outros cenários (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1356">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="eebc2-1357">Removeu algumas instâncias em que os soquetes travam</span><span class="sxs-lookup"><span data-stu-id="eebc2-1357">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="eebc2-1358">Correção de alguns erros de ptrace</span><span class="sxs-lookup"><span data-stu-id="eebc2-1358">Corrected some ptrace errors</span></span>
- <span data-ttu-id="eebc2-1359">Correção do problema com o WSL, permitindo que os nomes de um ou mais de 255 caracteres</span><span class="sxs-lookup"><span data-stu-id="eebc2-1359">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="eebc2-1360">Suporte aprimorado para caracteres que não são do inglês</span><span class="sxs-lookup"><span data-stu-id="eebc2-1360">Improved support for non-English characters</span></span>
- <span data-ttu-id="eebc2-1361">Adicionar dados atuais de fuso horário do Windows e definir como padrão</span><span class="sxs-lookup"><span data-stu-id="eebc2-1361">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="eebc2-1362">ID de dispositivo exclusivo para cada ponto de montagem (correção do JRE – GH #49)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1362">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="eebc2-1363">Correção do problema com caminhos que contêm "."</span><span class="sxs-lookup"><span data-stu-id="eebc2-1363">Correct issue with paths containing “.”</span></span> <span data-ttu-id="eebc2-1364">e ".."</span><span class="sxs-lookup"><span data-stu-id="eebc2-1364">and “..”</span></span>
- <span data-ttu-id="eebc2-1365">Suporte a FIFO adicionado (GH #71)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1365">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="eebc2-1366">Formato atualizado de reresolvible. conf para corresponder ao formato nativo do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="eebc2-1366">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="eebc2-1367">Algumas procfs limpeza</span><span class="sxs-lookup"><span data-stu-id="eebc2-1367">Some procfs cleanup</span></span>
- <span data-ttu-id="eebc2-1368">Ping habilitado para consoles do administrador (GH #18)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1368">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1369">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1369">Syscall Support</span></span>
<span data-ttu-id="eebc2-1370">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1370">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1371">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1371">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="eebc2-1372">Build 14342</span><span class="sxs-lookup"><span data-stu-id="eebc2-1372">Build 14342</span></span>
<span data-ttu-id="eebc2-1373">Para obter informações gerais do Windows sobre o Build 14342, o [blog do Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1373">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="eebc2-1374">Informações sobre VolFs e DriveFs podem ser encontradas no [blog do WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1374">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="eebc2-1375">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1375">Fixed</span></span>
- <span data-ttu-id="eebc2-1376">Corrigido o problema de instalação quando o usuário do Windows tinha caracteres Unicode no nome de usuário</span><span class="sxs-lookup"><span data-stu-id="eebc2-1376">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="eebc2-1377">A solução apt-get update udev nas perguntas frequentes agora é fornecida por padrão na primeira execução</span><span class="sxs-lookup"><span data-stu-id="eebc2-1377">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="eebc2-1378">Symlinks habilitados nos diretórios do<drive>DriveFs (/MNT/)</span><span class="sxs-lookup"><span data-stu-id="eebc2-1378">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="eebc2-1379">Symlinks agora funciona entre DriveFs e VolFs</span><span class="sxs-lookup"><span data-stu-id="eebc2-1379">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="eebc2-1380">Problema de análise de caminho de nível superior resolvido: ls.//agora funcionará como esperado</span><span class="sxs-lookup"><span data-stu-id="eebc2-1380">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="eebc2-1381">NPM instalar em DriveFs e as opções-g agora estão funcionando</span><span class="sxs-lookup"><span data-stu-id="eebc2-1381">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="eebc2-1382">Problema corrigido ao impedir que o servidor PHP seja iniciado</span><span class="sxs-lookup"><span data-stu-id="eebc2-1382">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="eebc2-1383">Valores de ambiente padrão atualizados, como $PATH para combinar mais de perto o Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1383">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="eebc2-1384">Adicionada uma tarefa de manutenção semanal no Windows para atualizar o cache do pacote apt</span><span class="sxs-lookup"><span data-stu-id="eebc2-1384">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="eebc2-1385">Correção do problema com a validação de cabeçalho ELF, WSL agora dá suporte a todas as opções de Melkor</span><span class="sxs-lookup"><span data-stu-id="eebc2-1385">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="eebc2-1386">O Shell do zsh é funcional</span><span class="sxs-lookup"><span data-stu-id="eebc2-1386">Zsh shell is functional</span></span>
- <span data-ttu-id="eebc2-1387">Binários go pré-compilados agora têm suporte</span><span class="sxs-lookup"><span data-stu-id="eebc2-1387">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="eebc2-1388">A solicitação na primeira execução do bash. exe agora está localizada corretamente</span><span class="sxs-lookup"><span data-stu-id="eebc2-1388">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="eebc2-1389">/proc/meminfo agora retorna informações corretas</span><span class="sxs-lookup"><span data-stu-id="eebc2-1389">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="eebc2-1390">Os soquetes agora têm suporte no VFS</span><span class="sxs-lookup"><span data-stu-id="eebc2-1390">Sockets now supported in VFS</span></span>
- <span data-ttu-id="eebc2-1391">/dev agora montado como tempfs</span><span class="sxs-lookup"><span data-stu-id="eebc2-1391">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="eebc2-1392">FIFO agora com suporte</span><span class="sxs-lookup"><span data-stu-id="eebc2-1392">Fifo now supported</span></span>
- <span data-ttu-id="eebc2-1393">Sistemas de vários núcleos agora mostrados corretamente em/proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1393">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="eebc2-1394">Aprimoramentos adicionais e mensagens de erro baixando durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="eebc2-1394">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="eebc2-1395">Melhorias de syscall e bugs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1395">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="eebc2-1396">Lista syscall com suporte abaixo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1396">Supported syscall list below.</span></span>
- <span data-ttu-id="eebc2-1397">Bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1397">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="eebc2-1398">Problemas Conhecidos</span><span class="sxs-lookup"><span data-stu-id="eebc2-1398">Known Issues</span></span>
- <span data-ttu-id="eebc2-1399">Não resolvendo '.. '</span><span class="sxs-lookup"><span data-stu-id="eebc2-1399">Not resolving ‘..’</span></span> <span data-ttu-id="eebc2-1400">corretamente no DriveFs em alguns casos</span><span class="sxs-lookup"><span data-stu-id="eebc2-1400">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1401">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1401">Syscall Support</span></span>
<span data-ttu-id="eebc2-1402">Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1402">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1403">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1403">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="eebc2-1404">Build 14332</span><span class="sxs-lookup"><span data-stu-id="eebc2-1404">Build 14332</span></span>

<span data-ttu-id="eebc2-1405">Para obter informações gerais do Windows sobre o Build 14332 visite o [blog do Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1405">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="eebc2-1406">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1406">Fixed</span></span>
- <span data-ttu-id="eebc2-1407">Melhor resolução. conf, incluindo a priorização de entradas DNS</span><span class="sxs-lookup"><span data-stu-id="eebc2-1407">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="eebc2-1408">Problema com a movimentação de arquivos e diretórios entre unidades/mnt e não/mnt</span><span class="sxs-lookup"><span data-stu-id="eebc2-1408">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="eebc2-1409">Agora, os arquivos tar podem ser criados com symlinks</span><span class="sxs-lookup"><span data-stu-id="eebc2-1409">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="eebc2-1410">Diretório/Run/Lock padrão adicionado na criação da instância</span><span class="sxs-lookup"><span data-stu-id="eebc2-1410">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="eebc2-1411">Atualizar/dev/null para retornar informações de estado adequadas</span><span class="sxs-lookup"><span data-stu-id="eebc2-1411">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="eebc2-1412">Erros adicionais ao baixar durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="eebc2-1412">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="eebc2-1413">Melhorias de syscall e bugs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1413">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="eebc2-1414">Lista syscall com suporte abaixo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1414">Supported syscall list below.</span></span>
- <span data-ttu-id="eebc2-1415">Aprimoramentos bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1415">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1416">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1416">Syscall Support</span></span>
<span data-ttu-id="eebc2-1417">Abaixo está a nova syscall que tem alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1417">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="eebc2-1418">O syscall nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1418">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="eebc2-1419">Build 14328</span><span class="sxs-lookup"><span data-stu-id="eebc2-1419">Build 14328</span></span>

<span data-ttu-id="eebc2-1420">Para obter informações gerais do Windows sobre o Build 14332 visite o [blog do Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1420">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="eebc2-1421">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="eebc2-1421">New Features</span></span>
* <span data-ttu-id="eebc2-1422">Agora dê suporte a usuários do Linux.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1422">Now support Linux users.</span></span>  <span data-ttu-id="eebc2-1423">A instalação do bash no Ubuntu no Windows solicitará a criação de um usuário do Linux.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1423">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="eebc2-1424">Para obter mais informações, visite https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="eebc2-1424">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="eebc2-1425">Hostname agora está definido como o nome do computador Windows, não há mais@localhost</span><span class="sxs-lookup"><span data-stu-id="eebc2-1425">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="eebc2-1426">Para obter mais informações sobre a compilação 14328, visite: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="eebc2-1426">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="eebc2-1427">Fixo</span><span class="sxs-lookup"><span data-stu-id="eebc2-1427">Fixed</span></span>
* <span data-ttu-id="eebc2-1428">Aprimoramentos do symlink para<drive> arquivos não/mnt/</span><span class="sxs-lookup"><span data-stu-id="eebc2-1428">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="eebc2-1429">NPM instalar agora funciona</span><span class="sxs-lookup"><span data-stu-id="eebc2-1429">npm install now works</span></span>
    * <span data-ttu-id="eebc2-1430">Agora, o JDK/JRE é instalável usando as instruções encontradas [aqui](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="eebc2-1430">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="eebc2-1431">problema conhecido: o symlinks não funciona para montagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1431">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="eebc2-1432">A funcionalidade estará disponível em uma compilação posterior</span><span class="sxs-lookup"><span data-stu-id="eebc2-1432">Functionality will be available in a later build</span></span>
* <span data-ttu-id="eebc2-1433">Top e htop agora são exibidos</span><span class="sxs-lookup"><span data-stu-id="eebc2-1433">top and htop now display</span></span>
* <span data-ttu-id="eebc2-1434">Mensagens de erro adicionais para algumas falhas de instalação</span><span class="sxs-lookup"><span data-stu-id="eebc2-1434">Additional error messages for some install failures</span></span>
* <span data-ttu-id="eebc2-1435">Melhorias de syscall e bugs.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1435">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="eebc2-1436">Lista syscall com suporte abaixo.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1436">Supported syscall list below.</span></span>
* <span data-ttu-id="eebc2-1437">Aprimoramentos bugs e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="eebc2-1437">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="eebc2-1438">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="eebc2-1438">Syscall Support</span></span>
<span data-ttu-id="eebc2-1439">Abaixo está uma lista de syscalls que têm alguma implementação em WSL.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1439">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="eebc2-1440">O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eebc2-1440">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
