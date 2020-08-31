---
title: Instalar o Subsistema Linux no Windows Server
description: Saiba como instalar o Subsistema Linux no Windows Server. O WSL está disponível para instalação no Windows Server 2019 (versão 1709) e posterior.
keywords: BashOnWindows, bash, wsl, windows, subsistema do windows para linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 501bbf78c2d9f59dad945af9c30571317240b79f
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866141"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="a7e80-105">Guia de instalação do Windows Server</span><span class="sxs-lookup"><span data-stu-id="a7e80-105">Windows Server Installation Guide</span></span>

<span data-ttu-id="a7e80-106">O Subsistema do Windows para Linux está disponível para instalação no Windows Server 2019 (versão 1709) e posterior.</span><span class="sxs-lookup"><span data-stu-id="a7e80-106">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="a7e80-107">Este guia explicará as etapas de habilitação do WSL em seu computador.</span><span class="sxs-lookup"><span data-stu-id="a7e80-107">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="a7e80-108">Habilitar o Subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="a7e80-108">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="a7e80-109">Para poder executar as distribuições do Linux no Windows, você deverá habilitar o recurso opcional "Subsistema do Windows para Linux" e reiniciar.</span><span class="sxs-lookup"><span data-stu-id="a7e80-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="a7e80-110">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="a7e80-110">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="a7e80-111">Baixar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="a7e80-111">Download a Linux distribution</span></span>

<span data-ttu-id="a7e80-112">Siga [estas instruções](install-manual.md) para baixar sua distribuição favorita do Linux.</span><span class="sxs-lookup"><span data-stu-id="a7e80-112">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="a7e80-113">Extrair e instalar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="a7e80-113">Extract and install a Linux distribution</span></span>

<span data-ttu-id="a7e80-114">Agora que você baixou uma distribuição do Linux, para extrair o conteúdo e instalá-lo manualmente, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="a7e80-114">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="a7e80-115">Extraia o conteúdo do pacote `<distro>.appx` usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a7e80-115">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="a7e80-116">Execute o aplicativo inicializador de distribuição na pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="a7e80-116">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="a7e80-117">O inicializador normalmente é chamado de `<distro>.exe` (por exemplo, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="a7e80-117">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Expansão da distribuição do Ubuntu no Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="a7e80-119">**Falha na instalação com o erro 0x8007007e**: Esse erro ocorre quando o sistema não é compatível com o WSL.</span><span class="sxs-lookup"><span data-stu-id="a7e80-119">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="a7e80-120">Garanta que você está executando o Windows Build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a7e80-120">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="a7e80-121">[Verifique seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="a7e80-121">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="a7e80-122">Certifique-se também de [confirmar se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled) e se o computador foi reiniciado após a habilitação do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7e80-122">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="a7e80-123">3. Adicione o caminho da distribuição ao caminho do ambiente do Windows (`C:\Users\Administrator\Ubuntu`, neste exemplo) usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a7e80-123">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="a7e80-124">Agora você pode iniciar sua distribuição em qualquer caminho digitando `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="a7e80-124">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="a7e80-125">Por exemplo: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="a7e80-125">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="a7e80-126">Agora que a distribuição está instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) antes de usar a distribuição.</span><span class="sxs-lookup"><span data-stu-id="a7e80-126">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
