---
title: Instalar o subsistema Linux no Windows Server
description: Instruções de instalação para o subsistema Linux no Windows Server.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Windows Server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269781"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="ba16f-104">Guia de instalação do Windows Server</span><span class="sxs-lookup"><span data-stu-id="ba16f-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="ba16f-105">Aplica-se ao Windows Server 2019 e posterior</span><span class="sxs-lookup"><span data-stu-id="ba16f-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="ba16f-106">Na//Build2017, a Microsoft anunciou que o subsistema do Windows para Linux estará [disponível no Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="ba16f-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="ba16f-107">Estas instruções demonstram como executar o subsistema do Windows para Linux no Windows Server 1709 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ba16f-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="ba16f-108">Habilitar o subsistema do Windows para Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="ba16f-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="ba16f-109">Para poder executar o Linux distribuições no Windows, você deve habilitar o recurso opcional "subsistema do Windows para Linux" e reinicializar.</span><span class="sxs-lookup"><span data-stu-id="ba16f-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="ba16f-110">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="ba16f-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="ba16f-111">Reinicie o computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="ba16f-111">Restart your computer when prompted.</span></span> <span data-ttu-id="ba16f-112">**Essa reinicialização é necessária** para garantir que o WSL possa iniciar um ambiente de execução confiável.</span><span class="sxs-lookup"><span data-stu-id="ba16f-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="ba16f-113">Baixar um distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="ba16f-113">Download a Linux distro</span></span>

<span data-ttu-id="ba16f-114">Siga [estas instruções](install-manual.md) para baixar sua distribuição do Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="ba16f-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="ba16f-115">Extrair e instalar um distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="ba16f-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="ba16f-116">Agora que você baixou um distribuição, Extraia seu conteúdo e instalou manualmente o distribuição:</span><span class="sxs-lookup"><span data-stu-id="ba16f-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="ba16f-117">Extraia `<distro>.appx` o conteúdo do pacote, por exemplo, usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ba16f-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="ba16f-118">Execute o iniciador distribuição para concluir a instalação, execute o aplicativo iniciador distribuição na pasta de `<distro>.exe`destino, denominada.</span><span class="sxs-lookup"><span data-stu-id="ba16f-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="ba16f-119">Por exemplo: `ubuntu.exe`, etc.</span><span class="sxs-lookup"><span data-stu-id="ba16f-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Expansão do Ubuntu distribuição no Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="ba16f-121">**Solução de problemas**</span><span class="sxs-lookup"><span data-stu-id="ba16f-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="ba16f-122">**A instalação falhou com o erro 0x8007007E**: Esse erro ocorre quando o sistema não dá suporte a WSL.</span><span class="sxs-lookup"><span data-stu-id="ba16f-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="ba16f-123">Certifique-se de que:</span><span class="sxs-lookup"><span data-stu-id="ba16f-123">Make sure that:</span></span>
    >   * <span data-ttu-id="ba16f-124">Você está executando o Windows Build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ba16f-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="ba16f-125">[Verifique sua compilação](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="ba16f-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="ba16f-126">O componente opcional do subsistema do Windows para Linux está habilitado e o computador foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="ba16f-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="ba16f-127">[Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="ba16f-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="ba16f-128">Adicione o caminho distribuição ao caminho do ambiente do Windows`C:\Users\Administrator\Ubuntu` (neste exemplo), por exemplo, usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ba16f-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="ba16f-129">Agora você pode iniciar o distribuição a partir de qualquer caminho `<distro>.exe`digitando.</span><span class="sxs-lookup"><span data-stu-id="ba16f-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="ba16f-130">Por exemplo: `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="ba16f-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="ba16f-131">Agora que seu distribuição do Linux está instalado, você deve [inicializar sua nova instância do distribuição](initialize-distro.md) antes de usar o distribuição.</span><span class="sxs-lookup"><span data-stu-id="ba16f-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
