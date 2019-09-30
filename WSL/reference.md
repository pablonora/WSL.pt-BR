---
title: Subsistema Windows para referência de comandos do Linux
description: Lista de comandos que gerenciam o Subsistema Windows para Linux
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: edd4b8216a25f519e36b8b99b626b0a4315f6039
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122746"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="eb07b-104">Referência de comandos para o Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="eb07b-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="eb07b-105">A melhor maneira de interagir com o Subsistema Windows para Linux é usar o comando `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="eb07b-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="eb07b-106">Abaixo está uma lista que contém todas as opções ao usar o `wsl.exe` da versão 1903 do Windows.</span><span class="sxs-lookup"><span data-stu-id="eb07b-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="eb07b-107">Usando: `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="eb07b-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="eb07b-108">Argumentos para executar binários do Linux</span><span class="sxs-lookup"><span data-stu-id="eb07b-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="eb07b-109">**Sem argumentos**</span><span class="sxs-lookup"><span data-stu-id="eb07b-109">**Without arguments**</span></span>

  <span data-ttu-id="eb07b-110">Se nenhuma linha de comando for fornecida, o wsl.exe iniciará o shell padrão.</span><span class="sxs-lookup"><span data-stu-id="eb07b-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="eb07b-111">**--exec, -e \<CommandLine>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="eb07b-112">Execute o comando especificado sem usar o shell do Linux padrão.</span><span class="sxs-lookup"><span data-stu-id="eb07b-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="eb07b-113">Passe a linha de comando restante do modo como ela está.</span><span class="sxs-lookup"><span data-stu-id="eb07b-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="eb07b-114">Os comandos acima também aceitam as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="eb07b-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="eb07b-115">**--distribution, -d \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="eb07b-116">Execute a distribuição especificada.</span><span class="sxs-lookup"><span data-stu-id="eb07b-116">Run the specified distribution.</span></span>

* <span data-ttu-id="eb07b-117">**--user, -u \<UserName>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="eb07b-118">Execute como o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="eb07b-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="eb07b-119">Argumentos para gerenciar o Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="eb07b-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="eb07b-120">**--export \<Distro> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="eb07b-121">Exporta a distribuição para um arquivo tar.</span><span class="sxs-lookup"><span data-stu-id="eb07b-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="eb07b-122">O nome de arquivo pode ser "-" para a saída padrão.</span><span class="sxs-lookup"><span data-stu-id="eb07b-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="eb07b-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="eb07b-124">Importa o arquivo tar especificado como uma nova distribuição.</span><span class="sxs-lookup"><span data-stu-id="eb07b-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="eb07b-125">O nome de arquivo pode ser "-" para a entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="eb07b-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="eb07b-126">**--list, -l [Options]**</span><span class="sxs-lookup"><span data-stu-id="eb07b-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="eb07b-127">Lista as distribuições.</span><span class="sxs-lookup"><span data-stu-id="eb07b-127">Lists distributions.</span></span>

  <span data-ttu-id="eb07b-128">Opções:</span><span class="sxs-lookup"><span data-stu-id="eb07b-128">Options:</span></span>
  * <span data-ttu-id="eb07b-129">**--all**</span><span class="sxs-lookup"><span data-stu-id="eb07b-129">**--all**</span></span>
      
    <span data-ttu-id="eb07b-130">Liste todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.</span><span class="sxs-lookup"><span data-stu-id="eb07b-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="eb07b-131">**--running**</span><span class="sxs-lookup"><span data-stu-id="eb07b-131">**--running**</span></span>
      
    <span data-ttu-id="eb07b-132">Liste somente as distribuições que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="eb07b-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="eb07b-133">**--set-default, -s \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="eb07b-134">Define a distribuição como o padrão.</span><span class="sxs-lookup"><span data-stu-id="eb07b-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="eb07b-135">**--terminate, -t \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="eb07b-136">Termina a distribuição especificada.</span><span class="sxs-lookup"><span data-stu-id="eb07b-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="eb07b-137">**--unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="eb07b-138">Cancela o registro da distribuição.</span><span class="sxs-lookup"><span data-stu-id="eb07b-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="eb07b-139">**--help** Exiba as informações de uso.</span><span class="sxs-lookup"><span data-stu-id="eb07b-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="eb07b-140">Comandos adicionais</span><span class="sxs-lookup"><span data-stu-id="eb07b-140">Additional Commands</span></span>

<span data-ttu-id="eb07b-141">Também há comandos históricos para interagir com o Subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="eb07b-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="eb07b-142">Sua funcionalidade é englobada no `wsl.exe`, mas ainda estão disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="eb07b-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="eb07b-143">Esse comando permite que você configure a distribuição do WSL.</span><span class="sxs-lookup"><span data-stu-id="eb07b-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="eb07b-144">Veja abaixo uma lista das opções.</span><span class="sxs-lookup"><span data-stu-id="eb07b-144">Below is a list of its options.</span></span>

<span data-ttu-id="eb07b-145">Usando: `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="eb07b-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="eb07b-146">Arguments</span><span class="sxs-lookup"><span data-stu-id="eb07b-146">Arguments</span></span>
* <span data-ttu-id="eb07b-147">**/l, /list [Options]**</span><span class="sxs-lookup"><span data-stu-id="eb07b-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="eb07b-148">Lista as distribuições registradas.</span><span class="sxs-lookup"><span data-stu-id="eb07b-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="eb07b-149">Opções:</span><span class="sxs-lookup"><span data-stu-id="eb07b-149">Options:</span></span>
    * <span data-ttu-id="eb07b-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="eb07b-150">**/all**</span></span>
    
      <span data-ttu-id="eb07b-151">Como opção, liste todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.</span><span class="sxs-lookup"><span data-stu-id="eb07b-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="eb07b-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="eb07b-152">**/running**</span></span>
      
      <span data-ttu-id="eb07b-153">Liste somente as distribuições que estão em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="eb07b-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="eb07b-154">**/s, /setdefault \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="eb07b-155">Define a distribuição como o padrão.</span><span class="sxs-lookup"><span data-stu-id="eb07b-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="eb07b-156">**/t, /terminate \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="eb07b-157">Termina a distribuição.</span><span class="sxs-lookup"><span data-stu-id="eb07b-157">Terminates the distribution.</span></span>

* <span data-ttu-id="eb07b-158">**/u, /unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="eb07b-159">Cancela o registro da distribuição.</span><span class="sxs-lookup"><span data-stu-id="eb07b-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="eb07b-160">**/upgrade \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="eb07b-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="eb07b-161">Atualiza a distribuição para o formato do sistema de arquivos WslFs.</span><span class="sxs-lookup"><span data-stu-id="eb07b-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="eb07b-162">Esse comando é usado para iniciar um shell Bash.</span><span class="sxs-lookup"><span data-stu-id="eb07b-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="eb07b-163">Abaixo estão as opções que você pode usar com este comando.</span><span class="sxs-lookup"><span data-stu-id="eb07b-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="eb07b-164">Usando: `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="eb07b-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="eb07b-165">**Nenhuma opção fornecida**</span><span class="sxs-lookup"><span data-stu-id="eb07b-165">**No Option given**</span></span>
  
  <span data-ttu-id="eb07b-166">Inicia o shell Bash no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="eb07b-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="eb07b-167">Se o shell Bash não estiver instalado automaticamente, ele executará o `lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="eb07b-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="eb07b-168">`bash ~` inicia o shell Bash no diretório base do usuário.</span><span class="sxs-lookup"><span data-stu-id="eb07b-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="eb07b-169">Semelhante à execução de `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="eb07b-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="eb07b-170">**-c "\<command>"**</span><span class="sxs-lookup"><span data-stu-id="eb07b-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="eb07b-171">Executa o comando, imprime a saída e sai de volta para o prompt de comando do Windows.</span><span class="sxs-lookup"><span data-stu-id="eb07b-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="eb07b-172">Exemplo: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="eb07b-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="eb07b-173">Comandos preteridos</span><span class="sxs-lookup"><span data-stu-id="eb07b-173">Deprecated Commands</span></span>

<span data-ttu-id="eb07b-174">O `lxrun.exe` foi o primeiro comando usado para instalar e gerenciar o Subsistema Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="eb07b-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="eb07b-175">Ele foi preterido no Windows 10 1803 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="eb07b-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="eb07b-176">O comando `lxrun.exe` pode ser usado para interagir diretamente com o [WSL (Subsistema Windows para Linux)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-).</span><span class="sxs-lookup"><span data-stu-id="eb07b-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="eb07b-177">Esses comandos são instalados no diretório `\Windows\System32` e podem ser executados em um prompt de comando do Windows ou no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eb07b-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="eb07b-178">Comando</span><span class="sxs-lookup"><span data-stu-id="eb07b-178">Command</span></span>                     | <span data-ttu-id="eb07b-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb07b-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="eb07b-180">O comando lxrun é usado para gerenciar a instância do WSL.</span><span class="sxs-lookup"><span data-stu-id="eb07b-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="eb07b-181">Inicia o processo de download e instalação.</span><span class="sxs-lookup"><span data-stu-id="eb07b-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="eb07b-182">**/y** pode ser adicionado para ignorar todos os prompts.</span><span class="sxs-lookup"><span data-stu-id="eb07b-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="eb07b-183">O prompt de confirmação é automaticamente aceito e o usuário padrão é definido como raiz.</span><span class="sxs-lookup"><span data-stu-id="eb07b-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="eb07b-184">Desinstala e exclui a imagem do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="eb07b-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="eb07b-185">Por padrão, isso não remove o diretório base do Ubuntu do usuário.</span><span class="sxs-lookup"><span data-stu-id="eb07b-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="eb07b-186">**/y** pode ser adicionado para aceitar automaticamente o prompt de confirmação</span><span class="sxs-lookup"><span data-stu-id="eb07b-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="eb07b-187">**/full** desinstala e exclui o diretório base do Ubuntu do usuário</span><span class="sxs-lookup"><span data-stu-id="eb07b-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="eb07b-188">Define o Bash padrão no usuário do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="eb07b-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="eb07b-189">Solicitará uma senha se o usuário especificado não existir.</span><span class="sxs-lookup"><span data-stu-id="eb07b-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="eb07b-190">Para obter mais informações, confira https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="eb07b-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="eb07b-191">**/y** ignora a solicitação de senha.</span><span class="sxs-lookup"><span data-stu-id="eb07b-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="eb07b-192">O usuário será criado sem uma senha.</span><span class="sxs-lookup"><span data-stu-id="eb07b-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="eb07b-193">Atualiza o índice do pacote do subsistema</span><span class="sxs-lookup"><span data-stu-id="eb07b-193">Updates the subsystem's package index</span></span>          |
