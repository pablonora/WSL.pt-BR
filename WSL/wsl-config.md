---
title: Gerenciar as distribuições do Linux
description: Listagem de referência e configuração de várias distribuições do Linux em execução no Subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 51099f21fe44fd8c7e8682332c939fbe6d5e5827
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269874"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="d2b8b-104">Gerenciar e configurar o Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="d2b8b-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="d2b8b-105">Aplicável ao Windows 10 Fall Creators Update e posteriores.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="d2b8b-106">Consulte nosso [guia de instalação](./install_guide.md) atualizado para experimentar novos recursos de gerenciamento e iniciar a execução de várias distribuições do Linux na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="d2b8b-107">Maneiras de executar o WSL</span><span class="sxs-lookup"><span data-stu-id="d2b8b-107">Ways to run WSL</span></span>

<span data-ttu-id="d2b8b-108">Há várias maneiras de executar o Linux com o Subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="d2b8b-109">`[distro]`, por exemplo, `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="d2b8b-110">`wsl.exe` ou `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="d2b8b-111">`wsl [command]` ou `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="d2b8b-112">Qual método deve ser usado depende do que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="d2b8b-113">Iniciar o WSL por distribuição</span><span class="sxs-lookup"><span data-stu-id="d2b8b-113">Launch WSL by distribution</span></span>

<span data-ttu-id="d2b8b-114">A execução de uma distribuição usando o aplicativo específico da distribuição inicia essa distribuição na própria janela do console.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Iniciar o WSL no menu Iniciar](media/start-launch.png)

<span data-ttu-id="d2b8b-116">É o mesmo que clicar em "Iniciar" na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Iniciar o WSL usando a Microsoft Store](media/store-launch.png)

<span data-ttu-id="d2b8b-118">Você também pode executar a distribuição na linha de comando executando `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="d2b8b-119">A desvantagem de executar uma distribuição da linha de comando dessa forma é que ela alterará automaticamente seu diretório de trabalho do diretório atual para o diretório base da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="d2b8b-120">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="d2b8b-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="d2b8b-121">wsl e wsl [comando]</span><span class="sxs-lookup"><span data-stu-id="d2b8b-121">wsl and wsl [command]</span></span>

<span data-ttu-id="d2b8b-122">A melhor maneira de executar o WSL na linha de comando é usando o `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="d2b8b-123">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="d2b8b-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="d2b8b-124">O `wsl` não apenas mantém o diretório de trabalho atual em vigor, como também permite que você execute um único comando ao longo dos comandos do Windows.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="d2b8b-125">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="d2b8b-125">**Example:**</span></span>

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

<span data-ttu-id="d2b8b-126">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="d2b8b-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="d2b8b-127">Como gerenciar várias distribuições do Linux</span><span class="sxs-lookup"><span data-stu-id="d2b8b-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="d2b8b-128">Windows 10, versão 1903 e posteriores</span><span class="sxs-lookup"><span data-stu-id="d2b8b-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="d2b8b-129">Você pode usar o `wsl.exe` para gerenciar suas distribuições no WSL (Subsistema Windows para Linux), incluindo a listagem de distribuições disponíveis, a configuração de uma distribuição padrão e a desinstalação de distribuições.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="d2b8b-130">Cada distribuição do Linux gerencia de forma independente suas próprias configurações.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="d2b8b-131">Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="d2b8b-132">Por exemplo, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="d2b8b-133">Listar distribuições</span><span class="sxs-lookup"><span data-stu-id="d2b8b-133">List distributions</span></span>

<span data-ttu-id="d2b8b-134">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="d2b8b-135">Lista as distribuições do Linux disponíveis para WSL.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="d2b8b-136">Se uma distribuição estiver listada, ela será instalada e estará pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="d2b8b-137">Lista todas as distribuições, incluindo aquelas que não são utilizáveis no momento.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="d2b8b-138">Elas podem estar no processo de instalação, desinstalação ou em um estado desfeito.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="d2b8b-139">Lista todas as distribuições que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="d2b8b-140">Definir uma distribuição padrão</span><span class="sxs-lookup"><span data-stu-id="d2b8b-140">Set a default distribution</span></span>

<span data-ttu-id="d2b8b-141">A distribuição do WSL padrão é aquela que é executada quando você executa `wsl` em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="d2b8b-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="d2b8b-143">Define uma distribuição padrão para `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="d2b8b-144">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="d2b8b-144">**Example:**</span></span>  
<span data-ttu-id="d2b8b-145">`wsl -s Ubuntu` definiria minha distribuição padrão como Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="d2b8b-146">Agora, quando eu executar o `wsl npm init`, ele será executado no Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="d2b8b-147">Se eu executar `wsl`, ele abrirá uma sessão do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="d2b8b-148">Cancelar o registro e reinstalar uma distribuição</span><span class="sxs-lookup"><span data-stu-id="d2b8b-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="d2b8b-149">Embora as distribuições do Linux possam ser instaladas por meio da Microsoft Store, elas não podem ser desinstaladas usando a loja.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="d2b8b-150">O WSL Config permite que as distribuições tenham o registro cancelado/sejam desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="d2b8b-151">O cancelamento do registro também permite que as distribuições sejam reinstaladas.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="d2b8b-152">**Cuidado:** Após o cancelamento do registro, todos os dados, as configurações e os softwares associados a essa distribuição serão permanentemente perdidos.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="d2b8b-153">A reinstalação pela loja instalará uma cópia limpa da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="d2b8b-154">Cancela o registro da distribuição do WSL para que possa ser reinstalado ou limpo.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="d2b8b-155">Por exemplo, `wsl --unregister Ubuntu` removeria o Ubuntu das distribuições disponíveis no WSL.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="d2b8b-156">Quando eu executar `wsl --list`, ele não será listado.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="d2b8b-157">Para reinstalar, localize a distribuição na Microsoft Store e selecione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="d2b8b-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="d2b8b-158">Execute como um usuário específico</span><span class="sxs-lookup"><span data-stu-id="d2b8b-158">Run as a specific user</span></span>

<span data-ttu-id="d2b8b-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="d2b8b-160">Execute o WSL como o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-160">Run WSL as the specified user.</span></span> <span data-ttu-id="d2b8b-161">Observe que o usuário deve existir dentro da distribuição do WSL.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="d2b8b-162">Executar uma distribuição específica</span><span class="sxs-lookup"><span data-stu-id="d2b8b-162">Run a specific distribution</span></span>

<span data-ttu-id="d2b8b-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="d2b8b-164">A execução de uma distribuição especificada do WSL pode ser usada para enviar comandos para uma distribuição específica sem precisar alterar o padrão.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="d2b8b-165">Versões anteriores ao Windows 10, versão 1903</span><span class="sxs-lookup"><span data-stu-id="d2b8b-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="d2b8b-166">O WSL Config (`wslconfig.exe`) é uma ferramenta de linha de comando para gerenciar distribuições do Linux em execução no WSL (Subsistema Windows para Linux).</span><span class="sxs-lookup"><span data-stu-id="d2b8b-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="d2b8b-167">Ele permite que você liste as distribuições disponíveis, defina uma distribuição padrão e desinstale as distribuições.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="d2b8b-168">Embora o WSL Config seja útil para configurações que abrangem ou coordenam distribuições, cada distribuição do Linux gerencia de forma independente suas próprias configurações.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="d2b8b-169">Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="d2b8b-170">Por exemplo, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="d2b8b-171">Para ver todas as opções disponíveis para wslconfig, execute: `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="d2b8b-172">Listar distribuições</span><span class="sxs-lookup"><span data-stu-id="d2b8b-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="d2b8b-173">Lista as distribuições do Linux disponíveis para WSL.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="d2b8b-174">Se uma distribuição estiver listada, ela será instalada e estará pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="d2b8b-175">Lista todas as distribuições, incluindo aquelas que não são utilizáveis no momento.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="d2b8b-176">Elas podem estar no processo de instalação, desinstalação ou em um estado desfeito.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="d2b8b-177">Definir uma distribuição padrão</span><span class="sxs-lookup"><span data-stu-id="d2b8b-177">Set a default distribution</span></span>

<span data-ttu-id="d2b8b-178">A distribuição do WSL padrão é aquela que é executada quando você executa `wsl` em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="d2b8b-179">Define uma distribuição padrão para `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="d2b8b-180">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="d2b8b-180">**Example:**</span></span>  
<span data-ttu-id="d2b8b-181">`wslconfig /setdefault Ubuntu` definiria minha distribuição padrão como Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="d2b8b-182">Agora, quando eu executar o `wsl npm init`, ele será executado no Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="d2b8b-183">Se eu executar `wsl`, ele abrirá uma sessão do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="d2b8b-184">Cancelar o registro e reinstalar uma distribuição</span><span class="sxs-lookup"><span data-stu-id="d2b8b-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="d2b8b-185">Embora as distribuições do Linux possam ser instaladas por meio da Microsoft Store, elas não podem ser desinstaladas usando a loja.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="d2b8b-186">O WSL Config permite que as distribuições tenham o registro cancelado/sejam desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="d2b8b-187">O cancelamento do registro também permite que as distribuições sejam reinstaladas.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="d2b8b-188">**Cuidado:** Após o cancelamento do registro, todos os dados, as configurações e os softwares associados a essa distribuição serão permanentemente perdidos.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="d2b8b-189">A reinstalação pela loja instalará uma cópia limpa da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="d2b8b-190">Cancela o registro da distribuição do WSL para que possa ser reinstalado ou limpo.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="d2b8b-191">Por exemplo, `wslconfig /unregister Ubuntu` removeria o Ubuntu das distribuições disponíveis no WSL.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="d2b8b-192">Quando eu executar `wslconfig /list`, ele não será listado.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="d2b8b-193">Para reinstalar, localize a distribuição na Microsoft Store e selecione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="d2b8b-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="d2b8b-194">Definir as configurações de inicialização do WSL</span><span class="sxs-lookup"><span data-stu-id="d2b8b-194">Set WSL launch settings</span></span>

> <span data-ttu-id="d2b8b-195">**Disponível no Participante do Programa Windows Insider Build 17093 e posteriores**</span><span class="sxs-lookup"><span data-stu-id="d2b8b-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="d2b8b-196">Configure automaticamente determinadas funcionalidades no WSL que serão aplicadas toda vez que você iniciar o subsistema usando `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="d2b8b-197">No momento, isso inclui opções de montagem automática e configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="d2b8b-198">`wsl.conf` está localizado em cada distribuição do Linux no `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="d2b8b-199">Se o arquivo não estiver lá, você mesmo poderá criá-lo.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="d2b8b-200">O WSL detectará a existência do arquivo e lerá seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="d2b8b-201">Se o arquivo estiver ausente ou malformado (ou seja, formatação de marcação inadequada), o WSL continuará a ser iniciado normalmente.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="d2b8b-202">Aqui está um arquivo `wsl.conf` de exemplo que você pode adicionar às suas distribuições:</span><span class="sxs-lookup"><span data-stu-id="d2b8b-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="d2b8b-203">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="d2b8b-203">Configuration Options</span></span>

<span data-ttu-id="d2b8b-204">Para manter as convenções .ini, as chaves são declaradas em uma seção.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="d2b8b-205">O WSL é compatível com duas seções: `automount` e `network`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="d2b8b-206">montagem automática</span><span class="sxs-lookup"><span data-stu-id="d2b8b-206">automount</span></span>

<span data-ttu-id="d2b8b-207">Seção: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-207">Section: `[automount]`</span></span>


| <span data-ttu-id="d2b8b-208">key</span><span class="sxs-lookup"><span data-stu-id="d2b8b-208">key</span></span>        | <span data-ttu-id="d2b8b-209">value</span><span class="sxs-lookup"><span data-stu-id="d2b8b-209">value</span></span>                          | <span data-ttu-id="d2b8b-210">padrão</span><span class="sxs-lookup"><span data-stu-id="d2b8b-210">default</span></span>      | <span data-ttu-id="d2b8b-211">observações</span><span class="sxs-lookup"><span data-stu-id="d2b8b-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b8b-212">habilitado</span><span class="sxs-lookup"><span data-stu-id="d2b8b-212">enabled</span></span>    | <span data-ttu-id="d2b8b-213">booliano</span><span class="sxs-lookup"><span data-stu-id="d2b8b-213">boolean</span></span>                        | <span data-ttu-id="d2b8b-214">verdadeiro</span><span class="sxs-lookup"><span data-stu-id="d2b8b-214">true</span></span>         | <span data-ttu-id="d2b8b-215">`true` causa unidades fixas (ou seja,</span><span class="sxs-lookup"><span data-stu-id="d2b8b-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="d2b8b-216">`C:/` ou `D:/`) a ser montado automaticamente com DrvFs em `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="d2b8b-217">`false` significa que as unidades não serão montadas automaticamente, mas você ainda poderá montá-las manualmente ou por meio do `fstab`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="d2b8b-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="d2b8b-218">mountFsTab</span></span> | <span data-ttu-id="d2b8b-219">booliano</span><span class="sxs-lookup"><span data-stu-id="d2b8b-219">boolean</span></span>                        | <span data-ttu-id="d2b8b-220">verdadeiro</span><span class="sxs-lookup"><span data-stu-id="d2b8b-220">true</span></span>         | <span data-ttu-id="d2b8b-221">O `true` define o `/etc/fstab` para ser processado no início do WSL.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="d2b8b-222">/etc/fstab é um arquivo no qual você pode declarar outros sistemas de arquivos, como um compartilhamento SMB.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="d2b8b-223">Assim, você pode montar esses sistemas de arquivos automaticamente no WSL na inicialização.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="d2b8b-224">raiz</span><span class="sxs-lookup"><span data-stu-id="d2b8b-224">root</span></span>       | <span data-ttu-id="d2b8b-225">String</span><span class="sxs-lookup"><span data-stu-id="d2b8b-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="d2b8b-226">Define o diretório em que as unidades fixas serão montadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="d2b8b-227">Por exemplo, se tiver um diretório no WSL no `/windir/` e especificá-lo como a raiz, você poderá esperar ver suas unidades fixas montadas em `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="d2b8b-228">opções</span><span class="sxs-lookup"><span data-stu-id="d2b8b-228">options</span></span>    | <span data-ttu-id="d2b8b-229">lista de valores separados por vírgulas</span><span class="sxs-lookup"><span data-stu-id="d2b8b-229">comma-separated list of values</span></span> | <span data-ttu-id="d2b8b-230">cadeia de caracteres vazia</span><span class="sxs-lookup"><span data-stu-id="d2b8b-230">empty string</span></span> | <span data-ttu-id="d2b8b-231">Esse valor é acrescentado à cadeia de caracteres de opções padrão de montagem DrvFs.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="d2b8b-232">**Somente opções específicas do DrvFs podem ser especificadas.**</span><span class="sxs-lookup"><span data-stu-id="d2b8b-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="d2b8b-233">As opções que o binário de montagem normalmente analisa em um sinalizador não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="d2b8b-234">Se você quiser especificar explicitamente essas opções, deverá incluir todas as unidades para as quais deseja fazer isso em /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="d2b8b-235">Por padrão, o WSL define o UID e o GID como o valor do usuário padrão (na distribuição do Ubuntu, o usuário padrão é criado com UID = 1.000, GID = 1.000).</span><span class="sxs-lookup"><span data-stu-id="d2b8b-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="d2b8b-236">Se o usuário especificar uma opção GID ou UID explicitamente por meio dessa chave, o valor associado será substituído.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="d2b8b-237">Caso contrário, o valor padrão será sempre acrescentado.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="d2b8b-238">**Observação:** Essas opções são aplicadas como opções de montagem para todas as unidades montadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="d2b8b-239">Para alterar as opções somente para uma unidade específica, use/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="d2b8b-240">rede</span><span class="sxs-lookup"><span data-stu-id="d2b8b-240">network</span></span>

<span data-ttu-id="d2b8b-241">Rótulo da seção: `[network]`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-241">Section label: `[network]`</span></span>

| <span data-ttu-id="d2b8b-242">key</span><span class="sxs-lookup"><span data-stu-id="d2b8b-242">key</span></span> | <span data-ttu-id="d2b8b-243">value</span><span class="sxs-lookup"><span data-stu-id="d2b8b-243">value</span></span> | <span data-ttu-id="d2b8b-244">padrão</span><span class="sxs-lookup"><span data-stu-id="d2b8b-244">default</span></span> | <span data-ttu-id="d2b8b-245">observações</span><span class="sxs-lookup"><span data-stu-id="d2b8b-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="d2b8b-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="d2b8b-246">generateHosts</span></span> | <span data-ttu-id="d2b8b-247">booliano</span><span class="sxs-lookup"><span data-stu-id="d2b8b-247">boolean</span></span> | `true` | <span data-ttu-id="d2b8b-248">O `true` define o WSL para gerar `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="d2b8b-249">O arquivo `hosts` contém um mapa estático do endereço IP correspondente de nomes de host.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="d2b8b-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="d2b8b-250">generateResolvConf</span></span> | <span data-ttu-id="d2b8b-251">booliano</span><span class="sxs-lookup"><span data-stu-id="d2b8b-251">boolean</span></span> | `true` | <span data-ttu-id="d2b8b-252">O `true` define o WSL para gerar `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="d2b8b-253">O `resolv.conf` contém uma lista DNS que é capaz de resolver um determinado nome de host para seu endereço IP.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="d2b8b-254">interop</span><span class="sxs-lookup"><span data-stu-id="d2b8b-254">interop</span></span>

<span data-ttu-id="d2b8b-255">Rótulo da seção: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="d2b8b-255">Section label: `[interop]`</span></span>

<span data-ttu-id="d2b8b-256">Essas opções estão disponíveis no Insider Build 17713 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="d2b8b-257">key</span><span class="sxs-lookup"><span data-stu-id="d2b8b-257">key</span></span> | <span data-ttu-id="d2b8b-258">value</span><span class="sxs-lookup"><span data-stu-id="d2b8b-258">value</span></span> | <span data-ttu-id="d2b8b-259">padrão</span><span class="sxs-lookup"><span data-stu-id="d2b8b-259">default</span></span> | <span data-ttu-id="d2b8b-260">observações</span><span class="sxs-lookup"><span data-stu-id="d2b8b-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="d2b8b-261">habilitado</span><span class="sxs-lookup"><span data-stu-id="d2b8b-261">enabled</span></span> | <span data-ttu-id="d2b8b-262">booliano</span><span class="sxs-lookup"><span data-stu-id="d2b8b-262">boolean</span></span> | `true` | <span data-ttu-id="d2b8b-263">Definir essa chave determinará se o WSL dará suporte à inicialização de processos do Windows.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="d2b8b-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="d2b8b-264">appendWindowsPath</span></span> | <span data-ttu-id="d2b8b-265">booliano</span><span class="sxs-lookup"><span data-stu-id="d2b8b-265">boolean</span></span> | `true` | <span data-ttu-id="d2b8b-266">Definir essa chave determinará se o WSL adicionará elementos de caminho do Windows à variável de ambiente $PATH.</span><span class="sxs-lookup"><span data-stu-id="d2b8b-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
