---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c031b1348a77e1dac967fae5e4df772e10a9084
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256339"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="be4bd-104">Instruções de instalação do WSL 2</span><span class="sxs-lookup"><span data-stu-id="be4bd-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="be4bd-105">Você pode assistir ao vídeo abaixo ou ler este artigo para saber como instalar o WSL2.</span><span class="sxs-lookup"><span data-stu-id="be4bd-105">You can watch the video below, or read on in this article to learn how to install WSL2.</span></span> 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

<span data-ttu-id="be4bd-106">Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="be4bd-106">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="be4bd-107">O WSL 2 só está disponível no Windows 10 builds 18917 ou superiores</span><span class="sxs-lookup"><span data-stu-id="be4bd-107">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="be4bd-108">Verifique se você tem o WSL instalado (você pode encontrar instruções para fazer isso [aqui](./install-win10.md)) e se está executando o Windows 10 **build 18917** ou superior</span><span class="sxs-lookup"><span data-stu-id="be4bd-108">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="be4bd-109">Para verificar se você está usando o build 18917 ou superior, ingresse [no Programa Windows Insider](https://insider.windows.com/en-us/) e selecione o anel modo Rápido ou Lento.</span><span class="sxs-lookup"><span data-stu-id="be4bd-109">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring or the 'Slow' ring.</span></span> 
   - <span data-ttu-id="be4bd-110">Você pode verificar a versão do Windows abrindo o prompt de comando e executando o comando `ver`.</span><span class="sxs-lookup"><span data-stu-id="be4bd-110">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="be4bd-111">Habilite o componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="be4bd-111">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="be4bd-112">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="be4bd-112">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="be4bd-113">Verifique quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="be4bd-113">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="be4bd-114">Habilite o componente opcional "Plataforma de máquina virtual" e verifique se o WSL está habilitado</span><span class="sxs-lookup"><span data-stu-id="be4bd-114">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="be4bd-115">Você precisará verificar se tem os componentes opcionais do Subsistema do Windows para Linux e da Plataforma de Máquina Virtual instalados.</span><span class="sxs-lookup"><span data-stu-id="be4bd-115">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="be4bd-116">Você pode fazer isso executando o seguinte comando no PowerShell:</span><span class="sxs-lookup"><span data-stu-id="be4bd-116">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="be4bd-117">Reinicie o computador para concluir a instalação dos dois componentes.</span><span class="sxs-lookup"><span data-stu-id="be4bd-117">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="be4bd-118">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="be4bd-118">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="be4bd-119">Se você não tiver uma distribuição do Linux instalada, consulte a página de documentação [Instalar no Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) para obter instruções sobre a instalação.</span><span class="sxs-lookup"><span data-stu-id="be4bd-119">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="be4bd-120">Para definir uma distribuição, execute:</span><span class="sxs-lookup"><span data-stu-id="be4bd-120">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="be4bd-121">e substitua `<Distro>` pelo nome real da sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="be4bd-121">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="be4bd-122">(Você pode encontrá-lo com o comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="be4bd-122">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="be4bd-123">Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.</span><span class="sxs-lookup"><span data-stu-id="be4bd-123">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="be4bd-124">Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:</span><span class="sxs-lookup"><span data-stu-id="be4bd-124">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="be4bd-125">Isso fará com que qualquer nova distribuição instalada seja inicializada como uma distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="be4bd-125">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="be4bd-126">Termine verificando quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="be4bd-126">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="be4bd-127">Para verificar quais versões do WSL cada distribuição está usando, execute o seguinte comando (somente disponível no Windows Build 18917 ou superior):</span><span class="sxs-lookup"><span data-stu-id="be4bd-127">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="be4bd-128">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="be4bd-128">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="be4bd-129">A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão".</span><span class="sxs-lookup"><span data-stu-id="be4bd-129">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="be4bd-130">Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="be4bd-130">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="be4bd-131">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="be4bd-131">Troubleshooting:</span></span> 

<span data-ttu-id="be4bd-132">Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="be4bd-132">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="be4bd-133">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="be4bd-133">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="be4bd-134">**Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="be4bd-134">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="be4bd-135">Verifique se a virtualização está habilitada dentro do BIOS do seu computador.</span><span class="sxs-lookup"><span data-stu-id="be4bd-135">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="be4bd-136">As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.</span><span class="sxs-lookup"><span data-stu-id="be4bd-136">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="be4bd-137">**Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="be4bd-137">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="be4bd-138">Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="be4bd-138">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="be4bd-139">Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="be4bd-139">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="be4bd-140">Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="be4bd-140">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="be4bd-141">**A operação solicitada não pôde ser concluída devido a uma limitação do sistema de disco virtual. Os arquivos do disco rígido virtual devem ser descompactados e descriptografados e não devem ser esparsos.**</span><span class="sxs-lookup"><span data-stu-id="be4bd-141">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="be4bd-142">Verifique o [thread 4103 do GitHub no WSL](https://github.com/microsoft/WSL/issues/4103) em que esse problema está sendo acompanhado para obter informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="be4bd-142">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="be4bd-143">**O termo 'wsl' não é reconhecido como nome de um cmdlet, uma função, um arquivo de script ou um programa operável.**</span><span class="sxs-lookup"><span data-stu-id="be4bd-143">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="be4bd-144">Verifique se o [componente opcional do Subsistema do Windows para Linux está instalado](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="be4bd-144">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="be4bd-145">Além disso, se você estiver usando um dispositivo Arm64 e executar esse comando do PowerShell, receberá esse erro.</span><span class="sxs-lookup"><span data-stu-id="be4bd-145">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="be4bd-146">Em vez disso, execute `wsl.exe` no [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) ou no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="be4bd-146">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
