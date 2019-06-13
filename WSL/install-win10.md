---
title: Instalar o subsistema do Windows para Linux (WSL) no Windows 10
description: Instruções de instalação para o subsistema Windows para Linux no Windows 10.
keywords: Instalar o BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10,
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d30a5883d648e084193659e997c55d203eb5a735
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035056"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="84861-104">Subsistema do Windows para o guia de instalação do Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="84861-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="84861-105">Instale o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="84861-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="84861-106">Antes de instalar qualquer distribuições do Linux para WSL, você deve garantir que o "Windows subsistema para Linux" recurso opcional está habilitado:</span><span class="sxs-lookup"><span data-stu-id="84861-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="84861-107">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="84861-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="84861-108">Reinicie o computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="84861-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="84861-109">Instalar sua distribuição do Linux de escolha</span><span class="sxs-lookup"><span data-stu-id="84861-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="84861-110">Para baixar e instalar seu distro(s) preferencial, você tem três opções:</span><span class="sxs-lookup"><span data-stu-id="84861-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="84861-111">Baixe e instale o Store do Windows (veja abaixo)</span><span class="sxs-lookup"><span data-stu-id="84861-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="84861-112">Baixe e instale o comando-linha/Script ([leia as instruções de instalação manual](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="84861-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="84861-113">Baixe e descompacte e instalar manualmente (para o Windows Server - [as instruções aqui](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="84861-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="84861-114">Windows 10 Fall Creators Update e posterior: Instalar a partir do Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="84861-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="84861-115">Esta seção destina-se a compilação 16215 ou posterior do Windows.</span><span class="sxs-lookup"><span data-stu-id="84861-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="84861-116">Siga estas etapas para [verificar seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="84861-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="84861-117">Abra o Microsoft Store e escolha sua distribuição do Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="84861-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Modo de exibição de distribuições do Linux no armazenamento do Windows](media/store.png)

    <span data-ttu-id="84861-119">Os links a seguir abrirá a página de armazenamento do Windows para cada distribuição:</span><span class="sxs-lookup"><span data-stu-id="84861-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="84861-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="84861-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="84861-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="84861-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="84861-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="84861-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="84861-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="84861-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="84861-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="84861-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="84861-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="84861-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="84861-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="84861-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="84861-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="84861-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="84861-128">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="84861-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="84861-129">WLinux</span><span class="sxs-lookup"><span data-stu-id="84861-129">WLinux</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="84861-130">WLinux Enterprise</span><span class="sxs-lookup"><span data-stu-id="84861-130">WLinux Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="84861-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="84861-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="84861-132">Página a distribuição, selecione "Obter"</span><span class="sxs-lookup"><span data-stu-id="84861-132">From the distro's page, select "Get"</span></span>

    ![Modo de exibição de distribuições do Linux no armazenamento do Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="84861-134">Concluir a inicialização de sua distribuição</span><span class="sxs-lookup"><span data-stu-id="84861-134">Complete initialization of your distro</span></span>
<span data-ttu-id="84861-135">Agora que sua distribuição do Linux é instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) uma vez, antes que ele pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="84861-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="84861-136">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="84861-136">Troubleshooting:</span></span> 

<span data-ttu-id="84861-137">Abaixo estão os erros relacionados e correções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="84861-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="84861-138">Consulte a [página de solução de problemas de WSL](troubleshooting.md) para outros erros comuns e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="84861-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="84861-139">**Instalação falhou com erro 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="84861-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="84861-140">O subsistema Windows para Linux é executado somente na unidade do sistema (geralmente, isso é seu `C:` unidade).</span><span class="sxs-lookup"><span data-stu-id="84861-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="84861-141">Certifique-se de que as distribuições são armazenadas na unidade do sistema:</span><span class="sxs-lookup"><span data-stu-id="84861-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="84861-142">Abra **as configurações** -> **armazenamento** -> **mais configurações de armazenamento: Alterar onde o novo conteúdo é salvo**
    ![imagem das configurações do sistema para instalar aplicativos na unidade c:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="84861-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="84861-143">**WslRegisterDistribution falhou com erro 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="84861-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="84861-144">O subsistema do Windows para o componente opcional do Linux não está habilitado:</span><span class="sxs-lookup"><span data-stu-id="84861-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="84861-145">Abra **painel de controle** -> **programas e recursos** -> \* \* Ativar ou desativar o recurso do Windows \* \* -> marque **subsistema Windows para Linux** ou usando o Cmdlet do PowerShell mencionado no início deste artigo.</span><span class="sxs-lookup"><span data-stu-id="84861-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
