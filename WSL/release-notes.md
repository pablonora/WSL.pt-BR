---
title: Notas sobre a versão do subsistema Windows para Linux
description: Notas sobre a versão do subsistema Windows para Linux.  Atualizado semanalmente.
keywords: notas sobre a versão, wsl, windows, subsistema do windows para linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 3df4d4b4e0c542a3e87306c01a14b7073eb5e677
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235942"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="0374c-105">Notas sobre a versão do subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="0374c-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-19555"></a><span data-ttu-id="0374c-106">Build 19555</span><span class="sxs-lookup"><span data-stu-id="0374c-106">Build 19555</span></span>
<span data-ttu-id="0374c-107">Para obter informações gerais do Windows sobre o build 19555, acesse o [blog do Windows](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span><span class="sxs-lookup"><span data-stu-id="0374c-107">For general Windows information on build 19555 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span></span>

* <span data-ttu-id="0374c-108">[WSL2] Use um cgroup de memória para limitar a quantidade de memória usada pelas operações de instalação e conversão [GH 4669]</span><span class="sxs-lookup"><span data-stu-id="0374c-108">[WSL2] Use a memory cgroup to limit the amount of memory used by install and conversion operations [GH 4669]</span></span>
* <span data-ttu-id="0374c-109">Torne o wsl.exe presente quando o componente opcional do Subsistema do Windows para Linux não estiver habilitado para aprimorar a descoberta de recursos.</span><span class="sxs-lookup"><span data-stu-id="0374c-109">Make wsl.exe present when the Windows Subsystem for Linux optional component is not enabled to improve feature discoverability.</span></span>
* <span data-ttu-id="0374c-110">Altere o wsl.exe para imprimir o texto de ajuda se o componente opcional do WSL não estiver instalado</span><span class="sxs-lookup"><span data-stu-id="0374c-110">Change wsl.exe to print help text if the WSL optional component is not installed</span></span>
* <span data-ttu-id="0374c-111">Corrija a condição de corrida ao criar instâncias</span><span class="sxs-lookup"><span data-stu-id="0374c-111">Fix race condition when creating instances</span></span>
* <span data-ttu-id="0374c-112">Crie wslclient.dll que contém todas as funcionalidades de linha de comando</span><span class="sxs-lookup"><span data-stu-id="0374c-112">Create wslclient.dll that contains all command line functionality</span></span>
* <span data-ttu-id="0374c-113">Impeça falhas durante a interrupção do serviço LxssManagerUser</span><span class="sxs-lookup"><span data-stu-id="0374c-113">Prevent crash during LxssManagerUser service stop</span></span>
* <span data-ttu-id="0374c-114">Corrija a falha rápida wslapi.dll quando o parâmetro distroName for NULL</span><span class="sxs-lookup"><span data-stu-id="0374c-114">Fix wslapi.dll fast fail when distroName parameter is NULL</span></span>

## <a name="build-19041"></a><span data-ttu-id="0374c-115">Build 19041</span><span class="sxs-lookup"><span data-stu-id="0374c-115">Build 19041</span></span>
<span data-ttu-id="0374c-116">Para obter informações gerais do Windows sobre o build 19041, acesse o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span><span class="sxs-lookup"><span data-stu-id="0374c-116">For general Windows information on build 19041 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span></span>

* <span data-ttu-id="0374c-117">[WSL2] Limpe a máscara de sinal antes de iniciar os processos</span><span class="sxs-lookup"><span data-stu-id="0374c-117">[WSL2] Clear the signal mask before launching the processes</span></span>
* <span data-ttu-id="0374c-118">[WSL2] Atualize o kernel do Linux para 4.19.84</span><span class="sxs-lookup"><span data-stu-id="0374c-118">[WSL2] Update Linux kernel to 4.19.84</span></span>
* <span data-ttu-id="0374c-119">Manipule a criação do symlink /etc/resolv.conf quando o symlink não for relativo</span><span class="sxs-lookup"><span data-stu-id="0374c-119">Handle creation of /etc/resolv.conf symlink when the symlink is non-relative</span></span>

## <a name="build-19028"></a><span data-ttu-id="0374c-120">Build 19028</span><span class="sxs-lookup"><span data-stu-id="0374c-120">Build 19028</span></span>
<span data-ttu-id="0374c-121">Para obter informações gerais do Windows sobre o build 19028, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span><span class="sxs-lookup"><span data-stu-id="0374c-121">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="0374c-122">[WSL2] Atualização do kernel do Linux para 4.19.81</span><span class="sxs-lookup"><span data-stu-id="0374c-122">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="0374c-123">[WSL2] Alteração da permissão padrão de /dev/net/tun para 0666 [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="0374c-123">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="0374c-124">[WSL2] Ajuste da quantidade padrão de memória atribuída à VM do Linux para 80% da memória do host</span><span class="sxs-lookup"><span data-stu-id="0374c-124">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="0374c-125">[WSL2] Correção do servidor de interoperabilidade para lidar com as solicitações usando um tempo limite para que chamadores inválidos não possam interromper o servidor</span><span class="sxs-lookup"><span data-stu-id="0374c-125">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="0374c-126">Build 19018</span><span class="sxs-lookup"><span data-stu-id="0374c-126">Build 19018</span></span>
<span data-ttu-id="0374c-127">Para obter informações gerais do Windows sobre o build 19018, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span><span class="sxs-lookup"><span data-stu-id="0374c-127">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="0374c-128">[WSL2] Uso do cache=mmap como padrão em montagens 9p para corrigir aplicativos dotnet</span><span class="sxs-lookup"><span data-stu-id="0374c-128">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="0374c-129">[WSL2] Correções para retransmissão de localhost [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="0374c-129">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="0374c-130">[WSL2] Introdução de uma montagem tmpfs compartilhada entre distribuições para compartilhar o estado entre elas</span><span class="sxs-lookup"><span data-stu-id="0374c-130">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="0374c-131">Correção da restauração de uma unidade de rede persistente para \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="0374c-131">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="0374c-132">Build 19013</span><span class="sxs-lookup"><span data-stu-id="0374c-132">Build 19013</span></span>
<span data-ttu-id="0374c-133">Para obter informações gerais sobre o Windows no build 19013, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span><span class="sxs-lookup"><span data-stu-id="0374c-133">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="0374c-134">[WSL2] Melhorar o desempenho de memória da VM do utilitário WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-134">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="0374c-135">A memória que não está mais em uso será liberada de volta para o host.</span><span class="sxs-lookup"><span data-stu-id="0374c-135">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="0374c-136">[WSL2] Atualização da versão do kernel para 4.19.79.</span><span class="sxs-lookup"><span data-stu-id="0374c-136">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="0374c-137">(adicione CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK e CONFIG_BRIDGE_VLAN_FILTERING).</span><span class="sxs-lookup"><span data-stu-id="0374c-137">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="0374c-138">[WSL2] Corrija a retransmissão de entrada para lidar com casos em que stdin é um identificador de pipe que não está fechado [GH 4424]</span><span class="sxs-lookup"><span data-stu-id="0374c-138">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="0374c-139">Faça a verificação de \\\\wsl$ case-insensitive.</span><span class="sxs-lookup"><span data-stu-id="0374c-139">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="0374c-140">Build 19002</span><span class="sxs-lookup"><span data-stu-id="0374c-140">Build 19002</span></span>
<span data-ttu-id="0374c-141">Para obter informações gerais do Windows sobre o Build 19002, acesse o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="0374c-141">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="0374c-142">[WSL] Correção de um problema com o tratamento de alguns caracteres Unicode: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="0374c-142">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="0374c-143">[WSL] Correção de casos raros em que distribuições podiam ter o registro cancelado se fossem iniciadas imediatamente após uma atualização de compilação a compilação.</span><span class="sxs-lookup"><span data-stu-id="0374c-143">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="0374c-144">[WSL] Correção de um problema secundário com wsl.exe: desligamentos em que os timers de ociosidade da instância não foram cancelados.</span><span class="sxs-lookup"><span data-stu-id="0374c-144">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="0374c-145">Build 18995</span><span class="sxs-lookup"><span data-stu-id="0374c-145">Build 18995</span></span>
<span data-ttu-id="0374c-146">Para obter informações gerais do Windows sobre o build 18995, acesse o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="0374c-146">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="0374c-147">[WSL2] Correção de um problema em que as montagens DrvFs pararam de funcionar após uma operação ter sido interrompida (por exemplo, ctrl-c) [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="0374c-147">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="0374c-148">[WSL2] Correção do tratamento de mensagens hvsocket muito grandes [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="0374c-148">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="0374c-149">[WSL2] Correção do problema com a interoperabilidade quando stdin é um arquivo [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="0374c-149">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="0374c-150">[WSL2] Correção da falha de serviço quando um estado de rede inesperado é encontrado [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="0374c-150">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="0374c-151">[WSL2] Consulta do nome da distribuição do servidor de interoperabilidade se o processo atual não tem a variável de ambiente</span><span class="sxs-lookup"><span data-stu-id="0374c-151">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="0374c-152">[WSL2] Correção do problema com a interoperabilidade quando stdin é um arquivo</span><span class="sxs-lookup"><span data-stu-id="0374c-152">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="0374c-153">[WSL2] Atualização da versão do kernel do Linux para 4.19.72</span><span class="sxs-lookup"><span data-stu-id="0374c-153">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="0374c-154">[WSL2] Adição da capacidade de especificar outros parâmetros de linha de comando do kernel por meio de .wslconfig</span><span class="sxs-lookup"><span data-stu-id="0374c-154">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="0374c-155">Build 18990</span><span class="sxs-lookup"><span data-stu-id="0374c-155">Build 18990</span></span>
<span data-ttu-id="0374c-156">Para obter informações gerais do Windows sobre o Build 18990, acesse o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="0374c-156">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="0374c-157">Melhora do desempenho das listagens de diretório em \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="0374c-157">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="0374c-158">[WSL2] Injetar entropia de inicialização adicional [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="0374c-158">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="0374c-159">[WSL2] Correção para interoperabilidade do Windows ao usar su/sudo [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="0374c-159">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="0374c-160">Build 18980</span><span class="sxs-lookup"><span data-stu-id="0374c-160">Build 18980</span></span>
<span data-ttu-id="0374c-161">Para obter informações gerais do Windows sobre o Build 18980, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="0374c-161">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="0374c-162">Correção da leitura de symlinks que negam FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="0374c-162">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="0374c-163">Isso inclui todas as symlinks que o Windows cria para compatibilidade com versões anteriores, tais como "C:\Documentos e Configurações" e diversos symlinks no diretório de perfil do usuário</span><span class="sxs-lookup"><span data-stu-id="0374c-163">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="0374c-164">Transformação do estado de sistema de arquivos inesperado em não fatal [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="0374c-164">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="0374c-165">[WSL2] Adição de suporte para arm64 se a CPU/firmware der suporte à virtualização</span><span class="sxs-lookup"><span data-stu-id="0374c-165">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="0374c-166">[WSL2] Permissão para que usuários sem privilégios exibam o log do kernel</span><span class="sxs-lookup"><span data-stu-id="0374c-166">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="0374c-167">[WSL2] Correção da retransmissão de saída quando os soquetes stdout/stderr tiverem sido fechados [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="0374c-167">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="0374c-168">[WSL2] Suporte para passagem de bateria e adaptador AC</span><span class="sxs-lookup"><span data-stu-id="0374c-168">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="0374c-169">[WSL2] Atualização do kernel do Linux para 4.19.67</span><span class="sxs-lookup"><span data-stu-id="0374c-169">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="0374c-170">Adição da capacidade de definir o nome de usuário padrão em /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="0374c-170">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="0374c-171">Build 18975</span><span class="sxs-lookup"><span data-stu-id="0374c-171">Build 18975</span></span>
<span data-ttu-id="0374c-172">Para obter informações gerais do Windows sobre o Build 18975, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="0374c-172">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="0374c-173">[WSL2] Corrigidos diversos problemas de confiabilidade do localhost [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="0374c-173">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="0374c-174">Build 18970</span><span class="sxs-lookup"><span data-stu-id="0374c-174">Build 18970</span></span>
<span data-ttu-id="0374c-175">Para obter informações gerais do Windows sobre o Build 18970, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="0374c-175">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="0374c-176">[WSL2] Sincronização da hora com a hora do host quando o sistema é retomado do estado de suspensão [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="0374c-176">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="0374c-177">[WSL2] Criar symlinks NT nos volumes do Windows quando possível.</span><span class="sxs-lookup"><span data-stu-id="0374c-177">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="0374c-178">[WSL2] Criação de distribuições nos namespaces UTS, IPC, PID e Mount.</span><span class="sxs-lookup"><span data-stu-id="0374c-178">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="0374c-179">[WSL2] Correção da retransmissão de porta localhost quando o servidor se associar ao localhost diretamente [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="0374c-179">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="0374c-180">[WSL2] Correção da interop quando a saída for redirecionada [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="0374c-180">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="0374c-181">[WSL2] Suporte à conversão de symlinks NT absolutos.</span><span class="sxs-lookup"><span data-stu-id="0374c-181">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="0374c-182">[WSL2] Atualização do kernel para 4.19.59</span><span class="sxs-lookup"><span data-stu-id="0374c-182">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="0374c-183">[WSL2] Definição correta da máscara de sub-rede para eth0.</span><span class="sxs-lookup"><span data-stu-id="0374c-183">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="0374c-184">[WSL2] Alteração da lógica para interromper o loop de trabalho do console quando o evento de saída for sinalizado.</span><span class="sxs-lookup"><span data-stu-id="0374c-184">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="0374c-185">[WSL2] Ejeção do vhd da distribuição quando a distribuição não está em execução.</span><span class="sxs-lookup"><span data-stu-id="0374c-185">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="0374c-186">[WSL2] Correção da biblioteca de análise de configuração para manipular corretamente valores vazios.</span><span class="sxs-lookup"><span data-stu-id="0374c-186">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="0374c-187">[WSL2] Dar suporte ao Docker Desktop criando montagens para múltiplas distribuições.</span><span class="sxs-lookup"><span data-stu-id="0374c-187">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="0374c-188">Uma distribuição pode optar por adotar esse comportamento ao adicionar a linha a seguir ao arquivo /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="0374c-188">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="0374c-189">Build 18945</span><span class="sxs-lookup"><span data-stu-id="0374c-189">Build 18945</span></span>
<span data-ttu-id="0374c-190">Para obter informações gerais do Windows sobre o Build 18945, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="0374c-190">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-191">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-191">WSL</span></span>
* <span data-ttu-id="0374c-192">[WSL2] Permissão para que soquetes TCP de escuta em WSL2 sejam acessíveis do host usando localhost:port</span><span class="sxs-lookup"><span data-stu-id="0374c-192">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="0374c-193">[WSL2] Correções para falhas de instalação/conversão e diagnóstico adicional para rastrear problemas futuros [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="0374c-193">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="0374c-194">[WSL2] Melhoria da capacidade de diagnóstico de problemas de rede WSL2</span><span class="sxs-lookup"><span data-stu-id="0374c-194">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="0374c-195">[WSL2] Atualização da versão do kernel para 4.19.55</span><span class="sxs-lookup"><span data-stu-id="0374c-195">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="0374c-196">[WSL2] Atualização do kernel com as opções de configuração necessárias para o Docker [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="0374c-196">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="0374c-197">[WSL2] Aumento do número de CPUs atribuídas à VM do utilitário leve para que seja o mesmo do host (anteriormente limitado em 8 por CONFIG_NR_CPUS na configuração do kernel) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="0374c-197">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="0374c-198">[WSL2] Criação de um arquivo de permuta para a VM leve do WSL2</span><span class="sxs-lookup"><span data-stu-id="0374c-198">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="0374c-199">[WSL2] Permissão para que as montagens de usuário fiquem visíveis por meio de \\\\wsl$\\distro (por exemplo, sshfs) [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="0374c-199">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="0374c-200">[WSL2] Melhoria do desempenho do sistema de arquivos 9p</span><span class="sxs-lookup"><span data-stu-id="0374c-200">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="0374c-201">[WSL2] Garantia de que a ACL do VHD não aumente sem limite [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="0374c-201">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="0374c-202">[WSL2] Atualização da configuração do kernel para dar suporte a squashfs e xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="0374c-202">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="0374c-203">[WSL2] Correção para a opção interop.enabled /etc/wsl.conf [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="0374c-203">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="0374c-204">[WSL2] Retorno de ENOTSUP se o sistema de arquivos não der suporte a EAs</span><span class="sxs-lookup"><span data-stu-id="0374c-204">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="0374c-205">[WSL2] Correção do travamento de CopyFile com \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="0374c-205">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="0374c-206">Alternância do umask padrão para 0022 e adição da configuração filesystem.umask a /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="0374c-206">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="0374c-207">Correção de wslpath para resolver symlinks adequadamente, isso foi regredido em 19h1 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="0374c-207">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="0374c-208">Introdução do arquivo %UserProfile%\\.wslconfig para ajuste de configurações WSL2</span><span class="sxs-lookup"><span data-stu-id="0374c-208">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="0374c-209">Build 18917</span><span class="sxs-lookup"><span data-stu-id="0374c-209">Build 18917</span></span>
<span data-ttu-id="0374c-210">Para obter informações gerais do Windows sobre o Build 18917, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="0374c-210">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-211">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-211">WSL</span></span>
* <span data-ttu-id="0374c-212">O WSL 2 já está disponível.</span><span class="sxs-lookup"><span data-stu-id="0374c-212">WSL 2 is now available!</span></span> <span data-ttu-id="0374c-213">Confira o [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="0374c-213">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="0374c-214">Correção de uma regressão em que a inicialização de processos do Windows via symlinks não funcionou corretamente [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="0374c-214">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="0374c-215">Adição das opções wsl.exe --list --verbose, wsl.exe --list --quiet e wsl.exe --import --version a wsl.exe</span><span class="sxs-lookup"><span data-stu-id="0374c-215">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="0374c-216">Adição da opção wsl.exe --shutdown</span><span class="sxs-lookup"><span data-stu-id="0374c-216">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="0374c-217">Plano 9: Permissão para que a abertura de um diretório para gravação seja realizada com sucesso</span><span class="sxs-lookup"><span data-stu-id="0374c-217">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="0374c-218">Build 18890</span><span class="sxs-lookup"><span data-stu-id="0374c-218">Build 18890</span></span>
<span data-ttu-id="0374c-219">Para obter informações gerais do Windows sobre o Build 18890, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="0374c-219">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-220">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-220">WSL</span></span>
* <span data-ttu-id="0374c-221">Vazamento de soquete sem bloqueio [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="0374c-221">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="0374c-222">A entrada de EOF para o terminal pode bloquear leituras subsequentes [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="0374c-222">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="0374c-223">Atualização do cabeçalho de resolv.conf para fazer referência a wsl.conf [discutido no GH 3928]</span><span class="sxs-lookup"><span data-stu-id="0374c-223">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="0374c-224">Deadlock no código de exclusão de epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="0374c-224">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="0374c-225">Manipulação de espaços em argumentos para --import e –export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="0374c-225">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="0374c-226">A extensão de arquivos mmap não funciona corretamente [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="0374c-226">Extending mmap'd files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="0374c-227">Correção do problema de o acesso ao ARM64 \\\\wsl$ não estar funcionando corretamente</span><span class="sxs-lookup"><span data-stu-id="0374c-227">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="0374c-228">Adição de um ícone padrão melhor para wsl.exe</span><span class="sxs-lookup"><span data-stu-id="0374c-228">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="0374c-229">Build 18342</span><span class="sxs-lookup"><span data-stu-id="0374c-229">Build 18342</span></span>
<span data-ttu-id="0374c-230">Para obter informações gerais do Windows sobre o Build 18342, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="0374c-230">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-231">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-231">WSL</span></span>
* <span data-ttu-id="0374c-232">Adicionamos a capacidade para os usuários acessarem arquivos do Linux em uma distribuição WSL do Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-232">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="0374c-233">Esses arquivos podem ser acessados por meio da linha de comando e aplicativos do Windows (tais como Explorador de Arquivos, VSCode, etc.) também podem interagir com eles.</span><span class="sxs-lookup"><span data-stu-id="0374c-233">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="0374c-234">Acesse seus arquivos navegando até \\\\wsl$\\<nome_da_distro> ou consulte uma lista de distribuições em execução navegando até \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="0374c-234">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="0374c-235">Adição de marcas de informações de CPU adicionais e correção dos valores de Cpus_allowed[_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="0374c-235">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="0374c-236">Suporte a exec de thread não líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="0374c-236">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="0374c-237">Tratamento de falhas de atualização de configuração como não fatais [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="0374c-237">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="0374c-238">Atualização de binfmt para lidar com deslocamentos adequadamente [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="0374c-238">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="0374c-239">Habilitação do mapeamento de unidades de rede para o Plano 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="0374c-239">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="0374c-240">Suporte à conversão de caminhos Windows -> Linux e Linux -> Windows para montagens de associação</span><span class="sxs-lookup"><span data-stu-id="0374c-240">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="0374c-241">Criação de seções somente leitura para mapeamentos em arquivos abertos como somente leitura</span><span class="sxs-lookup"><span data-stu-id="0374c-241">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="0374c-242">Build 18334</span><span class="sxs-lookup"><span data-stu-id="0374c-242">Build 18334</span></span>
<span data-ttu-id="0374c-243">Para obter informações gerais do Windows sobre o Build 18334, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="0374c-243">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-244">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-244">WSL</span></span>
* <span data-ttu-id="0374c-245">Recriação da maneira como o fuso horário do Windows é mapeado para um fuso horário do Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="0374c-245">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="0374c-246">Correção de vazamentos de memória e adição de novas funções de conversão de cadeia de caracteres [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="0374c-246">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="0374c-247">SIGCONT em um grupo de threads sem threads é um não operacional [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="0374c-247">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="0374c-248">Exibição correta dos descritores de arquivo de epoll e de soquete em /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="0374c-248">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="0374c-249">Build 18305</span><span class="sxs-lookup"><span data-stu-id="0374c-249">Build 18305</span></span>
<span data-ttu-id="0374c-250">Para obter informações gerais do Windows sobre o Build 18305, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="0374c-250">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-251">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-251">WSL</span></span>
* <span data-ttu-id="0374c-252">pthreads perdem o acesso a arquivos quando o thread primário sai [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="0374c-252">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="0374c-253">TIOCSCTTY deve ignorar o parâmetro "force", a menos que ele seja necessário [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="0374c-253">TIOCSCTTY should ignore the "force" parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="0374c-254">Melhorias na linha de comando do wsl.exe e adição de funcionalidade de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="0374c-254">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="0374c-255">Build 18277</span><span class="sxs-lookup"><span data-stu-id="0374c-255">Build 18277</span></span>
<span data-ttu-id="0374c-256">Para obter informações gerais do Windows sobre o Build 18277, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="0374c-256">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-257">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-257">WSL</span></span>
* <span data-ttu-id="0374c-258">Correção do erro "essa interface não é compatível" introduzido no build 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="0374c-258">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="0374c-259">O sinalizador MNT_FORCE agora é ignorado para a syscall umount [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="0374c-259">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="0374c-260">Alternância da interop de WSL para usar a API CreatePseudoConsole oficial</span><span class="sxs-lookup"><span data-stu-id="0374c-260">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="0374c-261">Nenhum valor de tempo limite mantido quando FUTEX_WAIT reinicializa</span><span class="sxs-lookup"><span data-stu-id="0374c-261">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="0374c-262">Build 18272</span><span class="sxs-lookup"><span data-stu-id="0374c-262">Build 18272</span></span>
<span data-ttu-id="0374c-263">Para obter informações gerais do Windows sobre o Build 18272, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="0374c-263">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-264">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-264">WSL</span></span>
* <span data-ttu-id="0374c-265">**AVISO:** Há um problema nesse build que torna o WSL inoperante.</span><span class="sxs-lookup"><span data-stu-id="0374c-265">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="0374c-266">Ao tentar iniciar a distribuição, você verá um erro "Não há suporte para essa interface".</span><span class="sxs-lookup"><span data-stu-id="0374c-266">When trying to launch your distribution you will see a "No such interface supported" error.</span></span> <span data-ttu-id="0374c-267">O problema foi corrigido e estará no build do Participante do Programa Windows Insider – Modo Rápido da próxima semana.</span><span class="sxs-lookup"><span data-stu-id="0374c-267">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="0374c-268">Se você tiver instalado esse build, poderá reverter a versão para o build anterior do Windows usando "Voltar para a versão anterior do Windows 10" em Configurações->Atualização e Segurança->Recuperação.</span><span class="sxs-lookup"><span data-stu-id="0374c-268">If you've installed this build you can roll back to the previous Windows build using "Go back to the previous version of Windows 10" in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="0374c-269">Build 18267</span><span class="sxs-lookup"><span data-stu-id="0374c-269">Build 18267</span></span>
<span data-ttu-id="0374c-270">Para obter informações gerais do Windows sobre o Build 18267, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="0374c-270">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-271">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-271">WSL</span></span>
* <span data-ttu-id="0374c-272">Correção do problema em que o processo zumbi pode não ser aproveitado e permanecer indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="0374c-272">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="0374c-273">WslRegisterDistribution trava se a mensagem de erro excede o comprimento máximo [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="0374c-273">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="0374c-274">Permissão para que o fsync tenha sucesso para arquivos somente leitura no DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="0374c-274">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="0374c-275">Verificação de que os diretórios /bin e /sbin existem antes de criar symlinks internos [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="0374c-275">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="0374c-276">Adicionado um mecanismo de tempo limite de encerramento de instância para instâncias de WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-276">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="0374c-277">O tempo limite está definido atualmente como 15 segundos, o que significa que a instância será encerrada 15 segundos após o último processo de WSL sair.</span><span class="sxs-lookup"><span data-stu-id="0374c-277">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="0374c-278">Para encerrar uma distribuição imediatamente, use:</span><span class="sxs-lookup"><span data-stu-id="0374c-278">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="0374c-279">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="0374c-279">Build 17763 (1809)</span></span>
<span data-ttu-id="0374c-280">Para obter informações gerais do Windows sobre o Build 17763, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="0374c-280">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-281">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-281">WSL</span></span>
* <span data-ttu-id="0374c-282">Verificação de permissão da syscall setpriority muito estrita para alterar a mesma prioridade de thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="0374c-282">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="0374c-283">Verificação de que o tempo de interrupção não polarizado é usado para o tempo de inicialização a fim de evitar retornar valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="0374c-283">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="0374c-284">Manipulação de symlinks no interpretador binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="0374c-284">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="0374c-285">Melhor manipulação da limpeza do descritor de arquivo de líder do grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="0374c-285">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="0374c-286">Alternância do WSL para usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter a fim de evitar o estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="0374c-286">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="0374c-287">A anexação ptrace pode causar um valor retornado insatisfatório de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="0374c-287">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="0374c-288">Correção de vários problemas relacionados ao AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="0374c-288">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="0374c-289">Correção do problema que poderá causar falha de interop de WSL se o diretório de trabalho atual tiver menos de 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="0374c-289">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="0374c-290">Impedimento de que um atraso de um segundo cause falhas em conexões de loopback para portas inexistentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="0374c-290">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="0374c-291">Adição do arquivo de stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="0374c-291">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="0374c-292">Informações de escopo de IPV6 mais precisas.</span><span class="sxs-lookup"><span data-stu-id="0374c-292">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="0374c-293">Suporte a PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="0374c-293">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="0374c-294">O sistema de arquivos de pipe limpa inadvertidamente o evento epoll disparado da borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="0374c-294">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="0374c-295">O executável do Win32 iniciado via symlink NTFS não respeita o nome do symlink [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="0374c-295">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="0374c-296">Suporte a zumbis melhorado [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="0374c-296">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="0374c-297">Adição de entradas wsl.conf para controlar o comportamento de interop do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="0374c-297">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="0374c-298">Correção para getsockname nem sempre retornando tipo de família de soquetes UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="0374c-298">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="0374c-299">Adição de suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="0374c-299">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="0374c-300">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="0374c-300">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="0374c-301">Suporte a interop em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="0374c-301">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="0374c-302">Correção do problema de verificação de permissão na pasta raiz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="0374c-302">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="0374c-303">Suporte limitado para os ioctls de teclado TTY KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="0374c-303">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="0374c-304">Os aplicativos da interface do usuário do Windows devem ser executados mesmo quando iniciados em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0374c-304">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="0374c-305">Adição da opção wsl-u ou --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="0374c-305">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="0374c-306">Correção de problemas de inicialização do WSL quando a inicialização rápida estiver habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="0374c-306">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="0374c-307">Os soquetes Unix precisam reter as credenciais de pares desconectados [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="0374c-307">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="0374c-308">Soquetes Unix sem bloqueio falhando indefinidamente com EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="0374c-308">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="0374c-309">case=off é o novo tipo de montagem de drvfs padrão [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="0374c-309">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="0374c-310">Confira [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0374c-310">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="0374c-311">Adição de wslconfig /terminate para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="0374c-311">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="0374c-312">Correção do problema com as entradas do menu de contexto do shell WSL que não manipulam corretamente caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="0374c-312">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="0374c-313">Exposição de diferenciação de maiúsculas e minúsculas por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="0374c-313">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="0374c-314">ARM64: Emulação de operações de manutenção de cache.</span><span class="sxs-lookup"><span data-stu-id="0374c-314">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="0374c-315">Resolução do [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="0374c-315">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="0374c-316">DrvFs: apenas caracteres de escape de saída no intervalo privado que correspondem a um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="0374c-316">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="0374c-317">Correção do erro OB1 (por um) na validação de tamanho do interpretador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="0374c-317">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="0374c-318">Timers absolutos do WSL com um tempo no passado não são disparados [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="0374c-318">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="0374c-319">Verificação de que os pontos de nova análise criados recentemente estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="0374c-319">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="0374c-320">Criação de forma atômica de diretórios que diferenciam maiúsculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="0374c-320">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="0374c-321">Corrigido um problema adicional em que operações multi-threaded poderiam retornar ENOENT mesmo que o arquivo existisse.</span><span class="sxs-lookup"><span data-stu-id="0374c-321">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="0374c-322">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="0374c-322">[GH 2712]</span></span>
* <span data-ttu-id="0374c-323">Correção da falha de inicialização do WSL quando o UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0374c-323">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="0374c-324">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="0374c-324">[GH 3020]</span></span>
* <span data-ttu-id="0374c-325">Adição do menu de contexto do Explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="0374c-325">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="0374c-326">Para usá-lo, mantenha a tecla Shift pressionada e clique com o botão direito do mouse quando estiver em uma janela do Explorer.</span><span class="sxs-lookup"><span data-stu-id="0374c-326">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="0374c-327">Correção do comportamento de não bloqueio de soquete do Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="0374c-327">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="0374c-328">Correção do comando do NetLink suspenso, conforme relatado no GH 2026.</span><span class="sxs-lookup"><span data-stu-id="0374c-328">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="0374c-329">Adição de suporte para os sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="0374c-329">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="0374c-330">Correção do problema com truncamento não causando eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="0374c-330">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="0374c-331">Adição da opção --exec para wsl.exe para invocar um único binário sem um shell.</span><span class="sxs-lookup"><span data-stu-id="0374c-331">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="0374c-332">Adição da opção --distribution a wsl.exe para selecionar uma distribuição específica.</span><span class="sxs-lookup"><span data-stu-id="0374c-332">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="0374c-333">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="0374c-333">Limited support for dmesg.</span></span> <span data-ttu-id="0374c-334">Os aplicativos agora podem fazer logon no dmesg.</span><span class="sxs-lookup"><span data-stu-id="0374c-334">Applications can now log to dmesg.</span></span> <span data-ttu-id="0374c-335">O driver do WSL registra informações limitadas no dmesg.</span><span class="sxs-lookup"><span data-stu-id="0374c-335">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="0374c-336">No futuro, isso pode ser estendido para transportar outras informações/diagnósticos do driver.</span><span class="sxs-lookup"><span data-stu-id="0374c-336">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="0374c-337">Observação: atualmente, o dmesg é compatível por meio da interface do dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="0374c-337">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="0374c-338">A interface syscall `syslog` ainda não é compatível.</span><span class="sxs-lookup"><span data-stu-id="0374c-338">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="0374c-339">Assim sendo, algumas das opções de linha de comando de `dmesg`, tais como `-S` e `-C`, não funcionam.</span><span class="sxs-lookup"><span data-stu-id="0374c-339">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="0374c-340">Alteração do GID e o modo padrão de dispositivos seriais para corresponder ao nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="0374c-340">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="0374c-341">O DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="0374c-341">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="0374c-342">Observação: O DrvFs tem algumas limitações sobre o nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="0374c-342">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="0374c-343">Alguns caracteres (tais como '/', ': ' e '\*') não são permitidos e os nomes de atributos estendidos não diferenciam maiúsculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-343">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="0374c-344">Build 18252 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="0374c-344">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="0374c-345">Para obter informações gerais do Windows sobre o Build 18252, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="0374c-345">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-346">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-346">WSL</span></span>
* <span data-ttu-id="0374c-347">Mover os binários init e bsdtar para fora da dll do lxssmanager e para uma pasta de ferramentas separada</span><span class="sxs-lookup"><span data-stu-id="0374c-347">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="0374c-348">Correção da corrida ao fechar o descritor de arquivo ao usar CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="0374c-348">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="0374c-349">Manipulação de campos opcionais em /proc/pid/mountinfo ao converter caminhos do DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-349">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="0374c-350">Permissão para que o DrvFs mknod tenha êxito sem suporte de metadados para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="0374c-350">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="0374c-351">Os arquivos somente leitura criados no DrvFs devem ter o atributo readonly definido [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="0374c-351">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="0374c-352">Adição do auxiliar /sbin/mount.drvfs para lidar com a montagem do DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-352">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="0374c-353">Uso da renomeação POSIX no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="0374c-353">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="0374c-354">Permissão para a conversão de caminho em volumes sem um GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="0374c-354">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="0374c-355">Build 17738 (rápido)</span><span class="sxs-lookup"><span data-stu-id="0374c-355">Build 17738 (Fast)</span></span>
<span data-ttu-id="0374c-356">Para obter informações gerais do Windows sobre o Build 17738, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="0374c-356">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-357">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-357">WSL</span></span>
* <span data-ttu-id="0374c-358">Verificação de permissão da syscall setpriority muito estrita para alterar a mesma prioridade de thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="0374c-358">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="0374c-359">Verificação de que o tempo de interrupção não polarizado é usado para o tempo de inicialização a fim de evitar retornar valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="0374c-359">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="0374c-360">Manipulação de symlinks no interpretador binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="0374c-360">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="0374c-361">Melhor manipulação da limpeza do descritor de arquivo de líder do grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="0374c-361">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="0374c-362">Build 17728 (rápido)</span><span class="sxs-lookup"><span data-stu-id="0374c-362">Build 17728 (Fast)</span></span>
<span data-ttu-id="0374c-363">Para obter informações gerais do Windows sobre o Build 17728, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="0374c-363">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-364">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-364">WSL</span></span>
* <span data-ttu-id="0374c-365">Alternância do WSL para usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter a fim de evitar o estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="0374c-365">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="0374c-366">A anexação ptrace pode causar um valor retornado insatisfatório de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="0374c-366">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="0374c-367">Correção de vários problemas relacionados ao AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="0374c-367">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="0374c-368">Correção do problema que poderá causar falha de interop de WSL se o diretório de trabalho atual tiver menos de 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="0374c-368">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="0374c-369">Build 18204 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="0374c-369">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="0374c-370">Para obter informações gerais do Windows sobre o Build 18204, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="0374c-370">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-371">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-371">WSL</span></span>
* <span data-ttu-id="0374c-372">O sistema de arquivos de pipe limpa inadvertidamente o evento epoll disparado da borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="0374c-372">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="0374c-373">O executável do Win32 iniciado via symlink NTFS não respeita o nome do symlink [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="0374c-373">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="0374c-374">Build 17723 (rápido)</span><span class="sxs-lookup"><span data-stu-id="0374c-374">Build 17723 (Fast)</span></span>
<span data-ttu-id="0374c-375">Para obter informações gerais do Windows sobre o Build 17723, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="0374c-375">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-376">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-376">WSL</span></span>
* <span data-ttu-id="0374c-377">Impedimento de que um atraso de um segundo cause falhas em conexões de loopback para portas inexistentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="0374c-377">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="0374c-378">Adição do arquivo de stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="0374c-378">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="0374c-379">Informações de escopo de IPV6 mais precisas.</span><span class="sxs-lookup"><span data-stu-id="0374c-379">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="0374c-380">Suporte a PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="0374c-380">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="0374c-381">O sistema de arquivos de pipe limpa inadvertidamente o evento epoll disparado da borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="0374c-381">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="0374c-382">O executável do Win32 iniciado via symlink NTFS não respeita o nome do symlink [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="0374c-382">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="0374c-383">Build 17713</span><span class="sxs-lookup"><span data-stu-id="0374c-383">Build 17713</span></span>
<span data-ttu-id="0374c-384">Para obter informações gerais do Windows sobre o Build 17713, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="0374c-384">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-385">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-385">WSL</span></span>
* <span data-ttu-id="0374c-386">Suporte a zumbis melhorado [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="0374c-386">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="0374c-387">Adição de entradas wsl.conf para controlar o comportamento de interop do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="0374c-387">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="0374c-388">Correção para getsockname nem sempre retornando tipo de família de soquetes UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="0374c-388">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="0374c-389">Adição de suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="0374c-389">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="0374c-390">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="0374c-390">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="0374c-391">Suporte a interop em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="0374c-391">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="0374c-392">Correção do problema de verificação de permissão na pasta raiz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="0374c-392">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="0374c-393">Suporte limitado para os ioctls de teclado TTY KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="0374c-393">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="0374c-394">Os aplicativos da interface do usuário do Windows devem ser executados mesmo quando iniciados em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0374c-394">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="0374c-395">Build 17704</span><span class="sxs-lookup"><span data-stu-id="0374c-395">Build 17704</span></span>
<span data-ttu-id="0374c-396">Para obter informações gerais do Windows sobre o Build 17704, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="0374c-396">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-397">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-397">WSL</span></span>
* <span data-ttu-id="0374c-398">Adição da opção wsl-u ou --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="0374c-398">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="0374c-399">Correção de problemas de inicialização do WSL quando a inicialização rápida estiver habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="0374c-399">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="0374c-400">Os soquetes Unix precisam reter as credenciais de pares desconectados [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="0374c-400">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="0374c-401">Soquetes Unix sem bloqueio falhando indefinidamente com EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="0374c-401">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="0374c-402">case=off é o novo tipo de montagem de drvfs padrão [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="0374c-402">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="0374c-403">Confira [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0374c-403">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="0374c-404">Adição de wslconfig /terminate para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="0374c-404">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="0374c-405">Build 17692</span><span class="sxs-lookup"><span data-stu-id="0374c-405">Build 17692</span></span>
<span data-ttu-id="0374c-406">Para obter informações gerais do Windows sobre o Build 17692, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="0374c-406">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-407">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-407">WSL</span></span>
* <span data-ttu-id="0374c-408">Correção do problema com as entradas do menu de contexto do shell WSL que não manipulam corretamente caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="0374c-408">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="0374c-409">Exposição de diferenciação de maiúsculas e minúsculas por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="0374c-409">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="0374c-410">ARM64: Emulação de operações de manutenção de cache.</span><span class="sxs-lookup"><span data-stu-id="0374c-410">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="0374c-411">Resolução do [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="0374c-411">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="0374c-412">DrvFs: apenas caracteres de escape de saída no intervalo privado que correspondem a um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="0374c-412">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="0374c-413">Build 17686</span><span class="sxs-lookup"><span data-stu-id="0374c-413">Build 17686</span></span>
<span data-ttu-id="0374c-414">Para obter informações gerais do Windows sobre o Build 17686, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="0374c-414">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-415">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-415">WSL</span></span>
* <span data-ttu-id="0374c-416">Correção do erro OB1 (por um) na validação de tamanho do interpretador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="0374c-416">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="0374c-417">Timers absolutos do WSL com um tempo no passado não são disparados [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="0374c-417">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="0374c-418">Verificação de que os pontos de nova análise criados recentemente estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="0374c-418">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="0374c-419">Criação de forma atômica de diretórios que diferenciam maiúsculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="0374c-419">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="0374c-420">Build 17677</span><span class="sxs-lookup"><span data-stu-id="0374c-420">Build 17677</span></span>
<span data-ttu-id="0374c-421">Para obter informações gerais do Windows sobre o Build 17677, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="0374c-421">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-422">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-422">WSL</span></span>
* <span data-ttu-id="0374c-423">Corrigido um problema adicional em que operações multi-threaded poderiam retornar ENOENT mesmo que o arquivo existisse.</span><span class="sxs-lookup"><span data-stu-id="0374c-423">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="0374c-424">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="0374c-424">[GH 2712]</span></span>
* <span data-ttu-id="0374c-425">Correção da falha de inicialização do WSL quando o UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0374c-425">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="0374c-426">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="0374c-426">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="0374c-427">Build 17666</span><span class="sxs-lookup"><span data-stu-id="0374c-427">Build 17666</span></span>
<span data-ttu-id="0374c-428">Para obter informações gerais do Windows sobre o Build 17666, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="0374c-428">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-429">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-429">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="0374c-430">AVISO: Há um problema que impede a execução do WSL em alguns chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="0374c-430">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="0374c-431">Uma correção está pronta e preparando-se para o branch do Build do Insider.</span><span class="sxs-lookup"><span data-stu-id="0374c-431">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="0374c-432">Adição do menu de contexto do Explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="0374c-432">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="0374c-433">Para usá-lo, mantenha a tecla Shift pressionada e clique com o botão direito do mouse quando estiver em uma janela do Explorer.</span><span class="sxs-lookup"><span data-stu-id="0374c-433">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="0374c-434">Correção do comportamento de não bloqueio de soquete do Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="0374c-434">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="0374c-435">Correção do comando do NetLink suspenso, conforme relatado no GH 2026.</span><span class="sxs-lookup"><span data-stu-id="0374c-435">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="0374c-436">Adição de suporte para os sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="0374c-436">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="0374c-437">Correção do problema com truncamento não causando eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="0374c-437">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="0374c-438">Adição da opção --exec para wsl.exe para invocar um único binário sem um shell.</span><span class="sxs-lookup"><span data-stu-id="0374c-438">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="0374c-439">Adição da opção --distribution a wsl.exe para selecionar uma distribuição específica.</span><span class="sxs-lookup"><span data-stu-id="0374c-439">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="0374c-440">Build 17655 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="0374c-440">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="0374c-441">Para obter informações gerais do Windows sobre o Build 17655, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="0374c-441">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-442">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-442">WSL</span></span>
* <span data-ttu-id="0374c-443">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="0374c-443">Limited support for dmesg.</span></span> <span data-ttu-id="0374c-444">Os aplicativos agora podem fazer logon no dmesg.</span><span class="sxs-lookup"><span data-stu-id="0374c-444">Applications can now log to dmesg.</span></span> <span data-ttu-id="0374c-445">O driver do WSL registra informações limitadas no dmesg.</span><span class="sxs-lookup"><span data-stu-id="0374c-445">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="0374c-446">No futuro, isso pode ser estendido para transportar outras informações/diagnósticos do driver.</span><span class="sxs-lookup"><span data-stu-id="0374c-446">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="0374c-447">Observação: atualmente, o dmesg é compatível por meio da interface do dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="0374c-447">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="0374c-448">A interface sycall `syslog` ainda não é compatível.</span><span class="sxs-lookup"><span data-stu-id="0374c-448">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="0374c-449">Assim sendo, algumas das opções de linha de comando de `dmesg`, tais como `-S` e `-C`, não funcionam.</span><span class="sxs-lookup"><span data-stu-id="0374c-449">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="0374c-450">Corrigido um problema em que operações multi-threaded poderiam retornar ENOENT mesmo que o arquivo existisse.</span><span class="sxs-lookup"><span data-stu-id="0374c-450">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="0374c-451">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="0374c-451">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="0374c-452">Build 17639 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="0374c-452">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="0374c-453">Para obter informações gerais do Windows sobre o Build 17639, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="0374c-453">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-454">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-454">WSL</span></span>
* <span data-ttu-id="0374c-455">Alteração do GID e o modo padrão de dispositivos seriais para corresponder ao nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="0374c-455">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="0374c-456">O DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="0374c-456">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="0374c-457">Observação: O DrvFs tem algumas limitações sobre o nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="0374c-457">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="0374c-458">Em particular, alguns caracteres (tais como '/', ': ' e '\*') não são permitidos e os nomes de atributos estendidos não diferenciam maiúsculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-458">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="0374c-459">Build 17133 (rápido)</span><span class="sxs-lookup"><span data-stu-id="0374c-459">Build 17133 (Fast)</span></span>
<span data-ttu-id="0374c-460">Para obter informações gerais do Windows sobre o Build 17133, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="0374c-460">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-461">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-461">WSL</span></span>
* <span data-ttu-id="0374c-462">Correção para o travamento no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-462">Fix for hang in WSL.</span></span> <span data-ttu-id="0374c-463">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="0374c-463">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="0374c-464">Build 17128 (rápido)</span><span class="sxs-lookup"><span data-stu-id="0374c-464">Build 17128 (Fast)</span></span>
<span data-ttu-id="0374c-465">Para obter informações gerais do Windows sobre o Build 17128, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="0374c-465">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-466">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-466">WSL</span></span>
* <span data-ttu-id="0374c-467">Não</span><span class="sxs-lookup"><span data-stu-id="0374c-467">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="0374c-468">Build 17627 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="0374c-468">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="0374c-469">Para obter informações gerais do Windows sobre o Build 17627, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="0374c-469">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-470">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-470">WSL</span></span>
* <span data-ttu-id="0374c-471">Adição de suporte para as operações que reconhecem o Futex PI.</span><span class="sxs-lookup"><span data-stu-id="0374c-471">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="0374c-472">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="0374c-472">[GH 1006]</span></span>
    * <span data-ttu-id="0374c-473">Observe que as prioridades não são atualmente um recurso WSL compatível para que haja limitações, mas o uso padrão deve ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="0374c-473">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="0374c-474">Suporte do Firewall do Windows a processos WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-474">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="0374c-475">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="0374c-475">[GH 1852]</span></span>
    * <span data-ttu-id="0374c-476">Por exemplo, para permitir que o processo Python WSL escute em qualquer porta, use o cmd do Windows com privilégios elevados: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="0374c-476">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="0374c-477">Para obter detalhes adicionais sobre como adicionar regras de firewall, confira este [link](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="0374c-477">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="0374c-478">Respeitar o shell padrão do usuário ao usar wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="0374c-478">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="0374c-479">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="0374c-479">[GH 2372]</span></span>
* <span data-ttu-id="0374c-480">Relatar todos os adaptadores de rede como Ethernet.</span><span class="sxs-lookup"><span data-stu-id="0374c-480">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="0374c-481">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="0374c-481">[GH 2996]</span></span>
* <span data-ttu-id="0374c-482">Melhor manipulação de arquivo /etc/passwd corrompido.</span><span class="sxs-lookup"><span data-stu-id="0374c-482">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="0374c-483">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="0374c-483">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="0374c-484">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-484">Console</span></span>
* <span data-ttu-id="0374c-485">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-486">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-486">LTP Results:</span></span>
<span data-ttu-id="0374c-487">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-487">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="0374c-488">Build 17618 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="0374c-488">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="0374c-489">Para obter informações gerais do Windows sobre o Build 17618, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="0374c-489">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-490">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-490">WSL</span></span>
* <span data-ttu-id="0374c-491">Introduzir a funcionalidade de pseudoconsole para interop NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="0374c-491">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="0374c-492">O mecanismo de instalação herdado (lxrun. exe) foi preterido.</span><span class="sxs-lookup"><span data-stu-id="0374c-492">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="0374c-493">O mecanismo compatível para a instalação de distribuições é por meio da Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="0374c-493">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="0374c-494">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-494">Console</span></span>
* <span data-ttu-id="0374c-495">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-496">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-496">LTP Results:</span></span>
<span data-ttu-id="0374c-497">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-497">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="0374c-498">Build 17110</span><span class="sxs-lookup"><span data-stu-id="0374c-498">Build 17110</span></span>
<span data-ttu-id="0374c-499">Para obter informações gerais do Windows sobre o Build 17110, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="0374c-499">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-500">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-500">WSL</span></span>
* <span data-ttu-id="0374c-501">Permitir que /init seja encerrado do Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="0374c-501">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="0374c-502">Por padrão, o DrvFs agora usa a diferenciação de maiúsculas e minúsculas por diretório (equivalente à opção de montagem "case=dir").</span><span class="sxs-lookup"><span data-stu-id="0374c-502">DrvFs now uses per-directory case sensitivity by default (equivalent to the "case=dir" mount option).</span></span>
    * <span data-ttu-id="0374c-503">O uso de "case=force" (o comportamento antigo) exige a configuração de uma chave do Registro.</span><span class="sxs-lookup"><span data-stu-id="0374c-503">Using "case=force" (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="0374c-504">Execute o seguinte comando para habilitar "case=force" se você precisar usá-lo: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="0374c-504">Run the following command to enable "case=force" if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="0374c-505">Se você tiver diretórios existentes criados com WSL na versão anterior do Windows que precisem diferenciar maiúsculas de minúsculas, use fsutil.exe para marcá-los como com diferenciação de maiúsculas e minúsculas: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="0374c-505">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="0374c-506">Termine cadeias de caracteres retornadas da syscall uname com NULL.</span><span class="sxs-lookup"><span data-stu-id="0374c-506">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="0374c-507">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-507">Console</span></span>
* <span data-ttu-id="0374c-508">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-508">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-509">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-509">LTP Results:</span></span>
<span data-ttu-id="0374c-510">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-510">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="0374c-511">Build 17107</span><span class="sxs-lookup"><span data-stu-id="0374c-511">Build 17107</span></span>
<span data-ttu-id="0374c-512">Para obter informações gerais do Windows sobre o Build 17107, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="0374c-512">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-513">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-513">WSL</span></span>
* <span data-ttu-id="0374c-514">Suporte a TCSETSF e TCSETSW nos pontos de extremidade mestre pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="0374c-514">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="0374c-515">A inicialização de processos de interop simultâneos pode resultar em EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="0374c-515">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="0374c-516">Correção de PTRACE_ATTACH para mostrar o status de rastreamento adequado em/proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="0374c-516">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="0374c-517">Correção da corrida em que os processos de curta duração clonados com os dois sinalizadores CLEARTID e SETTID podem ser encerrados sem limpar o endereço de TID.</span><span class="sxs-lookup"><span data-stu-id="0374c-517">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="0374c-518">Exibir uma mensagem durante a atualização dos diretórios do sistema de arquivos do Linux ao mudar de um build anterior ao 17093.</span><span class="sxs-lookup"><span data-stu-id="0374c-518">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="0374c-519">Para obter mais detalhes sobre as alterações do sistema de arquivos 17093, confira as notas sobre a versão para o [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="0374c-519">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="0374c-520">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-520">Console</span></span>
* <span data-ttu-id="0374c-521">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-521">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-522">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-522">LTP Results:</span></span>
<span data-ttu-id="0374c-523">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-523">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="0374c-524">Build 17101</span><span class="sxs-lookup"><span data-stu-id="0374c-524">Build 17101</span></span>
<span data-ttu-id="0374c-525">Para obter informações gerais do Windows sobre o Build 17101, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="0374c-525">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-526">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-526">WSL</span></span>
* <span data-ttu-id="0374c-527">Suporte para signalfd.</span><span class="sxs-lookup"><span data-stu-id="0374c-527">Support for signalfd.</span></span> <span data-ttu-id="0374c-528">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="0374c-528">[GH 129]</span></span>
* <span data-ttu-id="0374c-529">Suporte a nomes de arquivos que contêm caracteres NTFS ilícitos, codificando-os como caracteres Unicode privados.</span><span class="sxs-lookup"><span data-stu-id="0374c-529">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="0374c-530">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="0374c-530">[GH 1514]</span></span>
* <span data-ttu-id="0374c-531">A montagem automática fará fallback para somente leitura quando a gravação não for compatível.</span><span class="sxs-lookup"><span data-stu-id="0374c-531">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="0374c-532">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="0374c-532">[GH 2603]</span></span>
* <span data-ttu-id="0374c-533">Permissão para colagem de pares substitutos Unicode (como caracteres de Emoji).</span><span class="sxs-lookup"><span data-stu-id="0374c-533">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="0374c-534">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="0374c-534">[GH 2765]</span></span>
* <span data-ttu-id="0374c-535">Pseudoarquivos em /proc e /sys devem retornar prontidão para leitura e gravação de select, poll, epoll e outros. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="0374c-535">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="0374c-536">Correção do problema que pode fazer com que o serviço entre em loop infinito quando o Registro foi adulterado ou está corrompido.</span><span class="sxs-lookup"><span data-stu-id="0374c-536">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="0374c-537">Correção das mensagens do NetLink para trabalhar com a versão mais recente (upstream 4.14) do iproute2.</span><span class="sxs-lookup"><span data-stu-id="0374c-537">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="0374c-538">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-538">Console</span></span>
* <span data-ttu-id="0374c-539">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-539">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-540">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-540">LTP Results:</span></span>
<span data-ttu-id="0374c-541">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-541">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="0374c-542">Build 17093</span><span class="sxs-lookup"><span data-stu-id="0374c-542">Build 17093</span></span>
<span data-ttu-id="0374c-543">Para obter informações gerais do Windows sobre o Build 17093, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-543">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="0374c-544">Importante:</span><span class="sxs-lookup"><span data-stu-id="0374c-544">Important:</span></span>
<span data-ttu-id="0374c-545">Ao iniciar o WSL pela primeira vez após atualizar para esse build, ele precisa executar um certo trabalho de atualização dos diretórios do sistema de arquivos do Linux.</span><span class="sxs-lookup"><span data-stu-id="0374c-545">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="0374c-546">Isso pode levar vários minutos, então a inicialização do WSL pode parecer lenta.</span><span class="sxs-lookup"><span data-stu-id="0374c-546">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="0374c-547">Isso só deve ocorrer uma vez para cada distribuição instalada por meio da loja.</span><span class="sxs-lookup"><span data-stu-id="0374c-547">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="0374c-548">Suporte à diferenciação de maiúsculas e minúsculas melhorada no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="0374c-548">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="0374c-549">O DrvFs agora dá suporte à diferenciação de maiúsculas e minúsculas por diretório.</span><span class="sxs-lookup"><span data-stu-id="0374c-549">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="0374c-550">Esse é um novo sinalizador que pode ser definido em diretórios para indicar que todas as operações nesses diretórios devem ser tratadas como com diferenciação de maiúsculas de minúsculas, o que permite que até mesmo os aplicativos do Windows abram corretamente arquivos que diferem apenas por maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0374c-550">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="0374c-551">O DrvFs tem novas opções de montagem que controlam a diferenciação de maiúsculas e minúsculas em uma base por diretório</span><span class="sxs-lookup"><span data-stu-id="0374c-551">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="0374c-552">Case = Force: todos os diretórios são tratados como com diferenciação de maiúsculas de minúsculas (exceto a raiz da unidade).</span><span class="sxs-lookup"><span data-stu-id="0374c-552">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="0374c-553">Os novos diretórios criados com o WSL são marcados como com diferenciação de maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0374c-553">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="0374c-554">Esse é o comportamento herdado, exceto para marcação de novos diretórios como com diferenciação de maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0374c-554">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="0374c-555">case=dir: somente os diretórios com o sinalizador de diferenciação de maiúsculas e minúsculas por diretório são tratados como com diferenciação de maiúsculas e minúsculas; outros diretórios não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0374c-555">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="0374c-556">Os novos diretórios criados com o WSL são marcados como com diferenciação de maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0374c-556">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="0374c-557">case=off: somente os diretórios com o sinalizador de diferenciação de maiúsculas e minúsculas por diretório são tratados como com diferenciação de maiúsculas e minúsculas; outros diretórios não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0374c-557">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="0374c-558">Os novos diretórios criados com WSL são marcados como sem diferenciação de maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0374c-558">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="0374c-559">Observação: os diretórios criados pelo WSL em versões anteriores não têm esse sinalizador definido e, portanto, não serão tratados como diretórios que diferenciam maiúsculas de minúsculas se você usar a opção "case=dir".</span><span class="sxs-lookup"><span data-stu-id="0374c-559">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the "case=dir" option.</span></span> <span data-ttu-id="0374c-560">Uma maneira de definir esse sinalizador em diretórios existentes estará disponível em breve.</span><span class="sxs-lookup"><span data-stu-id="0374c-560">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="0374c-561">Exemplo de montagem com essas opções (para unidades existentes, você deve primeiro desmontar antes de poder montar com opções diferentes): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="0374c-561">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="0374c-562">Por enquanto, case=force ainda é a opção padrão.</span><span class="sxs-lookup"><span data-stu-id="0374c-562">For now, case=force is still the default option.</span></span> <span data-ttu-id="0374c-563">Isso será alterado para case=dir no futuro.</span><span class="sxs-lookup"><span data-stu-id="0374c-563">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="0374c-564">Agora você pode usar barras invertidas em caminhos do Windows ao montar o DrvFs, por exemplo: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="0374c-564">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="0374c-565">O WSL agora processa o arquivo/etc/fstab durante a inicialização da instância [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="0374c-565">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="0374c-566">Isso é feito antes da montagem automática de unidades de DrvFs; todas as unidades que já foram montadas por fstab não serão remontadas automaticamente, permitindo que você altere o ponto de montagem de unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="0374c-566">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="0374c-567">Esse comportamento pode ser desativado usando o wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="0374c-567">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="0374c-568">Os arquivos mount, mountinfo e mountstats em /proc escapam corretamente caracteres especiais, tais como barras invertidas e espaços [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="0374c-568">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="0374c-569">Arquivos especiais criados com o DrvFs, tais como links simbólicos do WSL, ou então FIFOs e soquetes quando os metadados estão habilitados, agora podem ser copiados e movidos do Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-569">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="0374c-570">O WSL é mais configurável com o wsl.conf</span><span class="sxs-lookup"><span data-stu-id="0374c-570">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="0374c-571">Adicionamos um método para que você configure automaticamente determinadas funcionalidades no WSL que serão aplicadas toda vez que você iniciar o subsistema.</span><span class="sxs-lookup"><span data-stu-id="0374c-571">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="0374c-572">Isso inclui opções de montagem automática e configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="0374c-572">This includes automount options and network configuration.</span></span> <span data-ttu-id="0374c-573">Saiba mais sobre isso em nossa postagem no blog em: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="0374c-573">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="0374c-574">O AF_UNIX permite conexões de soquete entre processos do Linux em WSL e em processos nativos do Windows</span><span class="sxs-lookup"><span data-stu-id="0374c-574">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="0374c-575">Os aplicativos do WSL e do Windows agora podem se comunicar entre si por meio de soquetes Unix.</span><span class="sxs-lookup"><span data-stu-id="0374c-575">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="0374c-576">Imagine que você deseja executar um serviço no Windows e disponibilizá-lo para aplicativos do Windows e do WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-576">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="0374c-577">Agora, isso é possível com os soquetes do UNIX.</span><span class="sxs-lookup"><span data-stu-id="0374c-577">Now, that's possible with Unix sockets.</span></span> <span data-ttu-id="0374c-578">Leia mais em nossa postagem no blog em https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="0374c-578">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-579">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-579">WSL</span></span>
* <span data-ttu-id="0374c-580">Suporte a mmap () com MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="0374c-580">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="0374c-581">Suporte a CLONE_PTRACE e CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="0374c-581">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="0374c-582">Manipulação do sinal de encerramento não SIGCHLD no clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="0374c-582">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="0374c-583">/proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches de stub [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="0374c-583">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="0374c-584">Erro ao carregar binários ELF que contêm cabeçalhos de carga com deslocamentos diferentes de zero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="0374c-584">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="0374c-585">Eliminação de todos os bytes de página à direita ao carregar imagens.</span><span class="sxs-lookup"><span data-stu-id="0374c-585">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="0374c-586">Redução dos casos em que o execve encerra o processo silenciosamente</span><span class="sxs-lookup"><span data-stu-id="0374c-586">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="0374c-587">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-587">Console</span></span>
* <span data-ttu-id="0374c-588">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-588">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-589">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-589">LTP Results:</span></span>
<span data-ttu-id="0374c-590">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-590">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="0374c-591">Build 17083</span><span class="sxs-lookup"><span data-stu-id="0374c-591">Build 17083</span></span>
<span data-ttu-id="0374c-592">Para obter informações gerais do Windows sobre o Build 17083, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-592">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-593">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-593">WSL</span></span>
* <span data-ttu-id="0374c-594">Corrigida a verificação de bug relacionada a epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="0374c-594">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="0374c-595">Corrigidos travamentos ao desativar a ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="0374c-595">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="0374c-596">Garantia de que as operações mmap parecem atômicas [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="0374c-596">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="0374c-597">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-597">Console</span></span>
* <span data-ttu-id="0374c-598">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-598">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-599">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-599">LTP Results:</span></span>
<span data-ttu-id="0374c-600">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-600">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="0374c-601">Build 17074</span><span class="sxs-lookup"><span data-stu-id="0374c-601">Build 17074</span></span>
<span data-ttu-id="0374c-602">Para obter informações gerais do Windows sobre o Build 17074, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-602">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-603">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-603">WSL</span></span>
* <span data-ttu-id="0374c-604">Corrigido formato de armazenamento de metadados do DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="0374c-604">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="0374c-605">**Importante:** Os metadados do DrvFs criados antes deste build serão exibidos incorretamente ou não serão exibidos em absoluto.</span><span class="sxs-lookup"><span data-stu-id="0374c-605">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="0374c-606">Para corrigir os arquivos afetados, use chmod e chown para aplicar novamente os metadados.</span><span class="sxs-lookup"><span data-stu-id="0374c-606">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="0374c-607">Corrigido o problema com vários sinais e syscalls reinicializáveis.</span><span class="sxs-lookup"><span data-stu-id="0374c-607">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="0374c-608">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-608">Console</span></span>
* <span data-ttu-id="0374c-609">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-609">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-610">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-610">LTP Results:</span></span>
<span data-ttu-id="0374c-611">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-611">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="0374c-612">Build 17063</span><span class="sxs-lookup"><span data-stu-id="0374c-612">Build 17063</span></span>
<span data-ttu-id="0374c-613">Para obter informações gerais do Windows sobre o Build 17063, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-613">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="0374c-614">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-614">WSL</span></span>
* <span data-ttu-id="0374c-615">O DrvFs dá suporte a metadados adicionais do Linux.</span><span class="sxs-lookup"><span data-stu-id="0374c-615">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="0374c-616">Isso permite definir o proprietário e o modo de arquivos usando chmod/chown e também criar arquivos especiais, tais como FIFOs, soquetes Unix e arquivos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0374c-616">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="0374c-617">Por enquanto, isso é desabilitado por padrão, pois ainda é experimental.</span><span class="sxs-lookup"><span data-stu-id="0374c-617">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="0374c-618">**Observação**:  Corrigimos um bug no formato de metadados usado pelo DrvFs.</span><span class="sxs-lookup"><span data-stu-id="0374c-618">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="0374c-619">Embora os metadados funcionem nesse Build para experimentação, os builds futuros não leem corretamente os metadados criados por esse build.</span><span class="sxs-lookup"><span data-stu-id="0374c-619">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="0374c-620">Talvez seja necessário atualizar manualmente o proprietário para arquivos modificados e os dispositivos com uma ID de dispositivo personalizada precisarão ser recriados.</span><span class="sxs-lookup"><span data-stu-id="0374c-620">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="0374c-621">Para habilitar, monte o DrvFs com a opção de metadados (para habilitá-lo em uma montagem existente, você precisa primeiro desmontá-lo):</span><span class="sxs-lookup"><span data-stu-id="0374c-621">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="0374c-622">As permissões do Linux são adicionadas como metadados adicionais ao arquivo e não afetam as permissões do Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-622">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="0374c-623">Lembre-se de que a edição de um arquivo usando um editor do Windows pode remover os metadados.</span><span class="sxs-lookup"><span data-stu-id="0374c-623">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="0374c-624">Nesse caso, o arquivo será revertido para as respectivas permissões padrão.</span><span class="sxs-lookup"><span data-stu-id="0374c-624">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="0374c-625">Adicionadas opções de montagem ao DrvFs para controlar arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="0374c-625">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="0374c-626">uid: a ID de usuário usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="0374c-626">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="0374c-627">gid: a ID de grupo usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="0374c-627">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="0374c-628">umask: uma máscara octal de permissões a serem excluídas para todos os arquivos e diretórios.</span><span class="sxs-lookup"><span data-stu-id="0374c-628">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="0374c-629">fmask: uma máscara octal de permissões a serem excluídas para todos os arquivos regulares.</span><span class="sxs-lookup"><span data-stu-id="0374c-629">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="0374c-630">dmask: uma máscara octal de permissões a serem excluídas para todos os diretórios.</span><span class="sxs-lookup"><span data-stu-id="0374c-630">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="0374c-631">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0374c-631">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="0374c-632">Combine com a opção de metadados para especificar permissões padrão para arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="0374c-632">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="0374c-633">Introduziu uma nova variável de ambiente, `WSLENV`, para configurar o modo como as variáveis de ambiente fluem entre WSL e Win32.</span><span class="sxs-lookup"><span data-stu-id="0374c-633">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="0374c-634">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0374c-634">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="0374c-635">`WSLENV` é uma lista delimitada por dois-pontos de variáveis de ambiente que pode ser incluída ao iniciar processos do WSL do Win32 ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="0374c-635">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="0374c-636">Cada variável pode ser sufixada com uma barra seguida por sinalizadores para especificar como ela é traduzida.</span><span class="sxs-lookup"><span data-stu-id="0374c-636">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="0374c-637">p: O valor é um caminho que deve ser traduzido entre caminhos WSL e Win32.</span><span class="sxs-lookup"><span data-stu-id="0374c-637">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="0374c-638">l: O valor é uma lista de caminhos.</span><span class="sxs-lookup"><span data-stu-id="0374c-638">l: The value is a list of paths.</span></span> <span data-ttu-id="0374c-639">No WSL, é uma lista delimitada por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="0374c-639">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="0374c-640">No Win32, é uma lista delimitada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="0374c-640">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="0374c-641">u: O valor só deve ser incluído ao invocar o WSL do Win32</span><span class="sxs-lookup"><span data-stu-id="0374c-641">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="0374c-642">w: O valor só deve ser incluído ao invocar o Win32 do WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-642">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="0374c-643">Você pode definir `WSLENV` em. bashrc ou no ambiente personalizado do Windows para seu usuário.</span><span class="sxs-lookup"><span data-stu-id="0374c-643">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="0374c-644">montagens do DrvFs preservam corretamente os carimbos de data/hora de tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="0374c-644">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="0374c-645">symlinks do DrvFs relatam o tamanho correto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="0374c-645">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="0374c-646">a leitura/gravação funciona para tamanhos de E/S muito grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="0374c-646">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="0374c-647">waitpid trabalha com IDs de grupo de processos (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="0374c-647">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="0374c-648">desempenho de mmap significativamente melhorado para grandes regiões de reserva; melhora o desempenho do ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="0374c-648">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="0374c-649">suporte a personalidades para READ_IMPLIES_EXEC; corrige maxima e clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="0374c-649">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="0374c-650">mprotect dá suporte a PROT_GROWSDOWN; corrige o clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="0374c-650">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="0374c-651">correções de falhas de página no modo de excesso de confirmação; corrige sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="0374c-651">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="0374c-652">o clone dá suporte a mais combinações de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="0374c-652">clone supports more flags combinations</span></span>
* <span data-ttu-id="0374c-653">Dar suporte a select/epoll de arquivos epoll (anteriormente, algo não operacional).</span><span class="sxs-lookup"><span data-stu-id="0374c-653">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="0374c-654">Notificar ptrace de syscalls não implementadas.</span><span class="sxs-lookup"><span data-stu-id="0374c-654">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="0374c-655">Desconsideração de interfaces que não estão em funcionamento ao gerar nomes de servidor resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="0374c-655">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="0374c-656">Enumeração das interfaces de rede sem endereço físico.</span><span class="sxs-lookup"><span data-stu-id="0374c-656">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="0374c-657">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="0374c-657">[GH 2685]</span></span>
* <span data-ttu-id="0374c-658">Pequenas correções de bug e melhorias.</span><span class="sxs-lookup"><span data-stu-id="0374c-658">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="0374c-659">Ferramentas do Linux disponíveis para desenvolvedores no Windows</span><span class="sxs-lookup"><span data-stu-id="0374c-659">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="0374c-660">A Cadeia de Ferramentas de Linha de Comando do Windows ferramentas inclui bsdtar (tar) e curl.</span><span class="sxs-lookup"><span data-stu-id="0374c-660">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="0374c-661">Leia [este blog](https://aka.ms/tarcurlwindows) para saber mais sobre a adição dessas duas novas ferramentas e veja como elas estão moldando a experiência do desenvolvedor no Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-661">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they're shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="0374c-662">`AF_UNIX` está disponível no SDK do Participante do Programa Windows Insider (17061+).</span><span class="sxs-lookup"><span data-stu-id="0374c-662">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="0374c-663">Leia [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para saber mais sobre o `AF_UNIX` e como os desenvolvedores do Windows podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="0374c-663">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="0374c-664">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-664">Console</span></span>
* <span data-ttu-id="0374c-665">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-665">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-666">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-666">LTP Results:</span></span>
<span data-ttu-id="0374c-667">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-667">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="0374c-668">Build 17046</span><span class="sxs-lookup"><span data-stu-id="0374c-668">Build 17046</span></span>

<span data-ttu-id="0374c-669">Para obter informações gerais do Windows sobre o Build 17046, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="0374c-669">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="0374c-670">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-670">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-671">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-671">WSL</span></span>
- <span data-ttu-id="0374c-672">Permissão para que processos sejam executados sem um terminal ativo.</span><span class="sxs-lookup"><span data-stu-id="0374c-672">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="0374c-673">[GH 709, 1007, 1511, 2252, 2391 e outros]</span><span class="sxs-lookup"><span data-stu-id="0374c-673">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="0374c-674">Melhor suporte a CLONE_VFORK e CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="0374c-674">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="0374c-675">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="0374c-675">[GH 1878, 2615]</span></span>
- <span data-ttu-id="0374c-676">Desconsideração de drivers de filtro de TDI para operações de rede WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-676">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="0374c-677">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="0374c-677">[GH 1554]</span></span>
- <span data-ttu-id="0374c-678">DrvFs cria NT symlinks quando determinadas condições são atendidas.</span><span class="sxs-lookup"><span data-stu-id="0374c-678">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="0374c-679">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="0374c-679">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="0374c-680">O destino do link precisa ser relativo, não pode cruzar nenhum ponto de montagem nem symlink e precisa existir.</span><span class="sxs-lookup"><span data-stu-id="0374c-680">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="0374c-681">O usuário deve ter SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (isso normalmente requer que você inicie o wsl.exe com privilégios elevados), a menos que o modo de desenvolvedor esteja ativado.</span><span class="sxs-lookup"><span data-stu-id="0374c-681">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="0374c-682">Em todas as outras situações, o DrvFs ainda cria symlinks do WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-682">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="0374c-683">Permissão para a execução de instâncias de WSL elevadas e não elevadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0374c-683">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="0374c-684">Suporte a /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="0374c-684">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="0374c-685">Adição de wslpath para realizar conversões de caminho WSL<->Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-685">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="0374c-686">[GH 522, 1243, 1834, 2327 e outros]</span><span class="sxs-lookup"><span data-stu-id="0374c-686">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with '/' instead of '\\'

      EX: wslpath 'c:\users'
  ```
  #### <a name="console"></a><span data-ttu-id="0374c-687">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-687">Console</span></span>
- <span data-ttu-id="0374c-688">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="0374c-688">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-689">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-689">LTP Results:</span></span>
<span data-ttu-id="0374c-690">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-690">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="0374c-691">Build 17040</span><span class="sxs-lookup"><span data-stu-id="0374c-691">Build 17040</span></span>

<span data-ttu-id="0374c-692">Para obter informações gerais do Windows sobre o Build 17040, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="0374c-692">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-693">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-693">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-694">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-694">WSL</span></span>
- <span data-ttu-id="0374c-695">Nenhuma correção desde o 17035.</span><span class="sxs-lookup"><span data-stu-id="0374c-695">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-696">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-696">Console</span></span>
- <span data-ttu-id="0374c-697">Nenhuma correção desde o 17035.</span><span class="sxs-lookup"><span data-stu-id="0374c-697">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-698">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-698">LTP Results:</span></span>
<span data-ttu-id="0374c-699">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-699">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="0374c-700">Build 17035</span><span class="sxs-lookup"><span data-stu-id="0374c-700">Build 17035</span></span>

<span data-ttu-id="0374c-701">Para obter informações gerais do Windows sobre o Build 17035, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="0374c-701">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-702">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-702">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-703">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-703">WSL</span></span>
- <span data-ttu-id="0374c-704">O acesso a arquivos no DrvFs pode ocasionalmente falhar com EINVAL.</span><span class="sxs-lookup"><span data-stu-id="0374c-704">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="0374c-705">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="0374c-705">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-706">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-706">Console</span></span>
- <span data-ttu-id="0374c-707">Um pouco de perda de cor ao inserir/excluir linhas no modo VT.</span><span class="sxs-lookup"><span data-stu-id="0374c-707">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-708">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-708">LTP Results:</span></span>
<span data-ttu-id="0374c-709">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-709">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="0374c-710">Build 17025</span><span class="sxs-lookup"><span data-stu-id="0374c-710">Build 17025</span></span>

<span data-ttu-id="0374c-711">Para obter informações gerais do Windows sobre o Build 17025, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="0374c-711">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-712">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-712">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-713">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-713">WSL</span></span>
- <span data-ttu-id="0374c-714">Inicialização dos processos iniciais em um novo grupo de processos de primeiro plano [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="0374c-714">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="0374c-715">Correções de entrega SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="0374c-715">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="0374c-716">Geração do nome de ponte virtual padrão se nenhum for fornecido [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="0374c-716">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="0374c-717">Implementação de /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="0374c-717">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="0374c-718">Mais correções de pipe stdout/stderr de interop.</span><span class="sxs-lookup"><span data-stu-id="0374c-718">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="0374c-719">Chamada do sistema syncfs de stub.</span><span class="sxs-lookup"><span data-stu-id="0374c-719">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-720">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-720">Console</span></span>
- <span data-ttu-id="0374c-721">Correção da conversão de VT de entrada para consoles de terceiros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="0374c-721">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-722">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-722">LTP Results:</span></span>
<span data-ttu-id="0374c-723">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-723">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="0374c-724">Build 17017</span><span class="sxs-lookup"><span data-stu-id="0374c-724">Build 17017</span></span>

<span data-ttu-id="0374c-725">Para obter informações gerais do Windows sobre o Build 17017, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="0374c-725">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-726">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-726">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-727">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-727">WSL</span></span>
- <span data-ttu-id="0374c-728">Desconsideração dos cabeçalhos de programa ELF vazios [GH 330].</span><span class="sxs-lookup"><span data-stu-id="0374c-728">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="0374c-729">Permissão para que o LxssManager Crie instâncias do WSL para usuários não interativos (SSH e suporte a tarefas agendadas) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="0374c-729">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="0374c-730">Suporte a cenários de ("início") WSL-> Win32-> WSL [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="0374c-730">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="0374c-731">Suporte limitado para encerramento de aplicativos de console invocados via interop [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="0374c-731">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="0374c-732">Suporte a opções de montagem para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="0374c-732">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="0374c-733">Ptrace bloqueando a inicialização do filho [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="0374c-733">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="0374c-734">EPOLLET com alguns eventos ausentes [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="0374c-734">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="0374c-735">Retorno de mais dados para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="0374c-735">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="0374c-736">Getdents com lseek fornece resultados incorretos.</span><span class="sxs-lookup"><span data-stu-id="0374c-736">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="0374c-737">Correção de alguns travamentos do aplicativo de interop Win32, aguardando a entrada em um pipe que não tem mais dados.</span><span class="sxs-lookup"><span data-stu-id="0374c-737">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="0374c-738">Suporte do O_ASYNC para arquivos tty/pty.</span><span class="sxs-lookup"><span data-stu-id="0374c-738">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="0374c-739">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-739">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-740">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-740">Console</span></span>
- <span data-ttu-id="0374c-741">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-741">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-742">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-742">LTP Results:</span></span>
<span data-ttu-id="0374c-743">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="0374c-743">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="0374c-744">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="0374c-744">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="0374c-745">Build 16288</span><span class="sxs-lookup"><span data-stu-id="0374c-745">Build 16288</span></span>

<span data-ttu-id="0374c-746">Para obter informações gerais do Windows sobre o Build 16288, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="0374c-746">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-747">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-747">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-748">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-748">WSL</span></span>
- <span data-ttu-id="0374c-749">Inicialização e relatório corretos de UID, GID e modo para descritores de arquivo de soquete [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="0374c-749">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="0374c-750">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-750">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-751">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-751">Console</span></span>
- <span data-ttu-id="0374c-752">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-752">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-753">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-753">LTP Results:</span></span>
<span data-ttu-id="0374c-754">Nenhuma alteração desde o 16273</span><span class="sxs-lookup"><span data-stu-id="0374c-754">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="0374c-755">Build 16278</span><span class="sxs-lookup"><span data-stu-id="0374c-755">Build 16278</span></span>

<span data-ttu-id="0374c-756">Para obter informações gerais do Windows sobre o Build 162738, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="0374c-756">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-757">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-757">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-758">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-758">WSL</span></span>
- <span data-ttu-id="0374c-759">Desmapeamento explícito de exibições mapeadas de seções com backup de arquivo ao dividir o estado LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="0374c-759">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="0374c-760">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-760">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-761">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-761">Console</span></span>
- <span data-ttu-id="0374c-762">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-762">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-763">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-763">LTP Results:</span></span>
<span data-ttu-id="0374c-764">Nenhuma alteração desde o 16273</span><span class="sxs-lookup"><span data-stu-id="0374c-764">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="0374c-765">Build 16275</span><span class="sxs-lookup"><span data-stu-id="0374c-765">Build 16275</span></span>

<span data-ttu-id="0374c-766">Para obter informações gerais do Windows sobre o Build 162735, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="0374c-766">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-767">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-767">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-768">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-768">WSL</span></span>
- <span data-ttu-id="0374c-769">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-769">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-770">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-770">Console</span></span>
- <span data-ttu-id="0374c-771">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-771">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-772">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-772">LTP Results:</span></span>
<span data-ttu-id="0374c-773">Nenhuma alteração desde o 16273</span><span class="sxs-lookup"><span data-stu-id="0374c-773">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="0374c-774">Build 16273</span><span class="sxs-lookup"><span data-stu-id="0374c-774">Build 16273</span></span>

<span data-ttu-id="0374c-775">Para obter informações gerais do Windows sobre o Build 16273, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-775">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-776">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-776">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-777">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-777">WSL</span></span>
- <span data-ttu-id="0374c-778">Corrigido um problema em que o DrvFs às vezes relatava o tipo de arquivo errado para diretórios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="0374c-778">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="0374c-779">Permissão para a criação de soquetes NETLINK_KOBJECT_UEVENT para desbloquear programas que usam uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="0374c-779">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="0374c-780">Adição de suporte para conexão sem bloqueio [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="0374c-780">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="0374c-781">Implementação do sinalizador de chamada do sistema de clone CLONE_FS [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="0374c-781">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="0374c-782">Correção de problemas relacionados à manipulação incorreta de guias ou aspas no interop NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="0374c-782">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="0374c-783">Resolução de erro de acesso negado ao tentar reinicializar instâncias de WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="0374c-783">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="0374c-784">Implementação das operações FUTEX_REQUEUE e FUTEX_CMP_REQUEUE do futex [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="0374c-784">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="0374c-785">Correção de permissões para vários arquivos SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="0374c-785">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="0374c-786">Correção do travamento da pilha do Haskell durante a instalação [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="0374c-786">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="0374c-787">Implementação dos sinalizadores 'C', 'O' e 'P' do binfmt_misc [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="0374c-787">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="0374c-788">Adição de /proc/sys/kernel/shmmax/shmmni e /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="0374c-788">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="0374c-789">Adição de suporte parcial para chamada do sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="0374c-789">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="0374c-790">SO_REUSEPORT de stub e adicionar suporte para SO_PASSCRED para soquetes netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="0374c-790">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="0374c-791">Retorno de códigos de erro diferentes de RegisterDistribuiton se uma distribuição estiver sendo instalada ou desinstalada no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-791">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="0374c-792">Permissão para o cancelamento de registro de distribuições de WSL parcialmente instaladas por meio de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="0374c-792">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="0374c-793">Correção do travamento do teste de soquete Python de udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="0374c-793">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="0374c-794">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-794">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-795">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-795">Console</span></span>
- <span data-ttu-id="0374c-796">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-796">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-797">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-797">LTP Results:</span></span>
<span data-ttu-id="0374c-798">Total de testes: 1904</span><span class="sxs-lookup"><span data-stu-id="0374c-798">Total Tests: 1904</span></span><br/>
<span data-ttu-id="0374c-799">Total de testes ignorados: 209</span><span class="sxs-lookup"><span data-stu-id="0374c-799">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="0374c-800">Total de falhas: 229</span><span class="sxs-lookup"><span data-stu-id="0374c-800">Total Failures: 229</span></span><br/>
[<span data-ttu-id="0374c-801">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-801">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="0374c-802">Build 16257</span><span class="sxs-lookup"><span data-stu-id="0374c-802">Build 16257</span></span>

<span data-ttu-id="0374c-803">Para obter informações gerais do Windows sobre o Build 16257, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-803">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-804">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-804">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-805">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-805">WSL</span></span>
- <span data-ttu-id="0374c-806">Implementação da chamada do sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="0374c-806">Implement prlimit64 system call</span></span>
- <span data-ttu-id="0374c-807">Adição de suporte para ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="0374c-807">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="0374c-808">MSG_MORE de stub para soquetes TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="0374c-808">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="0374c-809">Correção do comportamento de vetor auxiliar AT_EXECFN inválido [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="0374c-809">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="0374c-810">Correção do comportamento de copiar/colar para console/TTY e adição de melhor manipulação de buffer completo [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="0374c-810">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="0374c-811">Definição de AT_SECURE em vetor auxiliar para os programas set-user-ID e set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="0374c-811">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="0374c-812">Ponto de extremidade mestre de pseudoterminal não manipulando TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="0374c-812">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="0374c-813">Correção do que o lseek faz para rebobinar diretórios no LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="0374c-813">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="0374c-814">/dev/ptmx trava após uso intenso [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="0374c-814">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="0374c-815">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-815">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-816">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-816">Console</span></span>
- <span data-ttu-id="0374c-817">Correção para linhas horizontais/sublinhados em todos os lugares [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="0374c-817">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="0374c-818">Correção para a ordem de processo alterada, tornando o NPM mais difícil de fechar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="0374c-818">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="0374c-819">Adicionado nosso novo esquema de cores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="0374c-819">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-820">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-820">LTP Results:</span></span>
<span data-ttu-id="0374c-821">Nenhuma alteração desde o 16251</span><span class="sxs-lookup"><span data-stu-id="0374c-821">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="0374c-822">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-822">Syscall Support</span></span>
<span data-ttu-id="0374c-823">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-823">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-824">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-824">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="0374c-825">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="0374c-825">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>[<span data-ttu-id="0374c-826">Problema do GitHub n. 2392: Pastas do Windows não reconhecidas pelo WSL...</span><span class="sxs-lookup"><span data-stu-id="0374c-826">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="0374c-827">No build 16257, o WSL tem problemas para enumerar arquivos/pastas do Windows via `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="0374c-827">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="0374c-828">Esse problema foi corrigido e deve ser liberado no build do Insiders durante a semana que começa em 14/08/2017.</span><span class="sxs-lookup"><span data-stu-id="0374c-828">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="0374c-829">Build 16251</span><span class="sxs-lookup"><span data-stu-id="0374c-829">Build 16251</span></span>

<span data-ttu-id="0374c-830">Para obter informações gerais do Windows sobre o Build 16251, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-830">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-831">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-831">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-832">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-832">WSL</span></span>
- <span data-ttu-id="0374c-833">Remova a tag beta do componente opcional do WSL, confira esta [postagem no blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="0374c-833">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="0374c-834">Inicializar corretamente a UID e a GID salvas para os binários Set-User-ID e Set-Group-ID em exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="0374c-834">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="0374c-835">Adicionado suporte para ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="0374c-835">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="0374c-836">Adicionado suporte para ptrace PTRACE_GETFPREGS e PTRACE_GETREGSET com NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="0374c-836">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="0374c-837">Correção de ptrace para parar em sinais ignorados</span><span class="sxs-lookup"><span data-stu-id="0374c-837">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="0374c-838">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-838">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-839">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-839">Console</span></span>
- <span data-ttu-id="0374c-840">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-840">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-841">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-841">LTP Results:</span></span>
<span data-ttu-id="0374c-842">Número de testes aprovados: 768</span><span class="sxs-lookup"><span data-stu-id="0374c-842">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="0374c-843">Número de testes reprovados: 244</span><span class="sxs-lookup"><span data-stu-id="0374c-843">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="0374c-844">Número de testes ignorados: 96</span><span class="sxs-lookup"><span data-stu-id="0374c-844">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="0374c-845">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-845">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="0374c-846">Build 16241</span><span class="sxs-lookup"><span data-stu-id="0374c-846">Build 16241</span></span>

<span data-ttu-id="0374c-847">Para obter informações gerais do Windows sobre o Build 16241, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-847">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-848">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-848">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="0374c-849">WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-849">WSL</span></span>
- <span data-ttu-id="0374c-850">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-850">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="0374c-851">Console</span><span class="sxs-lookup"><span data-stu-id="0374c-851">Console</span></span>
- <span data-ttu-id="0374c-852">Correção para a geração do caractere errado como saída para as linhas de cruzamento DEC, originalmente relatadas [aqui](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="0374c-852">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="0374c-853">Correção para nenhum texto de saída sendo exibido na página de código 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="0374c-853">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="0374c-854">Não transfira as alterações feitas aos valores RGB de uma cor para outras partes da paleta na alteração de seleção.</span><span class="sxs-lookup"><span data-stu-id="0374c-854">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="0374c-855">Isso tornará a planilha de propriedades do console muito mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="0374c-855">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="0374c-856">Ctrl + S parece não funcionar corretamente</span><span class="sxs-lookup"><span data-stu-id="0374c-856">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="0374c-857">Sem negrito/sem esmaecimento totalmente ausentes dos códigos de escape ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="0374c-857">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="0374c-858">O console não dá suporte corretamente a temas de cor Vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="0374c-858">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="0374c-859">Não é possível colar determinados caracteres [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="0374c-859">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="0374c-860">O redimensionamento de refluxo interage de acordo com o redimensionamento de uma janela do Bash quando as coisas estão na linha de comando/edição [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="0374c-860">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="0374c-861">Ctrl + L deixa a tela suja [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="0374c-861">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="0374c-862">Bug de renderização do console ao exibir VT em HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="0374c-862">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="0374c-863">Caracteres japoneses parecem estranhos com o caractere Unicode U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="0374c-863">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="0374c-864">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-864">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="0374c-865">Build 16237</span><span class="sxs-lookup"><span data-stu-id="0374c-865">Build 16237</span></span>

<span data-ttu-id="0374c-866">Para obter informações gerais do Windows sobre o Build 16237, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-866">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-867">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-867">Fixed</span></span>
- <span data-ttu-id="0374c-868">Usar atributos padrão para arquivos sem EAs em lxfs (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="0374c-868">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="0374c-869">Adicionado suporte para distribuições que usam atributos estendidos</span><span class="sxs-lookup"><span data-stu-id="0374c-869">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="0374c-870">Correção do preenchimento das entradas retornadas por getdents e getdents64</span><span class="sxs-lookup"><span data-stu-id="0374c-870">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="0374c-871">Correção da verificação de permissões para a chamada do sistema shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="0374c-871">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="0374c-872">Corrigido o estado de epoll inicial incorreto para ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="0374c-872">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="0374c-873">Correção do DrvFs readdir não retornando todas as entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="0374c-873">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="0374c-874">Correção do LxFs readdir quando os arquivos estão desvinculados [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="0374c-874">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="0374c-875">Permissão para que arquivos do DrvFs não vinculados sejam reabertos por meio do procfs</span><span class="sxs-lookup"><span data-stu-id="0374c-875">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="0374c-876">Substituição da chave do Registro global adicionada para desabilitar os recursos do WSL (interop/montagem de unidade)</span><span class="sxs-lookup"><span data-stu-id="0374c-876">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="0374c-877">Correção da contagem de blocos incorretos em "stat" para o DrvFs (e o LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="0374c-877">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="0374c-878">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-878">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="0374c-879">Build 16232</span><span class="sxs-lookup"><span data-stu-id="0374c-879">Build 16232</span></span>

<span data-ttu-id="0374c-880">Para obter informações gerais do Windows sobre o Build 16232, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-880">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-881">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-881">Fixed</span></span>
- <span data-ttu-id="0374c-882">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-882">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="0374c-883">Build 16226</span><span class="sxs-lookup"><span data-stu-id="0374c-883">Build 16226</span></span>

<span data-ttu-id="0374c-884">Para obter informações gerais do Windows sobre o Build 16226, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-884">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-885">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-885">Fixed</span></span>
- <span data-ttu-id="0374c-886">suporte a syscalls relacionadas a xattr (getxattr, setxattr, listxattr e removexattr).</span><span class="sxs-lookup"><span data-stu-id="0374c-886">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="0374c-887">suporte a security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="0374c-887">security.capablity xattr support.</span></span>
- <span data-ttu-id="0374c-888">Compatibilidade aprimorada com determinados sistemas de arquivos e filtros, incluindo servidores SMB não MS.</span><span class="sxs-lookup"><span data-stu-id="0374c-888">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="0374c-889">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="0374c-889">[GH #1952]</span></span>
- <span data-ttu-id="0374c-890">Suporte aprimorado para espaços reservados do OneDrive, espaços reservados do GVFS e arquivos compactados do SO Compacto.</span><span class="sxs-lookup"><span data-stu-id="0374c-890">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="0374c-891">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-891">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="0374c-892">Build 16215</span><span class="sxs-lookup"><span data-stu-id="0374c-892">Build 16215</span></span>

<span data-ttu-id="0374c-893">Para obter informações gerais do Windows sobre o Build 16215, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-893">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-894">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-894">Fixed</span></span>
- <span data-ttu-id="0374c-895">O WSL não exige mais o modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="0374c-895">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="0374c-896">Suporte a junções de diretório no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="0374c-896">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="0374c-897">Manipulação da desinstalação de pacotes appx de distribuição do WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-897">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="0374c-898">Atualização do procfs para mostrar mapeamentos privados e compartilhados.</span><span class="sxs-lookup"><span data-stu-id="0374c-898">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="0374c-899">Adição de capacidade para o wslconfig.exe limpar as distribuições parcialmente instaladas ou desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="0374c-899">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="0374c-900">Adicionado suporte para IP_MTU_DISCOVER para soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="0374c-900">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="0374c-901">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="0374c-901">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="0374c-902">Inferência da família de protocolos para rotas para AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="0374c-902">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="0374c-903">Aprimoramentos de dispositivo serial [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="0374c-903">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="0374c-904">Build 16199</span><span class="sxs-lookup"><span data-stu-id="0374c-904">Build 16199</span></span>

<span data-ttu-id="0374c-905">Para obter informações gerais do Windows sobre o Build 16199, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-905">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-906">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-906">Fixed</span></span>
- <span data-ttu-id="0374c-907">Nenhuma alteração relacionada ao WSL nestas versões.</span><span class="sxs-lookup"><span data-stu-id="0374c-907">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="0374c-908">Build 16193</span><span class="sxs-lookup"><span data-stu-id="0374c-908">Build 16193</span></span>

<span data-ttu-id="0374c-909">Para obter informações gerais do Windows sobre o Build 16193, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-909">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-910">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-910">Fixed</span></span>
- <span data-ttu-id="0374c-911">Condição de corrida entre o envio de SIGCONT e um encerramento de um grupo de threads [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="0374c-911">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="0374c-912">alteração de dispositivos tty e pty para relatar FILE_DEVICE_NAMED_PIPE em vez de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="0374c-912">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="0374c-913">Correção de SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="0374c-913">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="0374c-914">A montagem do DrvFs foi movida para o daemon init [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="0374c-914">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="0374c-915">Adicionado suporte no DrvFs para os symlinks NT a seguir.</span><span class="sxs-lookup"><span data-stu-id="0374c-915">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="0374c-916">Build 16184</span><span class="sxs-lookup"><span data-stu-id="0374c-916">Build 16184</span></span>

<span data-ttu-id="0374c-917">Para obter informações gerais do Windows sobre o Build 16184, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-917">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-918">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-918">Fixed</span></span>
- <span data-ttu-id="0374c-919">Removida a tarefa de manutenção do pacote apt (lxrun.exe/update)</span><span class="sxs-lookup"><span data-stu-id="0374c-919">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="0374c-920">Corrigido problema em que a saída não aparecia nos processos do Windows no Node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="0374c-920">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="0374c-921">Flexibilização dos requisitos de alinhamento no lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="0374c-921">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="0374c-922">Corrigida a manipulação do sinalizador AT_EMPTY_PATH em um número de chamadas do sistema.</span><span class="sxs-lookup"><span data-stu-id="0374c-922">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="0374c-923">Corrigido o problema em que a exclusão de arquivos do DrvFs com identificadores abertos fazia com que o arquivo apresentasse comportamento indefinido [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="0374c-923">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="0374c-924">O /etc/hosts agora herdará entradas do arquivo de hosts do Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="0374c-924">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="0374c-925">Build 16179</span><span class="sxs-lookup"><span data-stu-id="0374c-925">Build 16179</span></span>

<span data-ttu-id="0374c-926">Para obter informações gerais do Windows sobre o Build 16179, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-926">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-927">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-927">Fixed</span></span>
- <span data-ttu-id="0374c-928">Nenhuma alteração de WSL nesta semana.</span><span class="sxs-lookup"><span data-stu-id="0374c-928">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="0374c-929">Build 16176</span><span class="sxs-lookup"><span data-stu-id="0374c-929">Build 16176</span></span>

<span data-ttu-id="0374c-930">Para obter informações gerais do Windows sobre o Build 16176, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-930">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-931">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-931">Fixed</span></span>

- [<span data-ttu-id="0374c-932">Suporte serial habilitado</span><span class="sxs-lookup"><span data-stu-id="0374c-932">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="0374c-933">Adicionada opção de soquete IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="0374c-933">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="0374c-934">Função pwritev implementada (ao carregar o arquivo para nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="0374c-934">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="0374c-935">Adicionadas opções de soquete IP IP_MULTICAST_IF e IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="0374c-935">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="0374c-936">Suporte para as opções de soquete IP_MULTICAST_LOOP e IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="0374c-936">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="0374c-937">Adicionada a opção de soquete IP(V6)_MTU para node, traceroute, dig, nslookup e host de aplicativos</span><span class="sxs-lookup"><span data-stu-id="0374c-937">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="0374c-938">Adicionada a opção de soquete IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="0374c-938">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="0374c-939">Aprimoramentos do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="0374c-939">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="0374c-940">Permitir a montagem de caminhos UNC</span><span class="sxs-lookup"><span data-stu-id="0374c-940">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="0374c-941">Habilitar o suporte a CDFS no DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-941">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="0374c-942">Manipulação correta das permissões para sistemas de arquivos de rede no DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-942">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="0374c-943">Adição de suporte para unidades remotas ao DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-943">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="0374c-944">Habilitação do suporte a FAT no DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-944">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="0374c-945">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-945">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-946">Resultados do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-946">LTP Results</span></span>
<span data-ttu-id="0374c-947">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="0374c-947">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="0374c-948">Build 16170</span><span class="sxs-lookup"><span data-stu-id="0374c-948">Build 16170</span></span>

<span data-ttu-id="0374c-949">Para obter informações gerais do Windows sobre o Build 16170, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-949">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="0374c-950">Lançamos uma nova [postagem no blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutindo nossos esforços para testar o WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-950">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="0374c-951">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-951">Fixed</span></span>

- <span data-ttu-id="0374c-952">Suporte à opção de soquete IP_ADD_MEMBERSHIP e IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="0374c-952">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="0374c-953">Adição de suporte para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="0374c-953">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="0374c-954">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="0374c-954">[GH 1692]</span></span>
- <span data-ttu-id="0374c-955">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-955">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-956">Resultados do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-956">LTP Results</span></span>
<span data-ttu-id="0374c-957">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="0374c-957">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="0374c-958">Build 15046 para a Atualização do Windows 10 para Criadores</span><span class="sxs-lookup"><span data-stu-id="0374c-958">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="0374c-959">Não há mais correções nem recursos do WSL planejados para inclusão na Atualização do Windows 10 para Criadores.</span><span class="sxs-lookup"><span data-stu-id="0374c-959">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="0374c-960">As notas sobre a versão do WSL serão retomadas nas próximas semanas para as adições direcionadas à próxima atualização importante do Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-960">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="0374c-961">Para obter informações gerais do Windows sobre o Build 15046 e futuras versões do Insider, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-961">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="0374c-962">Build 15042</span><span class="sxs-lookup"><span data-stu-id="0374c-962">Build 15042</span></span>

<span data-ttu-id="0374c-963">Para obter informações gerais do Windows sobre o Build 15042, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-963">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-964">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-964">Fixed</span></span>

- <span data-ttu-id="0374c-965">Correção de um deadlock ao remover um caminho que termina em ".."</span><span class="sxs-lookup"><span data-stu-id="0374c-965">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="0374c-966">Corrigido um problema em que FIONBIO não retornava 0 em caso de êxito [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="0374c-966">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="0374c-967">Corrigido um problema com leituras de comprimento zero de soquetes de datagrama inet</span><span class="sxs-lookup"><span data-stu-id="0374c-967">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="0374c-968">Correção de um possível deadlock devido à condição de corrida na pesquisa de inode do DrvFs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="0374c-968">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="0374c-969">Suporte estendido para dados complementares de soquete Unix; SCM_CREDENTIALS e SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="0374c-969">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="0374c-970">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-970">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-971">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-971">LTP Results:</span></span>
<span data-ttu-id="0374c-972">Número de testes aprovados: 737</span><span class="sxs-lookup"><span data-stu-id="0374c-972">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="0374c-973">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="0374c-973">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="0374c-974">Build 15031</span><span class="sxs-lookup"><span data-stu-id="0374c-974">Build 15031</span></span>

<span data-ttu-id="0374c-975">Para obter informações gerais do Windows sobre o Build 15031, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-975">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-976">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-976">Fixed</span></span>

- <span data-ttu-id="0374c-977">Corrigido um bug em que time(2) se comportava de maneira incorreta esporadicamente.</span><span class="sxs-lookup"><span data-stu-id="0374c-977">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="0374c-978">Corrigido um problema em que syscalls \*SIGPROCMASK poderiam corromper a máscara de sinal.</span><span class="sxs-lookup"><span data-stu-id="0374c-978">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="0374c-979">Agora, retorne o comprimento de linha de comando completo na notificação de criação de processo do WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-979">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="0374c-980">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="0374c-980">[GH 1632]</span></span>
- <span data-ttu-id="0374c-981">O WSL agora relata a saída do thread por meio de ptrace para travamentos do GDB.</span><span class="sxs-lookup"><span data-stu-id="0374c-981">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="0374c-982">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="0374c-982">[GH 1196]</span></span>
- <span data-ttu-id="0374c-983">Corrigido o bug em que ptys travam após E/S intensa de tmux.</span><span class="sxs-lookup"><span data-stu-id="0374c-983">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="0374c-984">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="0374c-984">[GH 1358]</span></span>
- <span data-ttu-id="0374c-985">Correção da validação de tempo limite em muitas chamadas do sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="0374c-985">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="0374c-986">Adicionado suporte a eventfd EFD_SEMAPHORE [GH 452]</span><span class="sxs-lookup"><span data-stu-id="0374c-986">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="0374c-987">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-987">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-988">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-988">LTP Results:</span></span>
<span data-ttu-id="0374c-989">Número de testes aprovados: 737</span><span class="sxs-lookup"><span data-stu-id="0374c-989">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="0374c-990">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="0374c-990">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="0374c-991">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-991">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="0374c-992">Build 15025</span><span class="sxs-lookup"><span data-stu-id="0374c-992">Build 15025</span></span>

<span data-ttu-id="0374c-993">Para obter informações gerais do Windows sobre o Build 15025, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-993">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-994">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-994">Fixed</span></span>

- <span data-ttu-id="0374c-995">Correção do bug que interrompeu o grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="0374c-995">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="0374c-996">Implementado o sinalizador EFD_SEMAPHORE para a syscall eventfd2 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="0374c-996">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="0374c-997">Implementado /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="0374c-997">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="0374c-998">Suporte de E/S controlada por sinal para soquetes de fluxo do Unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="0374c-998">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="0374c-999">Suporte a F_GETPIPE_SZ e F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="0374c-999">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="0374c-1000">Implementação da syscall recvmmsg() [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="0374c-1000">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="0374c-1001">Corrigido o bug em que epoll_wait() não estava aguardando [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="0374c-1001">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="0374c-1002">Implementação de /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="0374c-1002">Implement /proc/version_signature</span></span>
- <span data-ttu-id="0374c-1003">Tee syscall agora retornará uma falha se os dois descritores de arquivo se referirem ao mesmo pipe</span><span class="sxs-lookup"><span data-stu-id="0374c-1003">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="0374c-1004">Implementação do comportamento correto para SO_PEERCRED para soquetes Unix</span><span class="sxs-lookup"><span data-stu-id="0374c-1004">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="0374c-1005">Corrigido o tratamento de erro de parâmetro inválido da syscall tkill</span><span class="sxs-lookup"><span data-stu-id="0374c-1005">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="0374c-1006">Alterações para aumentar o desempenho do DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-1006">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="0374c-1007">Correção secundária para bloqueio de E/S do Ruby</span><span class="sxs-lookup"><span data-stu-id="0374c-1007">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="0374c-1008">Corrigido o erro em que recvmsg() retornava EINVAL para o sinalizador MSG_DONTWAIT para soquetes inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="0374c-1008">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="0374c-1009">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1009">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1010">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1010">LTP Results:</span></span>
<span data-ttu-id="0374c-1011">Número de testes aprovados: 732</span><span class="sxs-lookup"><span data-stu-id="0374c-1011">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="0374c-1012">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="0374c-1012">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="0374c-1013">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1013">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="0374c-1014">Build 15019</span><span class="sxs-lookup"><span data-stu-id="0374c-1014">Build 15019</span></span>

<span data-ttu-id="0374c-1015">Para obter informações gerais do Windows sobre o Build 15019, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1015">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1016">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1016">Fixed</span></span>

- <span data-ttu-id="0374c-1017">Correção do bug que reportava incorretamente o uso da CPU em procfs para ferramentas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="0374c-1017">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="0374c-1018">Ao chamar open() com O_TRUNC em um arquivo existente, INotifyPropertyChanged agora gera IN_MODIFY antes de IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="0374c-1018">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="0374c-1019">Correções para getsockopt SO_ERROR de soquetes Unix para habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="0374c-1019">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="0374c-1020">Implementação de /proc/sys/net/Core/SOMAXCONN para a linguagem GO</span><span class="sxs-lookup"><span data-stu-id="0374c-1020">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="0374c-1021">A tarefa de atualização em segundo plano do pacote apt-get agora executa oculta</span><span class="sxs-lookup"><span data-stu-id="0374c-1021">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="0374c-1022">Limpeza do escopo do localhost IPv6 (falha de Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="0374c-1022">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="0374c-1023">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1023">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1024">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1024">LTP Results:</span></span>
<span data-ttu-id="0374c-1025">Número de testes aprovados: 714</span><span class="sxs-lookup"><span data-stu-id="0374c-1025">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="0374c-1026">Número de não aprovados (com falha, ignorados, etc.): 249</span><span class="sxs-lookup"><span data-stu-id="0374c-1026">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="0374c-1027">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1027">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="0374c-1028">Build 15014</span><span class="sxs-lookup"><span data-stu-id="0374c-1028">Build 15014</span></span>

<span data-ttu-id="0374c-1029">Para obter informações gerais do Windows sobre o Build 15014, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="0374c-1029">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1030">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1030">Fixed</span></span>

- <span data-ttu-id="0374c-1031">Ctrl + C agora funciona conforme esperado</span><span class="sxs-lookup"><span data-stu-id="0374c-1031">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="0374c-1032">htop e ps auxw agora mostram a utilização de recursos correta (GH 516)</span><span class="sxs-lookup"><span data-stu-id="0374c-1032">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="0374c-1033">Conversão básica de exceções NT para sinais.</span><span class="sxs-lookup"><span data-stu-id="0374c-1033">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="0374c-1034">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="0374c-1034">(GH #513)</span></span>
- <span data-ttu-id="0374c-1035">agora, ao ficar sem espaço, fallocate falha com ENOSPC em vez de EINVAL (GH 1571)</span><span class="sxs-lookup"><span data-stu-id="0374c-1035">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="0374c-1036">Adicionado /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="0374c-1036">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="0374c-1037">Implementadas as chamadas de sistema semop e semtimedop</span><span class="sxs-lookup"><span data-stu-id="0374c-1037">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="0374c-1038">Corrigidos os erros de nslookup com as opções de soquete IP_RECVTOS e IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="0374c-1038">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="0374c-1039">Suporte para as opções de soquete IP_RECVTTL e IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="0374c-1039">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="0374c-1040">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1040">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1041">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1041">LTP Results:</span></span>
<span data-ttu-id="0374c-1042">Número de testes aprovados: 709</span><span class="sxs-lookup"><span data-stu-id="0374c-1042">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="0374c-1043">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="0374c-1043">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="0374c-1044">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1044">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="0374c-1045">Resumo das syscalls</span><span class="sxs-lookup"><span data-stu-id="0374c-1045">Syscall Summary</span></span>
<span data-ttu-id="0374c-1046">Total de syscalls: 384</span><span class="sxs-lookup"><span data-stu-id="0374c-1046">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="0374c-1047">Total de implementadas: 235</span><span class="sxs-lookup"><span data-stu-id="0374c-1047">Total Implemented: 235</span></span> </br>
<span data-ttu-id="0374c-1048">Total de fragmentadas: 22</span><span class="sxs-lookup"><span data-stu-id="0374c-1048">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="0374c-1049">Total de não implementadas: 127</span><span class="sxs-lookup"><span data-stu-id="0374c-1049">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="0374c-1050">Detalhamento</span><span class="sxs-lookup"><span data-stu-id="0374c-1050">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="0374c-1051">Build 15007</span><span class="sxs-lookup"><span data-stu-id="0374c-1051">Build 15007</span></span>

<span data-ttu-id="0374c-1052">Para obter informações gerais do Windows sobre o Build 15007, visite o [blog do Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="0374c-1052">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="0374c-1053">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="0374c-1053">Known Issue</span></span>

- <span data-ttu-id="0374c-1054">Há um bug conhecido em que o console não reconhece alguma entrada Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="0374c-1054">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="0374c-1055">Isso inclui o comando Ctrl + C, que funcionará como um pressionamento comum da tecla 'C'.</span><span class="sxs-lookup"><span data-stu-id="0374c-1055">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="0374c-1056">Solução alternativa: Mapeamento de uma tecla alternativa para Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="0374c-1056">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="0374c-1057">Por exemplo, para mapear Ctrl + K para Ctrl + C, faça isto: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="0374c-1057">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="0374c-1058">Este mapeamento é por terminal e precisará ser realizado *toda* vez que o Bash for inicializado.</span><span class="sxs-lookup"><span data-stu-id="0374c-1058">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="0374c-1059">Os usuários podem explorar a opção para incluir isto no `.bashrc` deles</span><span class="sxs-lookup"><span data-stu-id="0374c-1059">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="0374c-1060">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1060">Fixed</span></span>

- <span data-ttu-id="0374c-1061">Corrigido o problema em que executar o WSL consumiria 100% de um núcleo de CPU</span><span class="sxs-lookup"><span data-stu-id="0374c-1061">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="0374c-1062">A opção de soquete IP_PKTINFO, IPV6_RECVPKTINFO agora é compatível.</span><span class="sxs-lookup"><span data-stu-id="0374c-1062">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="0374c-1063">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="0374c-1063">(GH #851, 987)</span></span>
- <span data-ttu-id="0374c-1064">Truncamento do endereço físico do adaptador de rede para 16 bytes em lxcore (GH 1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="0374c-1064">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="0374c-1065">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1065">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1066">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1066">LTP Results:</span></span>
<span data-ttu-id="0374c-1067">Número de testes aprovados: 709</span><span class="sxs-lookup"><span data-stu-id="0374c-1067">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="0374c-1068">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="0374c-1068">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="0374c-1069">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1069">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="0374c-1070">Build 15002</span><span class="sxs-lookup"><span data-stu-id="0374c-1070">Build 15002</span></span>

<span data-ttu-id="0374c-1071">Para obter informações gerais do Windows sobre o Build 15002, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1071">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="0374c-1072">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="0374c-1072">Known Issue</span></span>

<span data-ttu-id="0374c-1073">Dois problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="0374c-1073">Two known issues:</span></span>
- <span data-ttu-id="0374c-1074">Há um bug conhecido em que o console não reconhece alguma entrada Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="0374c-1074">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="0374c-1075">Isso inclui o comando Ctrl + C, que funcionará como um pressionamento comum da tecla 'C'.</span><span class="sxs-lookup"><span data-stu-id="0374c-1075">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="0374c-1076">Solução alternativa: Mapeamento de uma tecla alternativa para Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="0374c-1076">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="0374c-1077">Por exemplo, para mapear Ctrl + K para Ctrl + C, faça isto: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="0374c-1077">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="0374c-1078">Este mapeamento é por terminal e precisará ser realizado *toda* vez que o Bash for inicializado.</span><span class="sxs-lookup"><span data-stu-id="0374c-1078">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="0374c-1079">Os usuários podem explorar a opção para incluir isto no `.bashrc` deles</span><span class="sxs-lookup"><span data-stu-id="0374c-1079">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="0374c-1080">Enquanto o WSL estiver em execução, um thread do sistema consumirá 100% de um núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="0374c-1080">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="0374c-1081">A causa raiz foi resolvida e corrigida internamente.</span><span class="sxs-lookup"><span data-stu-id="0374c-1081">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="0374c-1082">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1082">Fixed</span></span>

- <span data-ttu-id="0374c-1083">Todas as sessões do Bash agora devem ser criadas no mesmo nível de permissão.</span><span class="sxs-lookup"><span data-stu-id="0374c-1083">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="0374c-1084">Qualquer tentativa de iniciar uma sessão em um nível diferente será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="0374c-1084">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="0374c-1085">Isso significa que consoles com e sem privilégios de administrador não podem executar simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0374c-1085">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="0374c-1086">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="0374c-1086">(GH #626)</span></span>
<br/>
- <span data-ttu-id="0374c-1087">Implementadas as mensagens NETLINK_ROUTE a seguir (requer administrador do Windows)</span><span class="sxs-lookup"><span data-stu-id="0374c-1087">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="0374c-1088">RTM_NEWADDR (dá suporte a `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="0374c-1088">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="0374c-1089">RTM_NEWROUTE (dá suporte a `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="0374c-1089">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="0374c-1090">RTM_DELADDR (dá suporte a `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="0374c-1090">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="0374c-1091">RTM_DELROUTE (dá suporte a `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="0374c-1091">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="0374c-1092">A verificação de tarefa agendada para que os pacotes sejam atualizados não será mais executada em uma conexão limitada (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="0374c-1092">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="0374c-1093">Corrigido o erro em que o pipe fica preso, ou seja, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="0374c-1093">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="0374c-1094">Implementada a opção de soquete TCP_KEEPCNT (GH 843)</span><span class="sxs-lookup"><span data-stu-id="0374c-1094">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="0374c-1095">Implementada a opção de soquete IP_MTU_DISCOVER INET (GH 720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="0374c-1095">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="0374c-1096">Funcionalidade herdada removida para executar binários NT por meio de init com a pesquisa de caminho de NT.</span><span class="sxs-lookup"><span data-stu-id="0374c-1096">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="0374c-1097">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="0374c-1097">(GH #1325)</span></span>
- <span data-ttu-id="0374c-1098">Correção do modo de /dev/kmsg para permitir o acesso de grupo/outro acesso de leitura (0644) (GH 1321)</span><span class="sxs-lookup"><span data-stu-id="0374c-1098">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="0374c-1099">Implementado /proc/sys/kernel/random/uuid (GH 1092)</span><span class="sxs-lookup"><span data-stu-id="0374c-1099">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="0374c-1100">Erro corrigido em que a hora de início do processo era mostrada como no ano 2432 (GH 974)</span><span class="sxs-lookup"><span data-stu-id="0374c-1100">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="0374c-1101">Variável de ambiente TERM padrão alternada para xterm-256color (GH 1446)</span><span class="sxs-lookup"><span data-stu-id="0374c-1101">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="0374c-1102">Modificado o modo como a confirmação do processo é calculada durante o fork do processo.</span><span class="sxs-lookup"><span data-stu-id="0374c-1102">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="0374c-1103">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="0374c-1103">(GH #1286)</span></span>
- <span data-ttu-id="0374c-1104">Implementado /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="0374c-1104">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="0374c-1105">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="0374c-1105">(GH #1286)</span></span>
- <span data-ttu-id="0374c-1106">Implementado /proc/net/route file (GH 69)</span><span class="sxs-lookup"><span data-stu-id="0374c-1106">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="0374c-1107">Corrigido um erro em que o nome do atalho era localizado incorretamente (GH 696)</span><span class="sxs-lookup"><span data-stu-id="0374c-1107">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="0374c-1108">Corrigida a lógica de análise de ELF que estava validando incorretamente os cabeçalhos de programa e precisava ser menor que (ou igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="0374c-1108">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="0374c-1109">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="0374c-1109">(GH #1048)</span></span>
- <span data-ttu-id="0374c-1110">Implementado retorno de chamada statfs para procfs, sysfs, cgroupfs e binfmtfs (GH 1378)</span><span class="sxs-lookup"><span data-stu-id="0374c-1110">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="0374c-1111">Correção das janelas AptPackageIndexUpdate que não eram fechadas (GH 1184, também abordado em GH 1193)</span><span class="sxs-lookup"><span data-stu-id="0374c-1111">Fixed AptPackageIndexUpdate windows that won't close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="0374c-1112">Adicionado suporte a ADDR_NO_RANDOMIZE de personalidade de ASLR.</span><span class="sxs-lookup"><span data-stu-id="0374c-1112">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="0374c-1113">(GH 1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="0374c-1113">(GH #1148, 1128)</span></span>
- <span data-ttu-id="0374c-1114">Melhoria de PTRACE_GETSIGINFO e SIGSEGV para rastreamentos de pilha gdb apropriados durante o AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="0374c-1114">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="0374c-1115">A análise de ELF não falha mais para binários patchelf.</span><span class="sxs-lookup"><span data-stu-id="0374c-1115">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="0374c-1116">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="0374c-1116">(GH #471)</span></span>
- <span data-ttu-id="0374c-1117">DNS de VPN propagado para /etc/resolv.conf (GH 416, 1350)</span><span class="sxs-lookup"><span data-stu-id="0374c-1117">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="0374c-1118">Melhorias no fechamento de TCP para transferência de dados mais confiável.</span><span class="sxs-lookup"><span data-stu-id="0374c-1118">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="0374c-1119">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="0374c-1119">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="0374c-1120">Agora, o código de erro correto é retornado quando muitos arquivos estão abertos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="0374c-1120">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="0374c-1121">(GH 1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="0374c-1121">(GH #1126, 2090)</span></span>
- <span data-ttu-id="0374c-1122">O log de auditoria do Windows agora relata o nome da imagem no processo create audit.</span><span class="sxs-lookup"><span data-stu-id="0374c-1122">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="0374c-1123">Agora, falha normalmente ao iniciar bash.exe de dentro de uma janela do Bash</span><span class="sxs-lookup"><span data-stu-id="0374c-1123">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="0374c-1124">Mensagem de erro adicionada quando a interop não consegue acessar um diretório de trabalho em LxFs (ou seja, notepad.exe. bashrc)</span><span class="sxs-lookup"><span data-stu-id="0374c-1124">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="0374c-1125">Corrigido o problema em que o caminho do Windows era truncado no WSL</span><span class="sxs-lookup"><span data-stu-id="0374c-1125">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="0374c-1126">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1126">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1127">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1127">LTP Results:</span></span>
<span data-ttu-id="0374c-1128">Número de testes aprovados: 690</span><span class="sxs-lookup"><span data-stu-id="0374c-1128">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="0374c-1129">Número de não aprovados (com falha, ignorados, etc.): 274</span><span class="sxs-lookup"><span data-stu-id="0374c-1129">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="0374c-1130">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1130">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1131">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1131">Syscall Support</span></span>
<span data-ttu-id="0374c-1132">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1132">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1133">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1133">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="0374c-1134">Build 14986</span><span class="sxs-lookup"><span data-stu-id="0374c-1134">Build 14986</span></span>

<span data-ttu-id="0374c-1135">Para obter informações gerais do Windows sobre o Build 14986, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1135">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1136">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1136">Fixed</span></span>

- <span data-ttu-id="0374c-1137">Correção de verificações de bugs com NetLink e IOCTLs pty</span><span class="sxs-lookup"><span data-stu-id="0374c-1137">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="0374c-1138">A versão do kernel agora relata 4.4.0-43 para consistência com o Xenial</span><span class="sxs-lookup"><span data-stu-id="0374c-1138">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="0374c-1139">O bash.exe agora é iniciado quando a entrada é direcionada para 'nul:' (GH 1259)</span><span class="sxs-lookup"><span data-stu-id="0374c-1139">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="0374c-1140">IDs de thread agora são relatadas corretamente em procfs (GH 967)</span><span class="sxs-lookup"><span data-stu-id="0374c-1140">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="0374c-1141">Os sinalizadores IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR agora são compatíveis com inotify_add_watch() (GH 1280)</span><span class="sxs-lookup"><span data-stu-id="0374c-1141">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="0374c-1142">Implementado timer_create e chamadas de sistema relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0374c-1142">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="0374c-1143">Isso habilita o suporte a GHC (GH 307)</span><span class="sxs-lookup"><span data-stu-id="0374c-1143">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="0374c-1144">Corrigido o problema em que o ping retornava um tempo de 0,000 ms (GH 1296)</span><span class="sxs-lookup"><span data-stu-id="0374c-1144">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="0374c-1145">O código de erro correto é retornado quando muitos arquivos estão abertos.</span><span class="sxs-lookup"><span data-stu-id="0374c-1145">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="0374c-1146">Corrigido o problema no WSL em que a solicitação do NetLink para dados do adaptador de rede falharia com EINVAL se o endereço de hardware do adaptador fosse de 32 bytes (assim como na interface Teredo)</span><span class="sxs-lookup"><span data-stu-id="0374c-1146">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="0374c-1147">Observe que o utilitário "ip" do Linux contém um bug que faz com que ele falhe se o WSL relata um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="0374c-1147">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="0374c-1148">Esse é um bug em "ip", não no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1148">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="0374c-1149">O utilitário "ip" embute em código o tamanho do buffer de cadeia de caracteres usado para imprimir o endereço de hardware, e esse buffer é muito pequeno para imprimir um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="0374c-1149">The "ip" utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="0374c-1150">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1150">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1151">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1151">LTP Results:</span></span>
<span data-ttu-id="0374c-1152">Número de testes aprovados: 669</span><span class="sxs-lookup"><span data-stu-id="0374c-1152">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="0374c-1153">Número de não aprovados (com falha, ignorados, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="0374c-1153">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="0374c-1154">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1154">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1155">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1155">Syscall Support</span></span>
<span data-ttu-id="0374c-1156">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1156">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1157">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1157">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="0374c-1158">Build 14971</span><span class="sxs-lookup"><span data-stu-id="0374c-1158">Build 14971</span></span>

<span data-ttu-id="0374c-1159">Para obter informações gerais do Windows sobre o Build 14971, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1159">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1160">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1160">Fixed</span></span>

 - <span data-ttu-id="0374c-1161">Devido a circunstâncias além do nosso controle, não há atualizações nesse build para o Subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="0374c-1161">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="0374c-1162">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-1162">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1163">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1163">LTP Results:</span></span>
<span data-ttu-id="0374c-1164">Inalterado desde o 14965</span><span class="sxs-lookup"><span data-stu-id="0374c-1164">Unchanged from 14965</span></span> </br>
<span data-ttu-id="0374c-1165">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="0374c-1165">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="0374c-1166">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="0374c-1166">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="0374c-1167">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1167">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="0374c-1168">Build 14965</span><span class="sxs-lookup"><span data-stu-id="0374c-1168">Build 14965</span></span>

<span data-ttu-id="0374c-1169">Para obter informações gerais do Windows sobre o Build 14965, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1169">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1170">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1170">Fixed</span></span>

- <span data-ttu-id="0374c-1171">Suporte para RTM_GETLINK e RTM_GETADDR do protocolo NETLINK_ROUTE de soquetes NetLink (GH 468)</span><span class="sxs-lookup"><span data-stu-id="0374c-1171">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="0374c-1172">Habilita os comandos ip e ifconfig para enumeração de rede</span><span class="sxs-lookup"><span data-stu-id="0374c-1172">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="0374c-1173">Mais informações podem ser encontradas em nossa [postagem no blog de rede WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1173">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="0374c-1174">/sbin agora está no caminho do usuário por padrão</span><span class="sxs-lookup"><span data-stu-id="0374c-1174">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="0374c-1175">O caminho de usuário do NT agora é acrescentado ao caminho do WSL por padrão (ou seja, agora você pode digitar notepad.exe sem adicionar System32 ao caminho do Linux)</span><span class="sxs-lookup"><span data-stu-id="0374c-1175">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="0374c-1176">Adicionado suporte para /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="0374c-1176">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="0374c-1177">Os binários do NT agora podem ser iniciados do WSL quando o diretório de trabalho atual contém caracteres não ANSI (GH 1254)</span><span class="sxs-lookup"><span data-stu-id="0374c-1177">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="0374c-1178">Permissão para o desligamento no soquete de fluxo do Unix desconectado.</span><span class="sxs-lookup"><span data-stu-id="0374c-1178">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="0374c-1179">Adicionado suporte para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="0374c-1179">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="0374c-1180">Adicionado suporte para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="0374c-1180">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="0374c-1181">Corrigido o erro em que o pipe fica preso, ou seja, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="0374c-1181">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="0374c-1182">Manipulação das solicitações para se conectar ao terminal atual.</span><span class="sxs-lookup"><span data-stu-id="0374c-1182">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="0374c-1183">Marcação de /proc/<pid>/oom_score_adj como gravável.</span><span class="sxs-lookup"><span data-stu-id="0374c-1183">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="0374c-1184">Adição da pasta/sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="0374c-1184">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="0374c-1185">sched_setaffinity deve retornar o número de máscara de bits de afinidade</span><span class="sxs-lookup"><span data-stu-id="0374c-1185">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="0374c-1186">Correção da lógica de validação ELF que pressupõe incorretamente que os caminhos do interpretador devem ter menos de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0374c-1186">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="0374c-1187">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="0374c-1187">(GH #743)</span></span>
- <span data-ttu-id="0374c-1188">Descritores de arquivo abertos podem manter a janela do console aberta (GH 1187)</span><span class="sxs-lookup"><span data-stu-id="0374c-1188">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="0374c-1189">Corrigido um erro em que rename() falhava com barra à direita no nome de destino (GH 1008)</span><span class="sxs-lookup"><span data-stu-id="0374c-1189">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="0374c-1190">Implementação de /proc/net/dev file</span><span class="sxs-lookup"><span data-stu-id="0374c-1190">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="0374c-1191">Corrigida a ocorrência de pings de 0,000 ms devido à resolução do timer.</span><span class="sxs-lookup"><span data-stu-id="0374c-1191">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="0374c-1192">Implementado /proc/self/environ (GH 730)</span><span class="sxs-lookup"><span data-stu-id="0374c-1192">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="0374c-1193">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1193">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1194">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1194">LTP Results:</span></span>
<span data-ttu-id="0374c-1195">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="0374c-1195">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="0374c-1196">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="0374c-1196">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="0374c-1197">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1197">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="0374c-1198">Build 14959</span><span class="sxs-lookup"><span data-stu-id="0374c-1198">Build 14959</span></span>

<span data-ttu-id="0374c-1199">Para obter informações gerais do Windows sobre o Build 14959, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="0374c-1199">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1200">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1200">Fixed</span></span>

- <span data-ttu-id="0374c-1201">Notificação de processo Pico aprimorada para Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-1201">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="0374c-1202">Informações adicionais encontradas no [blog do WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1202">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="0374c-1203">Estabilidade aprimorada com a interop do Windows</span><span class="sxs-lookup"><span data-stu-id="0374c-1203">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="0374c-1204">Corrigido o erro 0x80070057 ao iniciar o bash.exe quando a EDP (proteção de dados empresariais) está habilitada</span><span class="sxs-lookup"><span data-stu-id="0374c-1204">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="0374c-1205">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1205">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1206">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1206">LTP Results:</span></span>
<span data-ttu-id="0374c-1207">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="0374c-1207">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="0374c-1208">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="0374c-1208">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="0374c-1209">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1209">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="0374c-1210">Build 14955</span><span class="sxs-lookup"><span data-stu-id="0374c-1210">Build 14955</span></span>

<span data-ttu-id="0374c-1211">Para obter informações gerais do Windows sobre o Build 14955, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="0374c-1211">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1212">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1212">Fixed</span></span>

 - <span data-ttu-id="0374c-1213">Devido a circunstâncias além do nosso controle, não há atualizações nesse build para o Subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="0374c-1213">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="0374c-1214">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-1214">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1215">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1215">LTP Results:</span></span>
<span data-ttu-id="0374c-1216">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="0374c-1216">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="0374c-1217">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="0374c-1217">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="0374c-1218">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1218">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="0374c-1219">Build 14951</span><span class="sxs-lookup"><span data-stu-id="0374c-1219">Build 14951</span></span>

<span data-ttu-id="0374c-1220">Para obter informações gerais do Windows sobre o Build 14951, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1220">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="0374c-1221">Novo recurso: Interoperabilidade entre Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="0374c-1221">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="0374c-1222">Os binários do Windows agora podem ser chamados diretamente da linha de comando do WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1222">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="0374c-1223">Isso dá aos usuários a capacidade de interagir com o ambiente e o sistema do Windows de uma maneira que não era possível.</span><span class="sxs-lookup"><span data-stu-id="0374c-1223">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="0374c-1224">Como um exemplo rápido, agora é possível que os usuários executem os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="0374c-1224">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="0374c-1225">Mais informações podem ser encontradas em:</span><span class="sxs-lookup"><span data-stu-id="0374c-1225">More information can be found at:</span></span>

- [<span data-ttu-id="0374c-1226">Blog da equipe do WSL para interop</span><span class="sxs-lookup"><span data-stu-id="0374c-1226">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="0374c-1227">Documentação de interop do MSDN</span><span class="sxs-lookup"><span data-stu-id="0374c-1227">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="0374c-1228">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1228">Fixed</span></span>

- <span data-ttu-id="0374c-1229">O Ubuntu 16.04 (Xenial) agora está instalado para todas as novas instâncias de WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1229">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="0374c-1230">Os usuários com instâncias 14.04 (confiáveis) existentes não serão atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0374c-1230">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="0374c-1231">A localidade definida durante a instalação agora é exibida</span><span class="sxs-lookup"><span data-stu-id="0374c-1231">Locale set during install is now displayed</span></span>
- <span data-ttu-id="0374c-1232">Melhorias de terminal, incluindo bugs em que o redirecionamento de um processo do WSL para um arquivo nem sempre funciona</span><span class="sxs-lookup"><span data-stu-id="0374c-1232">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="0374c-1233">O tempo de vida do console deve estar vinculado ao tempo de vida do bash.exe</span><span class="sxs-lookup"><span data-stu-id="0374c-1233">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="0374c-1234">O tamanho da janela do console deve usar um tamanho visível, não o tamanho do buffer</span><span class="sxs-lookup"><span data-stu-id="0374c-1234">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="0374c-1235">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1235">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1236">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1236">LTP Results:</span></span>
<span data-ttu-id="0374c-1237">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="0374c-1237">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="0374c-1238">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="0374c-1238">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="0374c-1239">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1239">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="0374c-1240">Build 14946</span><span class="sxs-lookup"><span data-stu-id="0374c-1240">Build 14946</span></span>

<span data-ttu-id="0374c-1241">Para obter informações gerais do Windows sobre o Build 14946, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="0374c-1241">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1242">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1242">Fixed</span></span>

- <span data-ttu-id="0374c-1243">Corrigido um problema que impedia a criação de contas de usuário do WSL para usuários com nomes de usuário NT contendo espaços ou aspas.</span><span class="sxs-lookup"><span data-stu-id="0374c-1243">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="0374c-1244">Altere VolFs e DrvFs para retornar 0 para a contagem de links do diretório em stat</span><span class="sxs-lookup"><span data-stu-id="0374c-1244">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="0374c-1245">Suporte à opção de soquete IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="0374c-1245">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="0374c-1246">Limite para um loop de E/S de console único por tty.</span><span class="sxs-lookup"><span data-stu-id="0374c-1246">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="0374c-1247">Por exemplo, o comando a seguir é possível:</span><span class="sxs-lookup"><span data-stu-id="0374c-1247">Example: the following command is possible:</span></span>
  - <span data-ttu-id="0374c-1248">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="0374c-1248">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="0374c-1249">substituição de espaços por tabulações em /proc/cpuinfo (GH 1115)</span><span class="sxs-lookup"><span data-stu-id="0374c-1249">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="0374c-1250">O DrvFs agora aparece em mountinfo com um nome que corresponde ao volume do Windows montado</span><span class="sxs-lookup"><span data-stu-id="0374c-1250">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="0374c-1251">/home e /root agora aparecem em mountinfo com os nomes corretos</span><span class="sxs-lookup"><span data-stu-id="0374c-1251">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="0374c-1252">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1252">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1253">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1253">LTP Results:</span></span>
<span data-ttu-id="0374c-1254">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="0374c-1254">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="0374c-1255">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="0374c-1255">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="0374c-1256">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1256">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="0374c-1257">Build 14942</span><span class="sxs-lookup"><span data-stu-id="0374c-1257">Build 14942</span></span>

<span data-ttu-id="0374c-1258">Para obter informações gerais do Windows sobre o Build 14942, visite o [blog do Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="0374c-1258">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1259">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1259">Fixed</span></span>

- <span data-ttu-id="0374c-1260">Correção de várias verificações de bug, incluindo a falha de rede "TENTATIVA DE EXECUTAR A MEMÓRIA NOEXECUTE", que bloqueava o SSH</span><span class="sxs-lookup"><span data-stu-id="0374c-1260">A number of bugchecks addressed, including the "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" networking crash which was blocking SSH</span></span>
- <span data-ttu-id="0374c-1261">o suporte do inotifiy para notificações geradas de aplicativos do Windows no DrvFs agora está em</span><span class="sxs-lookup"><span data-stu-id="0374c-1261">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="0374c-1262">Implementação de TCP_KEEPIDLE e TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="0374c-1262">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="0374c-1263">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="0374c-1263">(GH #695)</span></span>
- <span data-ttu-id="0374c-1264">Implementação da chamada do sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="0374c-1264">Implement the pivot_root system call</span></span>
- <span data-ttu-id="0374c-1265">Implementar opção de soquete para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="0374c-1265">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="0374c-1266">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1266">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="0374c-1267">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1267">LTP Results:</span></span>
<span data-ttu-id="0374c-1268">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="0374c-1268">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="0374c-1269">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="0374c-1269">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="0374c-1270">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1270">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1271">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1271">Syscall Support</span></span>
<span data-ttu-id="0374c-1272">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1272">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1273">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1273">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="0374c-1274">Build 14936</span><span class="sxs-lookup"><span data-stu-id="0374c-1274">Build 14936</span></span>

<span data-ttu-id="0374c-1275">Para obter informações gerais do Windows sobre o Build 14936, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1275">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="0374c-1276">Observação: O WSL instalará o Ubuntu versão 16.04 (Xenial) em vez do Ubuntu 14.04 (Trusty) em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="0374c-1276">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="0374c-1277">Essa alteração se aplicará a Participantes do Programa Windows Insider que estejam instalando novas instâncias (lxrun.exe /install ou primeira execução de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="0374c-1277">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="0374c-1278">As instâncias existentes com Trusty não serão atualizadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0374c-1278">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="0374c-1279">Os usuários podem atualizar sua imagem do Trusty para Xenial usando o comando do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="0374c-1279">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="0374c-1280">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="0374c-1280">Known Issue</span></span>
<span data-ttu-id="0374c-1281">O WSL está enfrentando um problema com algumas implementações de soquete.</span><span class="sxs-lookup"><span data-stu-id="0374c-1281">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="0374c-1282">A verificação de bug se manifesta como uma falha com o erro "TENTATIVA DE EXECUTAR A MEMÓRIA NOEXECUTE".</span><span class="sxs-lookup"><span data-stu-id="0374c-1282">The bugcheck manifests itself as a crash with the error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span></span>  <span data-ttu-id="0374c-1283">A manifestação mais comum desse problema é uma falha ao usar SSH.</span><span class="sxs-lookup"><span data-stu-id="0374c-1283">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="0374c-1284">A causa raiz é corrigida em builds internos e será enviada por push para pessoas na primeira oportunidade.</span><span class="sxs-lookup"><span data-stu-id="0374c-1284">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="0374c-1285">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1285">Fixed</span></span>

- <span data-ttu-id="0374c-1286">Implementada a chamada do sistema chroot</span><span class="sxs-lookup"><span data-stu-id="0374c-1286">Implemented the chroot system call</span></span>
- <span data-ttu-id="0374c-1287">Melhorias no inotifiy ~~incluindo suporte para notificações geradas de aplicativos do Windows no DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="0374c-1287">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="0374c-1288">Correção: O suporte do INotifyPropertyChanged para alterações provenientes de aplicativos do Windows não estão disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1288">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="0374c-1289">Associação de soquete a IPV6::<port n> agora dá suporte a IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996)</span><span class="sxs-lookup"><span data-stu-id="0374c-1289">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="0374c-1290">Comportamento de WNOWAIT implementado para a chamada do sistema waitid (GH 638)</span><span class="sxs-lookup"><span data-stu-id="0374c-1290">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="0374c-1291">Suporte para as opções de soquete de IP IP_HDRINCL e IP_TTL</span><span class="sxs-lookup"><span data-stu-id="0374c-1291">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="0374c-1292">read() de tamanho zero deve retornar imediatamente (GH 975)</span><span class="sxs-lookup"><span data-stu-id="0374c-1292">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="0374c-1293">Manipulação correta de nomes de arquivos e prefixos de nome de arquivo que não incluem um terminador nulo em um arquivo .tar.</span><span class="sxs-lookup"><span data-stu-id="0374c-1293">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="0374c-1294">Suporte do epoll para/dev/null</span><span class="sxs-lookup"><span data-stu-id="0374c-1294">epoll support for /dev/null</span></span>
- <span data-ttu-id="0374c-1295">Correção da origem de tempo /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="0374c-1295">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="0374c-1296">Bash-c agora é capaz de redirecionar para um arquivo</span><span class="sxs-lookup"><span data-stu-id="0374c-1296">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="0374c-1297">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1297">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1298">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1298">LTP Results:</span></span>
<span data-ttu-id="0374c-1299">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="0374c-1299">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="0374c-1300">Número de não aprovados (com falha, ignorados, etc.): 264</span><span class="sxs-lookup"><span data-stu-id="0374c-1300">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="0374c-1301">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1301">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1302">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1302">Syscall Support</span></span>
<span data-ttu-id="0374c-1303">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1303">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1304">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1304">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="0374c-1305">Build 14931</span><span class="sxs-lookup"><span data-stu-id="0374c-1305">Build 14931</span></span>

<span data-ttu-id="0374c-1306">Para obter informações gerais do Windows sobre o Build 14931, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1306">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1307">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1307">Fixed</span></span>

 - <span data-ttu-id="0374c-1308">Devido a circunstâncias além do nosso controle, não há atualizações nesse build para o Subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="0374c-1308">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="0374c-1309">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="0374c-1309">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="0374c-1310">Build 14926</span><span class="sxs-lookup"><span data-stu-id="0374c-1310">Build 14926</span></span>

<span data-ttu-id="0374c-1311">Para obter informações gerais do Windows sobre o Build 14926, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1311">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1312">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1312">Fixed</span></span>

- <span data-ttu-id="0374c-1313">O ping agora funciona em consoles sem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="0374c-1313">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="0374c-1314">O Ping6 agora é compatível, inclusive quando sem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="0374c-1314">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="0374c-1315">Suporte a INotifyPropertyChanged para arquivos modificados por meio de WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1315">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="0374c-1316">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="0374c-1316">(GH #216)</span></span>
  - <span data-ttu-id="0374c-1317">Sinalizadores compatíveis:</span><span class="sxs-lookup"><span data-stu-id="0374c-1317">Flags supported:</span></span>
    - <span data-ttu-id="0374c-1318">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="0374c-1318">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="0374c-1319">Eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="0374c-1319">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="0374c-1320">Atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="0374c-1320">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="0374c-1321">saída de leitura: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="0374c-1321">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="0374c-1322">Problema conhecido: a modificação de arquivos de aplicativos do Windows não gera nenhum evento</span><span class="sxs-lookup"><span data-stu-id="0374c-1322">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="0374c-1323">O soquete Unix agora dá suporte a SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="0374c-1323">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="0374c-1324">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="0374c-1324">LTP Results:</span></span>
<span data-ttu-id="0374c-1325">Número de testes aprovados: 651</span><span class="sxs-lookup"><span data-stu-id="0374c-1325">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="0374c-1326">Número de não aprovados (com falha, ignorados, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="0374c-1326">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="0374c-1327">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="0374c-1327">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="0374c-1328">Build 14915</span><span class="sxs-lookup"><span data-stu-id="0374c-1328">Build 14915</span></span>

<span data-ttu-id="0374c-1329">Para obter informações gerais do Windows sobre o Build 14915, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="0374c-1329">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1330">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1330">Fixed</span></span>
-  <span data-ttu-id="0374c-1331">Par de soquetes para soquetes de datagramas Unix (GH 262)</span><span class="sxs-lookup"><span data-stu-id="0374c-1331">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="0374c-1332">Suporte a soquetes Unix para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="0374c-1332">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="0374c-1333">Suporte a soquetes Unix para SO_BROADCAST (GH 568)</span><span class="sxs-lookup"><span data-stu-id="0374c-1333">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="0374c-1334">Suporte a soquetes Unix para SOCK_SEQPACKET (GH 758, 546)</span><span class="sxs-lookup"><span data-stu-id="0374c-1334">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="0374c-1335">Adição de suporte para envio, recebimento e desligamento de soquete de datagrama Unix</span><span class="sxs-lookup"><span data-stu-id="0374c-1335">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="0374c-1336">Correção de verificação de bugs devido à validação de parâmetro mmap inválida para endereços não fixos.</span><span class="sxs-lookup"><span data-stu-id="0374c-1336">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="0374c-1337">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="0374c-1337">(GH #847)</span></span>
- <span data-ttu-id="0374c-1338">Suporte para suspensão/retomada de estados de terminal</span><span class="sxs-lookup"><span data-stu-id="0374c-1338">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="0374c-1339">Suporte para ioctl TIOCPKT para desbloquear o utilitário de tela (GH 774)</span><span class="sxs-lookup"><span data-stu-id="0374c-1339">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="0374c-1340">Problema conhecido: Teclas de função não operacionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1340">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="0374c-1341">Correção de uma corrida em TimerFd que poderia fazer com que um membro 'ReaderReady' liberado fosse acessado pelo LxpTimerFdWorkerRoutine (GH 814)</span><span class="sxs-lookup"><span data-stu-id="0374c-1341">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="0374c-1342">Habilitar suporte à chamada do sistema reiniciável para futex, poll e clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="0374c-1342">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="0374c-1343">Adicionado suporte à montagem de associação</span><span class="sxs-lookup"><span data-stu-id="0374c-1343">Added bind mount support</span></span>
- <span data-ttu-id="0374c-1344">suporte a descompartilhamento para namespace de montagem</span><span class="sxs-lookup"><span data-stu-id="0374c-1344">unshare for mount namespace support</span></span>
    - <span data-ttu-id="0374c-1345">Problema conhecido: Ao criar um novo namespace de montagem `unshare(CLONE_NEWNS)` com o diretório de trabalho atual, ele continuará a apontar para o namespace antigo</span><span class="sxs-lookup"><span data-stu-id="0374c-1345">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="0374c-1346">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1346">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="0374c-1347">Build 14905</span><span class="sxs-lookup"><span data-stu-id="0374c-1347">Build 14905</span></span>

<span data-ttu-id="0374c-1348">Para obter informações gerais do Windows sobre o Build 14905, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1348">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1349">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1349">Fixed</span></span>
- <span data-ttu-id="0374c-1350">Agora, as chamadas reiniciáveis do sistema são compatíveis (GH 349, GH 520)</span><span class="sxs-lookup"><span data-stu-id="0374c-1350">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="0374c-1351">Symlinks para diretórios que terminam em / agora estão operacionais (GH 650)</span><span class="sxs-lookup"><span data-stu-id="0374c-1351">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="0374c-1352">Ioctl RNDGETENTCNT implementado para /dev/random</span><span class="sxs-lookup"><span data-stu-id="0374c-1352">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="0374c-1353">Implementados os arquivos /proc/[pid]/mounts, /proc/[pid]/mountinfo e /proc/[pid]/mountstats</span><span class="sxs-lookup"><span data-stu-id="0374c-1353">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="0374c-1354">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1354">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="0374c-1355">Build 14901</span><span class="sxs-lookup"><span data-stu-id="0374c-1355">Build 14901</span></span>
<span data-ttu-id="0374c-1356">Primeiro build de Participante do Programa Windows Insider para a versão de Atualização de Aniversário do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0374c-1356">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="0374c-1357">Para obter informações gerais do Windows sobre o Build 14901, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1357">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1358">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1358">Fixed</span></span>
- <span data-ttu-id="0374c-1359">Corrigido problema de barra à direita</span><span class="sxs-lookup"><span data-stu-id="0374c-1359">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="0374c-1360">Comandos como `$ mv a/c/ a/b/` agora funcionam</span><span class="sxs-lookup"><span data-stu-id="0374c-1360">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="0374c-1361">A instalação agora avisa se a localidade do Ubuntu deve ser definida como a localidade do Windows</span><span class="sxs-lookup"><span data-stu-id="0374c-1361">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="0374c-1362">Suporte do procfs para a pasta ns</span><span class="sxs-lookup"><span data-stu-id="0374c-1362">Procfs support for ns folder</span></span>
- <span data-ttu-id="0374c-1363">Adição de montagem e desmontagem para sistemas de arquivos tmpfs, procfs e sysfs</span><span class="sxs-lookup"><span data-stu-id="0374c-1363">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="0374c-1364">Corrigir a assinatura da ABI de 32 bits mknod[at]</span><span class="sxs-lookup"><span data-stu-id="0374c-1364">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="0374c-1365">Soquetes Unix movidos para o modelo de expedição</span><span class="sxs-lookup"><span data-stu-id="0374c-1365">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="0374c-1366">O tamanho do buffer de recebimento do soquete INET definido usando o setsockopt deve ser respeitado</span><span class="sxs-lookup"><span data-stu-id="0374c-1366">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="0374c-1367">Implementação do sinalizador de mensagem de recebimento do soquete do Unix MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="0374c-1367">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="0374c-1368">Redirecionamento de pipe stdin/stdout de processo do Linux (GH 2)</span><span class="sxs-lookup"><span data-stu-id="0374c-1368">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="0374c-1369">Permite o pipe de comandos bash -c no cmd.</span><span class="sxs-lookup"><span data-stu-id="0374c-1369">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="0374c-1370">Exemplo: >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="0374c-1370">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="0374c-1371">O Bash agora pode ser instalado em sistemas com diversos arquivos de paginação (GH 538, 358)</span><span class="sxs-lookup"><span data-stu-id="0374c-1371">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="0374c-1372">O tamanho do buffer do soquete INET padrão deve corresponder ao da configuração padrão do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="0374c-1372">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="0374c-1373">Alinhamento de syscalls xattr a listxattr</span><span class="sxs-lookup"><span data-stu-id="0374c-1373">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="0374c-1374">SIOCGIFCONF retorna apenas interfaces com um IPv4 válido</span><span class="sxs-lookup"><span data-stu-id="0374c-1374">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="0374c-1375">Correção da ação padrão de sinal quando injetado por ptrace</span><span class="sxs-lookup"><span data-stu-id="0374c-1375">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="0374c-1376">Implementação de /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="0374c-1376">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="0374c-1377">Uso de valores de registro de contexto de computador ao restaurar o contexto em sigreturn</span><span class="sxs-lookup"><span data-stu-id="0374c-1377">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="0374c-1378">Isso resolve o problema em que java e javac estavam travando para alguns usuários</span><span class="sxs-lookup"><span data-stu-id="0374c-1378">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="0374c-1379">Implementação de /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="0374c-1379">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1380">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1380">Syscall Support</span></span>
<span data-ttu-id="0374c-1381">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1381">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1382">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1382">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="0374c-1383">Build 14388 para Atualização de Aniversário do Windows 10</span><span class="sxs-lookup"><span data-stu-id="0374c-1383">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="0374c-1384">Para obter informações gerais do Windows sobre o Build 14388, visite o [blog do Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="0374c-1384">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="0374c-1385">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1385">Fixed</span></span>
- <span data-ttu-id="0374c-1386">Correções para preparar para a Atualização de Aniversário do Windows 10 em 02/08</span><span class="sxs-lookup"><span data-stu-id="0374c-1386">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="0374c-1387">Mais informações sobre WSL na atualização de aniversário podem ser encontradas em nosso [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="0374c-1387">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="0374c-1388">Build 14376</span><span class="sxs-lookup"><span data-stu-id="0374c-1388">Build 14376</span></span>
<span data-ttu-id="0374c-1389">Para obter informações gerais do Windows sobre o Build 14376, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1389">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="0374c-1390">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1390">Fixed</span></span>
- <span data-ttu-id="0374c-1391">Removidas algumas instâncias em que apt-get trava (GH 493)</span><span class="sxs-lookup"><span data-stu-id="0374c-1391">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="0374c-1392">Corrigido um problema em que as montagens vazias não eram manipuladas corretamente</span><span class="sxs-lookup"><span data-stu-id="0374c-1392">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="0374c-1393">Corrigido um problema em que ramdisks não eram montados corretamente</span><span class="sxs-lookup"><span data-stu-id="0374c-1393">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="0374c-1394">Alteração da aceitação de soquete do Unix para dar suporte a sinalizadores (GH 451 parcial)</span><span class="sxs-lookup"><span data-stu-id="0374c-1394">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="0374c-1395">Corrigida tela azul comum relacionada à rede</span><span class="sxs-lookup"><span data-stu-id="0374c-1395">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="0374c-1396">Corrigida tela azul ao acessar /proc/[pid]/task (GH 523)</span><span class="sxs-lookup"><span data-stu-id="0374c-1396">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="0374c-1397">Correção de alta utilização de CPU para alguns cenários de pty (GH 488, 504)</span><span class="sxs-lookup"><span data-stu-id="0374c-1397">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="0374c-1398">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1398">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="0374c-1399">Build 14371</span><span class="sxs-lookup"><span data-stu-id="0374c-1399">Build 14371</span></span>
<span data-ttu-id="0374c-1400">Para obter informações gerais do Windows sobre o Build 14371, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1400">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="0374c-1401">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1401">Fixed</span></span>
- <span data-ttu-id="0374c-1402">Corrigida corrida de tempo com SIGCHLD e wait() ao usar ptrace</span><span class="sxs-lookup"><span data-stu-id="0374c-1402">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="0374c-1403">Corrigido algum comportamento quando os caminhos têm uma / à direita (GH 432)</span><span class="sxs-lookup"><span data-stu-id="0374c-1403">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="0374c-1404">Corrigido um problema de falha ao renomear/desvincular devido a identificadores abertos para filhos</span><span class="sxs-lookup"><span data-stu-id="0374c-1404">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="0374c-1405">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1405">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="0374c-1406">Build 14366</span><span class="sxs-lookup"><span data-stu-id="0374c-1406">Build 14366</span></span>
<span data-ttu-id="0374c-1407">Para obter informações gerais do Windows sobre o Build 14366, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="0374c-1407">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="0374c-1408">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1408">Fixed</span></span>
- <span data-ttu-id="0374c-1409">Correção na criação de arquivo por meio de symlinks</span><span class="sxs-lookup"><span data-stu-id="0374c-1409">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="0374c-1410">Adicionado listxattr para o Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="0374c-1410">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="0374c-1411">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1411">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1412">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1412">Syscall Support</span></span>
-   <span data-ttu-id="0374c-1413">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1413">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1414">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1414">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="0374c-1415">Build 14361</span><span class="sxs-lookup"><span data-stu-id="0374c-1415">Build 14361</span></span>
<span data-ttu-id="0374c-1416">Para obter informações gerais do Windows sobre o Build 14361, visite o [blog do Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="0374c-1416">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="0374c-1417">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1417">Fixed</span></span>
- <span data-ttu-id="0374c-1418">O DrvFs agora diferencia maiúsculas de minúsculas ao executar no Bash usando Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-1418">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="0374c-1419">Os usuários podem usar case.txt e CASE.TXT nas respectivas unidades /mnt/c</span><span class="sxs-lookup"><span data-stu-id="0374c-1419">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="0374c-1420">A diferenciação de maiúsculas e minúsculas só é compatível no Bash usando Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-1420">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="0374c-1421">Quando fora do Bash, o NTFS relatará os arquivos corretamente, mas um comportamento inesperado poderá ocorrer ao interagir com os arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-1421">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="0374c-1422">A raiz de cada volume (ou seja, /mnt/c) não diferencia maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="0374c-1422">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="0374c-1423">É possível encontrar mais informações sobre como manipular esses arquivos no Windows [aqui](https://support.microsoft.com/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="0374c-1423">More information on handling these files in Windows can be found [here](https://support.microsoft.com/kb/100625).</span></span>
- <span data-ttu-id="0374c-1424">Suporte a pty/tty bastante aprimorado.</span><span class="sxs-lookup"><span data-stu-id="0374c-1424">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="0374c-1425">Aplicativos como TMUX agora são compatíveis (GH 40)</span><span class="sxs-lookup"><span data-stu-id="0374c-1425">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="0374c-1426">Corrigido um problema de instalação em que as contas de usuário nem sempre eram criadas</span><span class="sxs-lookup"><span data-stu-id="0374c-1426">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="0374c-1427">Estrutura de argumentos de linha de comando otimizada que permite uma lista de argumentos extremamente longa.</span><span class="sxs-lookup"><span data-stu-id="0374c-1427">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="0374c-1428">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="0374c-1428">(GH #153)</span></span>
- <span data-ttu-id="0374c-1429">Agora é possível excluir e usar chmod em arquivos read_only do DrvFs</span><span class="sxs-lookup"><span data-stu-id="0374c-1429">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="0374c-1430">Corrigidas algumas instâncias em que o terminal travava ao desconectar (GH 43)</span><span class="sxs-lookup"><span data-stu-id="0374c-1430">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="0374c-1431">chmod e chown agora funcionam em dispositivos tty</span><span class="sxs-lookup"><span data-stu-id="0374c-1431">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="0374c-1432">Permissão para conexão a 0.0.0.0 e a :: como localhost (GH 388)</span><span class="sxs-lookup"><span data-stu-id="0374c-1432">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="0374c-1433">Sendmsg/recvmsg agora aceitam um comprimento de vetor de E/S >1 (GH 376 parcial)</span><span class="sxs-lookup"><span data-stu-id="0374c-1433">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="0374c-1434">Os usuários agora podem recusar o arquivo de hosts gerado automaticamente (GH #398)</span><span class="sxs-lookup"><span data-stu-id="0374c-1434">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="0374c-1435">Correspondência automática da localidade do Linux à localidade do NT durante a instalação (GH 11)</span><span class="sxs-lookup"><span data-stu-id="0374c-1435">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="0374c-1436">Adicionado o arquivo /proc/sys/VM/swappiness (GH 306)</span><span class="sxs-lookup"><span data-stu-id="0374c-1436">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="0374c-1437">strace agora é encerrado corretamente</span><span class="sxs-lookup"><span data-stu-id="0374c-1437">strace now exits correctly</span></span>
- <span data-ttu-id="0374c-1438">Permissão para que os pipes sejam reabertos por meio de /proc/Self/FD (GH 222)</span><span class="sxs-lookup"><span data-stu-id="0374c-1438">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="0374c-1439">Ocultação de diretórios em %LOCALAPPDATA%\lxss do DrvFs (GH 270)</span><span class="sxs-lookup"><span data-stu-id="0374c-1439">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="0374c-1440">Melhor manipulação do bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="0374c-1440">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="0374c-1441">Agora, há suporte para comandos como "bash ~ -c ls" (GH 467)</span><span class="sxs-lookup"><span data-stu-id="0374c-1441">Commands like "bash ~ -c ls" now supported (GH #467)</span></span>
- <span data-ttu-id="0374c-1442">Os soquetes agora notificam que a leitura de epoll está disponível durante o desligamento (GH 271)</span><span class="sxs-lookup"><span data-stu-id="0374c-1442">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="0374c-1443">lxrun /uninstall desempenha melhor a exclusão de arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="0374c-1443">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="0374c-1444">ps-f corrigido (GH 246)</span><span class="sxs-lookup"><span data-stu-id="0374c-1444">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="0374c-1445">Suporte aprimorado para aplicativos x11, tais como xEmacs (GH 481)</span><span class="sxs-lookup"><span data-stu-id="0374c-1445">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="0374c-1446">Tamanho da pilha de thread inicial atualizado para corresponder à configuração padrão do Ubuntu e relatando o tamanho corretamente para a syscall get_rlimit (GH 172, 258)</span><span class="sxs-lookup"><span data-stu-id="0374c-1446">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="0374c-1447">Relatório aprimorado de nomes de imagem de processo do pico (por exemplo, para auditoria)</span><span class="sxs-lookup"><span data-stu-id="0374c-1447">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="0374c-1448">Implementado o /proc/mountinfo para o comando df</span><span class="sxs-lookup"><span data-stu-id="0374c-1448">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="0374c-1449">Corrigido o código de erro de symlink para o nome do filho.</span><span class="sxs-lookup"><span data-stu-id="0374c-1449">Fixed symlink error code for child name .</span></span> <span data-ttu-id="0374c-1450">e .</span><span class="sxs-lookup"><span data-stu-id="0374c-1450">and ..</span></span>
- <span data-ttu-id="0374c-1451">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1451">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1452">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1452">Syscall Support</span></span>
<span data-ttu-id="0374c-1453">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1453">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1454">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1454">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="0374c-1455">Build 14352</span><span class="sxs-lookup"><span data-stu-id="0374c-1455">Build 14352</span></span>
<span data-ttu-id="0374c-1456">Para obter informações gerais do Windows sobre o Build 14352, visite o [blog do Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="0374c-1456">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1457">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1457">Fixed</span></span>
- <span data-ttu-id="0374c-1458">Corrigido um problema em que arquivos grandes não eram baixados/criados corretamente.</span><span class="sxs-lookup"><span data-stu-id="0374c-1458">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="0374c-1459">Isso deve desbloquear o npm e outros cenários (GH 3, GH 313)</span><span class="sxs-lookup"><span data-stu-id="0374c-1459">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="0374c-1460">Removidas algumas instâncias em que soquetes travavam</span><span class="sxs-lookup"><span data-stu-id="0374c-1460">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="0374c-1461">Corrigidos alguns erros de ptrace</span><span class="sxs-lookup"><span data-stu-id="0374c-1461">Corrected some ptrace errors</span></span>
- <span data-ttu-id="0374c-1462">Corrigido um problema com o WSL permitindo nomes de arquivo maiores do que 255 caracteres</span><span class="sxs-lookup"><span data-stu-id="0374c-1462">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="0374c-1463">Suporte aprimorado para caracteres diferentes do inglês</span><span class="sxs-lookup"><span data-stu-id="0374c-1463">Improved support for non-English characters</span></span>
- <span data-ttu-id="0374c-1464">Adicionar os dados de fuso horário atual do Windows e definir como padrão</span><span class="sxs-lookup"><span data-stu-id="0374c-1464">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="0374c-1465">Identificações de dispositivo exclusivas para cada ponto de montagem (correção do JRE – GH 49)</span><span class="sxs-lookup"><span data-stu-id="0374c-1465">Unique device id's for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="0374c-1466">Correção do problema com caminhos contendo "." e ".."</span><span class="sxs-lookup"><span data-stu-id="0374c-1466">Correct issue with paths containing "." and ".."</span></span>
- <span data-ttu-id="0374c-1467">Adicionado suporte a PEPS (GH 71)</span><span class="sxs-lookup"><span data-stu-id="0374c-1467">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="0374c-1468">Atualizado formato de resolv.conf para corresponder ao formato nativo do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="0374c-1468">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="0374c-1469">Limpeza de alguns procfs</span><span class="sxs-lookup"><span data-stu-id="0374c-1469">Some procfs cleanup</span></span>
- <span data-ttu-id="0374c-1470">Ping habilitado para consoles do administrador (GH 18)</span><span class="sxs-lookup"><span data-stu-id="0374c-1470">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1471">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1471">Syscall Support</span></span>
<span data-ttu-id="0374c-1472">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1472">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1473">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1473">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="0374c-1474">Build 14342</span><span class="sxs-lookup"><span data-stu-id="0374c-1474">Build 14342</span></span>
<span data-ttu-id="0374c-1475">Para obter informações gerais do Windows sobre o Build 14342, visite o [blog do Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="0374c-1475">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="0374c-1476">Informações sobre VolFs e DriveFs podem ser encontradas no [blog do WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="0374c-1476">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="0374c-1477">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1477">Fixed</span></span>
- <span data-ttu-id="0374c-1478">Corrigido problema de instalação quando o usuário do Windows tinha caracteres Unicode no nome de usuário</span><span class="sxs-lookup"><span data-stu-id="0374c-1478">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="0374c-1479">A solução alternativa apt-get update udev nas perguntas frequentes agora é fornecida por padrão na primeira execução</span><span class="sxs-lookup"><span data-stu-id="0374c-1479">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="0374c-1480">Symlinks habilitados nos diretórios de DriveFs (/mnt/<drive>)</span><span class="sxs-lookup"><span data-stu-id="0374c-1480">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="0374c-1481">Symlinks agora funcionam entre DriveFs e VolFs</span><span class="sxs-lookup"><span data-stu-id="0374c-1481">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="0374c-1482">Problema de análise de caminho de nível superior resolvido: ls .// agora funcionará como esperado</span><span class="sxs-lookup"><span data-stu-id="0374c-1482">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="0374c-1483">A instalação de npm no DriveFs e as opções -g agora estão funcionando</span><span class="sxs-lookup"><span data-stu-id="0374c-1483">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="0374c-1484">Problema corrigido, impedindo a inicialização do servidor PHP</span><span class="sxs-lookup"><span data-stu-id="0374c-1484">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="0374c-1485">Valores de ambiente padrão atualizados, tais como $PATH para corresponder melhor ao Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="0374c-1485">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="0374c-1486">Adicionada uma tarefa de manutenção semanal no Windows para atualizar o cache do pacote apt</span><span class="sxs-lookup"><span data-stu-id="0374c-1486">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="0374c-1487">Corrigido um problema com a validação de cabeçalho ELF, o WSL agora dá suporte a todas as opções de Melkor</span><span class="sxs-lookup"><span data-stu-id="0374c-1487">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="0374c-1488">O shell do zsh está funcional</span><span class="sxs-lookup"><span data-stu-id="0374c-1488">Zsh shell is functional</span></span>
- <span data-ttu-id="0374c-1489">Binários do Go pré-compilados agora são compatíveis</span><span class="sxs-lookup"><span data-stu-id="0374c-1489">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="0374c-1490">O aviso na primeira execução do bash.exe agora está localizado corretamente</span><span class="sxs-lookup"><span data-stu-id="0374c-1490">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="0374c-1491">/proc/meminfo agora retorna informações corretas</span><span class="sxs-lookup"><span data-stu-id="0374c-1491">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="0374c-1492">Os soquetes agora são compatíveis com o VFS</span><span class="sxs-lookup"><span data-stu-id="0374c-1492">Sockets now supported in VFS</span></span>
- <span data-ttu-id="0374c-1493">/dev agora é montado como tempfs</span><span class="sxs-lookup"><span data-stu-id="0374c-1493">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="0374c-1494">PEPS agora é compatível</span><span class="sxs-lookup"><span data-stu-id="0374c-1494">Fifo now supported</span></span>
- <span data-ttu-id="0374c-1495">Sistemas de vários núcleos agora são mostrados corretamente em /proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="0374c-1495">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="0374c-1496">Aprimoramentos adicionais e mensagens de erro ao baixar durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="0374c-1496">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="0374c-1497">Melhorias e correções de bug em syscall.</span><span class="sxs-lookup"><span data-stu-id="0374c-1497">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="0374c-1498">Lista de syscalls compatíveis abaixo.</span><span class="sxs-lookup"><span data-stu-id="0374c-1498">Supported syscall list below.</span></span>
- <span data-ttu-id="0374c-1499">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1499">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="0374c-1500">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="0374c-1500">Known Issues</span></span>
- <span data-ttu-id="0374c-1501">Sem resolução para '..'</span><span class="sxs-lookup"><span data-stu-id="0374c-1501">Not resolving '..'</span></span> <span data-ttu-id="0374c-1502">corretamente no DriveFs em alguns casos</span><span class="sxs-lookup"><span data-stu-id="0374c-1502">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1503">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1503">Syscall Support</span></span>
<span data-ttu-id="0374c-1504">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1504">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="0374c-1505">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1505">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="0374c-1506">Build 14332</span><span class="sxs-lookup"><span data-stu-id="0374c-1506">Build 14332</span></span>

<span data-ttu-id="0374c-1507">Para obter informações gerais do Windows sobre o Build 14332, visite o [blog do Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="0374c-1507">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="0374c-1508">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1508">Fixed</span></span>
- <span data-ttu-id="0374c-1509">Melhor geração de resolv.conf, incluindo a priorização de entradas DNS</span><span class="sxs-lookup"><span data-stu-id="0374c-1509">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="0374c-1510">Problema com a movimentação de arquivos e diretórios entre unidades/mnt e não /mnt</span><span class="sxs-lookup"><span data-stu-id="0374c-1510">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="0374c-1511">Agora, os arquivos tar podem ser criados com symlinks</span><span class="sxs-lookup"><span data-stu-id="0374c-1511">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="0374c-1512">Diretório /run/lock padrão adicionado na criação da instância</span><span class="sxs-lookup"><span data-stu-id="0374c-1512">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="0374c-1513">Atualização de /dev/null para retornar informações de estado adequadas</span><span class="sxs-lookup"><span data-stu-id="0374c-1513">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="0374c-1514">Erros adicionais ao baixar durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="0374c-1514">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="0374c-1515">Melhorias e correções de bug em syscall.</span><span class="sxs-lookup"><span data-stu-id="0374c-1515">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="0374c-1516">Lista de syscalls compatíveis abaixo.</span><span class="sxs-lookup"><span data-stu-id="0374c-1516">Supported syscall list below.</span></span>
- <span data-ttu-id="0374c-1517">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1517">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1518">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1518">Syscall Support</span></span>
<span data-ttu-id="0374c-1519">Abaixo está a nova syscall que tem alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1519">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="0374c-1520">A syscall nessa lista é compatível com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com ela no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1520">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="0374c-1521">Build 14328</span><span class="sxs-lookup"><span data-stu-id="0374c-1521">Build 14328</span></span>

<span data-ttu-id="0374c-1522">Para obter informações gerais do Windows sobre o Build 14332, visite o [blog do Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="0374c-1522">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="0374c-1523">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="0374c-1523">New Features</span></span>
* <span data-ttu-id="0374c-1524">Agora dão suporte a usuários do Linux.</span><span class="sxs-lookup"><span data-stu-id="0374c-1524">Now support Linux users.</span></span>  <span data-ttu-id="0374c-1525">A instalação do Bash usando o Ubuntu no Windows solicitará a criação de um usuário do Linux.</span><span class="sxs-lookup"><span data-stu-id="0374c-1525">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="0374c-1526">Para obter mais informações, visite https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="0374c-1526">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="0374c-1527">O hostname agora está definido como o nome do computador Windows, não mais como @localhost</span><span class="sxs-lookup"><span data-stu-id="0374c-1527">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="0374c-1528">Para obter mais informações sobre o build 14328, visite: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="0374c-1528">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="0374c-1529">Fixo</span><span class="sxs-lookup"><span data-stu-id="0374c-1529">Fixed</span></span>
* <span data-ttu-id="0374c-1530">Aprimoramentos do symlink para arquivos não /mnt/<drive></span><span class="sxs-lookup"><span data-stu-id="0374c-1530">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="0374c-1531">A instalação de npm agora funciona</span><span class="sxs-lookup"><span data-stu-id="0374c-1531">npm install now works</span></span>
    * <span data-ttu-id="0374c-1532">Agora, o jdk/jre é instalável usando as instruções encontradas [aqui](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="0374c-1532">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="0374c-1533">problema conhecido: os symlinks não funcionam para montagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="0374c-1533">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="0374c-1534">A funcionalidade estará disponível em um build posterior</span><span class="sxs-lookup"><span data-stu-id="0374c-1534">Functionality will be available in a later build</span></span>
* <span data-ttu-id="0374c-1535">top e htop agora são exibidos</span><span class="sxs-lookup"><span data-stu-id="0374c-1535">top and htop now display</span></span>
* <span data-ttu-id="0374c-1536">Mensagens de erro adicionais para algumas falhas de instalação</span><span class="sxs-lookup"><span data-stu-id="0374c-1536">Additional error messages for some install failures</span></span>
* <span data-ttu-id="0374c-1537">Melhorias e correções de bug em syscall.</span><span class="sxs-lookup"><span data-stu-id="0374c-1537">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="0374c-1538">Lista de syscalls compatíveis abaixo.</span><span class="sxs-lookup"><span data-stu-id="0374c-1538">Supported syscall list below.</span></span>
* <span data-ttu-id="0374c-1539">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="0374c-1539">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="0374c-1540">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="0374c-1540">Syscall Support</span></span>
<span data-ttu-id="0374c-1541">Veja abaixo uma lista de syscalls que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="0374c-1541">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="0374c-1542">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="0374c-1542">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
