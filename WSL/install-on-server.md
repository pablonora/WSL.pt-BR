---
title: Instalar o Subsistema Linux no Windows Server
description: Instruções de instalação para o Subsistema Linux no Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema do windows para linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 805b7d266020c62e0c6f58889541517d44db3726
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153075"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="b34aa-104">Guia de instalação do Windows Server</span><span class="sxs-lookup"><span data-stu-id="b34aa-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="b34aa-105">O Subsistema do Windows para Linux está disponível para instalação no Windows Server 2019 (versão 1709) e posterior.</span><span class="sxs-lookup"><span data-stu-id="b34aa-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="b34aa-106">Este guia explicará as etapas de habilitação do WSL em seu computador.</span><span class="sxs-lookup"><span data-stu-id="b34aa-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="b34aa-107">Habilitar o Subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="b34aa-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="b34aa-108">Para poder executar as distribuições do Linux no Windows, você deverá habilitar o recurso opcional "Subsistema do Windows para Linux" e reiniciar.</span><span class="sxs-lookup"><span data-stu-id="b34aa-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="b34aa-109">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="b34aa-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

<span data-ttu-id="b34aa-110">**Se você estiver procurando 100% de compatibilidade com a chamada do sistema e desempenho de E/S mais rápido, leia abaixo para instalar o WSL 2!**</span><span class="sxs-lookup"><span data-stu-id="b34aa-110">**If you're looking for 100% system call compatibility and faster IO performance, read below to install WSL 2!**</span></span>

<span data-ttu-id="b34aa-111">O WSL 2 só está disponível no Windows 10, versão 2004, Build 19041 ou superiores.</span><span class="sxs-lookup"><span data-stu-id="b34aa-111">WSL 2 is only available in Windows 10, Version 2004, Build 19041 or higher.</span></span> <span data-ttu-id="b34aa-112">Você pode precisar [atualizar sua versão do Windows](ms-settings:windowsupdate).</span><span class="sxs-lookup"><span data-stu-id="b34aa-112">You may need to [update your Windows version](ms-settings:windowsupdate).</span></span>

<span data-ttu-id="b34aa-113">**Se continuar com o WSL 1, reinicie o computador quando solicitado e continue com a instalação [aqui](./install-on-server.md#download-a-linux-distribution)**</span><span class="sxs-lookup"><span data-stu-id="b34aa-113">**If continuing with WSL 1, restart your machine when prompted and continue with installation [here](./install-on-server.md#download-a-linux-distribution)**</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="b34aa-114">Habilitar o componente opcional "Plataforma de Máquina Virtual"</span><span class="sxs-lookup"><span data-stu-id="b34aa-114">Enable the Virtual Machine Platform optional component</span></span>

<span data-ttu-id="b34aa-115">Verifique se o componente opcional "Plataforma de Máquina Virtual" está instalado.</span><span class="sxs-lookup"><span data-stu-id="b34aa-115">Ensure the 'Virtual Machine Platform' optional component is installed.</span></span> <span data-ttu-id="b34aa-116">Você pode fazer isso executando o seguinte comando no PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b34aa-116">You can do that by running the following command in PowerShell:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="b34aa-117">Baixar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="b34aa-117">Download a Linux distribution</span></span>

<span data-ttu-id="b34aa-118">Siga [estas instruções](install-manual.md) para baixar sua distribuição favorita do Linux.</span><span class="sxs-lookup"><span data-stu-id="b34aa-118">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="b34aa-119">Extrair e instalar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="b34aa-119">Extract and install a Linux distribution</span></span>

<span data-ttu-id="b34aa-120">Agora que você baixou uma distribuição do Linux, para extrair o conteúdo e instalá-lo manualmente, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="b34aa-120">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="b34aa-121">Extraia o conteúdo do pacote `<distro>.appx` usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b34aa-121">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="b34aa-122">Execute o aplicativo inicializador de distribuição na pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="b34aa-122">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="b34aa-123">O inicializador normalmente é chamado de `<distro>.exe` (por exemplo, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="b34aa-123">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Expansão da distribuição do Ubuntu no Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="b34aa-125">**Falha na instalação com o erro 0x8007007e**: Esse erro ocorre quando o sistema não é compatível com o WSL.</span><span class="sxs-lookup"><span data-stu-id="b34aa-125">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="b34aa-126">Garanta que você está executando o Windows Build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b34aa-126">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="b34aa-127">[Verifique seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="b34aa-127">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="b34aa-128">Certifique-se também de [confirmar se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled) e se o computador foi reiniciado após a habilitação do recurso.</span><span class="sxs-lookup"><span data-stu-id="b34aa-128">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="b34aa-129">3. Adicione o caminho da distribuição ao caminho do ambiente do Windows (`C:\Users\Administrator\Ubuntu`, neste exemplo) usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b34aa-129">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="b34aa-130">Agora você pode iniciar sua distribuição em qualquer caminho digitando `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="b34aa-130">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="b34aa-131">Por exemplo: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="b34aa-131">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="b34aa-132">Agora que a distribuição está instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) antes de usar a distribuição.</span><span class="sxs-lookup"><span data-stu-id="b34aa-132">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
