---
title: Referência de comando do subsistema do Windows para Linux
description: Lista de comandos que gerenciam o subsistema do Windows para Linux
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307651"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="98319-104">Referência de comando para o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="98319-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="98319-105">A melhor maneira de interagir com o subsistema do Windows para Linux é usar o `wsl.exe` comando.</span><span class="sxs-lookup"><span data-stu-id="98319-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 

## `wsl.exe` 

<span data-ttu-id="98319-106">Abaixo está uma lista que contém todas as opções `wsl.exe` ao usar o da versão 1903 do Windows.</span><span class="sxs-lookup"><span data-stu-id="98319-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

* <span data-ttu-id="98319-107">Argumentos para executar binários do Linux:</span><span class="sxs-lookup"><span data-stu-id="98319-107">Arguments for running Linux binaries:</span></span>

    * <span data-ttu-id="98319-108">Se nenhuma linha de comando for fornecida, o WSL. exe iniciará o shell padrão.</span><span class="sxs-lookup"><span data-stu-id="98319-108">If no command line is provided, wsl.exe launches the default shell.</span></span>

    * <span data-ttu-id="98319-109">--Exec,-e<CommandLine></span><span class="sxs-lookup"><span data-stu-id="98319-109">--exec, -e <CommandLine></span></span>
        * <span data-ttu-id="98319-110">Execute o comando especificado sem usar o Shell do Linux padrão.</span><span class="sxs-lookup"><span data-stu-id="98319-110">Execute the specified command without using the default Linux shell.</span></span>

    * --
        * <span data-ttu-id="98319-111">Passe a linha de comando restante como está.</span><span class="sxs-lookup"><span data-stu-id="98319-111">Pass the remaining command line as is.</span></span>

* <span data-ttu-id="98319-112">Opções:</span><span class="sxs-lookup"><span data-stu-id="98319-112">Options:</span></span>
    * <span data-ttu-id="98319-113">--Distribution,-d<Distro></span><span class="sxs-lookup"><span data-stu-id="98319-113">--distribution, -d <Distro></span></span>
        * <span data-ttu-id="98319-114">Execute a distribuição especificada.</span><span class="sxs-lookup"><span data-stu-id="98319-114">Run the specified distribution.</span></span>

    * <span data-ttu-id="98319-115">--usuário,-u<UserName></span><span class="sxs-lookup"><span data-stu-id="98319-115">--user, -u <UserName></span></span>
        * <span data-ttu-id="98319-116">Executar como o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="98319-116">Run as the specified user.</span></span>

* <span data-ttu-id="98319-117">Argumentos para gerenciar o subsistema do Windows para Linux:</span><span class="sxs-lookup"><span data-stu-id="98319-117">Arguments for managing Windows Subsystem for Linux:</span></span>

    * <span data-ttu-id="98319-118">--exportar <Distro><FileName></span><span class="sxs-lookup"><span data-stu-id="98319-118">--export <Distro> <FileName></span></span>
        * <span data-ttu-id="98319-119">Exporta a distribuição para um arquivo tar.</span><span class="sxs-lookup"><span data-stu-id="98319-119">Exports the distribution to a tar file.</span></span>
        <span data-ttu-id="98319-120">O nome de arquivo pode ser-para saída padrão.</span><span class="sxs-lookup"><span data-stu-id="98319-120">The filename can be - for standard output.</span></span>

    * <span data-ttu-id="98319-121">--Import <Distro> <InstallLocation>[opções <FileName> ]</span><span class="sxs-lookup"><span data-stu-id="98319-121">--import <Distro> <InstallLocation> <FileName> [Options]</span></span>
        * <span data-ttu-id="98319-122">Importa o arquivo tar especificado como uma nova distribuição.</span><span class="sxs-lookup"><span data-stu-id="98319-122">Imports the specified tar file as a new distribution.</span></span>
        <span data-ttu-id="98319-123">O nome de arquivo pode ser-para entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="98319-123">The filename can be - for standard input.</span></span>

        * <span data-ttu-id="98319-124">Opções:</span><span class="sxs-lookup"><span data-stu-id="98319-124">Options:</span></span>
            * <span data-ttu-id="98319-125">--Version <Version> especifica a versão a ser usada para a nova distribuição.</span><span class="sxs-lookup"><span data-stu-id="98319-125">--version <Version> Specifies the version to use for the new distribution.</span></span>

    * <span data-ttu-id="98319-126">--List,-l [opções]</span><span class="sxs-lookup"><span data-stu-id="98319-126">--list, -l [Options]</span></span>
        * <span data-ttu-id="98319-127">Lista distribuições.</span><span class="sxs-lookup"><span data-stu-id="98319-127">Lists distributions.</span></span>

        * <span data-ttu-id="98319-128">Opções:</span><span class="sxs-lookup"><span data-stu-id="98319-128">Options:</span></span>
            * <span data-ttu-id="98319-129">--todos</span><span class="sxs-lookup"><span data-stu-id="98319-129">--all</span></span>
                * <span data-ttu-id="98319-130">Listar todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.</span><span class="sxs-lookup"><span data-stu-id="98319-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

            * <span data-ttu-id="98319-131">--executando</span><span class="sxs-lookup"><span data-stu-id="98319-131">--running</span></span>
                * <span data-ttu-id="98319-132">Lista somente as distribuições que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="98319-132">List only distributions that are currently running.</span></span>

    * <span data-ttu-id="98319-133">--Set-Default,-s<Distro></span><span class="sxs-lookup"><span data-stu-id="98319-133">--set-default, -s <Distro></span></span>
        * <span data-ttu-id="98319-134">Define a distribuição como o padrão.</span><span class="sxs-lookup"><span data-stu-id="98319-134">Sets the distribution as the default.</span></span>

    * <span data-ttu-id="98319-135">--Set-padrão-versão<Version></span><span class="sxs-lookup"><span data-stu-id="98319-135">--set-default-version <Version></span></span>
        * <span data-ttu-id="98319-136">Altera a versão de instalação padrão para novas distribuições.</span><span class="sxs-lookup"><span data-stu-id="98319-136">Changes the default install version for new distributions.</span></span>

    * <span data-ttu-id="98319-137">--Set-Version <Distro><Version></span><span class="sxs-lookup"><span data-stu-id="98319-137">--set-version <Distro> <Version></span></span>
        * <span data-ttu-id="98319-138">Altera a versão da distribuição especificada.</span><span class="sxs-lookup"><span data-stu-id="98319-138">Changes the version of the specified distribution.</span></span>

    * <span data-ttu-id="98319-139">--Terminate,-t<Distro></span><span class="sxs-lookup"><span data-stu-id="98319-139">--terminate, -t <Distro></span></span>
        * <span data-ttu-id="98319-140">Encerra a distribuição especificada.</span><span class="sxs-lookup"><span data-stu-id="98319-140">Terminates the specified distribution.</span></span>

    * <span data-ttu-id="98319-141">--cancelar registro<Distro></span><span class="sxs-lookup"><span data-stu-id="98319-141">--unregister <Distro></span></span>
        * <span data-ttu-id="98319-142">Cancela o registro da distribuição.</span><span class="sxs-lookup"><span data-stu-id="98319-142">Unregisters the distribution.</span></span>

    * <span data-ttu-id="98319-143">--help</span><span class="sxs-lookup"><span data-stu-id="98319-143">--help</span></span>
        * <span data-ttu-id="98319-144">Exibir informações de uso.</span><span class="sxs-lookup"><span data-stu-id="98319-144">Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="98319-145">Comandos adicionais</span><span class="sxs-lookup"><span data-stu-id="98319-145">Additional Commands</span></span>

<span data-ttu-id="98319-146">Também há comandos históricos para interagir com o subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="98319-146">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="98319-147">Sua funcionalidade é englobada no `wsl.exe`, mas ainda estão disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="98319-147">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="98319-148">Esse comando permite que você configure a distribuição do WSL.</span><span class="sxs-lookup"><span data-stu-id="98319-148">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="98319-149">Abaixo está uma lista de suas opções.</span><span class="sxs-lookup"><span data-stu-id="98319-149">Below is a list of its options.</span></span>

* <span data-ttu-id="98319-150">/l,/List [opção]</span><span class="sxs-lookup"><span data-stu-id="98319-150">/l, /list [Option]</span></span>
    * <span data-ttu-id="98319-151">Lista as distribuições registradas.</span><span class="sxs-lookup"><span data-stu-id="98319-151">Lists registered distributions.</span></span>
        * <span data-ttu-id="98319-152">/All – opcionalmente, liste todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.</span><span class="sxs-lookup"><span data-stu-id="98319-152">/all - Optionally list all distributions, including distributions that       are currently being installed or uninstalled.</span></span>

        * <span data-ttu-id="98319-153">/Running-lista somente as distribuições que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="98319-153">/running - List only distributions that are currently running.</span></span>

* <span data-ttu-id="98319-154">/s,/SetDefault<DistributionName></span><span class="sxs-lookup"><span data-stu-id="98319-154">/s, /setdefault <DistributionName></span></span>
    * <span data-ttu-id="98319-155">Define a distribuição como o padrão.</span><span class="sxs-lookup"><span data-stu-id="98319-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="98319-156">/t,/Terminate<DistributionName></span><span class="sxs-lookup"><span data-stu-id="98319-156">/t, /terminate <DistributionName></span></span>
    * <span data-ttu-id="98319-157">Encerra a distribuição.</span><span class="sxs-lookup"><span data-stu-id="98319-157">Terminates the distribution.</span></span>

* <span data-ttu-id="98319-158">/u,/Unregister<DistributionName></span><span class="sxs-lookup"><span data-stu-id="98319-158">/u, /unregister <DistributionName></span></span>
    * <span data-ttu-id="98319-159">Cancela o registro da distribuição.</span><span class="sxs-lookup"><span data-stu-id="98319-159">Unregisters the distribution.</span></span>

### `bash.exe`

<span data-ttu-id="98319-160">Esse comando é usado para iniciar um shell bash.</span><span class="sxs-lookup"><span data-stu-id="98319-160">This command is used to start a bash shell.</span></span> <span data-ttu-id="98319-161">Abaixo estão as opções que você pode usar com este comando.</span><span class="sxs-lookup"><span data-stu-id="98319-161">Below are the options you can use with this command.</span></span>

* <span data-ttu-id="98319-162">Nenhuma opção fornecida</span><span class="sxs-lookup"><span data-stu-id="98319-162">No Option given</span></span>
    * <span data-ttu-id="98319-163">Inicia o shell bash no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="98319-163">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="98319-164">Se o shell bash não for instalado automaticamente`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="98319-164">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* <span data-ttu-id="98319-165">bash ~</span><span class="sxs-lookup"><span data-stu-id="98319-165">bash ~</span></span>
    * <span data-ttu-id="98319-166">Inicia o shell bash no diretório base do usuário.</span><span class="sxs-lookup"><span data-stu-id="98319-166">Launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="98319-167">Semelhante à execução `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="98319-167">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="98319-168">bash-c "&lt;comando&gt;"</span><span class="sxs-lookup"><span data-stu-id="98319-168">bash -c "&lt;command&gt;"</span></span>
    * <span data-ttu-id="98319-169">Executa o comando, imprime a saída e sai de volta para o prompt de comando do Windows.</span><span class="sxs-lookup"><span data-stu-id="98319-169">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="98319-170">Exemplo`bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="98319-170">Example:  `bash -c "ls"`</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="98319-171">Comandos preteridos</span><span class="sxs-lookup"><span data-stu-id="98319-171">Deprecated Commands</span></span>

<span data-ttu-id="98319-172">O `lxrun.exe` foi o primeiro comando usado para instalar e gerenciar o subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="98319-172">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="98319-173">Ele foi preterido a partir do Windows 10 1803 e posterior.</span><span class="sxs-lookup"><span data-stu-id="98319-173">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="98319-174">O comando `lxrun.exe` pode ser usado para interagir diretamente com o subsistema do [Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .</span><span class="sxs-lookup"><span data-stu-id="98319-174">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="98319-175">Esses comandos são instalados no `\Windows\System32` diretório e podem ser executados em um prompt de comando do Windows ou no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="98319-175">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="98319-176">Comando</span><span class="sxs-lookup"><span data-stu-id="98319-176">Command</span></span>                     | <span data-ttu-id="98319-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="98319-177">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="98319-178">O comando lxrun é usado para gerenciar a instância WSL.</span><span class="sxs-lookup"><span data-stu-id="98319-178">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="98319-179">Inicia o processo de download e instalação.</span><span class="sxs-lookup"><span data-stu-id="98319-179">Starts the download and install process.</span></span> <br/> <span data-ttu-id="98319-180">**/y** pode ser adicionado para ignorar todos os prompts.</span><span class="sxs-lookup"><span data-stu-id="98319-180">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="98319-181">O prompt de confirmação é automaticamente aceito e o usuário padrão é definido como raiz.</span><span class="sxs-lookup"><span data-stu-id="98319-181">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="98319-182">Desinstala e exclui a imagem do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="98319-182">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="98319-183">Por padrão, isso não remove o diretório inicial do Ubuntu do usuário.</span><span class="sxs-lookup"><span data-stu-id="98319-183">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="98319-184">**/y** pode ser adicionado para aceitar automaticamente o prompt de confirmação</span><span class="sxs-lookup"><span data-stu-id="98319-184">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="98319-185">**/Full** desinstala e exclui o diretório inicial do Ubuntu do usuário</span><span class="sxs-lookup"><span data-stu-id="98319-185">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="98319-186">Define o bash padrão no usuário do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="98319-186">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="98319-187">Solicitará uma senha se o usuário especificado não existir.</span><span class="sxs-lookup"><span data-stu-id="98319-187">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="98319-188">Para obter mais informações, https://aka.ms/wslusers visite:.</span><span class="sxs-lookup"><span data-stu-id="98319-188">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="98319-189">**/y** Ignora promping para a senha.</span><span class="sxs-lookup"><span data-stu-id="98319-189">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="98319-190">O usuário será criado sem uma senha.</span><span class="sxs-lookup"><span data-stu-id="98319-190">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="98319-191">Atualiza o índice do pacote do subsistema</span><span class="sxs-lookup"><span data-stu-id="98319-191">Updates the subsystem's package index</span></span>          |
