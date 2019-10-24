---
title: Notas sobre a versão do subsistema Windows para Linux
description: Notas sobre a versão do subsistema Windows para Linux.  Atualizado semanalmente.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: dbc041c98081563d4f77b9fc186698fad8299c0d
ms.sourcegitcommit: 4beb93f80749ab4c8c6f0e6920ab7f809567e243
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2019
ms.locfileid: "72549574"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="be873-105">Notas sobre a versão do subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="be873-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-19002"></a><span data-ttu-id="be873-106">Build 19002</span><span class="sxs-lookup"><span data-stu-id="be873-106">Build 19002</span></span>
<span data-ttu-id="be873-107">Para obter informações gerais do Windows sobre o Build 19002, acesse o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="be873-107">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="be873-108">[WSL] Correção de um problema com o tratamento de alguns caracteres Unicode: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="be873-108">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="be873-109">[WSL] Correção de casos raros em que distribuições podiam ter o registro cancelado se fossem iniciadas imediatamente após uma atualização de compilação a compilação.</span><span class="sxs-lookup"><span data-stu-id="be873-109">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="be873-110">[WSL] Correção de um problema secundário com wsl.exe: desligamentos em que os timers de ociosidade da instância não foram cancelados.</span><span class="sxs-lookup"><span data-stu-id="be873-110">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="be873-111">Build 18995</span><span class="sxs-lookup"><span data-stu-id="be873-111">Build 18995</span></span>
<span data-ttu-id="be873-112">Para obter informações gerais do Windows sobre o build 18995, acesse o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="be873-112">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="be873-113">[WSL2] Correção de um problema em que as montagens DrvFs pararam de funcionar após uma operação ter sido interrompida (por exemplo, ctrl-c) [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="be873-113">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="be873-114">[WSL2] Correção do tratamento de mensagens hvsocket muito grandes [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="be873-114">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="be873-115">[WSL2] Correção do problema com a interoperabilidade quando stdin é um arquivo [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="be873-115">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="be873-116">[WSL2] Correção da falha de serviço quando um estado de rede inesperado é encontrado [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="be873-116">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="be873-117">[WSL2] Consulta do nome da distribuição do servidor de interoperabilidade se o processo atual não tem a variável de ambiente</span><span class="sxs-lookup"><span data-stu-id="be873-117">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="be873-118">[WSL2] Correção do problema com a interoperabilidade quando stdin é um arquivo</span><span class="sxs-lookup"><span data-stu-id="be873-118">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="be873-119">[WSL2] Atualização da versão do kernel do Linux para 4.19.72</span><span class="sxs-lookup"><span data-stu-id="be873-119">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="be873-120">[WSL2] Adição da capacidade de especificar outros parâmetros de linha de comando do kernel por meio de .wslconfig</span><span class="sxs-lookup"><span data-stu-id="be873-120">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments

```

## <a name="build-18990"></a><span data-ttu-id="be873-121">Build 18990</span><span class="sxs-lookup"><span data-stu-id="be873-121">Build 18990</span></span>
<span data-ttu-id="be873-122">Para obter informações gerais do Windows sobre o Build 18990, acesse o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="be873-122">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="be873-123">Melhora do desempenho das listagens de diretório em \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="be873-123">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="be873-124">[WSL2] Injetar entropia de inicialização adicional [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="be873-124">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="be873-125">[WSL2] Correção para interoperabilidade do Windows ao usar su/sudo [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="be873-125">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="be873-126">Build 18980</span><span class="sxs-lookup"><span data-stu-id="be873-126">Build 18980</span></span>
<span data-ttu-id="be873-127">Para obter informações gerais do Windows sobre o Build 18980, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="be873-127">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="be873-128">Correção da leitura de symlinks que negam FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="be873-128">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="be873-129">Isso inclui todas as symlinks que o Windows cria para compatibilidade com versões anteriores, tais como "C:\Documentos e Configurações" e diversos symlinks no diretório de perfil do usuário</span><span class="sxs-lookup"><span data-stu-id="be873-129">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="be873-130">Transformação do estado de sistema de arquivos inesperado em não fatal [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="be873-130">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="be873-131">[WSL2] Adição de suporte para arm64 se a CPU/firmware der suporte à virtualização</span><span class="sxs-lookup"><span data-stu-id="be873-131">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="be873-132">[WSL2] Permissão para que usuários sem privilégios exibam o log do kernel</span><span class="sxs-lookup"><span data-stu-id="be873-132">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="be873-133">[WSL2] Correção da retransmissão de saída quando os soquetes stdout/stderr tiverem sido fechados [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="be873-133">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="be873-134">[WSL2] Suporte para passagem de bateria e adaptador AC</span><span class="sxs-lookup"><span data-stu-id="be873-134">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="be873-135">[WSL2] Atualização do kernel do Linux para 4.19.67</span><span class="sxs-lookup"><span data-stu-id="be873-135">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="be873-136">Adição da capacidade de definir o nome de usuário padrão em /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="be873-136">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="be873-137">Build 18975</span><span class="sxs-lookup"><span data-stu-id="be873-137">Build 18975</span></span>
<span data-ttu-id="be873-138">Para obter informações gerais do Windows sobre o Build 18975, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="be873-138">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="be873-139">[WSL2] Corrigidos diversos problemas de confiabilidade do localhost [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="be873-139">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="be873-140">Build 18970</span><span class="sxs-lookup"><span data-stu-id="be873-140">Build 18970</span></span>
<span data-ttu-id="be873-141">Para obter informações gerais do Windows sobre o Build 18970, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="be873-141">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="be873-142">[WSL2] Sincronização da hora com a hora do host quando o sistema é retomado do estado de suspensão [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="be873-142">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="be873-143">[WSL2] Criar symlinks NT nos volumes do Windows quando possível.</span><span class="sxs-lookup"><span data-stu-id="be873-143">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="be873-144">[WSL2] Criação de distribuições nos namespaces UTS, IPC, PID e Mount.</span><span class="sxs-lookup"><span data-stu-id="be873-144">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="be873-145">[WSL2] Correção da retransmissão de porta localhost quando o servidor se associar ao localhost diretamente [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="be873-145">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="be873-146">[WSL2] Correção da interop quando a saída for redirecionada [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="be873-146">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="be873-147">[WSL2] Suporte à conversão de symlinks NT absolutos.</span><span class="sxs-lookup"><span data-stu-id="be873-147">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="be873-148">[WSL2] Atualização do kernel para 4.19.59</span><span class="sxs-lookup"><span data-stu-id="be873-148">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="be873-149">[WSL2] Definição correta da máscara de sub-rede para eth0.</span><span class="sxs-lookup"><span data-stu-id="be873-149">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="be873-150">[WSL2] Alteração da lógica para interromper o loop de trabalho do console quando o evento de saída for sinalizado.</span><span class="sxs-lookup"><span data-stu-id="be873-150">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="be873-151">[WSL2] Ejeção do vhd da distribuição quando a distribuição não está em execução.</span><span class="sxs-lookup"><span data-stu-id="be873-151">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="be873-152">[WSL2] Correção da biblioteca de análise de configuração para manipular corretamente valores vazios.</span><span class="sxs-lookup"><span data-stu-id="be873-152">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="be873-153">[WSL2] Dar suporte ao Docker Desktop criando montagens para múltiplas distribuições.</span><span class="sxs-lookup"><span data-stu-id="be873-153">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="be873-154">Uma distribuição pode optar por adotar esse comportamento ao adicionar a linha a seguir ao arquivo /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="be873-154">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="be873-155">Build 18945</span><span class="sxs-lookup"><span data-stu-id="be873-155">Build 18945</span></span>
<span data-ttu-id="be873-156">Para obter informações gerais do Windows sobre o Build 18945, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="be873-156">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-157">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-157">WSL</span></span>
* <span data-ttu-id="be873-158">[WSL2] Permissão para que soquetes TCP de escuta em WSL2 sejam acessíveis do host usando localhost:port</span><span class="sxs-lookup"><span data-stu-id="be873-158">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="be873-159">[WSL2] Correções para falhas de instalação/conversão e diagnóstico adicional para rastrear problemas futuros [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="be873-159">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="be873-160">[WSL2] Melhoria da capacidade de diagnóstico de problemas de rede WSL2</span><span class="sxs-lookup"><span data-stu-id="be873-160">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="be873-161">[WSL2] Atualização da versão do kernel para 4.19.55</span><span class="sxs-lookup"><span data-stu-id="be873-161">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="be873-162">[WSL2] Atualização do kernel com as opções de configuração necessárias para o Docker [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="be873-162">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="be873-163">[WSL2] Aumento do número de CPUs atribuídas à VM do utilitário leve para que seja o mesmo do host (anteriormente limitado em 8 por CONFIG_NR_CPUS na configuração do kernel) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="be873-163">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="be873-164">[WSL2] Criação de um arquivo de permuta para a VM leve do WSL2</span><span class="sxs-lookup"><span data-stu-id="be873-164">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="be873-165">[WSL2] Permissão para que as montagens de usuário fiquem visíveis por meio de \\\\wsl$\\distro (por exemplo, sshfs) [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="be873-165">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="be873-166">[WSL2] Melhoria do desempenho do sistema de arquivos 9p</span><span class="sxs-lookup"><span data-stu-id="be873-166">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="be873-167">[WSL2] Garantia de que a ACL do VHD não aumente sem limite [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="be873-167">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="be873-168">[WSL2] Atualização da configuração do kernel para dar suporte a squashfs e xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="be873-168">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="be873-169">[WSL2] Correção para a opção interop.enabled /etc/wsl.conf [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="be873-169">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="be873-170">[WSL2] Retorno de ENOTSUP se o sistema de arquivos não der suporte a EAs</span><span class="sxs-lookup"><span data-stu-id="be873-170">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="be873-171">[WSL2] Correção do travamento de CopyFile com \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="be873-171">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="be873-172">Alternância do umask padrão para 0022 e adição da configuração filesystem.umask a /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="be873-172">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="be873-173">Correção de wslpath para resolver symlinks adequadamente, isso foi regredido em 19h1 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="be873-173">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="be873-174">Introdução do arquivo %UserProfile%\\.wslconfig para ajuste de configurações WSL2</span><span class="sxs-lookup"><span data-stu-id="be873-174">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="be873-175">Build 18917</span><span class="sxs-lookup"><span data-stu-id="be873-175">Build 18917</span></span>
<span data-ttu-id="be873-176">Para obter informações gerais do Windows sobre o Build 18917, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="be873-176">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-177">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-177">WSL</span></span>
* <span data-ttu-id="be873-178">O WSL 2 já está disponível.</span><span class="sxs-lookup"><span data-stu-id="be873-178">WSL 2 is now available!</span></span> <span data-ttu-id="be873-179">Confira o [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="be873-179">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="be873-180">Correção de uma regressão em que a inicialização de processos do Windows via symlinks não funcionou corretamente [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="be873-180">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="be873-181">Adição das opções wsl.exe --list --verbose, wsl.exe --list --quiet e wsl.exe --import --version a wsl.exe</span><span class="sxs-lookup"><span data-stu-id="be873-181">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="be873-182">Adição da opção wsl.exe --shutdown</span><span class="sxs-lookup"><span data-stu-id="be873-182">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="be873-183">Plano 9: Permissão para que a abertura de um diretório para gravação seja realizada com sucesso</span><span class="sxs-lookup"><span data-stu-id="be873-183">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="be873-184">Build 18890</span><span class="sxs-lookup"><span data-stu-id="be873-184">Build 18890</span></span>
<span data-ttu-id="be873-185">Para obter informações gerais do Windows sobre o Build 18890, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="be873-185">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-186">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-186">WSL</span></span>
* <span data-ttu-id="be873-187">Vazamento de soquete sem bloqueio [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="be873-187">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="be873-188">A entrada de EOF para o terminal pode bloquear leituras subsequentes [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="be873-188">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="be873-189">Atualização do cabeçalho de resolv.conf para fazer referência a wsl.conf [discutido no GH 3928]</span><span class="sxs-lookup"><span data-stu-id="be873-189">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="be873-190">Deadlock no código de exclusão de epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="be873-190">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="be873-191">Manipulação de espaços em argumentos para --import e –export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="be873-191">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="be873-192">A extensão de arquivos mmap não funciona corretamente [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="be873-192">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="be873-193">Correção do problema de o acesso ao ARM64 \\\\wsl$ não estar funcionando corretamente</span><span class="sxs-lookup"><span data-stu-id="be873-193">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="be873-194">Adição de um ícone padrão melhor para wsl.exe</span><span class="sxs-lookup"><span data-stu-id="be873-194">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="be873-195">Build 18342</span><span class="sxs-lookup"><span data-stu-id="be873-195">Build 18342</span></span>
<span data-ttu-id="be873-196">Para obter informações gerais do Windows sobre o Build 18342, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="be873-196">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-197">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-197">WSL</span></span>
* <span data-ttu-id="be873-198">Adicionamos a capacidade para os usuários acessarem arquivos do Linux em uma distribuição WSL do Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-198">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="be873-199">Esses arquivos podem ser acessados por meio da linha de comando e aplicativos do Windows (tais como Explorador de Arquivos, VSCode, etc.) também podem interagir com eles.</span><span class="sxs-lookup"><span data-stu-id="be873-199">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="be873-200">Acesse seus arquivos navegando até \\\\wsl$\\<nome_da_distro> ou consulte uma lista de distribuições em execução navegando até \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="be873-200">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="be873-201">Adição de marcas de informações de CPU adicionais e correção dos valores de Cpus_allowed[_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="be873-201">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="be873-202">Suporte a exec de thread não líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="be873-202">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="be873-203">Tratamento de falhas de atualização de configuração como não fatais [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="be873-203">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="be873-204">Atualização de binfmt para lidar com deslocamentos adequadamente [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="be873-204">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="be873-205">Habilitação do mapeamento de unidades de rede para o Plano 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="be873-205">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="be873-206">Suporte à conversão de caminhos Windows -> Linux e Linux -> Windows para montagens de associação</span><span class="sxs-lookup"><span data-stu-id="be873-206">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="be873-207">Criação de seções somente leitura para mapeamentos em arquivos abertos como somente leitura</span><span class="sxs-lookup"><span data-stu-id="be873-207">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="be873-208">Build 18334</span><span class="sxs-lookup"><span data-stu-id="be873-208">Build 18334</span></span>
<span data-ttu-id="be873-209">Para obter informações gerais do Windows sobre o Build 18334, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="be873-209">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-210">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-210">WSL</span></span>
* <span data-ttu-id="be873-211">Recriação da maneira como o fuso horário do Windows é mapeado para um fuso horário do Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="be873-211">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="be873-212">Correção de vazamentos de memória e adição de novas funções de conversão de cadeia de caracteres [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="be873-212">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="be873-213">SIGCONT em um grupo de threads sem threads é um não operacional [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="be873-213">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="be873-214">Exibição correta dos descritores de arquivo de epoll e de soquete em /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="be873-214">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="be873-215">Build 18305</span><span class="sxs-lookup"><span data-stu-id="be873-215">Build 18305</span></span>
<span data-ttu-id="be873-216">Para obter informações gerais do Windows sobre o Build 18305, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="be873-216">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-217">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-217">WSL</span></span>
* <span data-ttu-id="be873-218">pthreads perdem o acesso a arquivos quando o thread primário sai [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="be873-218">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="be873-219">TIOCSCTTY deve ignorar o parâmetro "force", a menos que ele seja necessário [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="be873-219">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="be873-220">Melhorias na linha de comando do wsl.exe e adição de funcionalidade de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="be873-220">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="be873-221">Build 18277</span><span class="sxs-lookup"><span data-stu-id="be873-221">Build 18277</span></span>
<span data-ttu-id="be873-222">Para obter informações gerais do Windows sobre o Build 18277, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="be873-222">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-223">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-223">WSL</span></span>
* <span data-ttu-id="be873-224">Correção do erro "essa interface não é compatível" introduzido no build 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="be873-224">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="be873-225">O sinalizador MNT_FORCE agora é ignorado para a syscall umount [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="be873-225">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="be873-226">Alternância da interop de WSL para usar a API CreatePseudoConsole oficial</span><span class="sxs-lookup"><span data-stu-id="be873-226">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="be873-227">Nenhum valor de tempo limite mantido quando FUTEX_WAIT reinicializa</span><span class="sxs-lookup"><span data-stu-id="be873-227">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="be873-228">Build 18272</span><span class="sxs-lookup"><span data-stu-id="be873-228">Build 18272</span></span>
<span data-ttu-id="be873-229">Para obter informações gerais do Windows sobre o Build 18272, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="be873-229">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-230">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-230">WSL</span></span>
* <span data-ttu-id="be873-231">**AVISO:** Há um problema nesse build que torna o WSL inoperante.</span><span class="sxs-lookup"><span data-stu-id="be873-231">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="be873-232">Ao tentar iniciar sua distribuição, você verá um erro "Essa interface não é compatível".</span><span class="sxs-lookup"><span data-stu-id="be873-232">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="be873-233">O problema foi corrigido e estará no build do Participante do Programa Windows Insider – Modo Rápido da próxima semana.</span><span class="sxs-lookup"><span data-stu-id="be873-233">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="be873-234">Se você tiver instalado esse build, poderá reverter para o build anterior do Windows usando "Voltar para a versão anterior do Windows 10" em Configurações -> Atualização e Segurança -> Recuperação.</span><span class="sxs-lookup"><span data-stu-id="be873-234">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="be873-235">Build 18267</span><span class="sxs-lookup"><span data-stu-id="be873-235">Build 18267</span></span>
<span data-ttu-id="be873-236">Para obter informações gerais do Windows sobre o Build 18267, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="be873-236">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-237">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-237">WSL</span></span>
* <span data-ttu-id="be873-238">Correção do problema em que o processo zumbi pode não ser aproveitado e permanecer indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="be873-238">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="be873-239">WslRegisterDistribution trava se a mensagem de erro excede o comprimento máximo [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="be873-239">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="be873-240">Permissão para que o fsync tenha sucesso para arquivos somente leitura no DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="be873-240">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="be873-241">Verificação de que os diretórios /bin e /sbin existem antes de criar symlinks internos [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="be873-241">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="be873-242">Adicionado um mecanismo de tempo limite de encerramento de instância para instâncias de WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-242">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="be873-243">O tempo limite está definido atualmente como 15 segundos, o que significa que a instância será encerrada 15 segundos após o último processo de WSL sair.</span><span class="sxs-lookup"><span data-stu-id="be873-243">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="be873-244">Para encerrar uma distribuição imediatamente, use:</span><span class="sxs-lookup"><span data-stu-id="be873-244">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="be873-245">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="be873-245">Build 17763 (1809)</span></span>
<span data-ttu-id="be873-246">Para obter informações gerais do Windows sobre o Build 17763, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="be873-246">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-247">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-247">WSL</span></span>
* <span data-ttu-id="be873-248">Verificação de permissão da syscall setpriority muito estrita para alterar a mesma prioridade de thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="be873-248">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="be873-249">Verificação de que o tempo de interrupção não polarizado é usado para o tempo de inicialização a fim de evitar retornar valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="be873-249">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="be873-250">Manipulação de symlinks no interpretador binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="be873-250">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="be873-251">Melhor manipulação da limpeza do descritor de arquivo de líder do grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="be873-251">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="be873-252">Alternância do WSL para usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter a fim de evitar o estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="be873-252">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="be873-253">A anexação ptrace pode causar um valor retornado insatisfatório de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="be873-253">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="be873-254">Correção de vários problemas relacionados ao AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="be873-254">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="be873-255">Correção do problema que poderá causar falha de interop de WSL se o diretório de trabalho atual tiver menos de 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="be873-255">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="be873-256">Impedimento de que um atraso de um segundo cause falhas em conexões de loopback para portas inexistentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="be873-256">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="be873-257">Adição do arquivo de stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="be873-257">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="be873-258">Informações de escopo de IPV6 mais precisas.</span><span class="sxs-lookup"><span data-stu-id="be873-258">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="be873-259">Suporte a PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="be873-259">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="be873-260">O sistema de arquivos de pipe limpa inadvertidamente o evento epoll disparado da borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="be873-260">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="be873-261">O executável do Win32 iniciado via symlink NTFS não respeita o nome do symlink [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="be873-261">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="be873-262">Suporte a zumbis melhorado [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="be873-262">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="be873-263">Adição de entradas wsl.conf para controlar o comportamento de interop do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="be873-263">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="be873-264">Correção para getsockname nem sempre retornando tipo de família de soquetes UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="be873-264">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="be873-265">Adição de suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="be873-265">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="be873-266">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="be873-266">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="be873-267">Suporte a interop em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="be873-267">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="be873-268">Correção do problema de verificação de permissão na pasta raiz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="be873-268">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="be873-269">Suporte limitado para os ioctls de teclado TTY KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="be873-269">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="be873-270">Os aplicativos da interface do usuário do Windows devem ser executados mesmo quando iniciados em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="be873-270">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="be873-271">Adição da opção wsl-u ou --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="be873-271">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="be873-272">Correção de problemas de inicialização do WSL quando a inicialização rápida estiver habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="be873-272">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="be873-273">Os soquetes Unix precisam reter as credenciais de pares desconectados [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="be873-273">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="be873-274">Soquetes Unix sem bloqueio falhando indefinidamente com EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="be873-274">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="be873-275">case=off é o novo tipo de montagem de drvfs padrão [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="be873-275">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="be873-276">Confira [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="be873-276">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="be873-277">Adição de wslconfig /terminate para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="be873-277">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="be873-278">Correção do problema com as entradas do menu de contexto do shell WSL que não manipulam corretamente caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="be873-278">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="be873-279">Exposição de diferenciação de maiúsculas e minúsculas por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="be873-279">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="be873-280">ARM64: Emulação de operações de manutenção de cache.</span><span class="sxs-lookup"><span data-stu-id="be873-280">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="be873-281">Resolução do [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="be873-281">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="be873-282">DrvFs: apenas caracteres de escape de saída no intervalo privado que correspondem a um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="be873-282">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="be873-283">Correção do erro OB1 (por um) na validação de tamanho do interpretador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="be873-283">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="be873-284">Timers absolutos do WSL com um tempo no passado não são disparados [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="be873-284">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="be873-285">Verificação de que os pontos de nova análise criados recentemente estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="be873-285">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="be873-286">Criação de forma atômica de diretórios que diferenciam maiúsculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="be873-286">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="be873-287">Corrigido um problema adicional em que operações multi-threaded poderiam retornar ENOENT mesmo que o arquivo existisse.</span><span class="sxs-lookup"><span data-stu-id="be873-287">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="be873-288">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="be873-288">[GH 2712]</span></span>
* <span data-ttu-id="be873-289">Correção da falha de inicialização do WSL quando o UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="be873-289">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="be873-290">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="be873-290">[GH 3020]</span></span>
* <span data-ttu-id="be873-291">Adição do menu de contexto do Explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="be873-291">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="be873-292">Para usá-lo, mantenha a tecla Shift pressionada e clique com o botão direito do mouse quando estiver em uma janela do Explorer.</span><span class="sxs-lookup"><span data-stu-id="be873-292">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="be873-293">Correção do comportamento de não bloqueio de soquete do Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="be873-293">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="be873-294">Correção do comando do NetLink suspenso, conforme relatado no GH 2026.</span><span class="sxs-lookup"><span data-stu-id="be873-294">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="be873-295">Adição de suporte para os sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="be873-295">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="be873-296">Correção do problema com truncamento não causando eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="be873-296">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="be873-297">Adição da opção --exec para wsl.exe para invocar um único binário sem um shell.</span><span class="sxs-lookup"><span data-stu-id="be873-297">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="be873-298">Adição da opção --distribution a wsl.exe para selecionar uma distribuição específica.</span><span class="sxs-lookup"><span data-stu-id="be873-298">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="be873-299">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="be873-299">Limited support for dmesg.</span></span> <span data-ttu-id="be873-300">Os aplicativos agora podem fazer logon no dmesg.</span><span class="sxs-lookup"><span data-stu-id="be873-300">Applications can now log to dmesg.</span></span> <span data-ttu-id="be873-301">O driver do WSL registra informações limitadas no dmesg.</span><span class="sxs-lookup"><span data-stu-id="be873-301">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="be873-302">No futuro, isso pode ser estendido para transportar outras informações/diagnósticos do driver.</span><span class="sxs-lookup"><span data-stu-id="be873-302">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="be873-303">Observação: atualmente, o dmesg é compatível por meio da interface do dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="be873-303">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="be873-304">A interface syscall `syslog` ainda não é compatível.</span><span class="sxs-lookup"><span data-stu-id="be873-304">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="be873-305">Assim sendo, algumas das opções de linha de comando de `dmesg`, tais como `-S` e `-C`, não funcionam.</span><span class="sxs-lookup"><span data-stu-id="be873-305">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="be873-306">Alteração do GID e o modo padrão de dispositivos seriais para corresponder ao nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="be873-306">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="be873-307">O DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="be873-307">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="be873-308">Observação: O DrvFs tem algumas limitações sobre o nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="be873-308">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="be873-309">Alguns caracteres (tais como '/', ': ' e '\*') não são permitidos e os nomes de atributos estendidos não diferenciam maiúsculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-309">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="be873-310">Build 18252 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="be873-310">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="be873-311">Para obter informações gerais do Windows sobre o Build 18252, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="be873-311">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-312">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-312">WSL</span></span>
* <span data-ttu-id="be873-313">Mover os binários init e bsdtar para fora da dll do lxssmanager e para uma pasta de ferramentas separada</span><span class="sxs-lookup"><span data-stu-id="be873-313">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="be873-314">Correção da corrida ao fechar o descritor de arquivo ao usar CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="be873-314">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="be873-315">Manipulação de campos opcionais em /proc/pid/mountinfo ao converter caminhos do DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-315">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="be873-316">Permissão para que o DrvFs mknod tenha êxito sem suporte de metadados para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="be873-316">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="be873-317">Os arquivos somente leitura criados no DrvFs devem ter o atributo readonly definido [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="be873-317">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="be873-318">Adição do auxiliar /sbin/mount.drvfs para lidar com a montagem do DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-318">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="be873-319">Uso da renomeação POSIX no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="be873-319">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="be873-320">Permissão para a conversão de caminho em volumes sem um GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="be873-320">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="be873-321">Build 17738 (rápido)</span><span class="sxs-lookup"><span data-stu-id="be873-321">Build 17738 (Fast)</span></span>
<span data-ttu-id="be873-322">Para obter informações gerais do Windows sobre o Build 17738, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="be873-322">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-323">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-323">WSL</span></span>
* <span data-ttu-id="be873-324">Verificação de permissão da syscall setpriority muito estrita para alterar a mesma prioridade de thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="be873-324">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="be873-325">Verificação de que o tempo de interrupção não polarizado é usado para o tempo de inicialização a fim de evitar retornar valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="be873-325">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="be873-326">Manipulação de symlinks no interpretador binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="be873-326">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="be873-327">Melhor manipulação da limpeza do descritor de arquivo de líder do grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="be873-327">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="be873-328">Build 17728 (rápido)</span><span class="sxs-lookup"><span data-stu-id="be873-328">Build 17728 (Fast)</span></span>
<span data-ttu-id="be873-329">Para obter informações gerais do Windows sobre o Build 17728, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="be873-329">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-330">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-330">WSL</span></span>
* <span data-ttu-id="be873-331">Alternância do WSL para usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter a fim de evitar o estouro [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="be873-331">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="be873-332">A anexação ptrace pode causar um valor retornado insatisfatório de chamadas do sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="be873-332">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="be873-333">Correção de vários problemas relacionados ao AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="be873-333">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="be873-334">Correção do problema que poderá causar falha de interop de WSL se o diretório de trabalho atual tiver menos de 5 caracteres [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="be873-334">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="be873-335">Build 18204 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="be873-335">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="be873-336">Para obter informações gerais do Windows sobre o Build 18204, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="be873-336">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-337">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-337">WSL</span></span>
* <span data-ttu-id="be873-338">O sistema de arquivos de pipe limpa inadvertidamente o evento epoll disparado da borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="be873-338">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="be873-339">O executável do Win32 iniciado via symlink NTFS não respeita o nome do symlink [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="be873-339">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="be873-340">Build 17723 (rápido)</span><span class="sxs-lookup"><span data-stu-id="be873-340">Build 17723 (Fast)</span></span>
<span data-ttu-id="be873-341">Para obter informações gerais do Windows sobre o Build 17723, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="be873-341">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-342">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-342">WSL</span></span>
* <span data-ttu-id="be873-343">Impedimento de que um atraso de um segundo cause falhas em conexões de loopback para portas inexistentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="be873-343">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="be873-344">Adição do arquivo de stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="be873-344">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="be873-345">Informações de escopo de IPV6 mais precisas.</span><span class="sxs-lookup"><span data-stu-id="be873-345">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="be873-346">Suporte a PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="be873-346">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="be873-347">O sistema de arquivos de pipe limpa inadvertidamente o evento epoll disparado da borda [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="be873-347">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="be873-348">O executável do Win32 iniciado via symlink NTFS não respeita o nome do symlink [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="be873-348">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="be873-349">Build 17713</span><span class="sxs-lookup"><span data-stu-id="be873-349">Build 17713</span></span>
<span data-ttu-id="be873-350">Para obter informações gerais do Windows sobre o Build 17713, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="be873-350">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-351">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-351">WSL</span></span>
* <span data-ttu-id="be873-352">Suporte a zumbis melhorado [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="be873-352">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="be873-353">Adição de entradas wsl.conf para controlar o comportamento de interop do Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="be873-353">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="be873-354">Correção para getsockname nem sempre retornando tipo de família de soquetes UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="be873-354">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="be873-355">Adição de suporte para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="be873-355">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="be873-356">Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="be873-356">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="be873-357">Suporte a interop em VHDs montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="be873-357">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="be873-358">Correção do problema de verificação de permissão na pasta raiz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="be873-358">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="be873-359">Suporte limitado para os ioctls de teclado TTY KDGKBTYPE, KDGKBMODE e KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="be873-359">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="be873-360">Os aplicativos da interface do usuário do Windows devem ser executados mesmo quando iniciados em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="be873-360">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="be873-361">Build 17704</span><span class="sxs-lookup"><span data-stu-id="be873-361">Build 17704</span></span>
<span data-ttu-id="be873-362">Para obter informações gerais do Windows sobre o Build 17704, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="be873-362">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-363">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-363">WSL</span></span>
* <span data-ttu-id="be873-364">Adição da opção wsl-u ou --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="be873-364">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="be873-365">Correção de problemas de inicialização do WSL quando a inicialização rápida estiver habilitada [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="be873-365">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="be873-366">Os soquetes Unix precisam reter as credenciais de pares desconectados [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="be873-366">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="be873-367">Soquetes Unix sem bloqueio falhando indefinidamente com EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="be873-367">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="be873-368">case=off é o novo tipo de montagem de drvfs padrão [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="be873-368">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="be873-369">Confira [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="be873-369">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="be873-370">Adição de wslconfig /terminate para interromper a execução de distribuições.</span><span class="sxs-lookup"><span data-stu-id="be873-370">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="be873-371">Build 17692</span><span class="sxs-lookup"><span data-stu-id="be873-371">Build 17692</span></span>
<span data-ttu-id="be873-372">Para obter informações gerais do Windows sobre o Build 17692, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="be873-372">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-373">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-373">WSL</span></span>
* <span data-ttu-id="be873-374">Correção do problema com as entradas do menu de contexto do shell WSL que não manipulam corretamente caminhos com espaços.</span><span class="sxs-lookup"><span data-stu-id="be873-374">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="be873-375">Exposição de diferenciação de maiúsculas e minúsculas por diretório como um atributo estendido</span><span class="sxs-lookup"><span data-stu-id="be873-375">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="be873-376">ARM64: Emulação de operações de manutenção de cache.</span><span class="sxs-lookup"><span data-stu-id="be873-376">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="be873-377">Resolução do [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="be873-377">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="be873-378">DrvFs: apenas caracteres de escape de saída no intervalo privado que correspondem a um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="be873-378">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="be873-379">Build 17686</span><span class="sxs-lookup"><span data-stu-id="be873-379">Build 17686</span></span>
<span data-ttu-id="be873-380">Para obter informações gerais do Windows sobre o Build 17686, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="be873-380">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-381">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-381">WSL</span></span>
* <span data-ttu-id="be873-382">Correção do erro OB1 (por um) na validação de tamanho do interpretador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="be873-382">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="be873-383">Timers absolutos do WSL com um tempo no passado não são disparados [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="be873-383">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="be873-384">Verificação de que os pontos de nova análise criados recentemente estão listados como tal no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="be873-384">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="be873-385">Criação de forma atômica de diretórios que diferenciam maiúsculas de minúsculas no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="be873-385">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="be873-386">Build 17677</span><span class="sxs-lookup"><span data-stu-id="be873-386">Build 17677</span></span>
<span data-ttu-id="be873-387">Para obter informações gerais do Windows sobre o Build 17677, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="be873-387">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-388">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-388">WSL</span></span>
* <span data-ttu-id="be873-389">Corrigido um problema adicional em que operações multi-threaded poderiam retornar ENOENT mesmo que o arquivo existisse.</span><span class="sxs-lookup"><span data-stu-id="be873-389">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="be873-390">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="be873-390">[GH 2712]</span></span>
* <span data-ttu-id="be873-391">Correção da falha de inicialização do WSL quando o UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="be873-391">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="be873-392">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="be873-392">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="be873-393">Build 17666</span><span class="sxs-lookup"><span data-stu-id="be873-393">Build 17666</span></span>
<span data-ttu-id="be873-394">Para obter informações gerais do Windows sobre o Build 17666, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="be873-394">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-395">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-395">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="be873-396">AVISO: Há um problema que impede a execução do WSL em alguns chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="be873-396">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="be873-397">Uma correção está pronta e preparando-se para o branch do Build do Insider.</span><span class="sxs-lookup"><span data-stu-id="be873-397">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="be873-398">Adição do menu de contexto do Explorer para iniciar o WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="be873-398">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="be873-399">Para usá-lo, mantenha a tecla Shift pressionada e clique com o botão direito do mouse quando estiver em uma janela do Explorer.</span><span class="sxs-lookup"><span data-stu-id="be873-399">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="be873-400">Correção do comportamento de não bloqueio de soquete do Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="be873-400">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="be873-401">Correção do comando do NetLink suspenso, conforme relatado no GH 2026.</span><span class="sxs-lookup"><span data-stu-id="be873-401">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="be873-402">Adição de suporte para os sinalizadores de propagação de montagem [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="be873-402">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="be873-403">Correção do problema com truncamento não causando eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="be873-403">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="be873-404">Adição da opção --exec para wsl.exe para invocar um único binário sem um shell.</span><span class="sxs-lookup"><span data-stu-id="be873-404">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="be873-405">Adição da opção --distribution a wsl.exe para selecionar uma distribuição específica.</span><span class="sxs-lookup"><span data-stu-id="be873-405">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="be873-406">Build 17655 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="be873-406">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="be873-407">Para obter informações gerais do Windows sobre o Build 17655, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="be873-407">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-408">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-408">WSL</span></span>
* <span data-ttu-id="be873-409">Suporte limitado para dmesg.</span><span class="sxs-lookup"><span data-stu-id="be873-409">Limited support for dmesg.</span></span> <span data-ttu-id="be873-410">Os aplicativos agora podem fazer logon no dmesg.</span><span class="sxs-lookup"><span data-stu-id="be873-410">Applications can now log to dmesg.</span></span> <span data-ttu-id="be873-411">O driver do WSL registra informações limitadas no dmesg.</span><span class="sxs-lookup"><span data-stu-id="be873-411">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="be873-412">No futuro, isso pode ser estendido para transportar outras informações/diagnósticos do driver.</span><span class="sxs-lookup"><span data-stu-id="be873-412">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="be873-413">Observação: atualmente, o dmesg é compatível por meio da interface do dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="be873-413">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="be873-414">A interface sycall `syslog` ainda não é compatível.</span><span class="sxs-lookup"><span data-stu-id="be873-414">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="be873-415">Assim sendo, algumas das opções de linha de comando de `dmesg`, tais como `-S` e `-C`, não funcionam.</span><span class="sxs-lookup"><span data-stu-id="be873-415">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="be873-416">Corrigido um problema em que operações multi-threaded poderiam retornar ENOENT mesmo que o arquivo existisse.</span><span class="sxs-lookup"><span data-stu-id="be873-416">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="be873-417">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="be873-417">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="be873-418">Build 17639 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="be873-418">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="be873-419">Para obter informações gerais do Windows sobre o Build 17639, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="be873-419">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-420">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-420">WSL</span></span>
* <span data-ttu-id="be873-421">Alteração do GID e o modo padrão de dispositivos seriais para corresponder ao nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="be873-421">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="be873-422">O DrvFs agora dá suporte a atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="be873-422">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="be873-423">Observação: O DrvFs tem algumas limitações sobre o nome dos atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="be873-423">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="be873-424">Em particular, alguns caracteres (tais como '/', ': ' e '\*') não são permitidos e os nomes de atributos estendidos não diferenciam maiúsculas de minúsculas em DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-424">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="be873-425">Build 17133 (rápido)</span><span class="sxs-lookup"><span data-stu-id="be873-425">Build 17133 (Fast)</span></span>
<span data-ttu-id="be873-426">Para obter informações gerais do Windows sobre o Build 17133, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="be873-426">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-427">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-427">WSL</span></span>
* <span data-ttu-id="be873-428">Correção para o travamento no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-428">Fix for hang in WSL.</span></span> <span data-ttu-id="be873-429">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="be873-429">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="be873-430">Build 17128 (rápido)</span><span class="sxs-lookup"><span data-stu-id="be873-430">Build 17128 (Fast)</span></span>
<span data-ttu-id="be873-431">Para obter informações gerais do Windows sobre o Build 17128, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="be873-431">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-432">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-432">WSL</span></span>
* <span data-ttu-id="be873-433">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="be873-433">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="be873-434">Build 17627 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="be873-434">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="be873-435">Para obter informações gerais do Windows sobre o Build 17627, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="be873-435">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-436">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-436">WSL</span></span>
* <span data-ttu-id="be873-437">Adição de suporte para as operações que reconhecem o Futex PI.</span><span class="sxs-lookup"><span data-stu-id="be873-437">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="be873-438">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="be873-438">[GH 1006]</span></span>
    * <span data-ttu-id="be873-439">Observe que as prioridades não são atualmente um recurso WSL compatível para que haja limitações, mas o uso padrão deve ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="be873-439">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="be873-440">Suporte do Firewall do Windows a processos WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-440">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="be873-441">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="be873-441">[GH 1852]</span></span>
    * <span data-ttu-id="be873-442">Por exemplo, para permitir que o processo Python WSL escute em qualquer porta, use o cmd do Windows com privilégios elevados: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="be873-442">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="be873-443">Para obter detalhes adicionais sobre como adicionar regras de firewall, confira este [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="be873-443">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="be873-444">Respeitar o shell padrão do usuário ao usar wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="be873-444">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="be873-445">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="be873-445">[GH 2372]</span></span>
* <span data-ttu-id="be873-446">Relatar todos os adaptadores de rede como Ethernet.</span><span class="sxs-lookup"><span data-stu-id="be873-446">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="be873-447">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="be873-447">[GH 2996]</span></span>
* <span data-ttu-id="be873-448">Melhor manipulação de arquivo /etc/passwd corrompido.</span><span class="sxs-lookup"><span data-stu-id="be873-448">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="be873-449">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="be873-449">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="be873-450">Console</span><span class="sxs-lookup"><span data-stu-id="be873-450">Console</span></span>
* <span data-ttu-id="be873-451">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-451">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-452">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-452">LTP Results:</span></span>
<span data-ttu-id="be873-453">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-453">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="be873-454">Build 17618 (ignorar e prosseguir)</span><span class="sxs-lookup"><span data-stu-id="be873-454">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="be873-455">Para obter informações gerais do Windows sobre o Build 17618, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="be873-455">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-456">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-456">WSL</span></span>
* <span data-ttu-id="be873-457">Introduzir a funcionalidade de pseudoconsole para interop NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="be873-457">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="be873-458">O mecanismo de instalação herdado (lxrun. exe) foi preterido.</span><span class="sxs-lookup"><span data-stu-id="be873-458">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="be873-459">O mecanismo compatível para a instalação de distribuições é por meio da Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="be873-459">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="be873-460">Console</span><span class="sxs-lookup"><span data-stu-id="be873-460">Console</span></span>
* <span data-ttu-id="be873-461">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-461">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-462">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-462">LTP Results:</span></span>
<span data-ttu-id="be873-463">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-463">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="be873-464">Build 17110</span><span class="sxs-lookup"><span data-stu-id="be873-464">Build 17110</span></span>
<span data-ttu-id="be873-465">Para obter informações gerais do Windows sobre o Build 17110, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="be873-465">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-466">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-466">WSL</span></span>
* <span data-ttu-id="be873-467">Permitir que /init seja encerrado do Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="be873-467">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="be873-468">O DrvFs agora usa a diferenciação de maiúsculas e minúsculas por diretório por padrão (equivalente à opção de montagem "case = dir").</span><span class="sxs-lookup"><span data-stu-id="be873-468">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="be873-469">Usar "case=force" (o comportamento antigo) requer a definição de uma chave do Registro.</span><span class="sxs-lookup"><span data-stu-id="be873-469">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="be873-470">Execute o seguinte comando para habilitar "case=force" se você precisar usá-lo: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="be873-470">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="be873-471">Se você tiver diretórios existentes criados com WSL na versão anterior do Windows que precisem diferenciar maiúsculas de minúsculas, use fsutil.exe para marcá-los como com diferenciação de maiúsculas e minúsculas: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="be873-471">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="be873-472">Termine cadeias de caracteres retornadas da syscall uname com NULL.</span><span class="sxs-lookup"><span data-stu-id="be873-472">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="be873-473">Console</span><span class="sxs-lookup"><span data-stu-id="be873-473">Console</span></span>
* <span data-ttu-id="be873-474">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-474">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-475">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-475">LTP Results:</span></span>
<span data-ttu-id="be873-476">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-476">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="be873-477">Build 17107</span><span class="sxs-lookup"><span data-stu-id="be873-477">Build 17107</span></span>
<span data-ttu-id="be873-478">Para obter informações gerais do Windows sobre o Build 17107, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="be873-478">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-479">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-479">WSL</span></span>
* <span data-ttu-id="be873-480">Suporte a TCSETSF e TCSETSW nos pontos de extremidade mestre pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="be873-480">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="be873-481">A inicialização de processos de interop simultâneos pode resultar em EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="be873-481">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="be873-482">Correção de PTRACE_ATTACH para mostrar o status de rastreamento adequado em/proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="be873-482">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="be873-483">Correção da corrida em que os processos de curta duração clonados com os dois sinalizadores CLEARTID e SETTID podem ser encerrados sem limpar o endereço de TID.</span><span class="sxs-lookup"><span data-stu-id="be873-483">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="be873-484">Exibir uma mensagem durante a atualização dos diretórios do sistema de arquivos do Linux ao mudar de um build anterior ao 17093.</span><span class="sxs-lookup"><span data-stu-id="be873-484">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="be873-485">Para obter mais detalhes sobre as alterações do sistema de arquivos 17093, confira as notas sobre a versão para o [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="be873-485">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="be873-486">Console</span><span class="sxs-lookup"><span data-stu-id="be873-486">Console</span></span>
* <span data-ttu-id="be873-487">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-487">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-488">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-488">LTP Results:</span></span>
<span data-ttu-id="be873-489">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-489">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="be873-490">Build 17101</span><span class="sxs-lookup"><span data-stu-id="be873-490">Build 17101</span></span>
<span data-ttu-id="be873-491">Para obter informações gerais do Windows sobre o Build 17101, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="be873-491">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-492">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-492">WSL</span></span>
* <span data-ttu-id="be873-493">Suporte para signalfd.</span><span class="sxs-lookup"><span data-stu-id="be873-493">Support for signalfd.</span></span> <span data-ttu-id="be873-494">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="be873-494">[GH 129]</span></span>
* <span data-ttu-id="be873-495">Suporte a nomes de arquivos que contêm caracteres NTFS ilícitos, codificando-os como caracteres Unicode privados.</span><span class="sxs-lookup"><span data-stu-id="be873-495">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="be873-496">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="be873-496">[GH 1514]</span></span>
* <span data-ttu-id="be873-497">A montagem automática fará fallback para somente leitura quando a gravação não for compatível.</span><span class="sxs-lookup"><span data-stu-id="be873-497">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="be873-498">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="be873-498">[GH 2603]</span></span>
* <span data-ttu-id="be873-499">Permissão para colagem de pares substitutos Unicode (como caracteres de Emoji).</span><span class="sxs-lookup"><span data-stu-id="be873-499">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="be873-500">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="be873-500">[GH 2765]</span></span>
* <span data-ttu-id="be873-501">Pseudoarquivos em /proc e /sys devem retornar prontidão para leitura e gravação de select, poll, epoll e outros. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="be873-501">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="be873-502">Correção do problema que pode fazer com que o serviço entre em loop infinito quando o Registro foi adulterado ou está corrompido.</span><span class="sxs-lookup"><span data-stu-id="be873-502">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="be873-503">Correção das mensagens do NetLink para trabalhar com a versão mais recente (upstream 4.14) do iproute2.</span><span class="sxs-lookup"><span data-stu-id="be873-503">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="be873-504">Console</span><span class="sxs-lookup"><span data-stu-id="be873-504">Console</span></span>
* <span data-ttu-id="be873-505">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-505">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-506">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-506">LTP Results:</span></span>
<span data-ttu-id="be873-507">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-507">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="be873-508">Build 17093</span><span class="sxs-lookup"><span data-stu-id="be873-508">Build 17093</span></span>
<span data-ttu-id="be873-509">Para obter informações gerais do Windows sobre o Build 17093, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-509">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="be873-510">Importante:</span><span class="sxs-lookup"><span data-stu-id="be873-510">Important:</span></span>
<span data-ttu-id="be873-511">Ao iniciar o WSL pela primeira vez após atualizar para esse build, ele precisa executar um certo trabalho de atualização dos diretórios do sistema de arquivos do Linux.</span><span class="sxs-lookup"><span data-stu-id="be873-511">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="be873-512">Isso pode levar vários minutos, então a inicialização do WSL pode parecer lenta.</span><span class="sxs-lookup"><span data-stu-id="be873-512">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="be873-513">Isso só deve ocorrer uma vez para cada distribuição instalada por meio da loja.</span><span class="sxs-lookup"><span data-stu-id="be873-513">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="be873-514">Suporte à diferenciação de maiúsculas e minúsculas melhorada no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="be873-514">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="be873-515">O DrvFs agora dá suporte à diferenciação de maiúsculas e minúsculas por diretório.</span><span class="sxs-lookup"><span data-stu-id="be873-515">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="be873-516">Esse é um novo sinalizador que pode ser definido em diretórios para indicar que todas as operações nesses diretórios devem ser tratadas como com diferenciação de maiúsculas de minúsculas, o que permite que até mesmo os aplicativos do Windows abram corretamente arquivos que diferem apenas por maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be873-516">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="be873-517">O DrvFs tem novas opções de montagem que controlam a diferenciação de maiúsculas e minúsculas em uma base por diretório</span><span class="sxs-lookup"><span data-stu-id="be873-517">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="be873-518">Case = Force: todos os diretórios são tratados como com diferenciação de maiúsculas de minúsculas (exceto a raiz da unidade).</span><span class="sxs-lookup"><span data-stu-id="be873-518">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="be873-519">Os novos diretórios criados com o WSL são marcados como com diferenciação de maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be873-519">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="be873-520">Esse é o comportamento herdado, exceto para marcação de novos diretórios como com diferenciação de maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be873-520">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="be873-521">case=dir: somente os diretórios com o sinalizador de diferenciação de maiúsculas e minúsculas por diretório são tratados como com diferenciação de maiúsculas e minúsculas; outros diretórios não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be873-521">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="be873-522">Os novos diretórios criados com o WSL são marcados como com diferenciação de maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be873-522">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="be873-523">case=off: somente os diretórios com o sinalizador de diferenciação de maiúsculas e minúsculas por diretório são tratados como com diferenciação de maiúsculas e minúsculas; outros diretórios não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be873-523">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="be873-524">Os novos diretórios criados com WSL são marcados como sem diferenciação de maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be873-524">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="be873-525">Observação: os diretórios criados por WSL em versões anteriores não têm esse sinalizador definido, portanto, não serão tratados como com diferenciação de maiúsculas e minúsculas se você usar a opção "case=dir".</span><span class="sxs-lookup"><span data-stu-id="be873-525">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="be873-526">Uma maneira de definir esse sinalizador em diretórios existentes estará disponível em breve.</span><span class="sxs-lookup"><span data-stu-id="be873-526">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="be873-527">Exemplo de montagem com essas opções (para unidades existentes, você deve primeiro desmontar antes de poder montar com opções diferentes): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="be873-527">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="be873-528">Por enquanto, case=force ainda é a opção padrão.</span><span class="sxs-lookup"><span data-stu-id="be873-528">For now, case=force is still the default option.</span></span> <span data-ttu-id="be873-529">Isso será alterado para case=dir no futuro.</span><span class="sxs-lookup"><span data-stu-id="be873-529">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="be873-530">Agora você pode usar barras invertidas em caminhos do Windows ao montar o DrvFs, por exemplo: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="be873-530">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="be873-531">O WSL agora processa o arquivo/etc/fstab durante a inicialização da instância [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="be873-531">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="be873-532">Isso é feito antes da montagem automática de unidades de DrvFs; todas as unidades que já foram montadas por fstab não serão remontadas automaticamente, permitindo que você altere o ponto de montagem de unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="be873-532">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="be873-533">Esse comportamento pode ser desativado usando o wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="be873-533">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="be873-534">Os arquivos mount, mountinfo e mountstats em /proc escapam corretamente caracteres especiais, tais como barras invertidas e espaços [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="be873-534">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="be873-535">Arquivos especiais criados com o DrvFs, tais como links simbólicos do WSL, ou então FIFOs e soquetes quando os metadados estão habilitados, agora podem ser copiados e movidos do Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-535">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="be873-536">O WSL é mais configurável com o wsl.conf</span><span class="sxs-lookup"><span data-stu-id="be873-536">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="be873-537">Adicionamos um método para que você configure automaticamente determinadas funcionalidades no WSL que serão aplicadas toda vez que você iniciar o subsistema.</span><span class="sxs-lookup"><span data-stu-id="be873-537">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="be873-538">Isso inclui opções de montagem automática e configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="be873-538">This includes automount options and network configuration.</span></span> <span data-ttu-id="be873-539">Saiba mais sobre isso em nossa postagem no blog em: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="be873-539">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="be873-540">O AF_UNIX permite conexões de soquete entre processos do Linux em WSL e em processos nativos do Windows</span><span class="sxs-lookup"><span data-stu-id="be873-540">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="be873-541">Os aplicativos do WSL e do Windows agora podem se comunicar entre si por meio de soquetes Unix.</span><span class="sxs-lookup"><span data-stu-id="be873-541">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="be873-542">Imagine que você deseja executar um serviço no Windows e disponibilizá-lo para aplicativos do Windows e do WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-542">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="be873-543">Agora, isso é possível com os soquetes do Unix.</span><span class="sxs-lookup"><span data-stu-id="be873-543">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="be873-544">Leia mais em nossa postagem no blog em https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="be873-544">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-545">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-545">WSL</span></span>
* <span data-ttu-id="be873-546">Suporte a mmap () com MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="be873-546">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="be873-547">Suporte a CLONE_PTRACE e CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="be873-547">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="be873-548">Manipulação do sinal de encerramento não SIGCHLD no clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="be873-548">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="be873-549">/proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches de stub [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="be873-549">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="be873-550">Erro ao carregar binários ELF que contêm cabeçalhos de carga com deslocamentos diferentes de zero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="be873-550">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="be873-551">Eliminação de todos os bytes de página à direita ao carregar imagens.</span><span class="sxs-lookup"><span data-stu-id="be873-551">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="be873-552">Redução dos casos em que o execve encerra o processo silenciosamente</span><span class="sxs-lookup"><span data-stu-id="be873-552">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="be873-553">Console</span><span class="sxs-lookup"><span data-stu-id="be873-553">Console</span></span>
* <span data-ttu-id="be873-554">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-554">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-555">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-555">LTP Results:</span></span>
<span data-ttu-id="be873-556">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-556">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="be873-557">Build 17083</span><span class="sxs-lookup"><span data-stu-id="be873-557">Build 17083</span></span>
<span data-ttu-id="be873-558">Para obter informações gerais do Windows sobre o Build 17083, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-558">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-559">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-559">WSL</span></span>
* <span data-ttu-id="be873-560">Corrigida a verificação de bug relacionada a epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="be873-560">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="be873-561">Corrigidos travamentos ao desativar a ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="be873-561">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="be873-562">Garantia de que as operações mmap parecem atômicas [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="be873-562">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="be873-563">Console</span><span class="sxs-lookup"><span data-stu-id="be873-563">Console</span></span>
* <span data-ttu-id="be873-564">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-564">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-565">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-565">LTP Results:</span></span>
<span data-ttu-id="be873-566">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-566">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="be873-567">Build 17074</span><span class="sxs-lookup"><span data-stu-id="be873-567">Build 17074</span></span>
<span data-ttu-id="be873-568">Para obter informações gerais do Windows sobre o Build 17074, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-568">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-569">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-569">WSL</span></span>
* <span data-ttu-id="be873-570">Corrigido formato de armazenamento de metadados do DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="be873-570">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="be873-571">**Importante:** Os metadados do DrvFs criados antes deste build serão exibidos incorretamente ou não serão exibidos em absoluto.</span><span class="sxs-lookup"><span data-stu-id="be873-571">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="be873-572">Para corrigir os arquivos afetados, use chmod e chown para aplicar novamente os metadados.</span><span class="sxs-lookup"><span data-stu-id="be873-572">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="be873-573">Corrigido o problema com vários sinais e syscalls reinicializáveis.</span><span class="sxs-lookup"><span data-stu-id="be873-573">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="be873-574">Console</span><span class="sxs-lookup"><span data-stu-id="be873-574">Console</span></span>
* <span data-ttu-id="be873-575">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-575">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-576">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-576">LTP Results:</span></span>
<span data-ttu-id="be873-577">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-577">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="be873-578">Build 17063</span><span class="sxs-lookup"><span data-stu-id="be873-578">Build 17063</span></span>
<span data-ttu-id="be873-579">Para obter informações gerais do Windows sobre o Build 17063, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-579">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="be873-580">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-580">WSL</span></span>
* <span data-ttu-id="be873-581">O DrvFs dá suporte a metadados adicionais do Linux.</span><span class="sxs-lookup"><span data-stu-id="be873-581">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="be873-582">Isso permite definir o proprietário e o modo de arquivos usando chmod/chown e também criar arquivos especiais, tais como FIFOs, soquetes Unix e arquivos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be873-582">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="be873-583">Por enquanto, isso é desabilitado por padrão, pois ainda é experimental.</span><span class="sxs-lookup"><span data-stu-id="be873-583">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="be873-584">**Observação:**  Corrigimos um bug no formato de metadados usado pelo DrvFs.</span><span class="sxs-lookup"><span data-stu-id="be873-584">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="be873-585">Embora os metadados funcionem nesse Build para experimentação, os builds futuros não leem corretamente os metadados criados por esse build.</span><span class="sxs-lookup"><span data-stu-id="be873-585">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="be873-586">Talvez seja necessário atualizar manualmente o proprietário para arquivos modificados e os dispositivos com uma ID de dispositivo personalizada precisarão ser recriados.</span><span class="sxs-lookup"><span data-stu-id="be873-586">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="be873-587">Para habilitar, monte o DrvFs com a opção de metadados (para habilitá-lo em uma montagem existente, você precisa primeiro desmontá-lo):</span><span class="sxs-lookup"><span data-stu-id="be873-587">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="be873-588">As permissões do Linux são adicionadas como metadados adicionais ao arquivo e não afetam as permissões do Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-588">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="be873-589">Lembre-se de que a edição de um arquivo usando um editor do Windows pode remover os metadados.</span><span class="sxs-lookup"><span data-stu-id="be873-589">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="be873-590">Nesse caso, o arquivo será revertido para as respectivas permissões padrão.</span><span class="sxs-lookup"><span data-stu-id="be873-590">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="be873-591">Adicionadas opções de montagem ao DrvFs para controlar arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="be873-591">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="be873-592">uid: a ID de usuário usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="be873-592">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="be873-593">gid: a ID de grupo usada para o proprietário de todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="be873-593">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="be873-594">umask: uma máscara octal de permissões a serem excluídas para todos os arquivos e diretórios.</span><span class="sxs-lookup"><span data-stu-id="be873-594">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="be873-595">fmask: uma máscara octal de permissões a serem excluídas para todos os arquivos regulares.</span><span class="sxs-lookup"><span data-stu-id="be873-595">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="be873-596">dmask: uma máscara octal de permissões a serem excluídas para todos os diretórios.</span><span class="sxs-lookup"><span data-stu-id="be873-596">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="be873-597">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="be873-597">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="be873-598">Combine com a opção de metadados para especificar permissões padrão para arquivos sem metadados.</span><span class="sxs-lookup"><span data-stu-id="be873-598">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="be873-599">Introduziu uma nova variável de ambiente, `WSLENV`, para configurar o modo como as variáveis de ambiente fluem entre WSL e Win32.</span><span class="sxs-lookup"><span data-stu-id="be873-599">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="be873-600">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="be873-600">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="be873-601">`WSLENV` é uma lista delimitada por dois-pontos de variáveis de ambiente que pode ser incluída ao iniciar processos do WSL do Win32 ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="be873-601">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="be873-602">Cada variável pode ser sufixada com uma barra seguida por sinalizadores para especificar como ela é traduzida.</span><span class="sxs-lookup"><span data-stu-id="be873-602">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="be873-603">p: O valor é um caminho que deve ser traduzido entre caminhos WSL e Win32.</span><span class="sxs-lookup"><span data-stu-id="be873-603">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="be873-604">l: O valor é uma lista de caminhos.</span><span class="sxs-lookup"><span data-stu-id="be873-604">l: The value is a list of paths.</span></span> <span data-ttu-id="be873-605">No WSL, é uma lista delimitada por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="be873-605">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="be873-606">No Win32, é uma lista delimitada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="be873-606">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="be873-607">u: O valor só deve ser incluído ao invocar o WSL do Win32</span><span class="sxs-lookup"><span data-stu-id="be873-607">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="be873-608">w: O valor só deve ser incluído ao invocar o Win32 do WSL</span><span class="sxs-lookup"><span data-stu-id="be873-608">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="be873-609">Você pode definir `WSLENV` em. bashrc ou no ambiente personalizado do Windows para seu usuário.</span><span class="sxs-lookup"><span data-stu-id="be873-609">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="be873-610">montagens do DrvFs preservam corretamente os carimbos de data/hora de tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="be873-610">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="be873-611">symlinks do DrvFs relatam o tamanho correto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="be873-611">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="be873-612">a leitura/gravação funciona para tamanhos de E/S muito grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="be873-612">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="be873-613">waitpid trabalha com IDs de grupo de processos (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="be873-613">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="be873-614">desempenho de mmap significativamente melhorado para grandes regiões de reserva; melhora o desempenho do ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="be873-614">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="be873-615">suporte a personalidades para READ_IMPLIES_EXEC; corrige maxima e clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="be873-615">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="be873-616">mprotect dá suporte a PROT_GROWSDOWN; corrige o clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="be873-616">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="be873-617">correções de falhas de página no modo de excesso de confirmação; corrige sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="be873-617">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="be873-618">o clone dá suporte a mais combinações de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="be873-618">clone supports more flags combinations</span></span>
* <span data-ttu-id="be873-619">Dar suporte a select/epoll de arquivos epoll (anteriormente, algo não operacional).</span><span class="sxs-lookup"><span data-stu-id="be873-619">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="be873-620">Notificar ptrace de syscalls não implementadas.</span><span class="sxs-lookup"><span data-stu-id="be873-620">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="be873-621">Desconsideração de interfaces que não estão em funcionamento ao gerar nomes de servidor resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="be873-621">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="be873-622">Enumeração das interfaces de rede sem endereço físico.</span><span class="sxs-lookup"><span data-stu-id="be873-622">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="be873-623">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="be873-623">[GH 2685]</span></span>
* <span data-ttu-id="be873-624">Pequenas correções de bug e melhorias.</span><span class="sxs-lookup"><span data-stu-id="be873-624">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="be873-625">Ferramentas do Linux disponíveis para desenvolvedores no Windows</span><span class="sxs-lookup"><span data-stu-id="be873-625">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="be873-626">A Cadeia de Ferramentas de Linha de Comando do Windows ferramentas inclui bsdtar (tar) e curl.</span><span class="sxs-lookup"><span data-stu-id="be873-626">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="be873-627">Leia [este blog](https://aka.ms/tarcurlwindows) para saber mais sobre a adição dessas duas novas ferramentas e veja como elas estão moldando a experiência do desenvolvedor no Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-627">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="be873-628">`AF_UNIX` está disponível no SDK do Participante do Programa Windows Insider (17061+).</span><span class="sxs-lookup"><span data-stu-id="be873-628">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="be873-629">Leia [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para saber mais sobre o `AF_UNIX` e como os desenvolvedores do Windows podem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="be873-629">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="be873-630">Console</span><span class="sxs-lookup"><span data-stu-id="be873-630">Console</span></span>
* <span data-ttu-id="be873-631">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-631">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-632">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-632">LTP Results:</span></span>
<span data-ttu-id="be873-633">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-633">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="be873-634">Build 17046</span><span class="sxs-lookup"><span data-stu-id="be873-634">Build 17046</span></span>

<span data-ttu-id="be873-635">Para obter informações gerais do Windows sobre o Build 17046, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="be873-635">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="be873-636">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-636">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-637">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-637">WSL</span></span>
- <span data-ttu-id="be873-638">Permissão para que processos sejam executados sem um terminal ativo.</span><span class="sxs-lookup"><span data-stu-id="be873-638">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="be873-639">[GH 709, 1007, 1511, 2252, 2391 e outros]</span><span class="sxs-lookup"><span data-stu-id="be873-639">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="be873-640">Melhor suporte a CLONE_VFORK e CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="be873-640">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="be873-641">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="be873-641">[GH 1878, 2615]</span></span>
- <span data-ttu-id="be873-642">Desconsideração de drivers de filtro de TDI para operações de rede WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-642">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="be873-643">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="be873-643">[GH 1554]</span></span>
- <span data-ttu-id="be873-644">DrvFs cria NT symlinks quando determinadas condições são atendidas.</span><span class="sxs-lookup"><span data-stu-id="be873-644">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="be873-645">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="be873-645">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="be873-646">O destino do link precisa ser relativo, não pode cruzar nenhum ponto de montagem nem symlink e precisa existir.</span><span class="sxs-lookup"><span data-stu-id="be873-646">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="be873-647">O usuário deve ter SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (isso normalmente requer que você inicie o wsl.exe com privilégios elevados), a menos que o modo de desenvolvedor esteja ativado.</span><span class="sxs-lookup"><span data-stu-id="be873-647">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="be873-648">Em todas as outras situações, o DrvFs ainda cria symlinks do WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-648">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="be873-649">Permissão para a execução de instâncias de WSL elevadas e não elevadas simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="be873-649">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="be873-650">Suporte a /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="be873-650">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="be873-651">Adição de wslpath para realizar conversões de caminho WSL<->Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-651">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="be873-652">[GH 522, 1243, 1834, 2327 e outros]</span><span class="sxs-lookup"><span data-stu-id="be873-652">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="be873-653">Console</span><span class="sxs-lookup"><span data-stu-id="be873-653">Console</span></span>
- <span data-ttu-id="be873-654">Sem correções.</span><span class="sxs-lookup"><span data-stu-id="be873-654">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-655">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-655">LTP Results:</span></span>
<span data-ttu-id="be873-656">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-656">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="be873-657">Build 17040</span><span class="sxs-lookup"><span data-stu-id="be873-657">Build 17040</span></span>

<span data-ttu-id="be873-658">Para obter informações gerais do Windows sobre o Build 17040, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="be873-658">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-659">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-659">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-660">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-660">WSL</span></span>
- <span data-ttu-id="be873-661">Nenhuma correção desde o 17035.</span><span class="sxs-lookup"><span data-stu-id="be873-661">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="be873-662">Console</span><span class="sxs-lookup"><span data-stu-id="be873-662">Console</span></span>
- <span data-ttu-id="be873-663">Nenhuma correção desde o 17035.</span><span class="sxs-lookup"><span data-stu-id="be873-663">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-664">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-664">LTP Results:</span></span>
<span data-ttu-id="be873-665">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-665">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="be873-666">Build 17035</span><span class="sxs-lookup"><span data-stu-id="be873-666">Build 17035</span></span>

<span data-ttu-id="be873-667">Para obter informações gerais do Windows sobre o Build 17035, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="be873-667">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-668">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-668">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-669">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-669">WSL</span></span>
- <span data-ttu-id="be873-670">O acesso a arquivos no DrvFs pode ocasionalmente falhar com EINVAL.</span><span class="sxs-lookup"><span data-stu-id="be873-670">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="be873-671">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="be873-671">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="be873-672">Console</span><span class="sxs-lookup"><span data-stu-id="be873-672">Console</span></span>
- <span data-ttu-id="be873-673">Um pouco de perda de cor ao inserir/excluir linhas no modo VT.</span><span class="sxs-lookup"><span data-stu-id="be873-673">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-674">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-674">LTP Results:</span></span>
<span data-ttu-id="be873-675">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-675">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="be873-676">Build 17025</span><span class="sxs-lookup"><span data-stu-id="be873-676">Build 17025</span></span>

<span data-ttu-id="be873-677">Para obter informações gerais do Windows sobre o Build 17025, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="be873-677">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-678">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-678">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-679">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-679">WSL</span></span>
- <span data-ttu-id="be873-680">Inicialização dos processos iniciais em um novo grupo de processos de primeiro plano [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="be873-680">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="be873-681">Correções de entrega SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="be873-681">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="be873-682">Geração do nome de ponte virtual padrão se nenhum for fornecido [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="be873-682">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="be873-683">Implementação de /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="be873-683">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="be873-684">Mais correções de pipe stdout/stderr de interop.</span><span class="sxs-lookup"><span data-stu-id="be873-684">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="be873-685">Chamada do sistema syncfs de stub.</span><span class="sxs-lookup"><span data-stu-id="be873-685">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="be873-686">Console</span><span class="sxs-lookup"><span data-stu-id="be873-686">Console</span></span>
- <span data-ttu-id="be873-687">Correção da conversão de VT de entrada para consoles de terceiros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="be873-687">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-688">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-688">LTP Results:</span></span>
<span data-ttu-id="be873-689">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-689">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="be873-690">Build 17017</span><span class="sxs-lookup"><span data-stu-id="be873-690">Build 17017</span></span>

<span data-ttu-id="be873-691">Para obter informações gerais do Windows sobre o Build 17017, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="be873-691">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-692">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-692">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-693">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-693">WSL</span></span>
- <span data-ttu-id="be873-694">Desconsideração dos cabeçalhos de programa ELF vazios [GH 330].</span><span class="sxs-lookup"><span data-stu-id="be873-694">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="be873-695">Permissão para que o LxssManager Crie instâncias do WSL para usuários não interativos (SSH e suporte a tarefas agendadas) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="be873-695">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="be873-696">Suporte a cenários de ("início") WSL-> Win32-> WSL [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="be873-696">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="be873-697">Suporte limitado para encerramento de aplicativos de console invocados via interop [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="be873-697">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="be873-698">Suporte a opções de montagem para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="be873-698">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="be873-699">Ptrace bloqueando a inicialização do filho [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="be873-699">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="be873-700">EPOLLET com alguns eventos ausentes [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="be873-700">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="be873-701">Retorno de mais dados para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="be873-701">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="be873-702">Getdents com lseek fornece resultados incorretos.</span><span class="sxs-lookup"><span data-stu-id="be873-702">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="be873-703">Correção de alguns travamentos do aplicativo de interop Win32, aguardando a entrada em um pipe que não tem mais dados.</span><span class="sxs-lookup"><span data-stu-id="be873-703">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="be873-704">Suporte do O_ASYNC para arquivos tty/pty.</span><span class="sxs-lookup"><span data-stu-id="be873-704">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="be873-705">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-705">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="be873-706">Console</span><span class="sxs-lookup"><span data-stu-id="be873-706">Console</span></span>
- <span data-ttu-id="be873-707">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-707">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-708">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-708">LTP Results:</span></span>
<span data-ttu-id="be873-709">Testes em andamento.</span><span class="sxs-lookup"><span data-stu-id="be873-709">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="be873-710">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="be873-710">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="be873-711">Build 16288</span><span class="sxs-lookup"><span data-stu-id="be873-711">Build 16288</span></span>

<span data-ttu-id="be873-712">Para obter informações gerais do Windows sobre o Build 16288, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="be873-712">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-713">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-713">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-714">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-714">WSL</span></span>
- <span data-ttu-id="be873-715">Inicialização e relatório corretos de UID, GID e modo para descritores de arquivo de soquete [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="be873-715">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="be873-716">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-716">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="be873-717">Console</span><span class="sxs-lookup"><span data-stu-id="be873-717">Console</span></span>
- <span data-ttu-id="be873-718">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-718">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-719">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-719">LTP Results:</span></span>
<span data-ttu-id="be873-720">Nenhuma alteração desde o 16273</span><span class="sxs-lookup"><span data-stu-id="be873-720">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="be873-721">Build 16278</span><span class="sxs-lookup"><span data-stu-id="be873-721">Build 16278</span></span>

<span data-ttu-id="be873-722">Para obter informações gerais do Windows sobre o Build 162738, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="be873-722">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-723">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-723">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-724">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-724">WSL</span></span>
- <span data-ttu-id="be873-725">Desmapeamento explícito de exibições mapeadas de seções com backup de arquivo ao dividir o estado LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="be873-725">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="be873-726">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-726">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="be873-727">Console</span><span class="sxs-lookup"><span data-stu-id="be873-727">Console</span></span>
- <span data-ttu-id="be873-728">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-728">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-729">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-729">LTP Results:</span></span>
<span data-ttu-id="be873-730">Nenhuma alteração desde o 16273</span><span class="sxs-lookup"><span data-stu-id="be873-730">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="be873-731">Build 16275</span><span class="sxs-lookup"><span data-stu-id="be873-731">Build 16275</span></span>

<span data-ttu-id="be873-732">Para obter informações gerais do Windows sobre o Build 162735, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="be873-732">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-733">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-733">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-734">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-734">WSL</span></span>
- <span data-ttu-id="be873-735">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-735">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="be873-736">Console</span><span class="sxs-lookup"><span data-stu-id="be873-736">Console</span></span>
- <span data-ttu-id="be873-737">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-737">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-738">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-738">LTP Results:</span></span>
<span data-ttu-id="be873-739">Nenhuma alteração desde o 16273</span><span class="sxs-lookup"><span data-stu-id="be873-739">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="be873-740">Build 16273</span><span class="sxs-lookup"><span data-stu-id="be873-740">Build 16273</span></span>

<span data-ttu-id="be873-741">Para obter informações gerais do Windows sobre o Build 16273, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-741">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-742">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-742">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-743">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-743">WSL</span></span>
- <span data-ttu-id="be873-744">Corrigido um problema em que o DrvFs às vezes relatava o tipo de arquivo errado para diretórios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="be873-744">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="be873-745">Permissão para a criação de soquetes NETLINK_KOBJECT_UEVENT para desbloquear programas que usam uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="be873-745">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="be873-746">Adição de suporte para conexão sem bloqueio [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="be873-746">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="be873-747">Implementação do sinalizador de chamada do sistema de clone CLONE_FS [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="be873-747">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="be873-748">Correção de problemas relacionados à manipulação incorreta de guias ou aspas no interop NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="be873-748">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="be873-749">Resolução de erro de acesso negado ao tentar reinicializar instâncias de WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="be873-749">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="be873-750">Implementação das operações FUTEX_REQUEUE e FUTEX_CMP_REQUEUE do futex [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="be873-750">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="be873-751">Correção de permissões para vários arquivos SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="be873-751">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="be873-752">Correção do travamento da pilha do Haskell durante a instalação [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="be873-752">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="be873-753">Implementação dos sinalizadores 'C', 'O' e 'P' do binfmt_misc [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="be873-753">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="be873-754">Adição de /proc/sys/kernel/shmmax/shmmni e /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="be873-754">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="be873-755">Adição de suporte parcial para chamada do sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="be873-755">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="be873-756">SO_REUSEPORT de stub e adicionar suporte para SO_PASSCRED para soquetes netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="be873-756">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="be873-757">Retorno de códigos de erro diferentes de RegisterDistribuiton se uma distribuição estiver sendo instalada ou desinstalada no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-757">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="be873-758">Permissão para o cancelamento de registro de distribuições de WSL parcialmente instaladas por meio de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="be873-758">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="be873-759">Correção do travamento do teste de soquete Python de udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="be873-759">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="be873-760">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-760">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="be873-761">Console</span><span class="sxs-lookup"><span data-stu-id="be873-761">Console</span></span>
- <span data-ttu-id="be873-762">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-762">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-763">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-763">LTP Results:</span></span>
<span data-ttu-id="be873-764">Total de testes: 1904</span><span class="sxs-lookup"><span data-stu-id="be873-764">Total Tests: 1904</span></span><br/>
<span data-ttu-id="be873-765">Total de testes ignorados: 209</span><span class="sxs-lookup"><span data-stu-id="be873-765">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="be873-766">Total de falhas: 229</span><span class="sxs-lookup"><span data-stu-id="be873-766">Total Failures: 229</span></span><br/>
[<span data-ttu-id="be873-767">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-767">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="be873-768">Build 16257</span><span class="sxs-lookup"><span data-stu-id="be873-768">Build 16257</span></span>

<span data-ttu-id="be873-769">Para obter informações gerais do Windows sobre o Build 16257, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-769">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-770">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-770">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-771">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-771">WSL</span></span>
- <span data-ttu-id="be873-772">Implementação da chamada do sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="be873-772">Implement prlimit64 system call</span></span>
- <span data-ttu-id="be873-773">Adição de suporte para ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="be873-773">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="be873-774">MSG_MORE de stub para soquetes TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="be873-774">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="be873-775">Correção do comportamento de vetor auxiliar AT_EXECFN inválido [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="be873-775">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="be873-776">Correção do comportamento de copiar/colar para console/TTY e adição de melhor manipulação de buffer completo [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="be873-776">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="be873-777">Definição de AT_SECURE em vetor auxiliar para os programas set-user-ID e set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="be873-777">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="be873-778">Ponto de extremidade mestre de pseudoterminal não manipulando TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="be873-778">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="be873-779">Correção do que o lseek faz para rebobinar diretórios no LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="be873-779">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="be873-780">/dev/ptmx trava após uso intenso [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="be873-780">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="be873-781">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-781">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="be873-782">Console</span><span class="sxs-lookup"><span data-stu-id="be873-782">Console</span></span>
- <span data-ttu-id="be873-783">Correção para linhas horizontais/sublinhados em todos os lugares [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="be873-783">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="be873-784">Correção para a ordem de processo alterada, tornando o NPM mais difícil de fechar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="be873-784">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="be873-785">Adicionado nosso novo esquema de cores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="be873-785">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-786">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-786">LTP Results:</span></span>
<span data-ttu-id="be873-787">Nenhuma alteração desde o 16251</span><span class="sxs-lookup"><span data-stu-id="be873-787">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="be873-788">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-788">Syscall Support</span></span>
<span data-ttu-id="be873-789">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-789">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-790">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-790">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="be873-791">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="be873-791">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="be873-792">Problema do GitHub n. 2392: Pastas do Windows não reconhecidas pelo WSL...</span><span class="sxs-lookup"><span data-stu-id="be873-792">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="be873-793">No build 16257, o WSL tem problemas para enumerar arquivos/pastas do Windows via `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="be873-793">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="be873-794">Esse problema foi corrigido e deve ser liberado no build do Insiders durante a semana que começa em 14/08/2017.</span><span class="sxs-lookup"><span data-stu-id="be873-794">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="be873-795">Build 16251</span><span class="sxs-lookup"><span data-stu-id="be873-795">Build 16251</span></span>

<span data-ttu-id="be873-796">Para obter informações gerais do Windows sobre o Build 16251, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-796">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-797">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-797">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-798">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-798">WSL</span></span>
- <span data-ttu-id="be873-799">Remova a tag beta do componente opcional do WSL, confira esta [postagem no blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="be873-799">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="be873-800">Inicializar corretamente a UID e a GID salvas para os binários Set-User-ID e Set-Group-ID em exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="be873-800">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="be873-801">Adicionado suporte para ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="be873-801">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="be873-802">Adicionado suporte para ptrace PTRACE_GETFPREGS e PTRACE_GETREGSET com NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="be873-802">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="be873-803">Correção de ptrace para parar em sinais ignorados</span><span class="sxs-lookup"><span data-stu-id="be873-803">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="be873-804">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-804">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="be873-805">Console</span><span class="sxs-lookup"><span data-stu-id="be873-805">Console</span></span>
- <span data-ttu-id="be873-806">Nenhuma alteração relacionada ao console nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-806">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-807">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-807">LTP Results:</span></span>
<span data-ttu-id="be873-808">Número de testes aprovados: 768</span><span class="sxs-lookup"><span data-stu-id="be873-808">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="be873-809">Número de testes reprovados: 244</span><span class="sxs-lookup"><span data-stu-id="be873-809">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="be873-810">Número de testes ignorados: 96</span><span class="sxs-lookup"><span data-stu-id="be873-810">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="be873-811">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-811">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="be873-812">Build 16241</span><span class="sxs-lookup"><span data-stu-id="be873-812">Build 16241</span></span>

<span data-ttu-id="be873-813">Para obter informações gerais do Windows sobre o Build 16241, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-813">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-814">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-814">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="be873-815">WSL</span><span class="sxs-lookup"><span data-stu-id="be873-815">WSL</span></span>
- <span data-ttu-id="be873-816">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-816">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="be873-817">Console</span><span class="sxs-lookup"><span data-stu-id="be873-817">Console</span></span>
- <span data-ttu-id="be873-818">Correção para a geração do caractere errado como saída para as linhas de cruzamento DEC, originalmente relatadas [aqui](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="be873-818">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="be873-819">Correção para nenhum texto de saída sendo exibido na página de código 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="be873-819">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="be873-820">Não transfira as alterações feitas aos valores RGB de uma cor para outras partes da paleta na alteração de seleção.</span><span class="sxs-lookup"><span data-stu-id="be873-820">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="be873-821">Isso tornará a planilha de propriedades do console muito mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="be873-821">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="be873-822">Ctrl + S parece não funcionar corretamente</span><span class="sxs-lookup"><span data-stu-id="be873-822">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="be873-823">Sem negrito/sem esmaecimento totalmente ausentes dos códigos de escape ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="be873-823">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="be873-824">O console não dá suporte corretamente a temas de cor Vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="be873-824">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="be873-825">Não é possível colar determinados caracteres [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="be873-825">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="be873-826">O redimensionamento de refluxo interage de acordo com o redimensionamento de uma janela do Bash quando as coisas estão na linha de comando/edição [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="be873-826">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="be873-827">Ctrl + L deixa a tela suja [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="be873-827">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="be873-828">Bug de renderização do console ao exibir VT em HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="be873-828">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="be873-829">Caracteres japoneses parecem estranhos com o caractere Unicode U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="be873-829">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="be873-830">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-830">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="be873-831">Build 16237</span><span class="sxs-lookup"><span data-stu-id="be873-831">Build 16237</span></span>

<span data-ttu-id="be873-832">Para obter informações gerais do Windows sobre o Build 16237, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-832">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-833">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-833">Fixed</span></span>
- <span data-ttu-id="be873-834">Usar atributos padrão para arquivos sem EAs em lxfs (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="be873-834">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="be873-835">Adicionado suporte para distribuições que usam atributos estendidos</span><span class="sxs-lookup"><span data-stu-id="be873-835">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="be873-836">Correção do preenchimento das entradas retornadas por getdents e getdents64</span><span class="sxs-lookup"><span data-stu-id="be873-836">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="be873-837">Correção da verificação de permissões para a chamada do sistema shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="be873-837">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="be873-838">Corrigido o estado de epoll inicial incorreto para ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="be873-838">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="be873-839">Correção do DrvFs readdir não retornando todas as entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="be873-839">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="be873-840">Correção do LxFs readdir quando os arquivos estão desvinculados [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="be873-840">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="be873-841">Permissão para que arquivos do DrvFs não vinculados sejam reabertos por meio do procfs</span><span class="sxs-lookup"><span data-stu-id="be873-841">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="be873-842">Substituição da chave do Registro global adicionada para desabilitar os recursos do WSL (interop/montagem de unidade)</span><span class="sxs-lookup"><span data-stu-id="be873-842">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="be873-843">Correção da contagem de blocos incorretos em "stat" para o DrvFs (e o LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="be873-843">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="be873-844">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-844">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="be873-845">Build 16232</span><span class="sxs-lookup"><span data-stu-id="be873-845">Build 16232</span></span>

<span data-ttu-id="be873-846">Para obter informações gerais do Windows sobre o Build 16232, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-846">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-847">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-847">Fixed</span></span>
- <span data-ttu-id="be873-848">Nenhuma alteração relacionada ao WSL nesta versão.</span><span class="sxs-lookup"><span data-stu-id="be873-848">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="be873-849">Build 16226</span><span class="sxs-lookup"><span data-stu-id="be873-849">Build 16226</span></span>

<span data-ttu-id="be873-850">Para obter informações gerais do Windows sobre o Build 16226, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-850">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-851">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-851">Fixed</span></span>
- <span data-ttu-id="be873-852">suporte a syscalls relacionadas a xattr (getxattr, setxattr, listxattr e removexattr).</span><span class="sxs-lookup"><span data-stu-id="be873-852">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="be873-853">suporte a security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="be873-853">security.capablity xattr support.</span></span>
- <span data-ttu-id="be873-854">Compatibilidade aprimorada com determinados sistemas de arquivos e filtros, incluindo servidores SMB não MS.</span><span class="sxs-lookup"><span data-stu-id="be873-854">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="be873-855">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="be873-855">[GH #1952]</span></span>
- <span data-ttu-id="be873-856">Suporte aprimorado para espaços reservados do OneDrive, espaços reservados do GVFS e arquivos compactados do SO Compacto.</span><span class="sxs-lookup"><span data-stu-id="be873-856">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="be873-857">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-857">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="be873-858">Build 16215</span><span class="sxs-lookup"><span data-stu-id="be873-858">Build 16215</span></span>

<span data-ttu-id="be873-859">Para obter informações gerais do Windows sobre o Build 16215, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-859">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-860">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-860">Fixed</span></span>
- <span data-ttu-id="be873-861">O WSL não exige mais o modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="be873-861">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="be873-862">Suporte a junções de diretório no DrvFs.</span><span class="sxs-lookup"><span data-stu-id="be873-862">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="be873-863">Manipulação da desinstalação de pacotes appx de distribuição do WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-863">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="be873-864">Atualização do procfs para mostrar mapeamentos privados e compartilhados.</span><span class="sxs-lookup"><span data-stu-id="be873-864">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="be873-865">Adição de capacidade para o wslconfig.exe limpar as distribuições parcialmente instaladas ou desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="be873-865">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="be873-866">Adicionado suporte para IP_MTU_DISCOVER para soquetes TCP.</span><span class="sxs-lookup"><span data-stu-id="be873-866">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="be873-867">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="be873-867">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="be873-868">Inferência da família de protocolos para rotas para AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="be873-868">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="be873-869">Aprimoramentos de dispositivo serial [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="be873-869">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="be873-870">Build 16199</span><span class="sxs-lookup"><span data-stu-id="be873-870">Build 16199</span></span>

<span data-ttu-id="be873-871">Para obter informações gerais do Windows sobre o Build 16199, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-871">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-872">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-872">Fixed</span></span>
- <span data-ttu-id="be873-873">Nenhuma alteração relacionada ao WSL nestas versões.</span><span class="sxs-lookup"><span data-stu-id="be873-873">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="be873-874">Build 16193</span><span class="sxs-lookup"><span data-stu-id="be873-874">Build 16193</span></span>

<span data-ttu-id="be873-875">Para obter informações gerais do Windows sobre o Build 16193, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-875">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-876">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-876">Fixed</span></span>
- <span data-ttu-id="be873-877">Condição de corrida entre o envio de SIGCONT e um encerramento de um grupo de threads [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="be873-877">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="be873-878">alteração de dispositivos tty e pty para relatar FILE_DEVICE_NAMED_PIPE em vez de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="be873-878">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="be873-879">Correção de SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="be873-879">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="be873-880">A montagem do DrvFs foi movida para o daemon init [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="be873-880">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="be873-881">Adicionado suporte no DrvFs para os symlinks NT a seguir.</span><span class="sxs-lookup"><span data-stu-id="be873-881">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="be873-882">Build 16184</span><span class="sxs-lookup"><span data-stu-id="be873-882">Build 16184</span></span>

<span data-ttu-id="be873-883">Para obter informações gerais do Windows sobre o Build 16184, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-883">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-884">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-884">Fixed</span></span>
- <span data-ttu-id="be873-885">Removida a tarefa de manutenção do pacote apt (lxrun.exe/update)</span><span class="sxs-lookup"><span data-stu-id="be873-885">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="be873-886">Corrigido problema em que a saída não aparecia nos processos do Windows no Node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="be873-886">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="be873-887">Flexibilização dos requisitos de alinhamento no lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="be873-887">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="be873-888">Corrigida a manipulação do sinalizador AT_EMPTY_PATH em um número de chamadas do sistema.</span><span class="sxs-lookup"><span data-stu-id="be873-888">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="be873-889">Corrigido o problema em que a exclusão de arquivos do DrvFs com identificadores abertos fazia com que o arquivo apresentasse comportamento indefinido [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="be873-889">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="be873-890">O /etc/hosts agora herdará entradas do arquivo de hosts do Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="be873-890">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="be873-891">Build 16179</span><span class="sxs-lookup"><span data-stu-id="be873-891">Build 16179</span></span>

<span data-ttu-id="be873-892">Para obter informações gerais do Windows sobre o Build 16179, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-892">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-893">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-893">Fixed</span></span>
- <span data-ttu-id="be873-894">Nenhuma alteração de WSL nesta semana.</span><span class="sxs-lookup"><span data-stu-id="be873-894">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="be873-895">Build 16176</span><span class="sxs-lookup"><span data-stu-id="be873-895">Build 16176</span></span>

<span data-ttu-id="be873-896">Para obter informações gerais do Windows sobre o Build 16176, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-896">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-897">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-897">Fixed</span></span>

- [<span data-ttu-id="be873-898">Suporte serial habilitado</span><span class="sxs-lookup"><span data-stu-id="be873-898">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="be873-899">Adicionada opção de soquete IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="be873-899">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="be873-900">Função pwritev implementada (ao carregar o arquivo para nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="be873-900">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="be873-901">Adicionadas opções de soquete IP IP_MULTICAST_IF e IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="be873-901">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="be873-902">Suporte para as opções de soquete IP_MULTICAST_LOOP e IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="be873-902">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="be873-903">Adicionada a opção de soquete IP(V6)_MTU para node, traceroute, dig, nslookup e host de aplicativos</span><span class="sxs-lookup"><span data-stu-id="be873-903">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="be873-904">Adicionada a opção de soquete IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="be873-904">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="be873-905">Aprimoramentos do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="be873-905">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="be873-906">Permitir a montagem de caminhos UNC</span><span class="sxs-lookup"><span data-stu-id="be873-906">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="be873-907">Habilitar o suporte a CDFS no DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-907">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="be873-908">Manipulação correta das permissões para sistemas de arquivos de rede no DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-908">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="be873-909">Adição de suporte para unidades remotas ao DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-909">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="be873-910">Habilitação do suporte a FAT no DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-910">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="be873-911">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-911">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-912">Resultados do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-912">LTP Results</span></span>
<span data-ttu-id="be873-913">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="be873-913">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="be873-914">Build 16170</span><span class="sxs-lookup"><span data-stu-id="be873-914">Build 16170</span></span>

<span data-ttu-id="be873-915">Para obter informações gerais do Windows sobre o Build 16170, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-915">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="be873-916">Lançamos uma nova [postagem no blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutindo nossos esforços para testar o WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-916">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="be873-917">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-917">Fixed</span></span>

- <span data-ttu-id="be873-918">Suporte à opção de soquete IP_ADD_MEMBERSHIP e IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="be873-918">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="be873-919">Adição de suporte para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="be873-919">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="be873-920">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="be873-920">[GH 1692]</span></span>
- <span data-ttu-id="be873-921">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-921">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-922">Resultados do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-922">LTP Results</span></span>
<span data-ttu-id="be873-923">Nenhuma alteração desde 15042</span><span class="sxs-lookup"><span data-stu-id="be873-923">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="be873-924">Build 15046 para a Atualização do Windows 10 para Criadores</span><span class="sxs-lookup"><span data-stu-id="be873-924">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="be873-925">Não há mais correções nem recursos do WSL planejados para inclusão na Atualização do Windows 10 para Criadores.</span><span class="sxs-lookup"><span data-stu-id="be873-925">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="be873-926">As notas sobre a versão do WSL serão retomadas nas próximas semanas para as adições direcionadas à próxima atualização importante do Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-926">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="be873-927">Para obter informações gerais do Windows sobre o Build 15046 e futuras versões do Insider, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-927">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="be873-928">Build 15042</span><span class="sxs-lookup"><span data-stu-id="be873-928">Build 15042</span></span>

<span data-ttu-id="be873-929">Para obter informações gerais do Windows sobre o Build 15042, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-929">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-930">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-930">Fixed</span></span>

- <span data-ttu-id="be873-931">Correção de um deadlock ao remover um caminho que termina em ".."</span><span class="sxs-lookup"><span data-stu-id="be873-931">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="be873-932">Corrigido um problema em que FIONBIO não retornava 0 em caso de êxito [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="be873-932">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="be873-933">Corrigido um problema com leituras de comprimento zero de soquetes de datagrama inet</span><span class="sxs-lookup"><span data-stu-id="be873-933">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="be873-934">Correção de um possível deadlock devido à condição de corrida na pesquisa de inode do DrvFs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="be873-934">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="be873-935">Suporte estendido para dados complementares de soquete Unix; SCM_CREDENTIALS e SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="be873-935">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="be873-936">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-936">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-937">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-937">LTP Results:</span></span>
<span data-ttu-id="be873-938">Número de testes aprovados: 737</span><span class="sxs-lookup"><span data-stu-id="be873-938">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="be873-939">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="be873-939">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="be873-940">Build 15031</span><span class="sxs-lookup"><span data-stu-id="be873-940">Build 15031</span></span>

<span data-ttu-id="be873-941">Para obter informações gerais do Windows sobre o Build 15031, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-941">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-942">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-942">Fixed</span></span>

- <span data-ttu-id="be873-943">Corrigido um bug em que time(2) se comportava de maneira incorreta esporadicamente.</span><span class="sxs-lookup"><span data-stu-id="be873-943">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="be873-944">Corrigido um problema em que syscalls \*SIGPROCMASK poderiam corromper a máscara de sinal.</span><span class="sxs-lookup"><span data-stu-id="be873-944">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="be873-945">Agora, retorne o comprimento de linha de comando completo na notificação de criação de processo do WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-945">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="be873-946">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="be873-946">[GH 1632]</span></span>
- <span data-ttu-id="be873-947">O WSL agora relata a saída do thread por meio de ptrace para travamentos do GDB.</span><span class="sxs-lookup"><span data-stu-id="be873-947">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="be873-948">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="be873-948">[GH 1196]</span></span>
- <span data-ttu-id="be873-949">Corrigido o bug em que ptys travam após E/S intensa de tmux.</span><span class="sxs-lookup"><span data-stu-id="be873-949">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="be873-950">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="be873-950">[GH 1358]</span></span>
- <span data-ttu-id="be873-951">Correção da validação de tempo limite em muitas chamadas do sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="be873-951">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="be873-952">Adicionado suporte a eventfd EFD_SEMAPHORE [GH 452]</span><span class="sxs-lookup"><span data-stu-id="be873-952">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="be873-953">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-953">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-954">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-954">LTP Results:</span></span>
<span data-ttu-id="be873-955">Número de testes aprovados: 737</span><span class="sxs-lookup"><span data-stu-id="be873-955">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="be873-956">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="be873-956">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="be873-957">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-957">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="be873-958">Build 15025</span><span class="sxs-lookup"><span data-stu-id="be873-958">Build 15025</span></span>

<span data-ttu-id="be873-959">Para obter informações gerais do Windows sobre o Build 15025, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-959">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-960">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-960">Fixed</span></span>

- <span data-ttu-id="be873-961">Correção do bug que interrompeu o grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="be873-961">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="be873-962">Implementado o sinalizador EFD_SEMAPHORE para a syscall eventfd2 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="be873-962">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="be873-963">Implementado /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="be873-963">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="be873-964">Suporte de E/S controlada por sinal para soquetes de fluxo do Unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="be873-964">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="be873-965">Suporte a F_GETPIPE_SZ e F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="be873-965">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="be873-966">Implementação da syscall recvmmsg() [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="be873-966">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="be873-967">Corrigido o bug em que epoll_wait() não estava aguardando [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="be873-967">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="be873-968">Implementação de /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="be873-968">Implement /proc/version_signature</span></span>
- <span data-ttu-id="be873-969">Tee syscall agora retornará uma falha se os dois descritores de arquivo se referirem ao mesmo pipe</span><span class="sxs-lookup"><span data-stu-id="be873-969">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="be873-970">Implementação do comportamento correto para SO_PEERCRED para soquetes Unix</span><span class="sxs-lookup"><span data-stu-id="be873-970">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="be873-971">Corrigido o tratamento de erro de parâmetro inválido da syscall tkill</span><span class="sxs-lookup"><span data-stu-id="be873-971">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="be873-972">Alterações para aumentar o desempenho do DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-972">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="be873-973">Correção secundária para bloqueio de E/S do Ruby</span><span class="sxs-lookup"><span data-stu-id="be873-973">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="be873-974">Corrigido o erro em que recvmsg() retornava EINVAL para o sinalizador MSG_DONTWAIT para soquetes inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="be873-974">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="be873-975">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-975">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-976">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-976">LTP Results:</span></span>
<span data-ttu-id="be873-977">Número de testes aprovados: 732</span><span class="sxs-lookup"><span data-stu-id="be873-977">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="be873-978">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="be873-978">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="be873-979">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-979">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="be873-980">Build 15019</span><span class="sxs-lookup"><span data-stu-id="be873-980">Build 15019</span></span>

<span data-ttu-id="be873-981">Para obter informações gerais do Windows sobre o Build 15019, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-981">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-982">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-982">Fixed</span></span>

- <span data-ttu-id="be873-983">Correção do bug que reportava incorretamente o uso da CPU em procfs para ferramentas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="be873-983">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="be873-984">Ao chamar open() com O_TRUNC em um arquivo existente, INotifyPropertyChanged agora gera IN_MODIFY antes de IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="be873-984">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="be873-985">Correções para getsockopt SO_ERROR de soquetes Unix para habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="be873-985">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="be873-986">Implementação de /proc/sys/net/Core/SOMAXCONN para a linguagem GO</span><span class="sxs-lookup"><span data-stu-id="be873-986">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="be873-987">A tarefa de atualização em segundo plano do pacote apt-get agora executa oculta</span><span class="sxs-lookup"><span data-stu-id="be873-987">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="be873-988">Limpeza do escopo do localhost IPv6 (falha de Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="be873-988">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="be873-989">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-989">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-990">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-990">LTP Results:</span></span>
<span data-ttu-id="be873-991">Número de testes aprovados: 714</span><span class="sxs-lookup"><span data-stu-id="be873-991">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="be873-992">Número de não aprovados (com falha, ignorados, etc.): 249</span><span class="sxs-lookup"><span data-stu-id="be873-992">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="be873-993">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-993">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="be873-994">Build 15014</span><span class="sxs-lookup"><span data-stu-id="be873-994">Build 15014</span></span>

<span data-ttu-id="be873-995">Para obter informações gerais do Windows sobre o Build 15014, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="be873-995">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-996">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-996">Fixed</span></span>

- <span data-ttu-id="be873-997">Ctrl + C agora funciona conforme esperado</span><span class="sxs-lookup"><span data-stu-id="be873-997">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="be873-998">htop e ps auxw agora mostram a utilização de recursos correta (GH 516)</span><span class="sxs-lookup"><span data-stu-id="be873-998">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="be873-999">Conversão básica de exceções NT para sinais.</span><span class="sxs-lookup"><span data-stu-id="be873-999">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="be873-1000">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="be873-1000">(GH #513)</span></span>
- <span data-ttu-id="be873-1001">agora, ao ficar sem espaço, fallocate falha com ENOSPC em vez de EINVAL (GH 1571)</span><span class="sxs-lookup"><span data-stu-id="be873-1001">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="be873-1002">Adicionado /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="be873-1002">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="be873-1003">Implementadas as chamadas de sistema semop e semtimedop</span><span class="sxs-lookup"><span data-stu-id="be873-1003">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="be873-1004">Corrigidos os erros de nslookup com as opções de soquete IP_RECVTOS e IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="be873-1004">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="be873-1005">Suporte para as opções de soquete IP_RECVTTL e IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="be873-1005">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="be873-1006">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1006">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1007">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1007">LTP Results:</span></span>
<span data-ttu-id="be873-1008">Número de testes aprovados: 709</span><span class="sxs-lookup"><span data-stu-id="be873-1008">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="be873-1009">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="be873-1009">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="be873-1010">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1010">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="be873-1011">Resumo das syscalls</span><span class="sxs-lookup"><span data-stu-id="be873-1011">Syscall Summary</span></span>
<span data-ttu-id="be873-1012">Total de syscalls: 384</span><span class="sxs-lookup"><span data-stu-id="be873-1012">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="be873-1013">Total de implementadas: 235</span><span class="sxs-lookup"><span data-stu-id="be873-1013">Total Implemented: 235</span></span> </br>
<span data-ttu-id="be873-1014">Total de fragmentadas: 22</span><span class="sxs-lookup"><span data-stu-id="be873-1014">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="be873-1015">Total de não implementadas: 127</span><span class="sxs-lookup"><span data-stu-id="be873-1015">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="be873-1016">Detalhamento</span><span class="sxs-lookup"><span data-stu-id="be873-1016">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="be873-1017">Build 15007</span><span class="sxs-lookup"><span data-stu-id="be873-1017">Build 15007</span></span>

<span data-ttu-id="be873-1018">Para obter informações gerais do Windows sobre o Build 15007, visite o [blog do Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="be873-1018">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="be873-1019">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="be873-1019">Known Issue</span></span>

- <span data-ttu-id="be873-1020">Há um bug conhecido em que o console não reconhece alguma entrada Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="be873-1020">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="be873-1021">Isso incluiu o comando Ctrl + C, que agirá como um pressionamento comum de C.</span><span class="sxs-lookup"><span data-stu-id="be873-1021">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="be873-1022">Solução alternativa: Mapeamento de uma tecla alternativa para Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="be873-1022">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="be873-1023">Por exemplo, para mapear Ctrl + K para Ctrl + C, faça isto: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="be873-1023">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="be873-1024">Este mapeamento é por terminal e precisará ser realizado *toda* vez que o Bash for inicializado.</span><span class="sxs-lookup"><span data-stu-id="be873-1024">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="be873-1025">Os usuários podem explorar a opção para incluir isto no `.bashrc` deles</span><span class="sxs-lookup"><span data-stu-id="be873-1025">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="be873-1026">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1026">Fixed</span></span>

- <span data-ttu-id="be873-1027">Corrigido o problema em que executar o WSL consumiria 100% de um núcleo de CPU</span><span class="sxs-lookup"><span data-stu-id="be873-1027">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="be873-1028">A opção de soquete IP_PKTINFO, IPV6_RECVPKTINFO agora é compatível.</span><span class="sxs-lookup"><span data-stu-id="be873-1028">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="be873-1029">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="be873-1029">(GH #851, 987)</span></span>
- <span data-ttu-id="be873-1030">Truncamento do endereço físico do adaptador de rede para 16 bytes em lxcore (GH 1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="be873-1030">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="be873-1031">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1031">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1032">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1032">LTP Results:</span></span>
<span data-ttu-id="be873-1033">Número de testes aprovados: 709</span><span class="sxs-lookup"><span data-stu-id="be873-1033">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="be873-1034">Número de não aprovados (com falha, ignorados, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="be873-1034">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="be873-1035">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1035">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="be873-1036">Build 15002</span><span class="sxs-lookup"><span data-stu-id="be873-1036">Build 15002</span></span>

<span data-ttu-id="be873-1037">Para obter informações gerais do Windows sobre o Build 15002, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1037">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="be873-1038">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="be873-1038">Known Issue</span></span>

<span data-ttu-id="be873-1039">Dois problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="be873-1039">Two known issues:</span></span>
- <span data-ttu-id="be873-1040">Há um bug conhecido em que o console não reconhece alguma entrada Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="be873-1040">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="be873-1041">Isso incluiu o comando Ctrl + C, que agirá como um pressionamento comum de C.</span><span class="sxs-lookup"><span data-stu-id="be873-1041">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="be873-1042">Solução alternativa: Mapeamento de uma tecla alternativa para Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="be873-1042">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="be873-1043">Por exemplo, para mapear Ctrl + K para Ctrl + C, faça isto: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="be873-1043">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="be873-1044">Este mapeamento é por terminal e precisará ser realizado *toda* vez que o Bash for inicializado.</span><span class="sxs-lookup"><span data-stu-id="be873-1044">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="be873-1045">Os usuários podem explorar a opção para incluir isto no `.bashrc` deles</span><span class="sxs-lookup"><span data-stu-id="be873-1045">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="be873-1046">Enquanto o WSL estiver em execução, um thread do sistema consumirá 100% de um núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="be873-1046">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="be873-1047">A causa raiz foi resolvida e corrigida internamente.</span><span class="sxs-lookup"><span data-stu-id="be873-1047">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="be873-1048">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1048">Fixed</span></span>

- <span data-ttu-id="be873-1049">Todas as sessões do Bash agora devem ser criadas no mesmo nível de permissão.</span><span class="sxs-lookup"><span data-stu-id="be873-1049">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="be873-1050">Qualquer tentativa de iniciar uma sessão em um nível diferente será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="be873-1050">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="be873-1051">Isso significa que consoles com e sem privilégios de administrador não podem executar simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="be873-1051">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="be873-1052">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="be873-1052">(GH #626)</span></span>
<br/>
- <span data-ttu-id="be873-1053">Implementadas as mensagens NETLINK_ROUTE a seguir (requer administrador do Windows)</span><span class="sxs-lookup"><span data-stu-id="be873-1053">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="be873-1054">RTM_NEWADDR (dá suporte a `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="be873-1054">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="be873-1055">RTM_NEWROUTE (dá suporte a `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="be873-1055">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="be873-1056">RTM_DELADDR (dá suporte a `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="be873-1056">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="be873-1057">RTM_DELROUTE (dá suporte a `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="be873-1057">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="be873-1058">A verificação de tarefa agendada para que os pacotes sejam atualizados não será mais executada em uma conexão limitada (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="be873-1058">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="be873-1059">Corrigido o erro em que o pipe fica preso, ou seja, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="be873-1059">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="be873-1060">Implementada a opção de soquete TCP_KEEPCNT (GH 843)</span><span class="sxs-lookup"><span data-stu-id="be873-1060">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="be873-1061">Implementada a opção de soquete IP_MTU_DISCOVER INET (GH 720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="be873-1061">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="be873-1062">Funcionalidade herdada removida para executar binários NT por meio de init com a pesquisa de caminho de NT.</span><span class="sxs-lookup"><span data-stu-id="be873-1062">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="be873-1063">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="be873-1063">(GH #1325)</span></span>
- <span data-ttu-id="be873-1064">Correção do modo de /dev/kmsg para permitir o acesso de grupo/outro acesso de leitura (0644) (GH 1321)</span><span class="sxs-lookup"><span data-stu-id="be873-1064">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="be873-1065">Implementado /proc/sys/kernel/random/uuid (GH 1092)</span><span class="sxs-lookup"><span data-stu-id="be873-1065">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="be873-1066">Erro corrigido em que a hora de início do processo era mostrada como no ano 2432 (GH 974)</span><span class="sxs-lookup"><span data-stu-id="be873-1066">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="be873-1067">Variável de ambiente TERM padrão alternada para xterm-256color (GH 1446)</span><span class="sxs-lookup"><span data-stu-id="be873-1067">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="be873-1068">Modificado o modo como a confirmação do processo é calculada durante o fork do processo.</span><span class="sxs-lookup"><span data-stu-id="be873-1068">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="be873-1069">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="be873-1069">(GH #1286)</span></span>
- <span data-ttu-id="be873-1070">Implementado /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="be873-1070">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="be873-1071">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="be873-1071">(GH #1286)</span></span>
- <span data-ttu-id="be873-1072">Implementado /proc/net/route file (GH 69)</span><span class="sxs-lookup"><span data-stu-id="be873-1072">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="be873-1073">Corrigido um erro em que o nome do atalho era localizado incorretamente (GH 696)</span><span class="sxs-lookup"><span data-stu-id="be873-1073">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="be873-1074">Corrigida a lógica de análise de ELF que estava validando incorretamente os cabeçalhos de programa e precisava ser menor que (ou igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="be873-1074">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="be873-1075">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="be873-1075">(GH #1048)</span></span>
- <span data-ttu-id="be873-1076">Implementado retorno de chamada statfs para procfs, sysfs, cgroupfs e binfmtfs (GH 1378)</span><span class="sxs-lookup"><span data-stu-id="be873-1076">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="be873-1077">Corrigidas as janelas AptPackageIndexUpdate que não fechavam (GH 1184, também discutido em GH 1193)</span><span class="sxs-lookup"><span data-stu-id="be873-1077">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="be873-1078">Adicionado suporte a ADDR_NO_RANDOMIZE de personalidade de ASLR.</span><span class="sxs-lookup"><span data-stu-id="be873-1078">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="be873-1079">(GH 1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="be873-1079">(GH #1148, 1128)</span></span>
- <span data-ttu-id="be873-1080">Melhoria de PTRACE_GETSIGINFO e SIGSEGV para rastreamentos de pilha gdb apropriados durante o AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="be873-1080">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="be873-1081">A análise de ELF não falha mais para binários patchelf.</span><span class="sxs-lookup"><span data-stu-id="be873-1081">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="be873-1082">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="be873-1082">(GH #471)</span></span>
- <span data-ttu-id="be873-1083">DNS de VPN propagado para /etc/resolv.conf (GH 416, 1350)</span><span class="sxs-lookup"><span data-stu-id="be873-1083">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="be873-1084">Melhorias no fechamento de TCP para transferência de dados mais confiável.</span><span class="sxs-lookup"><span data-stu-id="be873-1084">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="be873-1085">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="be873-1085">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="be873-1086">Agora, o código de erro correto é retornado quando muitos arquivos estão abertos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="be873-1086">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="be873-1087">(GH 1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="be873-1087">(GH #1126, 2090)</span></span>
- <span data-ttu-id="be873-1088">O log de auditoria do Windows agora relata o nome da imagem no processo create audit.</span><span class="sxs-lookup"><span data-stu-id="be873-1088">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="be873-1089">Agora, falha normalmente ao iniciar bash.exe de dentro de uma janela do Bash</span><span class="sxs-lookup"><span data-stu-id="be873-1089">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="be873-1090">Mensagem de erro adicionada quando a interop não consegue acessar um diretório de trabalho em LxFs (ou seja, notepad.exe. bashrc)</span><span class="sxs-lookup"><span data-stu-id="be873-1090">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="be873-1091">Corrigido o problema em que o caminho do Windows era truncado no WSL</span><span class="sxs-lookup"><span data-stu-id="be873-1091">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="be873-1092">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1092">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1093">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1093">LTP Results:</span></span>
<span data-ttu-id="be873-1094">Número de testes aprovados: 690</span><span class="sxs-lookup"><span data-stu-id="be873-1094">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="be873-1095">Número de não aprovados (com falha, ignorados, etc.): 274</span><span class="sxs-lookup"><span data-stu-id="be873-1095">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="be873-1096">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1096">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="be873-1097">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1097">Syscall Support</span></span>
<span data-ttu-id="be873-1098">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1098">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1099">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1099">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="be873-1100">Build 14986</span><span class="sxs-lookup"><span data-stu-id="be873-1100">Build 14986</span></span>

<span data-ttu-id="be873-1101">Para obter informações gerais do Windows sobre o Build 14986, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1101">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1102">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1102">Fixed</span></span>

- <span data-ttu-id="be873-1103">Correção de verificações de bugs com NetLink e IOCTLs pty</span><span class="sxs-lookup"><span data-stu-id="be873-1103">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="be873-1104">A versão do kernel agora relata 4.4.0-43 para consistência com o Xenial</span><span class="sxs-lookup"><span data-stu-id="be873-1104">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="be873-1105">O bash.exe agora é iniciado quando a entrada é direcionada para 'nul:' (GH 1259)</span><span class="sxs-lookup"><span data-stu-id="be873-1105">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="be873-1106">IDs de thread agora são relatadas corretamente em procfs (GH 967)</span><span class="sxs-lookup"><span data-stu-id="be873-1106">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="be873-1107">Os sinalizadores IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR agora são compatíveis com inotify_add_watch() (GH 1280)</span><span class="sxs-lookup"><span data-stu-id="be873-1107">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="be873-1108">Implementado timer_create e chamadas de sistema relacionadas.</span><span class="sxs-lookup"><span data-stu-id="be873-1108">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="be873-1109">Isso habilita o suporte a GHC (GH 307)</span><span class="sxs-lookup"><span data-stu-id="be873-1109">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="be873-1110">Corrigido o problema em que o ping retornava um tempo de 0,000 ms (GH 1296)</span><span class="sxs-lookup"><span data-stu-id="be873-1110">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="be873-1111">O código de erro correto é retornado quando muitos arquivos estão abertos.</span><span class="sxs-lookup"><span data-stu-id="be873-1111">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="be873-1112">Corrigido o problema no WSL em que a solicitação do NetLink para dados do adaptador de rede falharia com EINVAL se o endereço de hardware do adaptador fosse de 32 bytes (assim como na interface Teredo)</span><span class="sxs-lookup"><span data-stu-id="be873-1112">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="be873-1113">Observe que o utilitário "ip" do Linux contém um bug que faz com que ele falhe se o WSL relata um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="be873-1113">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="be873-1114">Esse é um bug em "ip", não no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1114">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="be873-1115">O utilitário "ip" codifica o tamanho do buffer de cadeia de caracteres usado para imprimir o endereço de hardware e esse buffer é muito pequeno para imprimir um endereço de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="be873-1115">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="be873-1116">Correções e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1116">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1117">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1117">LTP Results:</span></span>
<span data-ttu-id="be873-1118">Número de testes aprovados: 669</span><span class="sxs-lookup"><span data-stu-id="be873-1118">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="be873-1119">Número de não aprovados (com falha, ignorados, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="be873-1119">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="be873-1120">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1120">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="be873-1121">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1121">Syscall Support</span></span>
<span data-ttu-id="be873-1122">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1122">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1123">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1123">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="be873-1124">Build 14971</span><span class="sxs-lookup"><span data-stu-id="be873-1124">Build 14971</span></span>

<span data-ttu-id="be873-1125">Para obter informações gerais do Windows sobre o Build 14971, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1125">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1126">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1126">Fixed</span></span>

 - <span data-ttu-id="be873-1127">Devido a circunstâncias além do nosso controle, não há atualizações nesse build para o Subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="be873-1127">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="be873-1128">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="be873-1128">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1129">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1129">LTP Results:</span></span>
<span data-ttu-id="be873-1130">Inalterado desde o 14965</span><span class="sxs-lookup"><span data-stu-id="be873-1130">Unchanged from 14965</span></span> </br>
<span data-ttu-id="be873-1131">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="be873-1131">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="be873-1132">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="be873-1132">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="be873-1133">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1133">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="be873-1134">Build 14965</span><span class="sxs-lookup"><span data-stu-id="be873-1134">Build 14965</span></span>

<span data-ttu-id="be873-1135">Para obter informações gerais do Windows sobre o Build 14965, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1135">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1136">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1136">Fixed</span></span>

- <span data-ttu-id="be873-1137">Suporte para RTM_GETLINK e RTM_GETADDR do protocolo NETLINK_ROUTE de soquetes NetLink (GH 468)</span><span class="sxs-lookup"><span data-stu-id="be873-1137">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="be873-1138">Habilita os comandos ip e ifconfig para enumeração de rede</span><span class="sxs-lookup"><span data-stu-id="be873-1138">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="be873-1139">Mais informações podem ser encontradas em nossa [postagem no blog de rede WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="be873-1139">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="be873-1140">/sbin agora está no caminho do usuário por padrão</span><span class="sxs-lookup"><span data-stu-id="be873-1140">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="be873-1141">O caminho de usuário do NT agora é acrescentado ao caminho do WSL por padrão (ou seja, agora você pode digitar notepad.exe sem adicionar System32 ao caminho do Linux)</span><span class="sxs-lookup"><span data-stu-id="be873-1141">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="be873-1142">Adicionado suporte para /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="be873-1142">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="be873-1143">Os binários do NT agora podem ser iniciados do WSL quando o diretório de trabalho atual contém caracteres não ANSI (GH 1254)</span><span class="sxs-lookup"><span data-stu-id="be873-1143">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="be873-1144">Permissão para o desligamento no soquete de fluxo do Unix desconectado.</span><span class="sxs-lookup"><span data-stu-id="be873-1144">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="be873-1145">Adicionado suporte para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="be873-1145">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="be873-1146">Adicionado suporte para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="be873-1146">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="be873-1147">Corrigido o erro em que o pipe fica preso, ou seja, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="be873-1147">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="be873-1148">Manipulação das solicitações para se conectar ao terminal atual.</span><span class="sxs-lookup"><span data-stu-id="be873-1148">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="be873-1149">Marcação de /proc/<pid>/oom_score_adj como gravável.</span><span class="sxs-lookup"><span data-stu-id="be873-1149">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="be873-1150">Adição da pasta/sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="be873-1150">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="be873-1151">sched_setaffinity deve retornar o número de máscara de bits de afinidade</span><span class="sxs-lookup"><span data-stu-id="be873-1151">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="be873-1152">Correção da lógica de validação ELF que pressupõe incorretamente que os caminhos do interpretador devem ter menos de 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="be873-1152">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="be873-1153">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="be873-1153">(GH #743)</span></span>
- <span data-ttu-id="be873-1154">Descritores de arquivo abertos podem manter a janela do console aberta (GH 1187)</span><span class="sxs-lookup"><span data-stu-id="be873-1154">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="be873-1155">Corrigido um erro em que rename() falhava com barra à direita no nome de destino (GH 1008)</span><span class="sxs-lookup"><span data-stu-id="be873-1155">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="be873-1156">Implementação de /proc/net/dev file</span><span class="sxs-lookup"><span data-stu-id="be873-1156">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="be873-1157">Corrigida a ocorrência de pings de 0,000 ms devido à resolução do timer.</span><span class="sxs-lookup"><span data-stu-id="be873-1157">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="be873-1158">Implementado /proc/self/environ (GH 730)</span><span class="sxs-lookup"><span data-stu-id="be873-1158">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="be873-1159">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1159">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1160">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1160">LTP Results:</span></span>
<span data-ttu-id="be873-1161">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="be873-1161">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="be873-1162">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="be873-1162">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="be873-1163">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1163">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="be873-1164">Build 14959</span><span class="sxs-lookup"><span data-stu-id="be873-1164">Build 14959</span></span>

<span data-ttu-id="be873-1165">Para obter informações gerais do Windows sobre o Build 14959, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="be873-1165">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1166">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1166">Fixed</span></span>

- <span data-ttu-id="be873-1167">Notificação de processo Pico aprimorada para Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-1167">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="be873-1168">Informações adicionais encontradas no [blog do WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="be873-1168">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="be873-1169">Estabilidade aprimorada com a interop do Windows</span><span class="sxs-lookup"><span data-stu-id="be873-1169">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="be873-1170">Corrigido o erro 0x80070057 ao iniciar o bash.exe quando a EDP (proteção de dados empresariais) está habilitada</span><span class="sxs-lookup"><span data-stu-id="be873-1170">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="be873-1171">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1171">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1172">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1172">LTP Results:</span></span>
<span data-ttu-id="be873-1173">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="be873-1173">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="be873-1174">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="be873-1174">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="be873-1175">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1175">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="be873-1176">Build 14955</span><span class="sxs-lookup"><span data-stu-id="be873-1176">Build 14955</span></span>

<span data-ttu-id="be873-1177">Para obter informações gerais do Windows sobre o Build 14955, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="be873-1177">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1178">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1178">Fixed</span></span>

 - <span data-ttu-id="be873-1179">Devido a circunstâncias além do nosso controle, não há atualizações nesse build para o Subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="be873-1179">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="be873-1180">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="be873-1180">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1181">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1181">LTP Results:</span></span>
<span data-ttu-id="be873-1182">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="be873-1182">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="be873-1183">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="be873-1183">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="be873-1184">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1184">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="be873-1185">Build 14951</span><span class="sxs-lookup"><span data-stu-id="be873-1185">Build 14951</span></span>

<span data-ttu-id="be873-1186">Para obter informações gerais do Windows sobre o Build 14951, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1186">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="be873-1187">Novo recurso: Interoperabilidade entre Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="be873-1187">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="be873-1188">Os binários do Windows agora podem ser chamados diretamente da linha de comando do WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1188">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="be873-1189">Isso dá aos usuários a capacidade de interagir com o ambiente e o sistema do Windows de uma maneira que não era possível.</span><span class="sxs-lookup"><span data-stu-id="be873-1189">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="be873-1190">Como um exemplo rápido, agora é possível que os usuários executem os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="be873-1190">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="be873-1191">Mais informações podem ser encontradas em:</span><span class="sxs-lookup"><span data-stu-id="be873-1191">More information can be found at:</span></span>

- [<span data-ttu-id="be873-1192">Blog da equipe do WSL para interop</span><span class="sxs-lookup"><span data-stu-id="be873-1192">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="be873-1193">Documentação de interop do MSDN</span><span class="sxs-lookup"><span data-stu-id="be873-1193">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="be873-1194">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1194">Fixed</span></span>

- <span data-ttu-id="be873-1195">O Ubuntu 16.04 (Xenial) agora está instalado para todas as novas instâncias de WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1195">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="be873-1196">Os usuários com instâncias 14.04 (confiáveis) existentes não serão atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="be873-1196">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="be873-1197">A localidade definida durante a instalação agora é exibida</span><span class="sxs-lookup"><span data-stu-id="be873-1197">Locale set during install is now displayed</span></span>
- <span data-ttu-id="be873-1198">Melhorias de terminal, incluindo bugs em que o redirecionamento de um processo do WSL para um arquivo nem sempre funciona</span><span class="sxs-lookup"><span data-stu-id="be873-1198">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="be873-1199">O tempo de vida do console deve estar vinculado ao tempo de vida do bash.exe</span><span class="sxs-lookup"><span data-stu-id="be873-1199">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="be873-1200">O tamanho da janela do console deve usar um tamanho visível, não o tamanho do buffer</span><span class="sxs-lookup"><span data-stu-id="be873-1200">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="be873-1201">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1201">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1202">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1202">LTP Results:</span></span>
<span data-ttu-id="be873-1203">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="be873-1203">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="be873-1204">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="be873-1204">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="be873-1205">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1205">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="be873-1206">Build 14946</span><span class="sxs-lookup"><span data-stu-id="be873-1206">Build 14946</span></span>

<span data-ttu-id="be873-1207">Para obter informações gerais do Windows sobre o Build 14946, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="be873-1207">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1208">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1208">Fixed</span></span>

- <span data-ttu-id="be873-1209">Corrigido um problema que impedia a criação de contas de usuário do WSL para usuários com nomes de usuário NT contendo espaços ou aspas.</span><span class="sxs-lookup"><span data-stu-id="be873-1209">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="be873-1210">Altere VolFs e DrvFs para retornar 0 para a contagem de links do diretório em stat</span><span class="sxs-lookup"><span data-stu-id="be873-1210">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="be873-1211">Suporte à opção de soquete IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="be873-1211">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="be873-1212">Limite para um loop de E/S de console único por tty.</span><span class="sxs-lookup"><span data-stu-id="be873-1212">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="be873-1213">Por exemplo, o comando a seguir é possível:</span><span class="sxs-lookup"><span data-stu-id="be873-1213">Example: the following command is possible:</span></span>
  - <span data-ttu-id="be873-1214">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="be873-1214">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="be873-1215">substituição de espaços por tabulações em /proc/cpuinfo (GH 1115)</span><span class="sxs-lookup"><span data-stu-id="be873-1215">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="be873-1216">O DrvFs agora aparece em mountinfo com um nome que corresponde ao volume do Windows montado</span><span class="sxs-lookup"><span data-stu-id="be873-1216">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="be873-1217">/home e /root agora aparecem em mountinfo com os nomes corretos</span><span class="sxs-lookup"><span data-stu-id="be873-1217">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="be873-1218">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1218">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1219">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1219">LTP Results:</span></span>
<span data-ttu-id="be873-1220">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="be873-1220">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="be873-1221">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="be873-1221">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="be873-1222">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1222">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="be873-1223">Build 14942</span><span class="sxs-lookup"><span data-stu-id="be873-1223">Build 14942</span></span>

<span data-ttu-id="be873-1224">Para obter informações gerais do Windows sobre o Build 14942, visite o [blog do Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="be873-1224">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1225">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1225">Fixed</span></span>

- <span data-ttu-id="be873-1226">Várias verificações de bug resolvidas, incluindo a falha de rede "TENTATIVA DE EXECUTAR A MEMÓRIA NOEXECUTE" que estava bloqueando o SSH</span><span class="sxs-lookup"><span data-stu-id="be873-1226">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="be873-1227">o suporte do inotifiy para notificações geradas de aplicativos do Windows no DrvFs agora está em</span><span class="sxs-lookup"><span data-stu-id="be873-1227">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="be873-1228">Implementação de TCP_KEEPIDLE e TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="be873-1228">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="be873-1229">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="be873-1229">(GH #695)</span></span>
- <span data-ttu-id="be873-1230">Implementação da chamada do sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="be873-1230">Implement the pivot_root system call</span></span>
- <span data-ttu-id="be873-1231">Implementar opção de soquete para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="be873-1231">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="be873-1232">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1232">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="be873-1233">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1233">LTP Results:</span></span>
<span data-ttu-id="be873-1234">Número de testes aprovados: 665</span><span class="sxs-lookup"><span data-stu-id="be873-1234">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="be873-1235">Número de não aprovados (com falha, ignorados, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="be873-1235">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="be873-1236">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1236">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="be873-1237">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1237">Syscall Support</span></span>
<span data-ttu-id="be873-1238">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1238">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1239">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1239">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="be873-1240">Build 14936</span><span class="sxs-lookup"><span data-stu-id="be873-1240">Build 14936</span></span>

<span data-ttu-id="be873-1241">Para obter informações gerais do Windows sobre o Build 14936, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1241">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="be873-1242">Observação: O WSL instalará o Ubuntu versão 16.04 (Xenial) em vez do Ubuntu 14.04 (Trusty) em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="be873-1242">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="be873-1243">Essa alteração se aplicará a Participantes do Programa Windows Insider que estejam instalando novas instâncias (lxrun.exe /install ou primeira execução de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="be873-1243">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="be873-1244">As instâncias existentes com Trusty não serão atualizadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="be873-1244">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="be873-1245">Os usuários podem atualizar sua imagem do Trusty para Xenial usando o comando do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="be873-1245">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="be873-1246">Problema conhecido</span><span class="sxs-lookup"><span data-stu-id="be873-1246">Known Issue</span></span>
<span data-ttu-id="be873-1247">O WSL está enfrentando um problema com algumas implementações de soquete.</span><span class="sxs-lookup"><span data-stu-id="be873-1247">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="be873-1248">A verificação de bugs se manifesta como uma falha com o erro "TENTATIVA DE EXECUTAR A MEMÓRIA NOEXECUTE".</span><span class="sxs-lookup"><span data-stu-id="be873-1248">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="be873-1249">A manifestação mais comum desse problema é uma falha ao usar SSH.</span><span class="sxs-lookup"><span data-stu-id="be873-1249">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="be873-1250">A causa raiz é corrigida em builds internos e será enviada por push para pessoas na primeira oportunidade.</span><span class="sxs-lookup"><span data-stu-id="be873-1250">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="be873-1251">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1251">Fixed</span></span>

- <span data-ttu-id="be873-1252">Implementada a chamada do sistema chroot</span><span class="sxs-lookup"><span data-stu-id="be873-1252">Implemented the chroot system call</span></span>
- <span data-ttu-id="be873-1253">Melhorias no inotifiy ~~incluindo suporte para notificações geradas de aplicativos do Windows no DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="be873-1253">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="be873-1254">Correção: O suporte do INotifyPropertyChanged para alterações provenientes de aplicativos do Windows não estão disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1254">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="be873-1255">Associação de soquete a IPV6::<port n> agora dá suporte a IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996)</span><span class="sxs-lookup"><span data-stu-id="be873-1255">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="be873-1256">Comportamento de WNOWAIT implementado para a chamada do sistema waitid (GH 638)</span><span class="sxs-lookup"><span data-stu-id="be873-1256">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="be873-1257">Suporte para as opções de soquete de IP IP_HDRINCL e IP_TTL</span><span class="sxs-lookup"><span data-stu-id="be873-1257">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="be873-1258">read() de tamanho zero deve retornar imediatamente (GH 975)</span><span class="sxs-lookup"><span data-stu-id="be873-1258">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="be873-1259">Manipulação correta de nomes de arquivos e prefixos de nome de arquivo que não incluem um terminador nulo em um arquivo .tar.</span><span class="sxs-lookup"><span data-stu-id="be873-1259">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="be873-1260">Suporte do epoll para/dev/null</span><span class="sxs-lookup"><span data-stu-id="be873-1260">epoll support for /dev/null</span></span>
- <span data-ttu-id="be873-1261">Correção da origem de tempo /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="be873-1261">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="be873-1262">Bash-c agora é capaz de redirecionar para um arquivo</span><span class="sxs-lookup"><span data-stu-id="be873-1262">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="be873-1263">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1263">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1264">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1264">LTP Results:</span></span>
<span data-ttu-id="be873-1265">Número de testes aprovados: 664</span><span class="sxs-lookup"><span data-stu-id="be873-1265">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="be873-1266">Número de não aprovados (com falha, ignorados, etc.): 264</span><span class="sxs-lookup"><span data-stu-id="be873-1266">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="be873-1267">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1267">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="be873-1268">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1268">Syscall Support</span></span>
<span data-ttu-id="be873-1269">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1269">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1270">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1270">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="be873-1271">Build 14931</span><span class="sxs-lookup"><span data-stu-id="be873-1271">Build 14931</span></span>

<span data-ttu-id="be873-1272">Para obter informações gerais do Windows sobre o Build 14931, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1272">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1273">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1273">Fixed</span></span>

 - <span data-ttu-id="be873-1274">Devido a circunstâncias além do nosso controle, não há atualizações nesse build para o Subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="be873-1274">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="be873-1275">As atualizações agendadas regularmente serão retomadas na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="be873-1275">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="be873-1276">Build 14926</span><span class="sxs-lookup"><span data-stu-id="be873-1276">Build 14926</span></span>

<span data-ttu-id="be873-1277">Para obter informações gerais do Windows sobre o Build 14926, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-1277">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1278">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1278">Fixed</span></span>

- <span data-ttu-id="be873-1279">O ping agora funciona em consoles sem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="be873-1279">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="be873-1280">O Ping6 agora é compatível, inclusive quando sem privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="be873-1280">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="be873-1281">Suporte a INotifyPropertyChanged para arquivos modificados por meio de WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1281">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="be873-1282">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="be873-1282">(GH #216)</span></span>
  - <span data-ttu-id="be873-1283">Sinalizadores compatíveis:</span><span class="sxs-lookup"><span data-stu-id="be873-1283">Flags supported:</span></span>
    - <span data-ttu-id="be873-1284">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="be873-1284">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="be873-1285">Eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="be873-1285">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="be873-1286">Atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="be873-1286">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="be873-1287">saída de leitura: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="be873-1287">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="be873-1288">Problema conhecido: a modificação de arquivos de aplicativos do Windows não gera nenhum evento</span><span class="sxs-lookup"><span data-stu-id="be873-1288">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="be873-1289">O soquete Unix agora dá suporte a SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="be873-1289">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="be873-1290">Resultados do LTP:</span><span class="sxs-lookup"><span data-stu-id="be873-1290">LTP Results:</span></span>
<span data-ttu-id="be873-1291">Número de testes aprovados: 651</span><span class="sxs-lookup"><span data-stu-id="be873-1291">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="be873-1292">Número de não aprovados (com falha, ignorados, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="be873-1292">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="be873-1293">Logs de execução de teste do LTP</span><span class="sxs-lookup"><span data-stu-id="be873-1293">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="be873-1294">Build 14915</span><span class="sxs-lookup"><span data-stu-id="be873-1294">Build 14915</span></span>

<span data-ttu-id="be873-1295">Para obter informações gerais do Windows sobre o Build 14915, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="be873-1295">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1296">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1296">Fixed</span></span>
-  <span data-ttu-id="be873-1297">Par de soquetes para soquetes de datagramas Unix (GH 262)</span><span class="sxs-lookup"><span data-stu-id="be873-1297">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="be873-1298">Suporte a soquetes Unix para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="be873-1298">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="be873-1299">Suporte a soquetes Unix para SO_BROADCAST (GH 568)</span><span class="sxs-lookup"><span data-stu-id="be873-1299">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="be873-1300">Suporte a soquetes Unix para SOCK_SEQPACKET (GH 758, 546)</span><span class="sxs-lookup"><span data-stu-id="be873-1300">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="be873-1301">Adição de suporte para envio, recebimento e desligamento de soquete de datagrama Unix</span><span class="sxs-lookup"><span data-stu-id="be873-1301">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="be873-1302">Correção de verificação de bugs devido à validação de parâmetro mmap inválida para endereços não fixos.</span><span class="sxs-lookup"><span data-stu-id="be873-1302">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="be873-1303">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="be873-1303">(GH #847)</span></span>
- <span data-ttu-id="be873-1304">Suporte para suspensão/retomada de estados de terminal</span><span class="sxs-lookup"><span data-stu-id="be873-1304">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="be873-1305">Suporte para ioctl TIOCPKT para desbloquear o utilitário de tela (GH 774)</span><span class="sxs-lookup"><span data-stu-id="be873-1305">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="be873-1306">Problema conhecido: Teclas de função não operacionais</span><span class="sxs-lookup"><span data-stu-id="be873-1306">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="be873-1307">Correção de uma corrida em TimerFd que poderia fazer com que um membro 'ReaderReady' liberado fosse acessado pelo LxpTimerFdWorkerRoutine (GH 814)</span><span class="sxs-lookup"><span data-stu-id="be873-1307">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="be873-1308">Habilitar suporte à chamada do sistema reiniciável para futex, poll e clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="be873-1308">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="be873-1309">Adicionado suporte à montagem de associação</span><span class="sxs-lookup"><span data-stu-id="be873-1309">Added bind mount support</span></span>
- <span data-ttu-id="be873-1310">suporte a descompartilhamento para namespace de montagem</span><span class="sxs-lookup"><span data-stu-id="be873-1310">unshare for mount namespace support</span></span>
    - <span data-ttu-id="be873-1311">Problema conhecido: Ao criar um novo namespace de montagem `unshare(CLONE_NEWNS)` com o diretório de trabalho atual, ele continuará a apontar para o namespace antigo</span><span class="sxs-lookup"><span data-stu-id="be873-1311">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="be873-1312">Melhorias e correções de bugs adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1312">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="be873-1313">Build 14905</span><span class="sxs-lookup"><span data-stu-id="be873-1313">Build 14905</span></span>

<span data-ttu-id="be873-1314">Para obter informações gerais do Windows sobre o Build 14905, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-1314">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1315">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1315">Fixed</span></span>
- <span data-ttu-id="be873-1316">Agora, as chamadas reiniciáveis do sistema são compatíveis (GH 349, GH 520)</span><span class="sxs-lookup"><span data-stu-id="be873-1316">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="be873-1317">Symlinks para diretórios que terminam em / agora estão operacionais (GH 650)</span><span class="sxs-lookup"><span data-stu-id="be873-1317">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="be873-1318">Ioctl RNDGETENTCNT implementado para /dev/random</span><span class="sxs-lookup"><span data-stu-id="be873-1318">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="be873-1319">Implementados os arquivos /proc/[pid]/mounts, /proc/[pid]/mountinfo e /proc/[pid]/mountstats</span><span class="sxs-lookup"><span data-stu-id="be873-1319">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="be873-1320">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1320">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="be873-1321">Build 14901</span><span class="sxs-lookup"><span data-stu-id="be873-1321">Build 14901</span></span>
<span data-ttu-id="be873-1322">Primeiro build de Participante do Programa Windows Insider para a versão de Atualização de Aniversário do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="be873-1322">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="be873-1323">Para obter informações gerais do Windows sobre o Build 14901, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1323">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1324">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1324">Fixed</span></span>
- <span data-ttu-id="be873-1325">Corrigido problema de barra à direita</span><span class="sxs-lookup"><span data-stu-id="be873-1325">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="be873-1326">Comandos como `$ mv a/c/ a/b/` agora funcionam</span><span class="sxs-lookup"><span data-stu-id="be873-1326">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="be873-1327">A instalação agora avisa se a localidade do Ubuntu deve ser definida como a localidade do Windows</span><span class="sxs-lookup"><span data-stu-id="be873-1327">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="be873-1328">Suporte do procfs para a pasta ns</span><span class="sxs-lookup"><span data-stu-id="be873-1328">Procfs support for ns folder</span></span>
- <span data-ttu-id="be873-1329">Adição de montagem e desmontagem para sistemas de arquivos tmpfs, procfs e sysfs</span><span class="sxs-lookup"><span data-stu-id="be873-1329">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="be873-1330">Corrigir a assinatura da ABI de 32 bits mknod[at]</span><span class="sxs-lookup"><span data-stu-id="be873-1330">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="be873-1331">Soquetes Unix movidos para o modelo de expedição</span><span class="sxs-lookup"><span data-stu-id="be873-1331">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="be873-1332">O tamanho do buffer de recebimento do soquete INET definido usando o setsockopt deve ser respeitado</span><span class="sxs-lookup"><span data-stu-id="be873-1332">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="be873-1333">Implementação do sinalizador de mensagem de recebimento do soquete do Unix MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="be873-1333">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="be873-1334">Redirecionamento de pipe stdin/stdout de processo do Linux (GH 2)</span><span class="sxs-lookup"><span data-stu-id="be873-1334">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="be873-1335">Permite o pipe de comandos bash -c no cmd.</span><span class="sxs-lookup"><span data-stu-id="be873-1335">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="be873-1336">Exemplo: >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="be873-1336">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="be873-1337">O Bash agora pode ser instalado em sistemas com diversos arquivos de paginação (GH 538, 358)</span><span class="sxs-lookup"><span data-stu-id="be873-1337">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="be873-1338">O tamanho do buffer do soquete INET padrão deve corresponder ao da configuração padrão do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="be873-1338">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="be873-1339">Alinhamento de syscalls xattr a listxattr</span><span class="sxs-lookup"><span data-stu-id="be873-1339">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="be873-1340">SIOCGIFCONF retorna apenas interfaces com um IPv4 válido</span><span class="sxs-lookup"><span data-stu-id="be873-1340">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="be873-1341">Correção da ação padrão de sinal quando injetado por ptrace</span><span class="sxs-lookup"><span data-stu-id="be873-1341">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="be873-1342">Implementação de /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="be873-1342">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="be873-1343">Uso de valores de registro de contexto de computador ao restaurar o contexto em sigreturn</span><span class="sxs-lookup"><span data-stu-id="be873-1343">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="be873-1344">Isso resolve o problema em que java e javac estavam travando para alguns usuários</span><span class="sxs-lookup"><span data-stu-id="be873-1344">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="be873-1345">Implementação de /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="be873-1345">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="be873-1346">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1346">Syscall Support</span></span>
<span data-ttu-id="be873-1347">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1347">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1348">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1348">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="be873-1349">Build 14388 para Atualização de Aniversário do Windows 10</span><span class="sxs-lookup"><span data-stu-id="be873-1349">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="be873-1350">Para obter informações gerais do Windows sobre o Build 14388, visite o [blog do Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="be873-1350">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="be873-1351">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1351">Fixed</span></span>
- <span data-ttu-id="be873-1352">Correções para preparar para a Atualização de Aniversário do Windows 10 em 02/08</span><span class="sxs-lookup"><span data-stu-id="be873-1352">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="be873-1353">Mais informações sobre WSL na atualização de aniversário podem ser encontradas em nosso [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="be873-1353">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="be873-1354">Build 14376</span><span class="sxs-lookup"><span data-stu-id="be873-1354">Build 14376</span></span>
<span data-ttu-id="be873-1355">Para obter informações gerais do Windows sobre o Build 14376, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="be873-1355">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="be873-1356">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1356">Fixed</span></span>
- <span data-ttu-id="be873-1357">Removidas algumas instâncias em que apt-get trava (GH 493)</span><span class="sxs-lookup"><span data-stu-id="be873-1357">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="be873-1358">Corrigido um problema em que as montagens vazias não eram manipuladas corretamente</span><span class="sxs-lookup"><span data-stu-id="be873-1358">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="be873-1359">Corrigido um problema em que ramdisks não eram montados corretamente</span><span class="sxs-lookup"><span data-stu-id="be873-1359">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="be873-1360">Alteração da aceitação de soquete do Unix para dar suporte a sinalizadores (GH 451 parcial)</span><span class="sxs-lookup"><span data-stu-id="be873-1360">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="be873-1361">Corrigida tela azul comum relacionada à rede</span><span class="sxs-lookup"><span data-stu-id="be873-1361">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="be873-1362">Corrigida tela azul ao acessar /proc/[pid]/task (GH 523)</span><span class="sxs-lookup"><span data-stu-id="be873-1362">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="be873-1363">Correção de alta utilização de CPU para alguns cenários de pty (GH 488, 504)</span><span class="sxs-lookup"><span data-stu-id="be873-1363">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="be873-1364">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1364">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="be873-1365">Build 14371</span><span class="sxs-lookup"><span data-stu-id="be873-1365">Build 14371</span></span>
<span data-ttu-id="be873-1366">Para obter informações gerais do Windows sobre o Build 14371, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="be873-1366">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="be873-1367">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1367">Fixed</span></span>
- <span data-ttu-id="be873-1368">Corrigida corrida de tempo com SIGCHLD e wait() ao usar ptrace</span><span class="sxs-lookup"><span data-stu-id="be873-1368">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="be873-1369">Corrigido algum comportamento quando os caminhos têm uma / à direita (GH 432)</span><span class="sxs-lookup"><span data-stu-id="be873-1369">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="be873-1370">Corrigido um problema de falha ao renomear/desvincular devido a identificadores abertos para filhos</span><span class="sxs-lookup"><span data-stu-id="be873-1370">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="be873-1371">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1371">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="be873-1372">Build 14366</span><span class="sxs-lookup"><span data-stu-id="be873-1372">Build 14366</span></span>
<span data-ttu-id="be873-1373">Para obter informações gerais do Windows sobre o Build 14366, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="be873-1373">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="be873-1374">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1374">Fixed</span></span>
- <span data-ttu-id="be873-1375">Correção na criação de arquivo por meio de symlinks</span><span class="sxs-lookup"><span data-stu-id="be873-1375">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="be873-1376">Adicionado listxattr para o Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="be873-1376">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="be873-1377">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1377">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="be873-1378">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1378">Syscall Support</span></span>
-   <span data-ttu-id="be873-1379">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1379">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1380">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1380">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="be873-1381">Build 14361</span><span class="sxs-lookup"><span data-stu-id="be873-1381">Build 14361</span></span>
<span data-ttu-id="be873-1382">Para obter informações gerais do Windows sobre o Build 14361, visite o [blog do Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="be873-1382">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="be873-1383">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1383">Fixed</span></span>
- <span data-ttu-id="be873-1384">O DrvFs agora diferencia maiúsculas de minúsculas ao executar no Bash usando Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-1384">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="be873-1385">Os usuários podem usar case.txt e CASE.TXT nas respectivas unidades /mnt/c</span><span class="sxs-lookup"><span data-stu-id="be873-1385">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="be873-1386">A diferenciação de maiúsculas e minúsculas só é compatível no Bash usando Ubuntu no Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-1386">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="be873-1387">Quando fora do Bash, o NTFS relatará os arquivos corretamente, mas um comportamento inesperado poderá ocorrer ao interagir com os arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-1387">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="be873-1388">A raiz de cada volume (ou seja, /mnt/c) não diferencia maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="be873-1388">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="be873-1389">É possível encontrar mais informações sobre como manipular esses arquivos no Windows [aqui](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="be873-1389">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="be873-1390">Suporte a pty/tty bastante aprimorado.</span><span class="sxs-lookup"><span data-stu-id="be873-1390">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="be873-1391">Aplicativos como TMUX agora são compatíveis (GH 40)</span><span class="sxs-lookup"><span data-stu-id="be873-1391">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="be873-1392">Corrigido um problema de instalação em que as contas de usuário nem sempre eram criadas</span><span class="sxs-lookup"><span data-stu-id="be873-1392">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="be873-1393">Estrutura de argumentos de linha de comando otimizada que permite uma lista de argumentos extremamente longa.</span><span class="sxs-lookup"><span data-stu-id="be873-1393">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="be873-1394">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="be873-1394">(GH #153)</span></span>
- <span data-ttu-id="be873-1395">Agora é possível excluir e usar chmod em arquivos read_only do DrvFs</span><span class="sxs-lookup"><span data-stu-id="be873-1395">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="be873-1396">Corrigidas algumas instâncias em que o terminal travava ao desconectar (GH 43)</span><span class="sxs-lookup"><span data-stu-id="be873-1396">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="be873-1397">chmod e chown agora funcionam em dispositivos tty</span><span class="sxs-lookup"><span data-stu-id="be873-1397">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="be873-1398">Permissão para conexão a 0.0.0.0 e a :: como localhost (GH 388)</span><span class="sxs-lookup"><span data-stu-id="be873-1398">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="be873-1399">Sendmsg/recvmsg agora aceitam um comprimento de vetor de E/S >1 (GH 376 parcial)</span><span class="sxs-lookup"><span data-stu-id="be873-1399">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="be873-1400">Os usuários agora podem recusar o arquivo de hosts gerado automaticamente (GH #398)</span><span class="sxs-lookup"><span data-stu-id="be873-1400">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="be873-1401">Correspondência automática da localidade do Linux à localidade do NT durante a instalação (GH 11)</span><span class="sxs-lookup"><span data-stu-id="be873-1401">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="be873-1402">Adicionado o arquivo /proc/sys/VM/swappiness (GH 306)</span><span class="sxs-lookup"><span data-stu-id="be873-1402">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="be873-1403">strace agora é encerrado corretamente</span><span class="sxs-lookup"><span data-stu-id="be873-1403">strace now exits correctly</span></span>
- <span data-ttu-id="be873-1404">Permissão para que os pipes sejam reabertos por meio de /proc/Self/FD (GH 222)</span><span class="sxs-lookup"><span data-stu-id="be873-1404">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="be873-1405">Ocultação de diretórios em %LOCALAPPDATA%\lxss do DrvFs (GH 270)</span><span class="sxs-lookup"><span data-stu-id="be873-1405">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="be873-1406">Melhor manipulação do bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="be873-1406">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="be873-1407">Comandos como "bash ~ -c ls" agora são compatíveis (GH 467)</span><span class="sxs-lookup"><span data-stu-id="be873-1407">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="be873-1408">Os soquetes agora notificam que a leitura de epoll está disponível durante o desligamento (GH 271)</span><span class="sxs-lookup"><span data-stu-id="be873-1408">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="be873-1409">lxrun /uninstall desempenha melhor a exclusão de arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="be873-1409">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="be873-1410">ps-f corrigido (GH 246)</span><span class="sxs-lookup"><span data-stu-id="be873-1410">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="be873-1411">Suporte aprimorado para aplicativos x11, tais como xEmacs (GH 481)</span><span class="sxs-lookup"><span data-stu-id="be873-1411">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="be873-1412">Tamanho da pilha de thread inicial atualizado para corresponder à configuração padrão do Ubuntu e relatando o tamanho corretamente para a syscall get_rlimit (GH 172, 258)</span><span class="sxs-lookup"><span data-stu-id="be873-1412">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="be873-1413">Relatório aprimorado de nomes de imagem de processo do pico (por exemplo, para auditoria)</span><span class="sxs-lookup"><span data-stu-id="be873-1413">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="be873-1414">Implementado o /proc/mountinfo para o comando df</span><span class="sxs-lookup"><span data-stu-id="be873-1414">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="be873-1415">Corrigido o código de erro de symlink para o nome do filho.</span><span class="sxs-lookup"><span data-stu-id="be873-1415">Fixed symlink error code for child name .</span></span> <span data-ttu-id="be873-1416">e ..</span><span class="sxs-lookup"><span data-stu-id="be873-1416">and ..</span></span>
- <span data-ttu-id="be873-1417">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1417">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="be873-1418">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1418">Syscall Support</span></span>
<span data-ttu-id="be873-1419">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1419">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1420">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1420">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="be873-1421">Build 14352</span><span class="sxs-lookup"><span data-stu-id="be873-1421">Build 14352</span></span>
<span data-ttu-id="be873-1422">Para obter informações gerais do Windows sobre o Build 14352, visite o [blog do Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="be873-1422">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="be873-1423">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1423">Fixed</span></span>
- <span data-ttu-id="be873-1424">Corrigido um problema em que arquivos grandes não eram baixados/criados corretamente.</span><span class="sxs-lookup"><span data-stu-id="be873-1424">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="be873-1425">Isso deve desbloquear o npm e outros cenários (GH 3, GH 313)</span><span class="sxs-lookup"><span data-stu-id="be873-1425">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="be873-1426">Removidas algumas instâncias em que soquetes travavam</span><span class="sxs-lookup"><span data-stu-id="be873-1426">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="be873-1427">Corrigidos alguns erros de ptrace</span><span class="sxs-lookup"><span data-stu-id="be873-1427">Corrected some ptrace errors</span></span>
- <span data-ttu-id="be873-1428">Corrigido um problema com o WSL permitindo nomes de arquivo maiores do que 255 caracteres</span><span class="sxs-lookup"><span data-stu-id="be873-1428">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="be873-1429">Suporte aprimorado para caracteres diferentes do inglês</span><span class="sxs-lookup"><span data-stu-id="be873-1429">Improved support for non-English characters</span></span>
- <span data-ttu-id="be873-1430">Adicionar os dados de fuso horário atual do Windows e definir como padrão</span><span class="sxs-lookup"><span data-stu-id="be873-1430">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="be873-1431">IDs de dispositivo exclusivas para cada ponto de montagem (correção de jre – GH 49)</span><span class="sxs-lookup"><span data-stu-id="be873-1431">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="be873-1432">Corrigido problema com caminhos contendo "."</span><span class="sxs-lookup"><span data-stu-id="be873-1432">Correct issue with paths containing “.”</span></span> <span data-ttu-id="be873-1433">e ".."</span><span class="sxs-lookup"><span data-stu-id="be873-1433">and “..”</span></span>
- <span data-ttu-id="be873-1434">Adicionado suporte a PEPS (GH 71)</span><span class="sxs-lookup"><span data-stu-id="be873-1434">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="be873-1435">Atualizado formato de resolv.conf para corresponder ao formato nativo do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="be873-1435">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="be873-1436">Limpeza de alguns procfs</span><span class="sxs-lookup"><span data-stu-id="be873-1436">Some procfs cleanup</span></span>
- <span data-ttu-id="be873-1437">Ping habilitado para consoles do administrador (GH 18)</span><span class="sxs-lookup"><span data-stu-id="be873-1437">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="be873-1438">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1438">Syscall Support</span></span>
<span data-ttu-id="be873-1439">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1439">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1440">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1440">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="be873-1441">Build 14342</span><span class="sxs-lookup"><span data-stu-id="be873-1441">Build 14342</span></span>
<span data-ttu-id="be873-1442">Para obter informações gerais do Windows sobre o Build 14342, visite o [blog do Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="be873-1442">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="be873-1443">Informações sobre VolFs e DriveFs podem ser encontradas no [blog do WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="be873-1443">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="be873-1444">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1444">Fixed</span></span>
- <span data-ttu-id="be873-1445">Corrigido problema de instalação quando o usuário do Windows tinha caracteres Unicode no nome de usuário</span><span class="sxs-lookup"><span data-stu-id="be873-1445">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="be873-1446">A solução alternativa apt-get update udev nas perguntas frequentes agora é fornecida por padrão na primeira execução</span><span class="sxs-lookup"><span data-stu-id="be873-1446">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="be873-1447">Symlinks habilitados nos diretórios de DriveFs (/mnt/<drive>)</span><span class="sxs-lookup"><span data-stu-id="be873-1447">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="be873-1448">Symlinks agora funcionam entre DriveFs e VolFs</span><span class="sxs-lookup"><span data-stu-id="be873-1448">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="be873-1449">Problema de análise de caminho de nível superior resolvido: ls .// agora funcionará como esperado</span><span class="sxs-lookup"><span data-stu-id="be873-1449">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="be873-1450">A instalação de npm no DriveFs e as opções -g agora estão funcionando</span><span class="sxs-lookup"><span data-stu-id="be873-1450">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="be873-1451">Problema corrigido, impedindo a inicialização do servidor PHP</span><span class="sxs-lookup"><span data-stu-id="be873-1451">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="be873-1452">Valores de ambiente padrão atualizados, tais como $PATH para corresponder melhor ao Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="be873-1452">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="be873-1453">Adicionada uma tarefa de manutenção semanal no Windows para atualizar o cache do pacote apt</span><span class="sxs-lookup"><span data-stu-id="be873-1453">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="be873-1454">Corrigido um problema com a validação de cabeçalho ELF, o WSL agora dá suporte a todas as opções de Melkor</span><span class="sxs-lookup"><span data-stu-id="be873-1454">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="be873-1455">O shell do zsh está funcional</span><span class="sxs-lookup"><span data-stu-id="be873-1455">Zsh shell is functional</span></span>
- <span data-ttu-id="be873-1456">Binários do Go pré-compilados agora são compatíveis</span><span class="sxs-lookup"><span data-stu-id="be873-1456">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="be873-1457">O aviso na primeira execução do bash.exe agora está localizado corretamente</span><span class="sxs-lookup"><span data-stu-id="be873-1457">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="be873-1458">/proc/meminfo agora retorna informações corretas</span><span class="sxs-lookup"><span data-stu-id="be873-1458">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="be873-1459">Os soquetes agora são compatíveis com o VFS</span><span class="sxs-lookup"><span data-stu-id="be873-1459">Sockets now supported in VFS</span></span>
- <span data-ttu-id="be873-1460">/dev agora é montado como tempfs</span><span class="sxs-lookup"><span data-stu-id="be873-1460">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="be873-1461">PEPS agora é compatível</span><span class="sxs-lookup"><span data-stu-id="be873-1461">Fifo now supported</span></span>
- <span data-ttu-id="be873-1462">Sistemas de vários núcleos agora são mostrados corretamente em /proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="be873-1462">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="be873-1463">Aprimoramentos adicionais e mensagens de erro ao baixar durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="be873-1463">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="be873-1464">Melhorias e correções de bug em syscall.</span><span class="sxs-lookup"><span data-stu-id="be873-1464">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="be873-1465">Lista de syscalls compatíveis abaixo.</span><span class="sxs-lookup"><span data-stu-id="be873-1465">Supported syscall list below.</span></span>
- <span data-ttu-id="be873-1466">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1466">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="be873-1467">Problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="be873-1467">Known Issues</span></span>
- <span data-ttu-id="be873-1468">Não resolvendo '..'</span><span class="sxs-lookup"><span data-stu-id="be873-1468">Not resolving ‘..’</span></span> <span data-ttu-id="be873-1469">corretamente no DriveFs em alguns casos</span><span class="sxs-lookup"><span data-stu-id="be873-1469">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="be873-1470">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1470">Syscall Support</span></span>
<span data-ttu-id="be873-1471">Veja abaixo uma lista de syscalls novas ou aprimoradas que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1471">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="be873-1472">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1472">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="be873-1473">Build 14332</span><span class="sxs-lookup"><span data-stu-id="be873-1473">Build 14332</span></span>

<span data-ttu-id="be873-1474">Para obter informações gerais do Windows sobre o Build 14332, visite o [blog do Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="be873-1474">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="be873-1475">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1475">Fixed</span></span>
- <span data-ttu-id="be873-1476">Melhor geração de resolv.conf, incluindo a priorização de entradas DNS</span><span class="sxs-lookup"><span data-stu-id="be873-1476">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="be873-1477">Problema com a movimentação de arquivos e diretórios entre unidades/mnt e não /mnt</span><span class="sxs-lookup"><span data-stu-id="be873-1477">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="be873-1478">Agora, os arquivos tar podem ser criados com symlinks</span><span class="sxs-lookup"><span data-stu-id="be873-1478">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="be873-1479">Diretório /run/lock padrão adicionado na criação da instância</span><span class="sxs-lookup"><span data-stu-id="be873-1479">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="be873-1480">Atualização de /dev/null para retornar informações de estado adequadas</span><span class="sxs-lookup"><span data-stu-id="be873-1480">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="be873-1481">Erros adicionais ao baixar durante a primeira execução</span><span class="sxs-lookup"><span data-stu-id="be873-1481">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="be873-1482">Melhorias e correções de bug em syscall.</span><span class="sxs-lookup"><span data-stu-id="be873-1482">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="be873-1483">Lista de syscalls compatíveis abaixo.</span><span class="sxs-lookup"><span data-stu-id="be873-1483">Supported syscall list below.</span></span>
- <span data-ttu-id="be873-1484">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1484">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="be873-1485">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1485">Syscall Support</span></span>
<span data-ttu-id="be873-1486">Abaixo está a nova syscall que tem alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1486">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="be873-1487">A syscall nessa lista é compatível com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com ela no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1487">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="be873-1488">Build 14328</span><span class="sxs-lookup"><span data-stu-id="be873-1488">Build 14328</span></span>

<span data-ttu-id="be873-1489">Para obter informações gerais do Windows sobre o Build 14332, visite o [blog do Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="be873-1489">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="be873-1490">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="be873-1490">New Features</span></span>
* <span data-ttu-id="be873-1491">Agora dão suporte a usuários do Linux.</span><span class="sxs-lookup"><span data-stu-id="be873-1491">Now support Linux users.</span></span>  <span data-ttu-id="be873-1492">A instalação do Bash usando o Ubuntu no Windows solicitará a criação de um usuário do Linux.</span><span class="sxs-lookup"><span data-stu-id="be873-1492">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="be873-1493">Para obter mais informações, visite https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="be873-1493">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="be873-1494">O hostname agora está definido como o nome do computador Windows, não mais como @localhost</span><span class="sxs-lookup"><span data-stu-id="be873-1494">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="be873-1495">Para obter mais informações sobre o build 14328, visite: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="be873-1495">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="be873-1496">Fixo</span><span class="sxs-lookup"><span data-stu-id="be873-1496">Fixed</span></span>
* <span data-ttu-id="be873-1497">Aprimoramentos do symlink para arquivos não /mnt/<drive></span><span class="sxs-lookup"><span data-stu-id="be873-1497">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="be873-1498">A instalação de npm agora funciona</span><span class="sxs-lookup"><span data-stu-id="be873-1498">npm install now works</span></span>
    * <span data-ttu-id="be873-1499">Agora, o jdk/jre é instalável usando as instruções encontradas [aqui](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="be873-1499">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="be873-1500">problema conhecido: os symlinks não funcionam para montagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="be873-1500">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="be873-1501">A funcionalidade estará disponível em um build posterior</span><span class="sxs-lookup"><span data-stu-id="be873-1501">Functionality will be available in a later build</span></span>
* <span data-ttu-id="be873-1502">top e htop agora são exibidos</span><span class="sxs-lookup"><span data-stu-id="be873-1502">top and htop now display</span></span>
* <span data-ttu-id="be873-1503">Mensagens de erro adicionais para algumas falhas de instalação</span><span class="sxs-lookup"><span data-stu-id="be873-1503">Additional error messages for some install failures</span></span>
* <span data-ttu-id="be873-1504">Melhorias e correções de bug em syscall.</span><span class="sxs-lookup"><span data-stu-id="be873-1504">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="be873-1505">Lista de syscalls compatíveis abaixo.</span><span class="sxs-lookup"><span data-stu-id="be873-1505">Supported syscall list below.</span></span>
* <span data-ttu-id="be873-1506">Correções de bug e melhorias adicionais</span><span class="sxs-lookup"><span data-stu-id="be873-1506">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="be873-1507">Suporte a syscall</span><span class="sxs-lookup"><span data-stu-id="be873-1507">Syscall Support</span></span>
<span data-ttu-id="be873-1508">Veja abaixo uma lista de syscalls que têm alguma implementação no WSL.</span><span class="sxs-lookup"><span data-stu-id="be873-1508">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="be873-1509">As syscalls nessa lista são compatíveis com pelo menos um cenário, mas talvez nem todos os parâmetros sejam compatíveis com elas no momento.</span><span class="sxs-lookup"><span data-stu-id="be873-1509">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
