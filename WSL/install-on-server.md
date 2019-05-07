---
title: Instale o subsistema do Linux no Windows Server
description: Instruções de instalação para o subsistema do Linux no Windows Server.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, do windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063614"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="cb7bb-104">Guia de instalação do Windows Server</span><span class="sxs-lookup"><span data-stu-id="cb7bb-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="cb7bb-105">Aplica-se ao Windows Server 2019 e posterior</span><span class="sxs-lookup"><span data-stu-id="cb7bb-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="cb7bb-106">No / / Build2017, a Microsoft anunciou que o subsistema do Windows para Linux serão [disponível no Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="cb7bb-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="cb7bb-107">Estas instruções explicam executando o subsistema Windows para Linux no Windows Server 1709 e posterior.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="cb7bb-108">Permitir que o subsistema Windows para Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="cb7bb-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="cb7bb-109">Antes de executar distribuições do Linux no Windows, você deve habilitar o recurso opcional de "Subsistema Windows para Linux" e reinicialize.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="cb7bb-110">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="cb7bb-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="cb7bb-111">Reinicie o computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-111">Restart your computer when prompted.</span></span> <span data-ttu-id="cb7bb-112">**Essa reinicialização é necessária** para garantir que o WSL pode iniciar um ambiente de execução confiável.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="cb7bb-113">Baixe uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="cb7bb-113">Download a Linux distro</span></span>

<span data-ttu-id="cb7bb-114">Siga [estas instruções](install-manual.md) para baixar sua distribuição do Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="cb7bb-115">Extrair e instalar uma distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="cb7bb-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="cb7bb-116">Agora que você baixou uma distribuição, extraia seu conteúdo e instalar manualmente a distribuição:</span><span class="sxs-lookup"><span data-stu-id="cb7bb-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="cb7bb-117">Extrair o `<distro>.appx` conteúdo do pacote, por exemplo, usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cb7bb-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. <span data-ttu-id="cb7bb-118">Execute o iniciador de distribuição para concluir a instalação, execute o aplicativo de iniciador de distribuição na pasta de destino, denominado `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="cb7bb-119">Por exemplo: `ubuntu.exe`, etc.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Distribuição expandida do Ubuntu no Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="cb7bb-121">**Solução de problemas**</span><span class="sxs-lookup"><span data-stu-id="cb7bb-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="cb7bb-122">**Falha na instalação com o erro 0x8007007e**: Esse erro ocorre quando o sistema não dá suporte a WSL.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="cb7bb-123">Certifique-se de que:</span><span class="sxs-lookup"><span data-stu-id="cb7bb-123">Make sure that:</span></span>
    >   * <span data-ttu-id="cb7bb-124">Você está executando o Windows build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="cb7bb-125">[Verificar seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="cb7bb-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="cb7bb-126">O subsistema do Windows para o componente opcional do Linux está habilitado e o computador for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="cb7bb-127">[Verifique se WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="cb7bb-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="cb7bb-128">Adicionar seu caminho de distribuição para o caminho de ambiente do Windows (`C:\Users\Administrator\Ubuntu` neste exemplo), por exemplo, usando o Powershell:</span><span class="sxs-lookup"><span data-stu-id="cb7bb-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="cb7bb-129">Agora você pode iniciar sua distribuição a partir de qualquer caminho digitando `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="cb7bb-130">Por exemplo: `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="cb7bb-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="cb7bb-131">Agora que sua distribuição do Linux é instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) antes de usar sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
