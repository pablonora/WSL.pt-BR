---
title: Instalar o WSL (Subsistema Windows para Linux) no Windows 10
description: Instruções de instalação para o Subsistema Windows para Linux no Windows 10.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, install
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200240"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="ddfbc-104">Guia de instalação do Subsistema Windows para Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="ddfbc-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="ddfbc-105">Instalar o Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="ddfbc-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="ddfbc-106">Antes de instalar distribuições do Linux para WSL, você deve garantir que o recurso opcional "Subsistema Windows para Linux" esteja habilitado:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="ddfbc-107">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="ddfbc-108">Reinicie seu computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="ddfbc-109">Instale a distribuição do Linux de sua escolha</span><span class="sxs-lookup"><span data-stu-id="ddfbc-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="ddfbc-110">Para baixar e instalar suas distribuições preferenciais, há três opções:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-110">To download and install your preferred distro(s), you have three choices:</span></span>
* <span data-ttu-id="ddfbc-111">Baixe e instale usando a Microsoft Store (consulte abaixo)</span><span class="sxs-lookup"><span data-stu-id="ddfbc-111">Download and install from the Microsoft Store (see below)</span></span>
* <span data-ttu-id="ddfbc-112">Baixe e instale usando a linha de comando/script ([leia as instruções de instalação no manual](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="ddfbc-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
* <span data-ttu-id="ddfbc-113">Baixe e descompacte e instale manualmente (for Windows Server – [instruções aqui](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="ddfbc-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="ddfbc-114">Windows 10 Fall Creators Update e posteriores: Instale usando a Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="ddfbc-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="ddfbc-115">Esta seção destina-se ao Windows build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="ddfbc-116">Siga estas etapas para [verificar seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="ddfbc-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="ddfbc-117">Abra a Microsoft Store e escolha sua distribuição do Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Exibição das distribuições do Linux na Microsoft Store](media/store.png)

    <span data-ttu-id="ddfbc-119">Os links a seguir abrirão a página da Microsoft Store para cada distribuição:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="ddfbc-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="ddfbc-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="ddfbc-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="ddfbc-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="ddfbc-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="ddfbc-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="ddfbc-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="ddfbc-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="ddfbc-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="ddfbc-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="ddfbc-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="ddfbc-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="ddfbc-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="ddfbc-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="ddfbc-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="ddfbc-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="ddfbc-128">Fedora Remix para WSL</span><span class="sxs-lookup"><span data-stu-id="ddfbc-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="ddfbc-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="ddfbc-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="ddfbc-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="ddfbc-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="ddfbc-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="ddfbc-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="ddfbc-132">Na página da distribuição, selecione "Obter"</span><span class="sxs-lookup"><span data-stu-id="ddfbc-132">From the distro's page, select "Get"</span></span>

    ![Exibição das distribuições do Linux na Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="ddfbc-134">Conclua a inicialização de sua distribuição</span><span class="sxs-lookup"><span data-stu-id="ddfbc-134">Complete initialization of your distro</span></span>
<span data-ttu-id="ddfbc-135">Agora que a distribuição do Linux está instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) uma vez, antes que possa ser usada.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ddfbc-136">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-136">Troubleshooting:</span></span> 

<span data-ttu-id="ddfbc-137">Veja abaixo erros relacionados e correções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="ddfbc-138">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros comuns e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="ddfbc-139">**Falha na instalação com o erro 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="ddfbc-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="ddfbc-140">O Subsistema Windows para Linux é executado somente na unidade do sistema (normalmente, a unidade `C:`).</span><span class="sxs-lookup"><span data-stu-id="ddfbc-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="ddfbc-141">Verifique se as distribuições estão armazenadas na unidade do sistema:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="ddfbc-142">Abra **Configurações** -> **Armazenamento** -> **Mais Configurações de Armazenamento: Altere onde o novo conteúdo é salvo**
    ![Imagem das configurações do sistema para instalar aplicativos na unidade C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="ddfbc-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="ddfbc-143">**WslRegisterDistribution falhou com o erro 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="ddfbc-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="ddfbc-144">O componente opcional do Subsistema Windows para Linux não está habilitado:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="ddfbc-145">Abra **Painel de Controle** -> **Programas e Recursos** -> **Ativar ou desativar recursos do Windows** -> marque **Subsistema Windows para Linux** ou use o cmdlet do PowerShell mencionado no início deste artigo.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
