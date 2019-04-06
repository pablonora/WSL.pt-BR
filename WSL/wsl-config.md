---
title: Gerenciar as distribuições do Linux
description: Fazer referência a listagem e configuração de várias distribuições do Linux em execução no subsistema do Windows para Linux.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063494"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="1448c-104">Gerenciar e configurar o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="1448c-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="1448c-105">Aplica-se ao Windows 10 Fall Creators Update e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="1448c-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="1448c-106">Consulte nossa atualizada [guia de instalação](./install_guide.md) Experimente os novos recursos de gerenciamento e inicie a execução de várias distribuições do Linux da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1448c-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Windows Store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="1448c-107">Maneiras de executar o WSL</span><span class="sxs-lookup"><span data-stu-id="1448c-107">Ways to run WSL</span></span>

<span data-ttu-id="1448c-108">Há muitas maneiras de executar o Linux com o subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="1448c-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. `[distro]` <span data-ttu-id="1448c-109">ie</span><span class="sxs-lookup"><span data-stu-id="1448c-109">ie</span></span> `ubuntu`
1. `wsl.exe` <span data-ttu-id="1448c-110">ou</span><span class="sxs-lookup"><span data-stu-id="1448c-110">or</span></span> `bash.exe`
1. `wsl [command]` <span data-ttu-id="1448c-111">ou</span><span class="sxs-lookup"><span data-stu-id="1448c-111">or</span></span> `bash -c [command]`

<span data-ttu-id="1448c-112">Qual método você deve usar depende do que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="1448c-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="1448c-113">Inicie o WSL por distribuição</span><span class="sxs-lookup"><span data-stu-id="1448c-113">Launch WSL by distribution</span></span>

<span data-ttu-id="1448c-114">Executando uma distribuição usando o aplicativo do específica de distribuição dessa distribuição na sua própria janela de console é iniciado.</span><span class="sxs-lookup"><span data-stu-id="1448c-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Inicie o WSL do menu Iniciar](media/start-launch.png)

<span data-ttu-id="1448c-116">É o mesmo que clicar em "Iniciar" na Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1448c-116">It is the same as clicking "Launch" in the Windows Store.</span></span>

![Inicie o WSL da Windows Store](media/store-launch.png)

<span data-ttu-id="1448c-118">Você também pode executar a distribuição da linha de comando executando `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="1448c-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="1448c-119">A desvantagem de usar uma distribuição da linha de comando dessa maneira é que ele será alterado automaticamente seu diretório de trabalho do diretório atual para o diretório de base da distribuição.</span><span class="sxs-lookup"><span data-stu-id="1448c-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

**<span data-ttu-id="1448c-120">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1448c-120">Example:</span></span>**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="1448c-121">wsl e wsl [comando]</span><span class="sxs-lookup"><span data-stu-id="1448c-121">wsl and wsl [command]</span></span>

<span data-ttu-id="1448c-122">A melhor maneira de executar o WSL da linha de comando está usando `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="1448c-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

**<span data-ttu-id="1448c-123">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1448c-123">Example:</span></span>**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="1448c-124">Não apenas `wsl` manter o diretório de trabalho atual no lugar, ele permite que você execute um único comando ao longo de comandos do Windows de lado.</span><span class="sxs-lookup"><span data-stu-id="1448c-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

**<span data-ttu-id="1448c-125">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1448c-125">Example:</span></span>**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

**<span data-ttu-id="1448c-126">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1448c-126">Example:</span></span>**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="1448c-127">Gerenciando várias distribuições do Linux</span><span class="sxs-lookup"><span data-stu-id="1448c-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="1448c-128">Windows 10, versão 1903 e posterior</span><span class="sxs-lookup"><span data-stu-id="1448c-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="1448c-129">Você pode usar `wsl.exe` para gerenciar suas distribuições no subsistema Windows para Linux (WSL), incluindo listagem distribuições disponíveis, definindo uma distribuição padrão e distribuições de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="1448c-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="1448c-130">Independentemente, cada distribuição Linux gerencia suas próprias configurações.</span><span class="sxs-lookup"><span data-stu-id="1448c-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="1448c-131">Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="1448c-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="1448c-132">Por exemplo `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="1448c-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="1448c-133">Lista de distribuições</span><span class="sxs-lookup"><span data-stu-id="1448c-133">List distributions</span></span>

`wsl -l` <span data-ttu-id="1448c-134">,</span><span class="sxs-lookup"><span data-stu-id="1448c-134">,</span></span> `wsl --list`  
<span data-ttu-id="1448c-135">Lista de distribuições do Linux disponíveis disponíveis para WSL.</span><span class="sxs-lookup"><span data-stu-id="1448c-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="1448c-136">Se uma distribuição estiver listada, ele é instalado e pronto para ser usado.</span><span class="sxs-lookup"><span data-stu-id="1448c-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="1448c-137">Lista todas as distribuições, incluindo aqueles que não podem ser usados no momento.</span><span class="sxs-lookup"><span data-stu-id="1448c-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="1448c-138">Eles podem estar no processo de instalação, desinstalação, ou estiverem em um estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="1448c-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="1448c-139">Lista todas as distribuições que estão sendo executados.</span><span class="sxs-lookup"><span data-stu-id="1448c-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="1448c-140">Defina uma distribuição padrão</span><span class="sxs-lookup"><span data-stu-id="1448c-140">Set a default distribution</span></span>

<span data-ttu-id="1448c-141">A distribuição de WSL padrão é o que é executado quando você executar `wsl` em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1448c-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wsl -s <DistributionName>`<span data-ttu-id="1448c-142">,</span><span class="sxs-lookup"><span data-stu-id="1448c-142">,</span></span> `wsl --setdefault <DistributionName>`

<span data-ttu-id="1448c-143">Define a distribuição padrão para `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="1448c-143">Sets the default distribution to `<DistributionName>`.</span></span>

**<span data-ttu-id="1448c-144">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1448c-144">Example:</span></span>**  
`wsl -s Ubuntu` <span data-ttu-id="1448c-145">definiria meu distribuição padrão para o Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="1448c-145">would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="1448c-146">Agora quando executo `wsl npm init` ele será executado no Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="1448c-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="1448c-147">Se eu executar `wsl` ela será aberta uma sessão do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="1448c-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="1448c-148">Cancelar o registro e reinstalar uma distribuição</span><span class="sxs-lookup"><span data-stu-id="1448c-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="1448c-149">Ao Linux distribuições podem ser instaladas por meio do Windows, armazenamento, eles não podem ser desinstalados por meio da loja.</span><span class="sxs-lookup"><span data-stu-id="1448c-149">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="1448c-150">WSL Config permite distribuições ser desinstalado/desregistrado.</span><span class="sxs-lookup"><span data-stu-id="1448c-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="1448c-151">O cancelamento do registro também permite que distribuições ser reinstalado.</span><span class="sxs-lookup"><span data-stu-id="1448c-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="1448c-152">**Cuidado:** Depois que o registro cancelado, todos os dados, configurações e software associado a essa distribuição serão permanentemente perdidas.</span><span class="sxs-lookup"><span data-stu-id="1448c-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="1448c-153">Reinstalar da loja instalará uma cópia limpa da distribuição.</span><span class="sxs-lookup"><span data-stu-id="1448c-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="1448c-154">Cancela o registro a distribuição do WSL para que possa ser reinstalado ou limpos.</span><span class="sxs-lookup"><span data-stu-id="1448c-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="1448c-155">Por exemplo: `wsl -unregister Ubuntu` removeria Ubuntu das distribuições disponíveis no WSL.</span><span class="sxs-lookup"><span data-stu-id="1448c-155">For example: `wsl -unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="1448c-156">Quando executo `wsl --list` não serão listado.</span><span class="sxs-lookup"><span data-stu-id="1448c-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="1448c-157">Para reinstalar, localize a distribuição em que a Windows Store e selecione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="1448c-157">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="1448c-158">Executar como um usuário específico</span><span class="sxs-lookup"><span data-stu-id="1448c-158">Run as a specific user</span></span>

`wsl -u <Username>`<span data-ttu-id="1448c-159">,</span><span class="sxs-lookup"><span data-stu-id="1448c-159">,</span></span> `wsl --user <Username>`

<span data-ttu-id="1448c-160">Execute o WSL como o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="1448c-160">Run WSL as the specified user.</span></span> <span data-ttu-id="1448c-161">Observe que o usuário deve existir dentro distribuição WSL.</span><span class="sxs-lookup"><span data-stu-id="1448c-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="1448c-162">Executar uma distribuição específica</span><span class="sxs-lookup"><span data-stu-id="1448c-162">Run a specific distribution</span></span>

`wsl --d <DistributionName>`<span data-ttu-id="1448c-163">,</span><span class="sxs-lookup"><span data-stu-id="1448c-163">,</span></span> `wsl --distribution <DistributionName>`

<span data-ttu-id="1448c-164">Executar uma distribuição especificada de WSL, pode ser usado para enviar comandos para uma distribuição específica sem precisar alterar o padrão.</span><span class="sxs-lookup"><span data-stu-id="1448c-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="1448c-165">Versões anteriores ao Windows 10, versão 1903</span><span class="sxs-lookup"><span data-stu-id="1448c-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="1448c-166">Configuração de WSL (`wslconfig.exe`) é uma ferramenta de linha de comando para gerenciar as distribuições do Linux em execução no subsistema do Windows para Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="1448c-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="1448c-167">Ele permite listar distribuições disponíveis, defina uma distribuição padrão e desinstalar as distribuições.</span><span class="sxs-lookup"><span data-stu-id="1448c-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="1448c-168">Enquanto o WSL configuração é útil para as configurações que abrangem ou coordenam as distribuições, cada distribuição Linux independentemente gerencia suas próprias configurações.</span><span class="sxs-lookup"><span data-stu-id="1448c-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="1448c-169">Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="1448c-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="1448c-170">Por exemplo `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="1448c-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="1448c-171">Para ver todas as opções disponíveis para wslconfig, execute:</span><span class="sxs-lookup"><span data-stu-id="1448c-171">To see all available options for wslconfig, run:</span></span>  `wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a><span data-ttu-id="1448c-172">Lista de distribuições</span><span class="sxs-lookup"><span data-stu-id="1448c-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="1448c-173">Lista de distribuições do Linux disponíveis disponíveis para WSL.</span><span class="sxs-lookup"><span data-stu-id="1448c-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="1448c-174">Se uma distribuição estiver listada, ele é instalado e pronto para ser usado.</span><span class="sxs-lookup"><span data-stu-id="1448c-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="1448c-175">Lista todas as distribuições, incluindo aqueles que não podem ser usados no momento.</span><span class="sxs-lookup"><span data-stu-id="1448c-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="1448c-176">Eles podem estar no processo de instalação, desinstalação, ou estiverem em um estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="1448c-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="1448c-177">Defina uma distribuição padrão</span><span class="sxs-lookup"><span data-stu-id="1448c-177">Set a default distribution</span></span>

<span data-ttu-id="1448c-178">A distribuição de WSL padrão é o que é executado quando você executar `wsl` em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="1448c-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="1448c-179">Define a distribuição padrão para `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="1448c-179">Sets the default distribution to `<DistributionName>`.</span></span>

**<span data-ttu-id="1448c-180">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="1448c-180">Example:</span></span>**  
`wslconfig /setdefault Ubuntu` <span data-ttu-id="1448c-181">definiria meu distribuição padrão para o Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="1448c-181">would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="1448c-182">Agora quando executo `wsl npm init` ele será executado no Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="1448c-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="1448c-183">Se eu executar `wsl` ela será aberta uma sessão do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="1448c-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="1448c-184">Cancelar o registro e reinstalar uma distribuição</span><span class="sxs-lookup"><span data-stu-id="1448c-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="1448c-185">Ao Linux distribuições podem ser instaladas por meio do Windows, armazenamento, eles não podem ser desinstalados por meio da loja.</span><span class="sxs-lookup"><span data-stu-id="1448c-185">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="1448c-186">WSL Config permite distribuições ser desinstalado/desregistrado.</span><span class="sxs-lookup"><span data-stu-id="1448c-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="1448c-187">O cancelamento do registro também permite que distribuições ser reinstalado.</span><span class="sxs-lookup"><span data-stu-id="1448c-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="1448c-188">**Cuidado:** Depois que o registro cancelado, todos os dados, configurações e software associado a essa distribuição serão permanentemente perdidas.</span><span class="sxs-lookup"><span data-stu-id="1448c-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="1448c-189">Reinstalar da loja instalará uma cópia limpa da distribuição.</span><span class="sxs-lookup"><span data-stu-id="1448c-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="1448c-190">Cancela o registro a distribuição do WSL para que possa ser reinstalado ou limpos.</span><span class="sxs-lookup"><span data-stu-id="1448c-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="1448c-191">Por exemplo: `wslconfig /unregister Ubuntu` removeria Ubuntu das distribuições disponíveis no WSL.</span><span class="sxs-lookup"><span data-stu-id="1448c-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="1448c-192">Quando executo `wslconfig /list` não serão listado.</span><span class="sxs-lookup"><span data-stu-id="1448c-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="1448c-193">Para reinstalar, localize a distribuição em que a Windows Store e selecione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="1448c-193">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="1448c-194">Definir configurações de inicialização WSL</span><span class="sxs-lookup"><span data-stu-id="1448c-194">Set WSL launch settings</span></span>

> **<span data-ttu-id="1448c-195">Disponível no Windows Insider Build 17093 e posterior</span><span class="sxs-lookup"><span data-stu-id="1448c-195">Available in Windows Insider Build 17093 and later</span></span>**

<span data-ttu-id="1448c-196">Configure automaticamente algumas funcionalidades em WSL que será aplicada sempre que iniciar o subsistema usando `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="1448c-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="1448c-197">Direita agora, isso inclui opções de montagem automática e configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="1448c-197">Right now, this includes automount options and network configuration.</span></span>

`wsl.conf` <span data-ttu-id="1448c-198">está localizado em cada distribuição do Linux em `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="1448c-198">is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="1448c-199">Se o arquivo não estiver lá, você pode criá-lo.</span><span class="sxs-lookup"><span data-stu-id="1448c-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="1448c-200">WSL detectará a existência do arquivo e irá ler seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1448c-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="1448c-201">Se o arquivo está ausente ou malformado (ou seja, inadequada marcação formatação), WSL continuará iniciar como normal.</span><span class="sxs-lookup"><span data-stu-id="1448c-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="1448c-202">Aqui está um exemplo `wsl.conf` arquivo você pode adicionar em suas distribuições:</span><span class="sxs-lookup"><span data-stu-id="1448c-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="1448c-203">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="1448c-203">Configuration Options</span></span>

<span data-ttu-id="1448c-204">Para manter as convenções. ini, as chaves são declaradas em uma seção.</span><span class="sxs-lookup"><span data-stu-id="1448c-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="1448c-205">WSL dá suporte a duas seções: `automount` e `network`.</span><span class="sxs-lookup"><span data-stu-id="1448c-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="1448c-206">Montagem automática</span><span class="sxs-lookup"><span data-stu-id="1448c-206">automount</span></span>

<span data-ttu-id="1448c-207">Seção:</span><span class="sxs-lookup"><span data-stu-id="1448c-207">Section:</span></span> `[automount]`


| <span data-ttu-id="1448c-208">key</span><span class="sxs-lookup"><span data-stu-id="1448c-208">key</span></span>        | <span data-ttu-id="1448c-209">value</span><span class="sxs-lookup"><span data-stu-id="1448c-209">value</span></span>                          | <span data-ttu-id="1448c-210">padrão</span><span class="sxs-lookup"><span data-stu-id="1448c-210">default</span></span>      | <span data-ttu-id="1448c-211">Notas</span><span class="sxs-lookup"><span data-stu-id="1448c-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1448c-212">habilitado</span><span class="sxs-lookup"><span data-stu-id="1448c-212">enabled</span></span>    | <span data-ttu-id="1448c-213">booliano</span><span class="sxs-lookup"><span data-stu-id="1448c-213">boolean</span></span>                        | <span data-ttu-id="1448c-214">verdadeiro</span><span class="sxs-lookup"><span data-stu-id="1448c-214">true</span></span>         | `true` <span data-ttu-id="1448c-215">causas (isto é, de unidades fixas</span><span class="sxs-lookup"><span data-stu-id="1448c-215">causes fixed drives (i.e</span></span> `C:/` <span data-ttu-id="1448c-216">ou `D:/`) deve ser montado automaticamente com DrvFs em `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="1448c-216">or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  `false` <span data-ttu-id="1448c-217">significa que unidades não ser montadas automaticamente, mas você ainda pode montá-los manualmente ou por meio de `fstab`.</span><span class="sxs-lookup"><span data-stu-id="1448c-217">means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="1448c-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="1448c-218">mountFsTab</span></span> | <span data-ttu-id="1448c-219">booliano</span><span class="sxs-lookup"><span data-stu-id="1448c-219">boolean</span></span>                        | <span data-ttu-id="1448c-220">verdadeiro</span><span class="sxs-lookup"><span data-stu-id="1448c-220">true</span></span>         | `true` <span data-ttu-id="1448c-221">define `/etc/fstab` a ser processada no início WSL.</span><span class="sxs-lookup"><span data-stu-id="1448c-221">sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="1448c-222">/etc/fstab é um arquivo em que você pode declarar outros sistemas de arquivos, como um compartilhamento SMB.</span><span class="sxs-lookup"><span data-stu-id="1448c-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="1448c-223">Assim, você pode montar esses sistemas de arquivos automaticamente em WSL no início do backup.</span><span class="sxs-lookup"><span data-stu-id="1448c-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="1448c-224">Raiz</span><span class="sxs-lookup"><span data-stu-id="1448c-224">root</span></span>       | <span data-ttu-id="1448c-225">String</span><span class="sxs-lookup"><span data-stu-id="1448c-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="1448c-226">Define o diretório em que unidades fixas serão montadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1448c-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="1448c-227">Por exemplo, se você tiver um diretório no WSL em `/windir/` e você especificar que como a raiz, você esperaria ver suas unidades fixas montadas em</span><span class="sxs-lookup"><span data-stu-id="1448c-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at</span></span> `/windir/c`                                                                                              |
| <span data-ttu-id="1448c-228">opções</span><span class="sxs-lookup"><span data-stu-id="1448c-228">options</span></span>    | <span data-ttu-id="1448c-229">lista separada por vírgulas de valores</span><span class="sxs-lookup"><span data-stu-id="1448c-229">comma-separated list of values</span></span> | <span data-ttu-id="1448c-230">Cadeia de caracteres vazia</span><span class="sxs-lookup"><span data-stu-id="1448c-230">empty string</span></span> | <span data-ttu-id="1448c-231">Esse valor é acrescentado à cadeia de opções de montagem padrão DrvFs.</span><span class="sxs-lookup"><span data-stu-id="1448c-231">This value is appended to the default DrvFs mount options string.</span></span> **<span data-ttu-id="1448c-232">Somente as opções de DrvFs específicas podem ser especificadas.</span><span class="sxs-lookup"><span data-stu-id="1448c-232">Only DrvFs-specific options can be specified.</span></span>** <span data-ttu-id="1448c-233">Não há suporte para as opções que a montagem binária normalmente analisaria em um sinalizador.</span><span class="sxs-lookup"><span data-stu-id="1448c-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="1448c-234">Se você quiser especificar explicitamente essas opções, você deve incluir cada unidade para o qual você deseja fazer isso em /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="1448c-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="1448c-235">Por padrão, o WSL define o uid e gid como o valor do usuário padrão (distribuição do Ubuntu, o usuário padrão é criado com o uid = 1000, gid = 1000).</span><span class="sxs-lookup"><span data-stu-id="1448c-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="1448c-236">Se o usuário especificar uma opção gid ou uid explicitamente por meio dessa chave, o valor associado será substituído.</span><span class="sxs-lookup"><span data-stu-id="1448c-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="1448c-237">Caso contrário, o valor padrão sempre será acrescentado.</span><span class="sxs-lookup"><span data-stu-id="1448c-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="1448c-238">**Observação:** Essas opções são aplicadas como as opções de montagem para todas as unidades montadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1448c-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="1448c-239">Para alterar as opções para apenas uma unidade específica, use o /etc/fstab em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1448c-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="1448c-240">rede</span><span class="sxs-lookup"><span data-stu-id="1448c-240">network</span></span>

<span data-ttu-id="1448c-241">Rótulo de seção:</span><span class="sxs-lookup"><span data-stu-id="1448c-241">Section label:</span></span> `[network]`

| <span data-ttu-id="1448c-242">key</span><span class="sxs-lookup"><span data-stu-id="1448c-242">key</span></span> | <span data-ttu-id="1448c-243">value</span><span class="sxs-lookup"><span data-stu-id="1448c-243">value</span></span> | <span data-ttu-id="1448c-244">padrão</span><span class="sxs-lookup"><span data-stu-id="1448c-244">default</span></span> | <span data-ttu-id="1448c-245">Notas</span><span class="sxs-lookup"><span data-stu-id="1448c-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="1448c-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="1448c-246">generateHosts</span></span> | <span data-ttu-id="1448c-247">booliano</span><span class="sxs-lookup"><span data-stu-id="1448c-247">boolean</span></span> | `true` | `true` <span data-ttu-id="1448c-248">Define o WSL para gerar `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="1448c-248">sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="1448c-249">O `hosts` arquivo contém um mapa estático do endereço IP correspondente de nomes de host.</span><span class="sxs-lookup"><span data-stu-id="1448c-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="1448c-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="1448c-250">generateResolvConf</span></span> | <span data-ttu-id="1448c-251">booliano</span><span class="sxs-lookup"><span data-stu-id="1448c-251">boolean</span></span> | `true` | `true` <span data-ttu-id="1448c-252">Definir WSL para gerar `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="1448c-252">set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="1448c-253">O `resolv.conf` contém uma lista DNS que são capazes de resolver um determinado nome de host para seu endereço IP.</span><span class="sxs-lookup"><span data-stu-id="1448c-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="1448c-254">Interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="1448c-254">interop</span></span>

<span data-ttu-id="1448c-255">Rótulo de seção:</span><span class="sxs-lookup"><span data-stu-id="1448c-255">Section label:</span></span> `[interop]`

<span data-ttu-id="1448c-256">Essas opções estão disponíveis no Insider Build 17713 e posterior.</span><span class="sxs-lookup"><span data-stu-id="1448c-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="1448c-257">key</span><span class="sxs-lookup"><span data-stu-id="1448c-257">key</span></span> | <span data-ttu-id="1448c-258">value</span><span class="sxs-lookup"><span data-stu-id="1448c-258">value</span></span> | <span data-ttu-id="1448c-259">padrão</span><span class="sxs-lookup"><span data-stu-id="1448c-259">default</span></span> | <span data-ttu-id="1448c-260">Notas</span><span class="sxs-lookup"><span data-stu-id="1448c-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="1448c-261">habilitado</span><span class="sxs-lookup"><span data-stu-id="1448c-261">enabled</span></span> | <span data-ttu-id="1448c-262">booliano</span><span class="sxs-lookup"><span data-stu-id="1448c-262">boolean</span></span> | `true` | <span data-ttu-id="1448c-263">Configuração de chave nesse determinará se WSL oferece suporte a processos do Windows iniciar.</span><span class="sxs-lookup"><span data-stu-id="1448c-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="1448c-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="1448c-264">appendWindowsPath</span></span> | <span data-ttu-id="1448c-265">booliano</span><span class="sxs-lookup"><span data-stu-id="1448c-265">boolean</span></span> | `true` | <span data-ttu-id="1448c-266">Configuração de chave nesse determinará se WSL adicionará os elementos de caminho do Windows para a variável de ambiente $PATH.</span><span class="sxs-lookup"><span data-stu-id="1448c-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
