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
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063284"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="1d330-104">Subsistema do Windows para o guia de instalação do Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="1d330-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="1d330-105">Instale o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="1d330-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="1d330-106">Antes de instalar qualquer distribuições do Linux para WSL, você deve garantir que o "Windows subsistema para Linux" recurso opcional está habilitado:</span><span class="sxs-lookup"><span data-stu-id="1d330-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="1d330-107">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="1d330-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="1d330-108">Reinicie o computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="1d330-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="1d330-109">Instalar sua distribuição do Linux de escolha</span><span class="sxs-lookup"><span data-stu-id="1d330-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="1d330-110">Para baixar e instalar seu distro(s) preferencial, você tem três opções:</span><span class="sxs-lookup"><span data-stu-id="1d330-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="1d330-111">Baixe e instale o Store do Windows (veja abaixo)</span><span class="sxs-lookup"><span data-stu-id="1d330-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="1d330-112">Baixe e instale o comando-linha/Script ([leia as instruções de instalação manual](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="1d330-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="1d330-113">Baixe e descompacte e instalar manualmente (para o Windows Server - [as instruções aqui](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="1d330-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="1d330-114">Windows 10 Fall Creators Update e posterior: Instalar a partir do Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="1d330-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="1d330-115">Esta seção destina-se a compilação 16215 ou posterior do Windows.</span><span class="sxs-lookup"><span data-stu-id="1d330-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="1d330-116">Siga estas etapas para [verificar seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="1d330-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="1d330-117">Abra o Microsoft Store e escolha sua distribuição do Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="1d330-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Modo de exibição de distribuições do Linux no armazenamento do Windows](media/store.png)

    <span data-ttu-id="1d330-119">Os links a seguir abrirá a página de armazenamento do Windows para cada distribuição:</span><span class="sxs-lookup"><span data-stu-id="1d330-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="1d330-120">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="1d330-120">Ubuntu</span></span>](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [<span data-ttu-id="1d330-121">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="1d330-121">OpenSUSE</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="1d330-122">SLES</span><span class="sxs-lookup"><span data-stu-id="1d330-122">SLES</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="1d330-123">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="1d330-123">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="1d330-124">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="1d330-124">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. <span data-ttu-id="1d330-125">Página a distribuição, selecione "Obter"</span><span class="sxs-lookup"><span data-stu-id="1d330-125">From the distro's page, select "Get"</span></span>

    ![Modo de exibição de distribuições do Linux no armazenamento do Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="1d330-127">Concluir a inicialização de sua distribuição</span><span class="sxs-lookup"><span data-stu-id="1d330-127">Complete initialization of your distro</span></span>
<span data-ttu-id="1d330-128">Agora que sua distribuição do Linux é instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) uma vez, antes que ele pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="1d330-128">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1d330-129">Solução de problemas:</span><span class="sxs-lookup"><span data-stu-id="1d330-129">Troubleshooting:</span></span> 

<span data-ttu-id="1d330-130">Abaixo estão os erros relacionados e correções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="1d330-130">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="1d330-131">Consulte a [página de solução de problemas de WSL](troubleshooting.md) para outros erros comuns e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="1d330-131">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="1d330-132">**Instalação falhou com erro 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="1d330-132">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="1d330-133">O subsistema Windows para Linux é executado somente na unidade do sistema (geralmente, isso é seu `C:` unidade).</span><span class="sxs-lookup"><span data-stu-id="1d330-133">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="1d330-134">Certifique-se de que as distribuições são armazenadas na unidade do sistema:</span><span class="sxs-lookup"><span data-stu-id="1d330-134">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="1d330-135">Abra **as configurações** -> **armazenamento** -> **mais configurações de armazenamento: Alterar onde o novo conteúdo é salvo**
    ![imagem das configurações do sistema para instalar aplicativos na unidade c:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="1d330-135">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
