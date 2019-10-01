---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 386b6793f00300bc9dabd1613cfd69b19d222f0b
ms.sourcegitcommit: eb7b572388c6bddbf6e8ad8d01927660fe66aecf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/01/2019
ms.locfileid: "71692463"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="c4a13-104">Instruções de instalação do WSL 2</span><span class="sxs-lookup"><span data-stu-id="c4a13-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="c4a13-105">Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="c4a13-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="c4a13-106">O WSL 2 só está disponível no Windows 10 Builds 18917 ou superior</span><span class="sxs-lookup"><span data-stu-id="c4a13-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="c4a13-107">Verifique se você tem o WSL instalado (você pode encontrar instruções para fazer isso [aqui](./install-win10.md)) e se está executando o Windows 10 **Build 18917** ou superior</span><span class="sxs-lookup"><span data-stu-id="c4a13-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="c4a13-108">Para verificar se você está usando o Build 18917 ou superior, ingresse [no programa Windows Insider](https://insider.windows.com/en-us/) e selecione o anel "rápido".</span><span class="sxs-lookup"><span data-stu-id="c4a13-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="c4a13-109">Você pode verificar a versão do Windows abrindo o prompt de comando e `ver` executando o comando.</span><span class="sxs-lookup"><span data-stu-id="c4a13-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="c4a13-110">Habilite o componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="c4a13-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="c4a13-111">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="c4a13-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="c4a13-112">Verifique quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="c4a13-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="c4a13-113">Habilite o componente opcional ' plataforma de máquina virtual ' e verifique se o WSL está habilitado</span><span class="sxs-lookup"><span data-stu-id="c4a13-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="c4a13-114">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="c4a13-114">Open PowerShell as an Administrator and run:</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="c4a13-115">Isso garantirá que os componentes opcionais da plataforma de máquina virtual e do subsistema do Windows para Linux estejam instalados.</span><span class="sxs-lookup"><span data-stu-id="c4a13-115">This will make sure that both the Virtual Machine Platform and Windows Subsystem for Linux optional components are installed.</span></span> <span data-ttu-id="c4a13-116">Depois de executar esses comandos, você precisará reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="c4a13-116">After you've run these commands you'll need to restart your computer.</span></span> 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="c4a13-117">Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="c4a13-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="c4a13-118">No PowerShell, execute:</span><span class="sxs-lookup"><span data-stu-id="c4a13-118">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="c4a13-119">e substitua `<Distro>` pelo nome real da sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="c4a13-119">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="c4a13-120">(Você pode encontrá-lo com o comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="c4a13-120">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="c4a13-121">Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.</span><span class="sxs-lookup"><span data-stu-id="c4a13-121">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="c4a13-122">Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:</span><span class="sxs-lookup"><span data-stu-id="c4a13-122">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="c4a13-123">Isso fará com que qualquer nova distribuição instalada seja inicializada como uma distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="c4a13-123">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="c4a13-124">Termine verificando quais versões do WSL suas distribuições estão usando</span><span class="sxs-lookup"><span data-stu-id="c4a13-124">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="c4a13-125">Para verificar quais versões do WSL cada distribuição está usando, use o seguinte comando (disponível somente no Windows Build 18917 ou superior):</span><span class="sxs-lookup"><span data-stu-id="c4a13-125">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="c4a13-126">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="c4a13-126">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="c4a13-127">A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão".</span><span class="sxs-lookup"><span data-stu-id="c4a13-127">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="c4a13-128">Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="c4a13-128">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="c4a13-129">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="c4a13-129">Troubleshooting:</span></span> 

<span data-ttu-id="c4a13-130">Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="c4a13-130">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="c4a13-131">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="c4a13-131">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="c4a13-132">**Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="c4a13-132">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="c4a13-133">Verifique se a virtualização está habilitada dentro do BIOS do seu computador.</span><span class="sxs-lookup"><span data-stu-id="c4a13-133">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="c4a13-134">As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.</span><span class="sxs-lookup"><span data-stu-id="c4a13-134">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="c4a13-135">**Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="c4a13-135">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="c4a13-136">Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="c4a13-136">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="c4a13-137">Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="c4a13-137">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="c4a13-138">Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="c4a13-138">You can find the full WSL install instructions [here](./install-win10.md).</span></span>