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
ms.localizationpriority: high
ms.openlocfilehash: edd4b8216a25f519e36b8b99b626b0a4315f6039
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122746"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="20416-104">Referência de comando para o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="20416-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="20416-105">A melhor maneira de interagir com o subsistema do Windows para Linux é usar o `wsl.exe` comando.</span><span class="sxs-lookup"><span data-stu-id="20416-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="20416-106">Abaixo está uma lista que contém todas as opções `wsl.exe` ao usar o da versão 1903 do Windows.</span><span class="sxs-lookup"><span data-stu-id="20416-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="20416-107">Usando`wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="20416-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="20416-108">Argumentos para executar binários do Linux</span><span class="sxs-lookup"><span data-stu-id="20416-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="20416-109">**Sem argumentos**</span><span class="sxs-lookup"><span data-stu-id="20416-109">**Without arguments**</span></span>

  <span data-ttu-id="20416-110">Se nenhuma linha de comando for fornecida, o WSL. exe iniciará o shell padrão.</span><span class="sxs-lookup"><span data-stu-id="20416-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="20416-111">**--Exec,-e \<linha de comando >**</span><span class="sxs-lookup"><span data-stu-id="20416-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="20416-112">Execute o comando especificado sem usar o Shell do Linux padrão.</span><span class="sxs-lookup"><span data-stu-id="20416-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="20416-113">Passe a linha de comando restante como está.</span><span class="sxs-lookup"><span data-stu-id="20416-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="20416-114">Os comandos acima também aceitam as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="20416-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="20416-115">**--Distribution,-d \<distribuição >**</span><span class="sxs-lookup"><span data-stu-id="20416-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="20416-116">Execute a distribuição especificada.</span><span class="sxs-lookup"><span data-stu-id="20416-116">Run the specified distribution.</span></span>

* <span data-ttu-id="20416-117">**--User,-u \<nome de usuário >**</span><span class="sxs-lookup"><span data-stu-id="20416-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="20416-118">Executar como o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="20416-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="20416-119">Argumentos para gerenciar o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="20416-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="20416-120">**--exportar \<distribuição > \<nome do arquivo >**</span><span class="sxs-lookup"><span data-stu-id="20416-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="20416-121">Exporta a distribuição para um arquivo tar.</span><span class="sxs-lookup"><span data-stu-id="20416-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="20416-122">O nome de arquivo pode ser-para saída padrão.</span><span class="sxs-lookup"><span data-stu-id="20416-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="20416-123">**--Import \<distribuição > \<InstallLocation > \<filename >**</span><span class="sxs-lookup"><span data-stu-id="20416-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="20416-124">Importa o arquivo tar especificado como uma nova distribuição.</span><span class="sxs-lookup"><span data-stu-id="20416-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="20416-125">O nome de arquivo pode ser-para entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="20416-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="20416-126">**--List,-l [opções]**</span><span class="sxs-lookup"><span data-stu-id="20416-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="20416-127">Lista distribuições.</span><span class="sxs-lookup"><span data-stu-id="20416-127">Lists distributions.</span></span>

  <span data-ttu-id="20416-128">Opções:</span><span class="sxs-lookup"><span data-stu-id="20416-128">Options:</span></span>
  * <span data-ttu-id="20416-129">**--todos**</span><span class="sxs-lookup"><span data-stu-id="20416-129">**--all**</span></span>
      
    <span data-ttu-id="20416-130">Listar todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.</span><span class="sxs-lookup"><span data-stu-id="20416-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="20416-131">**--executando**</span><span class="sxs-lookup"><span data-stu-id="20416-131">**--running**</span></span>
      
    <span data-ttu-id="20416-132">Lista somente as distribuições que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="20416-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="20416-133">**--Set-Default,-s \<distribuição >**</span><span class="sxs-lookup"><span data-stu-id="20416-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="20416-134">Define a distribuição como o padrão.</span><span class="sxs-lookup"><span data-stu-id="20416-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="20416-135">**--Terminate,-t \<distribuição >**</span><span class="sxs-lookup"><span data-stu-id="20416-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="20416-136">Encerra a distribuição especificada.</span><span class="sxs-lookup"><span data-stu-id="20416-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="20416-137">**--cancelar registro \<de distribuição >**</span><span class="sxs-lookup"><span data-stu-id="20416-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="20416-138">Cancela o registro da distribuição.</span><span class="sxs-lookup"><span data-stu-id="20416-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="20416-139">**--ajuda** Exibir informações de uso.</span><span class="sxs-lookup"><span data-stu-id="20416-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="20416-140">Comandos adicionais</span><span class="sxs-lookup"><span data-stu-id="20416-140">Additional Commands</span></span>

<span data-ttu-id="20416-141">Também há comandos históricos para interagir com o subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="20416-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="20416-142">Sua funcionalidade é englobada no `wsl.exe`, mas ainda estão disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="20416-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="20416-143">Esse comando permite que você configure a distribuição do WSL.</span><span class="sxs-lookup"><span data-stu-id="20416-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="20416-144">Abaixo está uma lista de suas opções.</span><span class="sxs-lookup"><span data-stu-id="20416-144">Below is a list of its options.</span></span>

<span data-ttu-id="20416-145">Usando`wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="20416-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="20416-146">Argumentos</span><span class="sxs-lookup"><span data-stu-id="20416-146">Arguments</span></span>
* <span data-ttu-id="20416-147">**/l,/List [opções]**</span><span class="sxs-lookup"><span data-stu-id="20416-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="20416-148">Lista as distribuições registradas.</span><span class="sxs-lookup"><span data-stu-id="20416-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="20416-149">Opções:</span><span class="sxs-lookup"><span data-stu-id="20416-149">Options:</span></span>
    * <span data-ttu-id="20416-150">**/All**</span><span class="sxs-lookup"><span data-stu-id="20416-150">**/all**</span></span>
    
      <span data-ttu-id="20416-151">Opcionalmente, liste todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.</span><span class="sxs-lookup"><span data-stu-id="20416-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="20416-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="20416-152">**/running**</span></span>
      
      <span data-ttu-id="20416-153">Lista somente as distribuições que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="20416-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="20416-154">**/s,/SetDefault \<distribuição >**</span><span class="sxs-lookup"><span data-stu-id="20416-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="20416-155">Define a distribuição como o padrão.</span><span class="sxs-lookup"><span data-stu-id="20416-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="20416-156">**/t,/Terminate \<distribuição >**</span><span class="sxs-lookup"><span data-stu-id="20416-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="20416-157">Encerra a distribuição.</span><span class="sxs-lookup"><span data-stu-id="20416-157">Terminates the distribution.</span></span>

* <span data-ttu-id="20416-158">**/u,/Unregister \<distribuição >**</span><span class="sxs-lookup"><span data-stu-id="20416-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="20416-159">Cancela o registro da distribuição.</span><span class="sxs-lookup"><span data-stu-id="20416-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="20416-160">**> \</upgrade distribuição**</span><span class="sxs-lookup"><span data-stu-id="20416-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="20416-161">Atualiza a distribuição para o formato do sistema de arquivos WslFs.</span><span class="sxs-lookup"><span data-stu-id="20416-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="20416-162">Esse comando é usado para iniciar um shell bash.</span><span class="sxs-lookup"><span data-stu-id="20416-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="20416-163">Abaixo estão as opções que você pode usar com este comando.</span><span class="sxs-lookup"><span data-stu-id="20416-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="20416-164">Usando`bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="20416-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="20416-165">**Nenhuma opção fornecida**</span><span class="sxs-lookup"><span data-stu-id="20416-165">**No Option given**</span></span>
  
  <span data-ttu-id="20416-166">Inicia o shell bash no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="20416-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="20416-167">Se o shell bash não for instalado automaticamente`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="20416-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="20416-168">`bash ~`inicia o shell bash no diretório base do usuário.</span><span class="sxs-lookup"><span data-stu-id="20416-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="20416-169">Semelhante à execução `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="20416-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="20416-170">**-c "\<> de comando"**</span><span class="sxs-lookup"><span data-stu-id="20416-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="20416-171">Executa o comando, imprime a saída e sai de volta para o prompt de comando do Windows.</span><span class="sxs-lookup"><span data-stu-id="20416-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="20416-172">Exemplo: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="20416-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="20416-173">Comandos preteridos</span><span class="sxs-lookup"><span data-stu-id="20416-173">Deprecated Commands</span></span>

<span data-ttu-id="20416-174">O `lxrun.exe` foi o primeiro comando usado para instalar e gerenciar o subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="20416-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="20416-175">Ele foi preterido a partir do Windows 10 1803 e posterior.</span><span class="sxs-lookup"><span data-stu-id="20416-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="20416-176">O comando `lxrun.exe` pode ser usado para interagir diretamente com o subsistema do [Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .</span><span class="sxs-lookup"><span data-stu-id="20416-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="20416-177">Esses comandos são instalados no `\Windows\System32` diretório e podem ser executados em um prompt de comando do Windows ou no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="20416-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="20416-178">Comando</span><span class="sxs-lookup"><span data-stu-id="20416-178">Command</span></span>                     | <span data-ttu-id="20416-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="20416-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="20416-180">O comando lxrun é usado para gerenciar a instância WSL.</span><span class="sxs-lookup"><span data-stu-id="20416-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="20416-181">Inicia o processo de download e instalação.</span><span class="sxs-lookup"><span data-stu-id="20416-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="20416-182">**/y** pode ser adicionado para ignorar todos os prompts.</span><span class="sxs-lookup"><span data-stu-id="20416-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="20416-183">O prompt de confirmação é automaticamente aceito e o usuário padrão é definido como raiz.</span><span class="sxs-lookup"><span data-stu-id="20416-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="20416-184">Desinstala e exclui a imagem do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="20416-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="20416-185">Por padrão, isso não remove o diretório inicial do Ubuntu do usuário.</span><span class="sxs-lookup"><span data-stu-id="20416-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="20416-186">**/y** pode ser adicionado para aceitar automaticamente o prompt de confirmação</span><span class="sxs-lookup"><span data-stu-id="20416-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="20416-187">**/Full** desinstala e exclui o diretório inicial do Ubuntu do usuário</span><span class="sxs-lookup"><span data-stu-id="20416-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="20416-188">Define o bash padrão no usuário do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="20416-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="20416-189">Solicitará uma senha se o usuário especificado não existir.</span><span class="sxs-lookup"><span data-stu-id="20416-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="20416-190">Para obter mais informações, https://aka.ms/wslusers visite:.</span><span class="sxs-lookup"><span data-stu-id="20416-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="20416-191">**/y** Ignora promping para a senha.</span><span class="sxs-lookup"><span data-stu-id="20416-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="20416-192">O usuário será criado sem uma senha.</span><span class="sxs-lookup"><span data-stu-id="20416-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="20416-193">Atualiza o índice do pacote do subsistema</span><span class="sxs-lookup"><span data-stu-id="20416-193">Updates the subsystem's package index</span></span>          |
