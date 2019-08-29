---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 6b7ed18480ea88200d00b67a3a6dc859947397db
ms.sourcegitcommit: 6f10b40f6199538c8eedf6301f02b7d70ead3fe7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70117837"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="66542-104">Instruções de instalação do WSL 2</span><span class="sxs-lookup"><span data-stu-id="66542-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="66542-105">Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="66542-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="66542-106">Verifique se você tem o WSL instalado (você pode encontrar instruções para fazer isso [aqui](./install-win10.md)) e se está executando o Windows 10 Build 18917 ou superior</span><span class="sxs-lookup"><span data-stu-id="66542-106">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 build 18917 or higher</span></span>
   - <span data-ttu-id="66542-107">Para verificar se você está usando o Build 18917 ou superior, ingresse [no programa Windows](https://insider.windows.com/en-us/) Insider e selecione o anel "rápido".</span><span class="sxs-lookup"><span data-stu-id="66542-107">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="66542-108">Você pode verificar a versão do Windows abrindo o prompt de comando e `ver` executando o comando.</span><span class="sxs-lookup"><span data-stu-id="66542-108">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="66542-109">Habilite o componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="66542-109">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="66542-110">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="66542-110">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="66542-111">Verifique quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="66542-111">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="66542-112">Habilite o componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="66542-112">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="66542-113">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="66542-113">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="66542-114">Depois que essas alterações forem habilitadas, você precisará reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="66542-114">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="66542-115">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="66542-115">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="66542-116">No PowerShell, execute:</span><span class="sxs-lookup"><span data-stu-id="66542-116">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="66542-117">e substitua `<Distro>` pelo nome real da sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="66542-117">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="66542-118">(Você pode encontrá-lo com o comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="66542-118">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="66542-119">Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.</span><span class="sxs-lookup"><span data-stu-id="66542-119">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="66542-120">Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:</span><span class="sxs-lookup"><span data-stu-id="66542-120">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="66542-121">Isso fará com que qualquer nova distribuição instalada seja inicializada como uma distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="66542-121">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="66542-122">Termine verificando quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="66542-122">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="66542-123">Para verificar quais versões do WSL cada distribuição está usando, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="66542-123">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="66542-124">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="66542-124">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="66542-125">A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão".</span><span class="sxs-lookup"><span data-stu-id="66542-125">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="66542-126">Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="66542-126">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="66542-127">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="66542-127">Troubleshooting:</span></span> 

<span data-ttu-id="66542-128">Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="66542-128">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="66542-129">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="66542-129">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="66542-130">**Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="66542-130">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="66542-131">Verifique se a virtualização está habilitada dentro do BIOS do seu computador.</span><span class="sxs-lookup"><span data-stu-id="66542-131">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="66542-132">As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.</span><span class="sxs-lookup"><span data-stu-id="66542-132">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="66542-133">**Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="66542-133">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="66542-134">Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="66542-134">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="66542-135">Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="66542-135">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="66542-136">Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="66542-136">You can find the full WSL install instructions [here](./install-win10.md).</span></span>