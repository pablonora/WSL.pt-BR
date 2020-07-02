---
title: Instalar o Subsistema Linux no Windows Server
description: Instruções de instalação para o Subsistema Linux no Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema do windows para linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ebcd7f6b10d2b734b1f2a66f64a5e3292855bcf4
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671013"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="0a54d-104">Guia de instalação do Windows Server</span><span class="sxs-lookup"><span data-stu-id="0a54d-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="0a54d-105">O Subsistema do Windows para Linux está disponível para instalação no Windows Server 2019 (versão 1709) e posterior.</span><span class="sxs-lookup"><span data-stu-id="0a54d-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="0a54d-106">Este guia explicará as etapas de habilitação do WSL em seu computador.</span><span class="sxs-lookup"><span data-stu-id="0a54d-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="0a54d-107">Habilitar o Subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="0a54d-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="0a54d-108">Para poder executar as distribuições do Linux no Windows, você deverá habilitar o recurso opcional "Subsistema do Windows para Linux" e reiniciar.</span><span class="sxs-lookup"><span data-stu-id="0a54d-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="0a54d-109">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="0a54d-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="0a54d-110">Baixar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="0a54d-110">Download a Linux distribution</span></span>

<span data-ttu-id="0a54d-111">Siga [estas instruções](install-manual.md) para baixar sua distribuição favorita do Linux.</span><span class="sxs-lookup"><span data-stu-id="0a54d-111">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="0a54d-112">Extrair e instalar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="0a54d-112">Extract and install a Linux distribution</span></span>

<span data-ttu-id="0a54d-113">Agora que você baixou uma distribuição do Linux, para extrair o conteúdo e instalá-lo manualmente, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="0a54d-113">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="0a54d-114">Extraia o conteúdo do pacote `<distro>.appx` usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0a54d-114">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="0a54d-115">Execute o aplicativo inicializador de distribuição na pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="0a54d-115">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="0a54d-116">O inicializador normalmente é chamado de `<distro>.exe` (por exemplo, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="0a54d-116">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Expansão da distribuição do Ubuntu no Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="0a54d-118">**Falha na instalação com o erro 0x8007007e**: Esse erro ocorre quando o sistema não é compatível com o WSL.</span><span class="sxs-lookup"><span data-stu-id="0a54d-118">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="0a54d-119">Garanta que você está executando o Windows Build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0a54d-119">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="0a54d-120">[Verifique seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="0a54d-120">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="0a54d-121">Certifique-se também de [confirmar se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled) e se o computador foi reiniciado após a habilitação do recurso.</span><span class="sxs-lookup"><span data-stu-id="0a54d-121">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="0a54d-122">3. Adicione o caminho da distribuição ao caminho do ambiente do Windows (`C:\Users\Administrator\Ubuntu`, neste exemplo) usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0a54d-122">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="0a54d-123">Agora você pode iniciar sua distribuição em qualquer caminho digitando `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="0a54d-123">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="0a54d-124">Por exemplo: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="0a54d-124">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="0a54d-125">Agora que a distribuição está instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) antes de usar a distribuição.</span><span class="sxs-lookup"><span data-stu-id="0a54d-125">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
