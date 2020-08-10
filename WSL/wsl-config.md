---
title: Gerenciar as distribuições do Linux
description: Listagem de referência e configuração de várias distribuições do Linux em execução no Subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: b8aa740233f3ac9517744212eb7b362a18378822
ms.sourcegitcommit: 90577817a9321949da2a3971b4c78bb00f6d977f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "88039409"
---
# <a name="wsl-commands-and-launch-configurations"></a><span data-ttu-id="bcb4d-104">Comandos do WSL e configurações de inicialização</span><span class="sxs-lookup"><span data-stu-id="bcb4d-104">WSL commands and launch configurations</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="bcb4d-105">Maneiras de executar o WSL</span><span class="sxs-lookup"><span data-stu-id="bcb4d-105">Ways to run WSL</span></span>

<span data-ttu-id="bcb4d-106">Há várias maneiras de executar uma distribuição do Linux com o WSL depois que ele é [instalado](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="bcb4d-106">There are several ways to run a Linux distribution with WSL once it's [installed](install-win10.md).</span></span>

1. <span data-ttu-id="bcb4d-107">Abra sua distribuição do Linux visitando o menu Iniciar do Windows e digitando o nome de suas distribuições instaladas.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-107">Open your Linux distribution by visiting the Windows Start menu and typing the name of your installed distributions.</span></span> <span data-ttu-id="bcb4d-108">Por exemplo: "Ubuntu".</span><span class="sxs-lookup"><span data-stu-id="bcb4d-108">For example: "Ubuntu".</span></span>
2. <span data-ttu-id="bcb4d-109">No prompt de comando do Windows ou no PowerShell, insira o nome da sua distribuição instalada.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-109">From Windows Command Prompt or PowerShell, enter the name of your installed distribution.</span></span> <span data-ttu-id="bcb4d-110">Por exemplo: `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-110">For example: `ubuntu`</span></span>
3. <span data-ttu-id="bcb4d-111">No prompt de comando do Windows ou no PowerShell, para abrir sua distribuição do Linux padrão dentro da linha de comando atual, digite: `wsl.exe` .</span><span class="sxs-lookup"><span data-stu-id="bcb4d-111">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter: `wsl.exe`.</span></span>
4. <span data-ttu-id="bcb4d-112">No prompt de comando do Windows ou no PowerShell, para abrir sua distribuição do Linux padrão dentro da linha de comando atual, digite: `wsl [command]` .</span><span class="sxs-lookup"><span data-stu-id="bcb4d-112">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter:`wsl [command]`.</span></span>

<span data-ttu-id="bcb4d-113">Qual método deve ser usado depende do que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-113">Which method you should use depends on what you're doing.</span></span> <span data-ttu-id="bcb4d-114">Se você tiver aberto uma linha de comando WSL em um prompt do Windows ou janela do PowerShell e quiser sair, insira o comando: `exit` .</span><span class="sxs-lookup"><span data-stu-id="bcb4d-114">If you've opened a WSL command line within a Windows Prompt or PowerShell window and want to exit, enter the command: `exit`.</span></span>

## <a name="launch-wsl-by-distribution"></a><span data-ttu-id="bcb4d-115">Iniciar o WSL por distribuição</span><span class="sxs-lookup"><span data-stu-id="bcb4d-115">Launch WSL by distribution</span></span>

<span data-ttu-id="bcb4d-116">A execução de uma distribuição usando o aplicativo específico da distribuição inicia essa distribuição na própria janela do console.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-116">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Iniciar o WSL no menu Iniciar](media/start-launch.png)

<span data-ttu-id="bcb4d-118">É o mesmo que clicar em "Iniciar" na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-118">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Iniciar o WSL usando a Microsoft Store](media/store-launch.png)

<span data-ttu-id="bcb4d-120">Você também pode executar a distribuição na linha de comando executando `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-120">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="bcb4d-121">A desvantagem de executar uma distribuição da linha de comando dessa forma é que ela alterará automaticamente seu diretório de trabalho do diretório atual para o diretório base da distribuição.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-121">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="bcb4d-122">**Exemplo: (usando o PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-122">**Example: (using PowerShell)**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="bcb4d-123">wsl e wsl [comando]</span><span class="sxs-lookup"><span data-stu-id="bcb4d-123">wsl and wsl [command]</span></span>

<span data-ttu-id="bcb4d-124">A melhor maneira de executar o WSL na linha de comando é usando o `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-124">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="bcb4d-125">**Exemplo: (usando o PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-125">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="bcb4d-126">O `wsl` não apenas mantém o diretório de trabalho atual em vigor, como também permite que você execute um único comando ao longo dos comandos do Windows.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-126">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="bcb4d-127">**Exemplo: (usando o PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-127">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

<span data-ttu-id="bcb4d-128">**Exemplo: (usando o PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-128">**Example: (using PowerShell)**</span></span>

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

## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="bcb4d-129">Como gerenciar várias distribuições do Linux</span><span class="sxs-lookup"><span data-stu-id="bcb4d-129">Managing multiple Linux Distributions</span></span>

<span data-ttu-id="bcb4d-130">No Windows 10 versão 1903 [e posterior](ms-settings:windowsupdate), você pode usar o `wsl.exe` para gerenciar suas distribuições no subsistema do Windows para Linux (WSL), incluindo a listagem de distribuições disponíveis, a definição de uma distribuição padrão e a desinstalação de distribuições.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-130">In Windows 10 Version 1903 [and later](ms-settings:windowsupdate), you can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="bcb4d-131">Cada distribuição do Linux gerencia de forma independente suas próprias configurações.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-131">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="bcb4d-132">Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-132">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="bcb4d-133">Por exemplo, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-133">For example `ubuntu /?`.</span></span>

## <a name="list-distributions"></a><span data-ttu-id="bcb4d-134">Listar distribuições</span><span class="sxs-lookup"><span data-stu-id="bcb4d-134">List distributions</span></span>

<span data-ttu-id="bcb4d-135">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-135">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="bcb4d-136">Lista as distribuições do Linux disponíveis para WSL.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-136">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="bcb4d-137">Se uma distribuição estiver listada, ela será instalada e estará pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-137">If a distribution is listed, it's installed and ready to use.</span></span>

<span data-ttu-id="bcb4d-138">`wsl --list --all`Lista todas as distribuições, incluindo aquelas que não são utilizáveis no momento.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-138">`wsl --list --all` Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="bcb4d-139">Elas podem estar no processo de instalação, desinstalação ou em um estado desfeito.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-139">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="bcb4d-140">`wsl --list --running`Lista todas as distribuições que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-140">`wsl --list --running` Lists all distributions that are currently running.</span></span>

## <a name="set-a-default-distribution"></a><span data-ttu-id="bcb4d-141">Definir uma distribuição padrão</span><span class="sxs-lookup"><span data-stu-id="bcb4d-141">Set a default distribution</span></span>

<span data-ttu-id="bcb4d-142">A distribuição do WSL padrão é aquela que é executada quando você executa `wsl` em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-142">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="bcb4d-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="bcb4d-144">Define uma distribuição padrão para `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-144">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="bcb4d-145">**Exemplo: (usando o PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-145">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="bcb4d-146">`wsl -s Ubuntu` definiria minha distribuição padrão como Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-146">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="bcb4d-147">Agora, quando eu executar o `wsl npm init`, ele será executado no Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-147">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="bcb4d-148">Se eu executar `wsl`, ele abrirá uma sessão do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-148">If I run `wsl` it will open an Ubuntu session.</span></span>

## <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="bcb4d-149">Cancelar o registro e reinstalar uma distribuição</span><span class="sxs-lookup"><span data-stu-id="bcb4d-149">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="bcb4d-150">Embora as distribuições do Linux possam ser instaladas por meio da Microsoft Store, elas não podem ser desinstaladas usando a loja.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-150">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="bcb4d-151">O WSL Config permite que as distribuições tenham o registro cancelado/sejam desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-151">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="bcb4d-152">O cancelamento do registro também permite que as distribuições sejam reinstaladas.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-152">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="bcb4d-153">**Cuidado:** Após o registro, todos os dados, as configurações e os softwares associados a essa distribuição serão permanentemente perdidos.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-153">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="bcb4d-154">A reinstalação pela loja instalará uma cópia limpa da distribuição.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-154">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="bcb4d-155">Cancela o registro da distribuição do WSL para que possa ser reinstalado ou limpo.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-155">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="bcb4d-156">Por exemplo, `wsl --unregister Ubuntu` removeria o Ubuntu das distribuições disponíveis no WSL.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-156">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="bcb4d-157">Quando eu executar `wsl --list`, ele não será listado.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-157">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="bcb4d-158">Para reinstalar, localize a distribuição na Microsoft Store e selecione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="bcb4d-158">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="run-as-a-specific-user"></a><span data-ttu-id="bcb4d-159">Execute como um usuário específico</span><span class="sxs-lookup"><span data-stu-id="bcb4d-159">Run as a specific user</span></span>

<span data-ttu-id="bcb4d-160">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-160">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="bcb4d-161">Execute o WSL como o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-161">Run WSL as the specified user.</span></span> <span data-ttu-id="bcb4d-162">Observe que o usuário deve existir dentro da distribuição do WSL.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-162">Please note that user must exist inside of the WSL distribution.</span></span>

## <a name="change-the-default-user-for-a-distribution"></a><span data-ttu-id="bcb4d-163">Alterar o usuário padrão para uma distribuição</span><span class="sxs-lookup"><span data-stu-id="bcb4d-163">Change the default user for a distribution</span></span>

`<DistributionName> config --default-user <Username>`

<span data-ttu-id="bcb4d-164">Altere o usuário padrão para o seu logon de distribuição.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-164">Change the default user that for your distribution log-in.</span></span> <span data-ttu-id="bcb4d-165">O usuário já deve existir dentro da distribuição para se tornar o usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-165">The user has to already exist inside the distribution in order to become the default user.</span></span> 

<span data-ttu-id="bcb4d-166">Por exemplo: `ubuntu config --default-user johndoe` alteraria o usuário padrão para a distribuição do Ubuntu para o usuário "davibarros".</span><span class="sxs-lookup"><span data-stu-id="bcb4d-166">For example: `ubuntu config --default-user johndoe` would change the default user for the Ubuntu distribution to the "johndoe" user.</span></span>

> [!NOTE]
> <span data-ttu-id="bcb4d-167">Se você estiver tendo problemas para descobrir o nome da sua distribuição, consulte [listar distribuições](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) para o comando para listar o nome oficial das distribuições instaladas.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-167">If you are having trouble figuring out the name of your distribution, see [List distributions](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) for the command to list the official name of the installed distributions.</span></span> 

## <a name="run-a-specific-distribution"></a><span data-ttu-id="bcb4d-168">Executar uma distribuição específica</span><span class="sxs-lookup"><span data-stu-id="bcb4d-168">Run a specific distribution</span></span>

<span data-ttu-id="bcb4d-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="bcb4d-170">A execução de uma distribuição especificada do WSL pode ser usada para enviar comandos para uma distribuição específica sem precisar alterar o padrão.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-170">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a><span data-ttu-id="bcb4d-171">Gerenciando várias distribuições Linux em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="bcb4d-171">Managing multiple Linux Distributions in earlier Windows versions</span></span>

<span data-ttu-id="bcb4d-172">No Windows 10 antes da versão 1903, a ferramenta de linha de comando WSL config ( `wslconfig.exe` ) deve ser usada para gerenciar as distribuições do Linux em execução no subsistema do Windows para Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="bcb4d-172">In Windows 10 prior to version 1903, the WSL Config (`wslconfig.exe`) command-line tool should be used to manage Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="bcb4d-173">Ele permite que você liste as distribuições disponíveis, defina uma distribuição padrão e desinstale as distribuições.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-173">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="bcb4d-174">Embora o WSL Config seja útil para configurações que abrangem ou coordenam distribuições, cada distribuição do Linux gerencia de forma independente suas próprias configurações.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-174">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="bcb4d-175">Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-175">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="bcb4d-176">Por exemplo, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-176">For example `ubuntu /?`.</span></span>

<span data-ttu-id="bcb4d-177">Para ver todas as opções disponíveis para wslconfig, execute: `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-177">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

<span data-ttu-id="bcb4d-178">Para listar distribuições, use:</span><span class="sxs-lookup"><span data-stu-id="bcb4d-178">To list distributions, use:</span></span>

`wslconfig /list`  
<span data-ttu-id="bcb4d-179">Lista as distribuições do Linux disponíveis para WSL.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-179">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="bcb4d-180">Se uma distribuição estiver listada, ela será instalada e estará pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-180">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="bcb4d-181">Lista todas as distribuições, incluindo aquelas que não são utilizáveis no momento.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-181">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="bcb4d-182">Elas podem estar no processo de instalação, desinstalação ou em um estado desfeito.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-182">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="bcb4d-183">Para definir uma distribuição padrão que é executada quando você executa `wsl` em uma linha de comando:</span><span class="sxs-lookup"><span data-stu-id="bcb4d-183">To set a default distribution that runs when you run `wsl` on a command line:</span></span>

<span data-ttu-id="bcb4d-184">`wslconfig /setdefault <DistributionName>`Define a distribuição padrão como `<DistributionName>` .</span><span class="sxs-lookup"><span data-stu-id="bcb4d-184">`wslconfig /setdefault <DistributionName>` Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="bcb4d-185">**Exemplo: (usando o PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-185">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="bcb4d-186">`wslconfig /setdefault Ubuntu` definiria minha distribuição padrão como Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-186">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="bcb4d-187">Agora, quando eu executar o `wsl npm init`, ele será executado no Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-187">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="bcb4d-188">Se eu executar `wsl`, ele abrirá uma sessão do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-188">If I run `wsl` it will open an Ubuntu session.</span></span>

<span data-ttu-id="bcb4d-189">Para cancelar o registro e reinstalar uma distribuição:</span><span class="sxs-lookup"><span data-stu-id="bcb4d-189">To unregister and reinstall a distribution:</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="bcb4d-190">Cancela o registro da distribuição do WSL para que possa ser reinstalado ou limpo.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="bcb4d-191">Por exemplo, `wslconfig /unregister Ubuntu` removeria o Ubuntu das distribuições disponíveis no WSL.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="bcb4d-192">Quando eu executar `wslconfig /list`, ele não será listado.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="bcb4d-193">Para reinstalar, localize a distribuição na Microsoft Store e selecione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="bcb4d-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="configure-per-distro-launch-settings-with-wslconf"></a><span data-ttu-id="bcb4d-194">Definir configurações de inicialização por distribuição com wslconf</span><span class="sxs-lookup"><span data-stu-id="bcb4d-194">Configure per distro launch settings with wslconf</span></span>

> <span data-ttu-id="bcb4d-195">**Disponível no Windows Build 17093 e posterior**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-195">**Available in Windows Build 17093 and later**</span></span>

<span data-ttu-id="bcb4d-196">Configure automaticamente determinadas funcionalidades no WSL que serão aplicadas toda vez que você iniciar o subsistema usando `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span>

<span data-ttu-id="bcb4d-197">No momento, isso inclui opções de montagem automática e configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="bcb4d-198">`wsl.conf` está localizado em cada distribuição do Linux no `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="bcb4d-199">Se o arquivo não estiver lá, você mesmo poderá criá-lo.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="bcb4d-200">O WSL detectará a existência do arquivo e lerá seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="bcb4d-201">Se o arquivo estiver ausente ou malformado (ou seja, formatação de marcação inadequada), o WSL continuará a ser iniciado normalmente.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="bcb4d-202">Aqui está um arquivo de exemplo `wsl.conf` que você pode adicionar a suas distribuições:</span><span class="sxs-lookup"><span data-stu-id="bcb4d-202">Here is a sample `wsl.conf` file you could add into your distributions:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="bcb4d-203">Opções de configuração</span><span class="sxs-lookup"><span data-stu-id="bcb4d-203">Configuration Options</span></span>

<span data-ttu-id="bcb4d-204">Para manter as convenções .ini, as chaves são declaradas em uma seção.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="bcb4d-205">O WSL é compatível com duas seções: `automount` e `network`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="bcb4d-206">montagem automática</span><span class="sxs-lookup"><span data-stu-id="bcb4d-206">automount</span></span>

<span data-ttu-id="bcb4d-207">Seção: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-207">Section: `[automount]`</span></span>

| <span data-ttu-id="bcb4d-208">key</span><span class="sxs-lookup"><span data-stu-id="bcb4d-208">key</span></span>        | <span data-ttu-id="bcb4d-209">value</span><span class="sxs-lookup"><span data-stu-id="bcb4d-209">value</span></span>                          | <span data-ttu-id="bcb4d-210">default</span><span class="sxs-lookup"><span data-stu-id="bcb4d-210">default</span></span>      | <span data-ttu-id="bcb4d-211">observações</span><span class="sxs-lookup"><span data-stu-id="bcb4d-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb4d-212">habilitado</span><span class="sxs-lookup"><span data-stu-id="bcb4d-212">enabled</span></span>    | <span data-ttu-id="bcb4d-213">booliano</span><span class="sxs-lookup"><span data-stu-id="bcb4d-213">boolean</span></span>                        | <span data-ttu-id="bcb4d-214">verdadeiro</span><span class="sxs-lookup"><span data-stu-id="bcb4d-214">true</span></span>         | <span data-ttu-id="bcb4d-215">`true` causa unidades fixas (ou seja,</span><span class="sxs-lookup"><span data-stu-id="bcb4d-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="bcb4d-216">`C:/` ou `D:/`) a ser montado automaticamente com DrvFs em `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="bcb4d-217">`false`significa que as unidades não serão montadas automaticamente, mas você ainda poderá montá-las manualmente ou por meio do `fstab` .</span><span class="sxs-lookup"><span data-stu-id="bcb4d-217">`false` means drives won't be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="bcb4d-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="bcb4d-218">mountFsTab</span></span> | <span data-ttu-id="bcb4d-219">booliano</span><span class="sxs-lookup"><span data-stu-id="bcb4d-219">boolean</span></span>                        | <span data-ttu-id="bcb4d-220">verdadeiro</span><span class="sxs-lookup"><span data-stu-id="bcb4d-220">true</span></span>         | <span data-ttu-id="bcb4d-221">O `true` define o `/etc/fstab` para ser processado no início do WSL.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="bcb4d-222">/etc/fstab é um arquivo no qual você pode declarar outros sistemas de arquivos, como um compartilhamento SMB.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="bcb4d-223">Assim, você pode montar esses sistemas de arquivos automaticamente no WSL na inicialização.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="bcb4d-224">raiz</span><span class="sxs-lookup"><span data-stu-id="bcb4d-224">root</span></span>       | <span data-ttu-id="bcb4d-225">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="bcb4d-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="bcb4d-226">Define o diretório em que as unidades fixas serão montadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="bcb4d-227">Por exemplo, se tiver um diretório no WSL no `/windir/` e especificá-lo como a raiz, você poderá esperar ver suas unidades fixas montadas em `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="bcb4d-228">opções</span><span class="sxs-lookup"><span data-stu-id="bcb4d-228">options</span></span>    | <span data-ttu-id="bcb4d-229">lista de valores separados por vírgulas</span><span class="sxs-lookup"><span data-stu-id="bcb4d-229">comma-separated list of values</span></span> | <span data-ttu-id="bcb4d-230">cadeia de caracteres vazia</span><span class="sxs-lookup"><span data-stu-id="bcb4d-230">empty string</span></span> | <span data-ttu-id="bcb4d-231">Esse valor é acrescentado à cadeia de caracteres de opções padrão de montagem DrvFs.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="bcb4d-232">**Somente opções específicas do DrvFs podem ser especificadas.**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="bcb4d-233">As opções que o binário de montagem normalmente analisa em um sinalizador não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="bcb4d-234">Se você quiser especificar explicitamente essas opções, deverá incluir todas as unidades para as quais deseja fazer isso em /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="bcb4d-235">Por padrão, o WSL define o UID e o GID como o valor do usuário padrão (na distribuição do Ubuntu, o usuário padrão é criado com UID = 1.000, GID = 1.000).</span><span class="sxs-lookup"><span data-stu-id="bcb4d-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="bcb4d-236">Se o usuário especificar uma opção GID ou UID explicitamente por meio dessa chave, o valor associado será substituído.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="bcb4d-237">Caso contrário, o valor padrão será sempre acrescentado.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="bcb4d-238">**Observação**: Essas opções são aplicadas como opções de montagem para todas as unidades montadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="bcb4d-239">Para alterar as opções somente para uma unidade específica, use/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="mount-options"></a><span data-ttu-id="bcb4d-240">Opções de montagem</span><span class="sxs-lookup"><span data-stu-id="bcb4d-240">Mount options</span></span>

<span data-ttu-id="bcb4d-241">A configuração de diferentes opções de montagem para unidades do Windows (DrvFs) pode controlar como as permissões de arquivos são calculadas para arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="bcb4d-242">As seguintes opções estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="bcb4d-242">The following options are available:</span></span>

| <span data-ttu-id="bcb4d-243">Chave</span><span class="sxs-lookup"><span data-stu-id="bcb4d-243">Key</span></span> | <span data-ttu-id="bcb4d-244">Descrição</span><span class="sxs-lookup"><span data-stu-id="bcb4d-244">Description</span></span> | <span data-ttu-id="bcb4d-245">Padrão</span><span class="sxs-lookup"><span data-stu-id="bcb4d-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="bcb4d-246">uid</span><span class="sxs-lookup"><span data-stu-id="bcb4d-246">uid</span></span>| <span data-ttu-id="bcb4d-247">A ID de usuário usada para o proprietário de todos os arquivos</span><span class="sxs-lookup"><span data-stu-id="bcb4d-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="bcb4d-248">A ID de usuário padrão de sua distribuição WSL (na primeira instalação, o padrão dela é 1000)</span><span class="sxs-lookup"><span data-stu-id="bcb4d-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="bcb4d-249">gid</span><span class="sxs-lookup"><span data-stu-id="bcb4d-249">gid</span></span>| <span data-ttu-id="bcb4d-250">A ID de grupo usada para o proprietário de todos os arquivos</span><span class="sxs-lookup"><span data-stu-id="bcb4d-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="bcb4d-251">A ID de grupo padrão de sua distribuição WSL (na primeira instalação, o padrão dela é 1000)</span><span class="sxs-lookup"><span data-stu-id="bcb4d-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="bcb4d-252">umask</span><span class="sxs-lookup"><span data-stu-id="bcb4d-252">umask</span></span> | <span data-ttu-id="bcb4d-253">Uma máscara octal de permissões a serem excluídas para todos os arquivos e diretórios</span><span class="sxs-lookup"><span data-stu-id="bcb4d-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="bcb4d-254">000</span><span class="sxs-lookup"><span data-stu-id="bcb4d-254">000</span></span>
|<span data-ttu-id="bcb4d-255">fmask</span><span class="sxs-lookup"><span data-stu-id="bcb4d-255">fmask</span></span> | <span data-ttu-id="bcb4d-256">Uma máscara octal de permissões a serem excluídas para todos os arquivos</span><span class="sxs-lookup"><span data-stu-id="bcb4d-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="bcb4d-257">000</span><span class="sxs-lookup"><span data-stu-id="bcb4d-257">000</span></span>
|<span data-ttu-id="bcb4d-258">dmask</span><span class="sxs-lookup"><span data-stu-id="bcb4d-258">dmask</span></span> | <span data-ttu-id="bcb4d-259">Uma máscara octal de permissões a serem excluídas para todos os diretórios</span><span class="sxs-lookup"><span data-stu-id="bcb4d-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="bcb4d-260">000</span><span class="sxs-lookup"><span data-stu-id="bcb4d-260">000</span></span>

<span data-ttu-id="bcb4d-261">**Observação**: as máscaras de permissão passam por uma operação OR lógica antes de serem aplicadas a arquivos ou diretórios.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-261">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="bcb4d-262">rede</span><span class="sxs-lookup"><span data-stu-id="bcb4d-262">network</span></span>

<span data-ttu-id="bcb4d-263">Rótulo da seção: `[network]`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-263">Section label: `[network]`</span></span>

| <span data-ttu-id="bcb4d-264">key</span><span class="sxs-lookup"><span data-stu-id="bcb4d-264">key</span></span> | <span data-ttu-id="bcb4d-265">value</span><span class="sxs-lookup"><span data-stu-id="bcb4d-265">value</span></span> | <span data-ttu-id="bcb4d-266">default</span><span class="sxs-lookup"><span data-stu-id="bcb4d-266">default</span></span> | <span data-ttu-id="bcb4d-267">observações</span><span class="sxs-lookup"><span data-stu-id="bcb4d-267">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="bcb4d-268">generateHosts</span><span class="sxs-lookup"><span data-stu-id="bcb4d-268">generateHosts</span></span> | <span data-ttu-id="bcb4d-269">booliano</span><span class="sxs-lookup"><span data-stu-id="bcb4d-269">boolean</span></span> | `true` | <span data-ttu-id="bcb4d-270">O `true` define o WSL para gerar `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-270">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="bcb4d-271">O arquivo `hosts` contém um mapa estático do endereço IP correspondente de nomes de host.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-271">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="bcb4d-272">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="bcb4d-272">generateResolvConf</span></span> | <span data-ttu-id="bcb4d-273">booliano</span><span class="sxs-lookup"><span data-stu-id="bcb4d-273">boolean</span></span> | `true` | <span data-ttu-id="bcb4d-274">O `true` define o WSL para gerar `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-274">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="bcb4d-275">O `resolv.conf` contém uma lista DNS que é capaz de resolver um determinado nome de host para seu endereço IP.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-275">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="bcb4d-276">interop</span><span class="sxs-lookup"><span data-stu-id="bcb4d-276">interop</span></span>

<span data-ttu-id="bcb4d-277">Rótulo da seção: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-277">Section label: `[interop]`</span></span>

<span data-ttu-id="bcb4d-278">Essas opções estão disponíveis no Insider Build 17713 e posterior.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-278">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="bcb4d-279">key</span><span class="sxs-lookup"><span data-stu-id="bcb4d-279">key</span></span> | <span data-ttu-id="bcb4d-280">value</span><span class="sxs-lookup"><span data-stu-id="bcb4d-280">value</span></span> | <span data-ttu-id="bcb4d-281">default</span><span class="sxs-lookup"><span data-stu-id="bcb4d-281">default</span></span> | <span data-ttu-id="bcb4d-282">observações</span><span class="sxs-lookup"><span data-stu-id="bcb4d-282">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="bcb4d-283">habilitado</span><span class="sxs-lookup"><span data-stu-id="bcb4d-283">enabled</span></span> | <span data-ttu-id="bcb4d-284">booliano</span><span class="sxs-lookup"><span data-stu-id="bcb4d-284">boolean</span></span> | `true` | <span data-ttu-id="bcb4d-285">Definir essa chave determinará se o WSL dará suporte à inicialização de processos do Windows.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-285">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="bcb4d-286">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="bcb4d-286">appendWindowsPath</span></span> | <span data-ttu-id="bcb4d-287">booliano</span><span class="sxs-lookup"><span data-stu-id="bcb4d-287">boolean</span></span> | `true` | <span data-ttu-id="bcb4d-288">Definir essa chave determinará se o WSL adicionará elementos de caminho do Windows à variável de ambiente $PATH.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-288">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> |

#### <a name="user"></a><span data-ttu-id="bcb4d-289">usuário</span><span class="sxs-lookup"><span data-stu-id="bcb4d-289">user</span></span>

<span data-ttu-id="bcb4d-290">Rótulo da seção: `[user]`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-290">Section label: `[user]`</span></span>

<span data-ttu-id="bcb4d-291">Essas opções estão disponíveis no Build 18980 e posterior.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-291">These options are available in Build 18980 and later.</span></span>

| <span data-ttu-id="bcb4d-292">chave</span><span class="sxs-lookup"><span data-stu-id="bcb4d-292">key</span></span> | <span data-ttu-id="bcb4d-293">value</span><span class="sxs-lookup"><span data-stu-id="bcb4d-293">value</span></span> | <span data-ttu-id="bcb4d-294">default</span><span class="sxs-lookup"><span data-stu-id="bcb4d-294">default</span></span> | <span data-ttu-id="bcb4d-295">HDInsight</span><span class="sxs-lookup"><span data-stu-id="bcb4d-295">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="bcb4d-296">default</span><span class="sxs-lookup"><span data-stu-id="bcb4d-296">default</span></span> | <span data-ttu-id="bcb4d-297">string</span><span class="sxs-lookup"><span data-stu-id="bcb4d-297">string</span></span> | <span data-ttu-id="bcb4d-298">O nome de usuário inicial criado na primeira execução</span><span class="sxs-lookup"><span data-stu-id="bcb4d-298">The initial username created on first run</span></span> | <span data-ttu-id="bcb4d-299">Definir essa chave especifica qual usuário executar como ao iniciar pela primeira vez uma sessão WSL.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-299">Setting this key specifies which user to run as when first starting a WSL session.</span></span> |

## <a name="configure-global-options-with-wslconfig"></a><span data-ttu-id="bcb4d-300">Configurar opções globais com. wslconfig</span><span class="sxs-lookup"><span data-stu-id="bcb4d-300">Configure global options with .wslconfig</span></span>

> <span data-ttu-id="bcb4d-301">**Disponível no Windows Build 19041 e posterior**</span><span class="sxs-lookup"><span data-stu-id="bcb4d-301">**Available in Windows Build 19041 and later**</span></span>

<span data-ttu-id="bcb4d-302">Você pode configurar opções de WSL globais colocando um `.wslconfig` arquivo no diretório raiz da pasta Users: `C:\Users\<yourUserName>\.wslconfig` .</span><span class="sxs-lookup"><span data-stu-id="bcb4d-302">You can configure global WSL options by placing a `.wslconfig` file into the root directory of your users folder: `C:\Users\<yourUserName>\.wslconfig`.</span></span> <span data-ttu-id="bcb4d-303">Muitos desses arquivos estão relacionados ao WSL 2, tenha em mente que talvez seja necessário executar `wsl --shutdown` para desligar a VM do WSL 2 e reiniciar sua instância do WSL para que essas alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-303">Many of these files are related to WSL 2, please keep in mind you may need to run `wsl --shutdown` to shut down the WSL 2 VM and then restart your WSL instance for these changes to take affect.</span></span>

<span data-ttu-id="bcb4d-304">Aqui está um arquivo. wslconfig de exemplo:</span><span class="sxs-lookup"><span data-stu-id="bcb4d-304">Here is a sample .wslconfig file:</span></span>

```console
[wsl2]
kernel=C:\\temp\\myCustomKernel
memory=4GB # Limits VM memory in WSL 2 to 4 GB
processors=2 # Makes the WSL 2 VM use two virtual processors
```

<span data-ttu-id="bcb4d-305">Esse arquivo pode conter as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="bcb4d-305">This file can contain the following options:</span></span>

### <a name="wsl-2-settings"></a><span data-ttu-id="bcb4d-306">Configurações do WSL 2</span><span class="sxs-lookup"><span data-stu-id="bcb4d-306">WSL 2 Settings</span></span>

<span data-ttu-id="bcb4d-307">Rótulo da seção: `[wsl2]`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-307">Section label: `[wsl2]`</span></span>

<span data-ttu-id="bcb4d-308">Essas configurações afetam a VM que alimenta qualquer distribuição WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-308">These settings affect the VM that powers any WSL 2 distribution.</span></span>

| <span data-ttu-id="bcb4d-309">chave</span><span class="sxs-lookup"><span data-stu-id="bcb4d-309">key</span></span> | <span data-ttu-id="bcb4d-310">value</span><span class="sxs-lookup"><span data-stu-id="bcb4d-310">value</span></span> | <span data-ttu-id="bcb4d-311">default</span><span class="sxs-lookup"><span data-stu-id="bcb4d-311">default</span></span> | <span data-ttu-id="bcb4d-312">HDInsight</span><span class="sxs-lookup"><span data-stu-id="bcb4d-312">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="bcb4d-313">kernel</span><span class="sxs-lookup"><span data-stu-id="bcb4d-313">kernel</span></span> | <span data-ttu-id="bcb4d-314">string</span><span class="sxs-lookup"><span data-stu-id="bcb4d-314">string</span></span> | <span data-ttu-id="bcb4d-315">A caixa de entrada fornecida pelo kernel criado pela Microsoft</span><span class="sxs-lookup"><span data-stu-id="bcb4d-315">The Microsoft built kernel provided inbox</span></span> | <span data-ttu-id="bcb4d-316">Um caminho absoluto do Windows para um kernel personalizado do Linux.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-316">An absolute Windows path to a custom Linux kernel.</span></span> |
| <span data-ttu-id="bcb4d-317">memória</span><span class="sxs-lookup"><span data-stu-id="bcb4d-317">memory</span></span> | <span data-ttu-id="bcb4d-318">tamanho</span><span class="sxs-lookup"><span data-stu-id="bcb4d-318">size</span></span> | <span data-ttu-id="bcb4d-319">80% da memória total no Windows \*</span><span class="sxs-lookup"><span data-stu-id="bcb4d-319">80% of your total memory on Windows \*</span></span> | <span data-ttu-id="bcb4d-320">A quantidade de memória a ser atribuída à VM WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-320">How much memory to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="bcb4d-321">processadores</span><span class="sxs-lookup"><span data-stu-id="bcb4d-321">processors</span></span> | <span data-ttu-id="bcb4d-322">número</span><span class="sxs-lookup"><span data-stu-id="bcb4d-322">number</span></span> | <span data-ttu-id="bcb4d-323">O mesmo número de processadores no Windows</span><span class="sxs-lookup"><span data-stu-id="bcb4d-323">The same number of processors on Windows</span></span> | <span data-ttu-id="bcb4d-324">Quantos processadores atribuir à VM WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-324">How many processors to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="bcb4d-325">localhostForwarding</span><span class="sxs-lookup"><span data-stu-id="bcb4d-325">localhostForwarding</span></span> | <span data-ttu-id="bcb4d-326">booleano</span><span class="sxs-lookup"><span data-stu-id="bcb4d-326">boolean</span></span> | `true` | <span data-ttu-id="bcb4d-327">Booliano especificando se as portas vinculadas ao curinga ou localhost na VM WSL 2 devem ser conectadas do host via localhost: Port.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-327">Boolean specifying if ports bound to wildcard or localhost in the WSL 2 VM should be connectable from the host via localhost:port.</span></span> |
| <span data-ttu-id="bcb4d-328">kernelCommandLine</span><span class="sxs-lookup"><span data-stu-id="bcb4d-328">kernelCommandLine</span></span> | <span data-ttu-id="bcb4d-329">string</span><span class="sxs-lookup"><span data-stu-id="bcb4d-329">string</span></span> | <span data-ttu-id="bcb4d-330">Em Branco</span><span class="sxs-lookup"><span data-stu-id="bcb4d-330">Blank</span></span> | <span data-ttu-id="bcb4d-331">Argumentos de linha de comando de kernel adicionais.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-331">Additional kernel command line arguments.</span></span> |
| <span data-ttu-id="bcb4d-332">swap</span><span class="sxs-lookup"><span data-stu-id="bcb4d-332">swap</span></span> | <span data-ttu-id="bcb4d-333">tamanho</span><span class="sxs-lookup"><span data-stu-id="bcb4d-333">size</span></span> | <span data-ttu-id="bcb4d-334">25% do tamanho da memória no Windows arredondado para os GB mais próximos</span><span class="sxs-lookup"><span data-stu-id="bcb4d-334">25% of memory size on Windows rounded up to the nearest GB</span></span> | <span data-ttu-id="bcb4d-335">Quanto espaço de permuta adicionar à VM WSL 2, 0 para nenhum arquivo de permuta.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-335">How much swap space to add to the WSL 2 VM, 0 for no swap file.</span></span> |
| <span data-ttu-id="bcb4d-336">Permuta</span><span class="sxs-lookup"><span data-stu-id="bcb4d-336">swapFile</span></span> | <span data-ttu-id="bcb4d-337">string</span><span class="sxs-lookup"><span data-stu-id="bcb4d-337">string</span></span> | <span data-ttu-id="bcb4d-338">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span><span class="sxs-lookup"><span data-stu-id="bcb4d-338">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span></span> | <span data-ttu-id="bcb4d-339">Um caminho absoluto do Windows para o disco rígido virtual de permuta.</span><span class="sxs-lookup"><span data-stu-id="bcb4d-339">An absolute Windows path to the swap virtual hard disk.</span></span> |

* <span data-ttu-id="bcb4d-340">Observação: esse valor é verdadeiro para a compilação 19041 do Windows e pode ser diferente no Windows Builds no programa pessoas internas</span><span class="sxs-lookup"><span data-stu-id="bcb4d-340">Note: This value is true for Windows Build 19041 and may be different in Windows builds in the Insiders program</span></span>

<span data-ttu-id="bcb4d-341">As entradas com o `path` valor devem ser caminhos do Windows com barras invertidas de escape, por exemplo:`C:\\Temp\\myCustomKernel`</span><span class="sxs-lookup"><span data-stu-id="bcb4d-341">Entries with the `path` value must be Windows paths with escaped backslashes, e.g: `C:\\Temp\\myCustomKernel`</span></span>

<span data-ttu-id="bcb4d-342">As entradas com o `size` valor devem ser um tamanho seguido por uma unidade, por exemplo, `8GB` ou `512MB` .</span><span class="sxs-lookup"><span data-stu-id="bcb4d-342">Entries with the `size` value must be a size followed by a unit, for example `8GB` or `512MB`.</span></span>
