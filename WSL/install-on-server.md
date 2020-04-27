---
title: Instalar o Subsistema Linux no Windows Server
description: Instruções de instalação para o Subsistema Linux no Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema do windows para linux, windowssubsystem, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256389"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="e2ee1-104">Guia de instalação do Windows Server</span><span class="sxs-lookup"><span data-stu-id="e2ee1-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="e2ee1-105">Aplica-se ao Windows Server 2019 e posteriores</span><span class="sxs-lookup"><span data-stu-id="e2ee1-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="e2ee1-106">No //Build2017, a Microsoft anunciou que o Subsistema do Windows para Linux estará [disponível no Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="e2ee1-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="e2ee1-107">Essas instruções demonstram como executar o Subsistema do Windows para Linux no Windows Server 1709 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="e2ee1-108">Habilitar o WSL (Subsistema do Windows para Linux)</span><span class="sxs-lookup"><span data-stu-id="e2ee1-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="e2ee1-109">Para poder executar as distribuições do Linux no Windows, você deverá habilitar o recurso opcional "Subsistema do Windows para Linux" e reiniciar.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="e2ee1-110">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="e2ee1-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="e2ee1-111">Reinicie seu computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-111">Restart your computer when prompted.</span></span> <span data-ttu-id="e2ee1-112">**Essa reinicialização é necessária** para que o WSL possa ser iniciado em um ambiente de execução confiável.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="e2ee1-113">Baixar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="e2ee1-113">Download a Linux distro</span></span>

<span data-ttu-id="e2ee1-114">Siga [estas instruções](install-manual.md) para baixar sua distribuição favorita do Linux.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="e2ee1-115">Extrair e instalar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="e2ee1-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="e2ee1-116">Agora que você baixou uma distribuição, extraia o conteúdo dela e instale-a manualmente:</span><span class="sxs-lookup"><span data-stu-id="e2ee1-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="e2ee1-117">Extraia o conteúdo `<distro>.appx` do pacote, por exemplo, usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e2ee1-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="e2ee1-118">Execute o inicializador da distribuição para concluir a instalação e execute o aplicativo inicializador da distribuição na pasta de destino, denominada `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="e2ee1-119">Por exemplo: `ubuntu.exe` etc.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Expansão da distribuição do Ubuntu no Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="e2ee1-121">**Solução de problemas**</span><span class="sxs-lookup"><span data-stu-id="e2ee1-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="e2ee1-122">**Falha na instalação com o erro 0x8007007e**: Esse erro ocorre quando o sistema não é compatível com o WSL.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="e2ee1-123">Certifique-se de que:</span><span class="sxs-lookup"><span data-stu-id="e2ee1-123">Make sure that:</span></span>
    >   * <span data-ttu-id="e2ee1-124">Você está executando o Windows Build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="e2ee1-125">[Verifique seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="e2ee1-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="e2ee1-126">O componente opcional do Subsistema Windows para Linux está habilitado e o computador foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="e2ee1-127">[Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="e2ee1-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="e2ee1-128">Adicione o caminho da distribuição ao caminho do ambiente do Windows (`C:\Users\Administrator\Ubuntu`, neste exemplo), por exemplo, usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e2ee1-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="e2ee1-129">Agora você pode iniciar a distribuição em qualquer caminho digitando `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="e2ee1-130">Por exemplo: `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="e2ee1-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="e2ee1-131">Agora que a distribuição do Linux está instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) antes de usar sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="e2ee1-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
