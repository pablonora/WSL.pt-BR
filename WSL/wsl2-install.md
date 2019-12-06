---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 65c0440a95637708881c00558cba6c7985f89ec0
ms.sourcegitcommit: 522af20edfba4d4a9e429327389967a83e6d1156
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/06/2019
ms.locfileid: "74881373"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="561bc-104">Instruções de instalação do WSL 2</span><span class="sxs-lookup"><span data-stu-id="561bc-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="561bc-105">Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="561bc-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="561bc-106">O WSL 2 só está disponível no Windows 10 Builds 18917 ou superior</span><span class="sxs-lookup"><span data-stu-id="561bc-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="561bc-107">Verifique se você tem o WSL instalado (você pode encontrar instruções para fazer isso [aqui](./install-win10.md)) e se está executando o Windows 10 **Build 18917** ou superior</span><span class="sxs-lookup"><span data-stu-id="561bc-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="561bc-108">Para verificar se você está usando o Build 18917 ou superior, ingresse [no programa Windows Insider](https://insider.windows.com/en-us/) e selecione o anel "rápido" ou "lento".</span><span class="sxs-lookup"><span data-stu-id="561bc-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring or the 'Slow' ring.</span></span> 
   - <span data-ttu-id="561bc-109">Você pode verificar a versão do Windows abrindo o prompt de comando e executando o comando `ver`.</span><span class="sxs-lookup"><span data-stu-id="561bc-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="561bc-110">Habilite o componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="561bc-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="561bc-111">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="561bc-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="561bc-112">Verifique quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="561bc-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="561bc-113">Habilite o componente opcional ' plataforma de máquina virtual ' e verifique se o WSL está habilitado</span><span class="sxs-lookup"><span data-stu-id="561bc-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="561bc-114">Você precisará certificar-se de ter os componentes opcionais do subsistema do Windows para Linux e da plataforma de máquina virtual instalados.</span><span class="sxs-lookup"><span data-stu-id="561bc-114">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="561bc-115">Você pode fazer isso executando o seguinte comando no PowerShell:</span><span class="sxs-lookup"><span data-stu-id="561bc-115">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="561bc-116">Reinicie o computador para concluir a instalação dos dois componentes.</span><span class="sxs-lookup"><span data-stu-id="561bc-116">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="561bc-117">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="561bc-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="561bc-118">Se você não tiver um distribuição do Linux instalado, consulte a página [instalar no Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs para obter instruções sobre como instalar um.</span><span class="sxs-lookup"><span data-stu-id="561bc-118">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="561bc-119">Para definir um distribuição, execute:</span><span class="sxs-lookup"><span data-stu-id="561bc-119">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="561bc-120">e substitua `<Distro>` pelo nome real da sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="561bc-120">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="561bc-121">(Você pode encontrá-lo com o comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="561bc-121">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="561bc-122">Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.</span><span class="sxs-lookup"><span data-stu-id="561bc-122">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="561bc-123">Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:</span><span class="sxs-lookup"><span data-stu-id="561bc-123">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="561bc-124">Isso fará com que qualquer nova distribuição instalada seja inicializada como uma distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="561bc-124">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="561bc-125">Termine verificando quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="561bc-125">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="561bc-126">Para verificar quais versões do WSL cada distribuição está usando, use o seguinte comando (disponível somente no Windows Build 18917 ou superior):</span><span class="sxs-lookup"><span data-stu-id="561bc-126">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="561bc-127">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="561bc-127">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="561bc-128">A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão".</span><span class="sxs-lookup"><span data-stu-id="561bc-128">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="561bc-129">Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="561bc-129">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="561bc-130">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="561bc-130">Troubleshooting:</span></span> 

<span data-ttu-id="561bc-131">Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="561bc-131">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="561bc-132">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="561bc-132">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="561bc-133">**Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="561bc-133">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="561bc-134">Verifique se a virtualização está habilitada dentro do BIOS do seu computador.</span><span class="sxs-lookup"><span data-stu-id="561bc-134">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="561bc-135">As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.</span><span class="sxs-lookup"><span data-stu-id="561bc-135">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="561bc-136">**Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="561bc-136">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="561bc-137">Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="561bc-137">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="561bc-138">Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="561bc-138">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="561bc-139">Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="561bc-139">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="561bc-140">**A operação solicitada não pôde ser concluída devido a uma limitação do sistema de disco virtual. Os arquivos do disco rígido virtual devem ser descompactados e descriptografados e não devem ser esparsos.**</span><span class="sxs-lookup"><span data-stu-id="561bc-140">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="561bc-141">Verifique o [thread do GitHub WSL #4103](https://github.com/microsoft/WSL/issues/4103) onde esse problema está sendo acompanhado para obter informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="561bc-141">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="561bc-142">**O termo ' WSL ' não é reconhecido como o nome de um cmdlet, função, arquivo de script ou programa operável.**</span><span class="sxs-lookup"><span data-stu-id="561bc-142">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="561bc-143">Verifique se o [componente opcional do subsistema do Windows para Linux está instalado](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="561bc-143">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="561bc-144">Além disso, se você estiver usando um dispositivo Arm64 e executar esse comando do PowerShell, receberá esse erro.</span><span class="sxs-lookup"><span data-stu-id="561bc-144">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="561bc-145">Em vez disso, execute `wsl.exe` do [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6)ou do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="561bc-145">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
