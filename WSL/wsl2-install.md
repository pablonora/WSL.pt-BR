---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91994f3a075436c022acb9dadeea072142687b72
ms.sourcegitcommit: cf6d8e277ed3102f8f879b9f39ba0966d4ea6135
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2019
ms.locfileid: "74164336"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="e825d-104">Instruções de instalação do WSL 2</span><span class="sxs-lookup"><span data-stu-id="e825d-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="e825d-105">Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="e825d-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="e825d-106">O WSL 2 só está disponível no Windows 10 Builds 18917 ou superior</span><span class="sxs-lookup"><span data-stu-id="e825d-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="e825d-107">Verifique se você tem o WSL instalado (você pode encontrar instruções para fazer isso [aqui](./install-win10.md)) e se está executando o Windows 10 **Build 18917** ou superior</span><span class="sxs-lookup"><span data-stu-id="e825d-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="e825d-108">Para verificar se você está usando o Build 18917 ou superior, ingresse [no programa Windows Insider](https://insider.windows.com/en-us/) e selecione o anel "rápido".</span><span class="sxs-lookup"><span data-stu-id="e825d-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="e825d-109">Você pode verificar a versão do Windows abrindo o prompt de comando e executando o comando `ver`.</span><span class="sxs-lookup"><span data-stu-id="e825d-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="e825d-110">Habilite o componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="e825d-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="e825d-111">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="e825d-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="e825d-112">Verifique quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="e825d-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="e825d-113">Habilite o componente opcional ' plataforma de máquina virtual ' e verifique se o WSL está habilitado</span><span class="sxs-lookup"><span data-stu-id="e825d-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="e825d-114">Para habilitar o componente ' plataforma de máquina virtual ', abra o PowerShell como administrador e execute o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="e825d-114">To enable the 'Virtual Machine Platform' component open PowerShell as an administrator and run the command below.</span></span> <span data-ttu-id="e825d-115">Se você estiver instalando o WSL pela primeira vez, selecione ' não ' quando for solicitada uma reinicialização, pois será necessário reiniciar o computador assim mesmo após instalar o componente opcional ' subsistema do Windows para Linux '.</span><span class="sxs-lookup"><span data-stu-id="e825d-115">If you are installing WSL for the first time then select 'No' when prompted for a restart, as you will need to restart your machine anyway after installing the 'Windows Subsystem for Linux' optional component.</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

<span data-ttu-id="e825d-116">Você também precisará certificar-se de que o componente opcional do subsistema do Windows para Linux esteja habilitado.</span><span class="sxs-lookup"><span data-stu-id="e825d-116">You will also need to make sure that the Windows Subsystem for Linux optional component is enabled.</span></span> <span data-ttu-id="e825d-117">Você pode fazer isso executando o seguinte comando em uma janela do PowerShell com privilégios de administrador:</span><span class="sxs-lookup"><span data-stu-id="e825d-117">You can do this by running the following command from a PowerShell window with administrator privileges:</span></span> 

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="e825d-118">Reinicie o computador para concluir a instalação dos dois componentes.</span><span class="sxs-lookup"><span data-stu-id="e825d-118">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="e825d-119">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="e825d-119">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="e825d-120">Se você não tiver um distribuição do Linux instalado, consulte a página [instalar no Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs para obter instruções sobre como instalar um.</span><span class="sxs-lookup"><span data-stu-id="e825d-120">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="e825d-121">No PowerShell, execute:</span><span class="sxs-lookup"><span data-stu-id="e825d-121">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="e825d-122">e substitua `<Distro>` pelo nome real da sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="e825d-122">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="e825d-123">(Você pode encontrá-lo com o comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="e825d-123">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="e825d-124">Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.</span><span class="sxs-lookup"><span data-stu-id="e825d-124">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="e825d-125">Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:</span><span class="sxs-lookup"><span data-stu-id="e825d-125">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="e825d-126">Isso fará com que qualquer nova distribuição instalada seja inicializada como uma distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="e825d-126">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="e825d-127">Termine verificando quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="e825d-127">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="e825d-128">Para verificar quais versões do WSL cada distribuição está usando, use o seguinte comando (disponível somente no Windows Build 18917 ou superior):</span><span class="sxs-lookup"><span data-stu-id="e825d-128">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="e825d-129">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="e825d-129">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="e825d-130">A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão".</span><span class="sxs-lookup"><span data-stu-id="e825d-130">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="e825d-131">Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="e825d-131">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="e825d-132">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="e825d-132">Troubleshooting:</span></span> 

<span data-ttu-id="e825d-133">Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="e825d-133">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="e825d-134">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="e825d-134">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="e825d-135">**Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="e825d-135">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="e825d-136">Verifique se a virtualização está habilitada dentro do BIOS do seu computador.</span><span class="sxs-lookup"><span data-stu-id="e825d-136">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="e825d-137">As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.</span><span class="sxs-lookup"><span data-stu-id="e825d-137">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="e825d-138">**Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="e825d-138">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="e825d-139">Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="e825d-139">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="e825d-140">Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="e825d-140">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="e825d-141">Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="e825d-141">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="e825d-142">**A operação solicitada não pôde ser concluída devido a uma limitação do sistema de disco virtual. Os arquivos do disco rígido virtual devem ser descompactados e descriptografados e não devem ser esparsos.**</span><span class="sxs-lookup"><span data-stu-id="e825d-142">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="e825d-143">Verifique o [thread do GitHub WSL #4103](https://github.com/microsoft/WSL/issues/4103) onde esse problema está sendo acompanhado para obter informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="e825d-143">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>