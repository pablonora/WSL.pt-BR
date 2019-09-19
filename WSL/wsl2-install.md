---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: bced0fd0bf948842b8c465f645aa5c368c2f4335
ms.sourcegitcommit: ebc6ae7e7546a6d33644e68788fa0215028859b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/17/2019
ms.locfileid: "71070308"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="f76cf-104">Instruções de instalação do WSL 2</span><span class="sxs-lookup"><span data-stu-id="f76cf-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="f76cf-105">Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="f76cf-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="f76cf-106">Verifique se você tem o WSL instalado (você pode encontrar instruções para fazer isso [aqui](./install-win10.md)) e se está executando o Windows 10 Build 18917 ou superior</span><span class="sxs-lookup"><span data-stu-id="f76cf-106">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 build 18917 or higher</span></span>
   - <span data-ttu-id="f76cf-107">Para verificar se você está usando o Build 18917 ou superior, ingresse [no programa Windows Insider](https://insider.windows.com/en-us/) e selecione o anel "rápido".</span><span class="sxs-lookup"><span data-stu-id="f76cf-107">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="f76cf-108">Você pode verificar a versão do Windows abrindo o prompt de comando e `ver` executando o comando.</span><span class="sxs-lookup"><span data-stu-id="f76cf-108">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="f76cf-109">Habilite o componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="f76cf-109">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="f76cf-110">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="f76cf-110">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="f76cf-111">Verifique quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="f76cf-111">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="f76cf-112">Habilite o componente opcional ' plataforma de máquina virtual ' e verifique se o WSL está habilitado</span><span class="sxs-lookup"><span data-stu-id="f76cf-112">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="f76cf-113">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="f76cf-113">Open PowerShell as an Administrator and run:</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="f76cf-114">Isso garantirá que os componentes opcionais da plataforma de máquina virtual e do subsistema do Windows para Linux estejam instalados.</span><span class="sxs-lookup"><span data-stu-id="f76cf-114">This will make sure that both the Virtual Machine Platform and Windows Subsystem for Linux optional components are installed.</span></span> <span data-ttu-id="f76cf-115">Depois de executar esses comandos, você precisará reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="f76cf-115">After you've run these commands you'll need to restart your computer.</span></span> 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="f76cf-116">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="f76cf-116">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="f76cf-117">No PowerShell, execute:</span><span class="sxs-lookup"><span data-stu-id="f76cf-117">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="f76cf-118">e substitua `<Distro>` pelo nome real da sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="f76cf-118">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="f76cf-119">(Você pode encontrá-lo com o comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="f76cf-119">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="f76cf-120">Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.</span><span class="sxs-lookup"><span data-stu-id="f76cf-120">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="f76cf-121">Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:</span><span class="sxs-lookup"><span data-stu-id="f76cf-121">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="f76cf-122">Isso fará com que qualquer nova distribuição instalada seja inicializada como uma distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f76cf-122">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="f76cf-123">Termine verificando quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="f76cf-123">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="f76cf-124">Para verificar quais versões do WSL cada distribuição está usando, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f76cf-124">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="f76cf-125">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="f76cf-125">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="f76cf-126">A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão".</span><span class="sxs-lookup"><span data-stu-id="f76cf-126">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="f76cf-127">Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f76cf-127">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="f76cf-128">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="f76cf-128">Troubleshooting:</span></span> 

<span data-ttu-id="f76cf-129">Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f76cf-129">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="f76cf-130">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="f76cf-130">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="f76cf-131">**Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="f76cf-131">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="f76cf-132">Verifique se a virtualização está habilitada dentro do BIOS do seu computador.</span><span class="sxs-lookup"><span data-stu-id="f76cf-132">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="f76cf-133">As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.</span><span class="sxs-lookup"><span data-stu-id="f76cf-133">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="f76cf-134">**Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="f76cf-134">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="f76cf-135">Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="f76cf-135">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="f76cf-136">Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="f76cf-136">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="f76cf-137">Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="f76cf-137">You can find the full WSL install instructions [here](./install-win10.md).</span></span>