---
title: Baixar manualmente o subsistema do Windows para Linux (WSL) distribuições
description: Instruções sobre como baixar manualmente o subsistema do Windows para distribuições do Linux.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema do Windows para Linux, WSL, subsistema do Windows, distribuição, Ubuntu, openSUSE, SLES, Debian, Kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: aa0b42748115045105bb4e6eae91493bfee11d09
ms.sourcegitcommit: 467b6c8e9716d1a60dbf9f7658fd9579da365b58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2020
ms.locfileid: "77624920"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="3076c-104">Baixar manualmente os pacotes do subsistema do Windows para Linux distribuição</span><span class="sxs-lookup"><span data-stu-id="3076c-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="3076c-105">Há vários cenários nos quais você pode não ser possível (ou deseja) instalar o WSL Linux distribuições por meio do Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="3076c-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="3076c-106">Especificamente, você pode estar executando um SKU de sistema operacional de área de trabalho do Windows Server ou de LTSC (manutenção de longo prazo) que não dá suporte a Microsoft Store, ou suas políticas de rede corporativa e/ou administradores para não permitir o uso de Microsoft Store em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="3076c-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="3076c-107">Nesses casos, embora o WSL em si esteja disponível, como baixar e instalar o Linux distribuições no WSL se você não puder acessar o armazenamento?</span><span class="sxs-lookup"><span data-stu-id="3076c-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="3076c-108">Observação: os **ambientes de Shell de linha de comando, incluindo cmd, PowerShell e Linux/WSL distribuições, não têm permissão para serem executados no modo Windows 10 S**.</span><span class="sxs-lookup"><span data-stu-id="3076c-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="3076c-109">Essa restrição existe para garantir a integridade e os objetivos de segurança que o modo S fornece: leia [esta postagem](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3076c-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="3076c-110">Baixando o distribuições</span><span class="sxs-lookup"><span data-stu-id="3076c-110">Downloading distros</span></span>

<span data-ttu-id="3076c-111">Se o aplicativo Microsoft Store não estiver disponível, você poderá baixar e instalar manualmente o distribuições do Linux clicando nestes links:</span><span class="sxs-lookup"><span data-stu-id="3076c-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
<!-- * [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm) -->
* <span data-ttu-id="3076c-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="3076c-112">Ubuntu 18.04</span></span>
* <span data-ttu-id="3076c-113">Ubuntu 18, 4 ARM</span><span class="sxs-lookup"><span data-stu-id="3076c-113">Ubuntu 18.04 ARM</span></span>
* [<span data-ttu-id="3076c-114">Ubuntu 16, 4</span><span class="sxs-lookup"><span data-stu-id="3076c-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="3076c-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="3076c-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="3076c-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="3076c-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="3076c-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="3076c-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="3076c-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="3076c-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="3076c-119">Fedora Remix para WSL</span><span class="sxs-lookup"><span data-stu-id="3076c-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="3076c-120">Isso fará com que os pacotes de `<distro>.appx` sejam baixados em uma pasta de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="3076c-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="3076c-121">Siga as [instruções de instalação](#installing-your-distro) para instalar suas distribuiçãos baixadas.</span><span class="sxs-lookup"><span data-stu-id="3076c-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="3076c-122">Baixando o distribuições por meio da linha de comando</span><span class="sxs-lookup"><span data-stu-id="3076c-122">Downloading distros via the command line</span></span>
<span data-ttu-id="3076c-123">Se preferir, você também pode baixar seus distribuição (s) preferenciais por meio da linha de comando:</span><span class="sxs-lookup"><span data-stu-id="3076c-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="3076c-124">Baixar usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="3076c-124">Download using PowerShell</span></span>
 <span data-ttu-id="3076c-125">Para baixar o distribuições usando o PowerShell, use o cmdlet [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) .</span><span class="sxs-lookup"><span data-stu-id="3076c-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="3076c-126">Aqui está um exemplo de instrução para baixar o Ubuntu 16, 4.</span><span class="sxs-lookup"><span data-stu-id="3076c-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="3076c-127">Se o download estiver demorando muito, desative a barra de progresso definindo `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="3076c-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="3076c-128">Baixar usando ondulação</span><span class="sxs-lookup"><span data-stu-id="3076c-128">Download using curl</span></span>
<span data-ttu-id="3076c-129">A atualização do Windows 10 Spring 2018 (ou posterior) inclui o [Utilitário de linha de comando de ondulação](https://curl.haxx.se/) popular com o qual você pode invocar solicitações da Web (ou seja, comandos http Get, post, put, etc.) da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="3076c-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="3076c-130">Você pode usar `curl.exe` para baixar o distribuições acima:</span><span class="sxs-lookup"><span data-stu-id="3076c-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="3076c-131">No exemplo acima, `curl.exe` é executado (não apenas `curl`) para garantir que, no PowerShell, o executável de ondulação real seja invocado, não o alias de ondulação do PowerShell para [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="3076c-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="3076c-132">Observação: o uso de `curl` pode ser preferível se você precisar invocar/gerar script de etapas de download usando o shell cmd e/ou `.bat` / scripts `.cmd`.</span><span class="sxs-lookup"><span data-stu-id="3076c-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="3076c-133">Instalando seu distribuição</span><span class="sxs-lookup"><span data-stu-id="3076c-133">Installing your distro</span></span>
<span data-ttu-id="3076c-134">Se você estiver usando o Windows 10, poderá instalar o distribuição com o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3076c-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="3076c-135">Basta navegar para a pasta que contém o distribuição baixado acima e, nesse diretório, execute o comando a seguir, em que `app_name` é o nome do seu arquivo distribuição. Appx.</span><span class="sxs-lookup"><span data-stu-id="3076c-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="3076c-136">Se você estiver usando o Windows Server, poderá encontrar as instruções de instalação na página de documentação do [Windows Server](install-on-server.md) .</span><span class="sxs-lookup"><span data-stu-id="3076c-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="3076c-137">Depois de instalar o distribuição, consulte a página [etapas de inicialização](initialize-distro.md) para inicializar o novo distribuição.</span><span class="sxs-lookup"><span data-stu-id="3076c-137">Once your distro is installed please refer to the [Initialization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
