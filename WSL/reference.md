---
title: Subsistema do Windows para referência de comando do Linux
description: Lista de comandos que gerenciam o subsistema Windows para Linux
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063574"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="e74e7-104">Referência de comandos do subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="e74e7-104">Command Reference for Windows Subsystem for Linux</span></span>

> `lxrun.exe` <span data-ttu-id="e74e7-105">é preterido a partir do Windows 10 1803 e posterior.</span><span class="sxs-lookup"><span data-stu-id="e74e7-105">is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="e74e7-106">O comando `lxrun.exe` pode ser usado para interagir com o [subsistema Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) diretamente.</span><span class="sxs-lookup"><span data-stu-id="e74e7-106">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="e74e7-107">Esses comandos são instalados no `\Windows\System32` diretório e pode ser executado dentro de um prompt de comando do Windows ou no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e74e7-107">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

* `lxrun.exe` <span data-ttu-id="e74e7-108">é usado para gerenciar o WSL.</span><span class="sxs-lookup"><span data-stu-id="e74e7-108">is used to manage WSL.</span></span>  <span data-ttu-id="e74e7-109">Esse comando pode ser usado para instalar ou desinstalar a imagem do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="e74e7-109">This command can be used to install or uninstall the Ubuntu image.</span></span>


| <span data-ttu-id="e74e7-110">Comando</span><span class="sxs-lookup"><span data-stu-id="e74e7-110">Command</span></span>                     | <span data-ttu-id="e74e7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e74e7-111">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `bash`                      | <span data-ttu-id="e74e7-112">Inicia o shell do Bash no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="e74e7-112">Launches the Bash shell in the current directory.</span></span>  <span data-ttu-id="e74e7-113">Se o shell Bash não é instalado automaticamente será executado</span><span class="sxs-lookup"><span data-stu-id="e74e7-113">If the Bash shell is not installed automatically runs</span></span> `lxrun /install` |
| `bash ~`                    | <span data-ttu-id="e74e7-114">O shell bash é iniciado no diretório base do Ubuntu do usuário.</span><span class="sxs-lookup"><span data-stu-id="e74e7-114">Launches the bash shell into the user's Ubuntu home directory.</span></span>  <span data-ttu-id="e74e7-115">Semelhante à execução de cd ~</span><span class="sxs-lookup"><span data-stu-id="e74e7-115">Similar to running cd ~</span></span>            |
| `bash -c "<command>"`       | <span data-ttu-id="e74e7-116">Executa o comando, imprime a saída e sai de volta para o prompt de comando do Windows.</span><span class="sxs-lookup"><span data-stu-id="e74e7-116">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="e74e7-117">Exemplo: **bash -c "ls"**</span><span class="sxs-lookup"><span data-stu-id="e74e7-117">Example:  **bash -c "ls"**</span></span> |

<p>

| <span data-ttu-id="e74e7-118">Comando</span><span class="sxs-lookup"><span data-stu-id="e74e7-118">Command</span></span>                     | <span data-ttu-id="e74e7-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="e74e7-119">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="e74e7-120">O comando lxrun é usado para gerenciar a instância WSL.</span><span class="sxs-lookup"><span data-stu-id="e74e7-120">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="e74e7-121">Inicia o download e o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="e74e7-121">Starts the download and install process.</span></span> <br/> <span data-ttu-id="e74e7-122">**/y** podem ser adicionados para ignorar todos os prompts.</span><span class="sxs-lookup"><span data-stu-id="e74e7-122">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="e74e7-123">O prompt de confirmação é aceito automaticamente e o usuário padrão é definido como raiz.</span><span class="sxs-lookup"><span data-stu-id="e74e7-123">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="e74e7-124">Desinstala e exclui a imagem do Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="e74e7-124">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="e74e7-125">Por padrão isso não remove o diretório base do Ubuntu do usuário.</span><span class="sxs-lookup"><span data-stu-id="e74e7-125">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="e74e7-126">**/y** podem ser adicionados ao aceitar automaticamente o prompt de confirmação</span><span class="sxs-lookup"><span data-stu-id="e74e7-126">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="e74e7-127">**completas** desinstala e exclui o diretório base do Ubuntu do usuário</span><span class="sxs-lookup"><span data-stu-id="e74e7-127">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="e74e7-128">Define o padrão do Bash no Ubuntu usuário.</span><span class="sxs-lookup"><span data-stu-id="e74e7-128">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="e74e7-129">Solicitará uma senha se o usuário especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="e74e7-129">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="e74e7-130">Para obter mais informações, visite: https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="e74e7-130">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="e74e7-131">**/y** promping ignora a senha.</span><span class="sxs-lookup"><span data-stu-id="e74e7-131">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="e74e7-132">O usuário será criado sem uma senha.</span><span class="sxs-lookup"><span data-stu-id="e74e7-132">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="e74e7-133">Atualiza o índice do pacote do subsistema</span><span class="sxs-lookup"><span data-stu-id="e74e7-133">Updates the subsystem's package index</span></span>          |
