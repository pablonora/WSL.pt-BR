---
title: Instalar o subsistema do Windows para Linux (WSL) no Windows 10
description: Instruções de instalação para o subsistema do Windows para Linux no Windows 10.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10, instalar
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499288"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="7f8e1-104">Guia de instalação do subsistema do Windows para Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="7f8e1-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="7f8e1-105">Instalar o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="7f8e1-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="7f8e1-106">Antes de instalar qualquer distribuições do Linux para WSL, você deve garantir que o recurso opcional "subsistema do Windows para Linux" esteja habilitado:</span><span class="sxs-lookup"><span data-stu-id="7f8e1-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="7f8e1-107">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="7f8e1-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="7f8e1-108">Reinicie o computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="7f8e1-109">Instale sua distribuição do Linux de sua escolha</span><span class="sxs-lookup"><span data-stu-id="7f8e1-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="7f8e1-110">Para baixar e instalar seus distribuição (s) preferenciais, você tem três opções:</span><span class="sxs-lookup"><span data-stu-id="7f8e1-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="7f8e1-111">Baixar e instalar do Microsoft Store (veja abaixo)</span><span class="sxs-lookup"><span data-stu-id="7f8e1-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="7f8e1-112">Baixar e instalar a partir da linha de comando/script ([Leia as instruções de instalação manual](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="7f8e1-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="7f8e1-113">Baixe e descompacte e instale manualmente (para Windows Server- [instruções aqui](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="7f8e1-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="7f8e1-114">Atualização dos criadores de outono do Windows 10 e posterior: Instalar do Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7f8e1-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="7f8e1-115">Esta seção destina-se ao Windows Build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="7f8e1-116">Siga estas etapas para [verificar sua compilação](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="7f8e1-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="7f8e1-117">Abra o Microsoft Store e escolha sua distribuição do Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Exibição de distribuições do Linux no Microsoft Store](media/store.png)

    <span data-ttu-id="7f8e1-119">Os links a seguir abrirão a página da Microsoft Store para cada distribuição:</span><span class="sxs-lookup"><span data-stu-id="7f8e1-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="7f8e1-120">Ubuntu 16, 4 LTS</span><span class="sxs-lookup"><span data-stu-id="7f8e1-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="7f8e1-121">Ubuntu 18, 4 LTS</span><span class="sxs-lookup"><span data-stu-id="7f8e1-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="7f8e1-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="7f8e1-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="7f8e1-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="7f8e1-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="7f8e1-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="7f8e1-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="7f8e1-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="7f8e1-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="7f8e1-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="7f8e1-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="7f8e1-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="7f8e1-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="7f8e1-128">Fedora Remix para WSL</span><span class="sxs-lookup"><span data-stu-id="7f8e1-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="7f8e1-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="7f8e1-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="7f8e1-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="7f8e1-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="7f8e1-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="7f8e1-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="7f8e1-132">Na página do distribuição, selecione "obter"</span><span class="sxs-lookup"><span data-stu-id="7f8e1-132">From the distro's page, select "Get"</span></span>

    ![Exibição de distribuições do Linux na Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="7f8e1-134">Concluir a inicialização do seu distribuição</span><span class="sxs-lookup"><span data-stu-id="7f8e1-134">Complete initialization of your distro</span></span>
<span data-ttu-id="7f8e1-135">Agora que o distribuição do Linux está instalado, você deve [inicializar a nova instância do distribuição](initialize-distro.md) uma vez, antes que possa ser usada.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="7f8e1-136">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="7f8e1-136">Troubleshooting:</span></span> 

<span data-ttu-id="7f8e1-137">Abaixo estão os erros relacionados e as correções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="7f8e1-138">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para obter outros erros comuns e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="7f8e1-139">**Falha na instalação com o erro 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="7f8e1-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="7f8e1-140">O subsistema do Windows para Linux é executado somente na unidade do sistema (normalmente, `C:` essa é a unidade).</span><span class="sxs-lookup"><span data-stu-id="7f8e1-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="7f8e1-141">Verifique se os distribuições estão armazenados na unidade do sistema:</span><span class="sxs-lookup"><span data-stu-id="7f8e1-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="7f8e1-142">Abra **configurações** ->  armazenamento -> mais configurações de armazenamento: \*\* Alterar onde o novo conteúdo é\*\*salvo
    ![imagem das configurações do sistema para instalar aplicativos na unidade C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="7f8e1-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="7f8e1-143">**WslRegisterDistribution falhou com o erro 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="7f8e1-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="7f8e1-144">O componente opcional do subsistema do Windows para Linux não está habilitado:</span><span class="sxs-lookup"><span data-stu-id="7f8e1-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="7f8e1-145">Abra o **painel** -> de controle**programas e recursos** -> \* \* ativar ou desativar o recurso do Windows \* \*-> verificar o subsistema **do Windows para Linux** ou usar o cmdlet do PowerShell mencionado no início deste artigo.</span><span class="sxs-lookup"><span data-stu-id="7f8e1-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
