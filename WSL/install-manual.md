---
title: Baixar manualmente o subsistema do Windows para distribuições do Linux (WSL)
description: Instruções sobre como baixar manualmente o subsistema do Windows para distribuições do Linux.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, WSL, subsistema do windows, distribuição, ubuntu, openSUSE, kali SLES, debian,
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063564"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="8e773-104">Baixar manualmente o subsistema do Windows para pacotes de distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="8e773-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="8e773-105">Há vários cenários em que você pode não ser capaz de (ou deseja) para instalar as distribuições de Linux WSL por meio do Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="8e773-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="8e773-106">Especificamente, você pode estar executando um SKU de sistema operacional que não oferece suporte a Microsoft Store, ou suas políticas de rede corporativa e/ou administradores para não permitir o uso da Microsoft Store em seu ambiente de desktop manutenção de longo prazo (LTSB/LTSC) ou o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="8e773-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="8e773-107">Nesses casos, enquanto WSL em si estiver disponível, como você baixar e instalar distribuições do Linux no WSL se você não pode acessar o armazenamento?</span><span class="sxs-lookup"><span data-stu-id="8e773-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="8e773-108">Observação: **Ambientes de shell de linha de comando, incluindo distribuições de Linux/SWL, PowerShell e Cmd não têm permissão para executar no modo do Windows 10 S**.</span><span class="sxs-lookup"><span data-stu-id="8e773-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="8e773-109">Essa restrição existe para garantir que as metas de integridade e segurança de modo S oferece: Leia [esta postagem](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8e773-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="8e773-110">Baixando distribuições</span><span class="sxs-lookup"><span data-stu-id="8e773-110">Downloading distros</span></span>

<span data-ttu-id="8e773-111">Se o aplicativo Microsoft Store não estiver disponível, você pode baixar e instalar manualmente as distribuições de Linux clicando estes links:</span><span class="sxs-lookup"><span data-stu-id="8e773-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="8e773-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="8e773-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="8e773-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="8e773-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="8e773-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="8e773-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="8e773-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="8e773-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="8e773-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="8e773-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="8e773-117">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="8e773-117">OpenSUSE</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="8e773-118">SLES</span><span class="sxs-lookup"><span data-stu-id="8e773-118">SLES</span></span>](https://aka.ms/wsl-sles-12)

<span data-ttu-id="8e773-119">Isso fará com que o `<distro>.appx` pacotes para baixar uma pasta de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="8e773-119">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="8e773-120">Siga as [instruções de instalação](#installing-your-distro) para instalar seu distro(s) baixado.</span><span class="sxs-lookup"><span data-stu-id="8e773-120">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="8e773-121">Download de Distribuições por meio da linha de comando</span><span class="sxs-lookup"><span data-stu-id="8e773-121">Downloading distros via the command line</span></span>
<span data-ttu-id="8e773-122">Se você preferir, você também pode baixar o distro(s) preferido por meio da linha de comando:</span><span class="sxs-lookup"><span data-stu-id="8e773-122">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="8e773-123">Baixe usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="8e773-123">Download using PowerShell</span></span>
 <span data-ttu-id="8e773-124">Para baixar as distribuições usando o PowerShell, use o [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e773-124">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="8e773-125">Aqui está um exemplo de instrução para baixar o Ubuntu 16.04.</span><span class="sxs-lookup"><span data-stu-id="8e773-125">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="8e773-126">Se o download estiver demorando muito tempo, desativar a barra de progresso, definindo `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="8e773-126">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="8e773-127">Baixe usando o curl</span><span class="sxs-lookup"><span data-stu-id="8e773-127">Download using curl</span></span>
<span data-ttu-id="8e773-128">Atualização do Windows 10 primavera 2018 (ou posterior) inclui a popular [curl do utilitário de linha de comando](https://curl.haxx.se/) com a qual você pode invocar as solicitações da web (ou seja, HTTP GET, POST, PUT, comandos etc.) na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="8e773-128">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="8e773-129">Você pode usar `curl.exe` para baixar as distribuições acima:</span><span class="sxs-lookup"><span data-stu-id="8e773-129">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="8e773-130">No exemplo acima, `curl.exe` é executado (não apenas `curl`) garantir que, no PowerShell, o executável real curl invocado, não a rotação do PowerShell para o alias [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="8e773-130">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="8e773-131">Observação: Usando o `curl` pode ser preferível se você precisar invocar/script as etapas de download usando o shell de Cmd e/ou `.bat`  /  `.cmd` scripts.</span><span class="sxs-lookup"><span data-stu-id="8e773-131">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="8e773-132">Instalando sua distribuição</span><span class="sxs-lookup"><span data-stu-id="8e773-132">Installing your distro</span></span>
<span data-ttu-id="8e773-133">Para obter instruções sobre como instalar seu distro(s) baixado, consulte o [área de trabalho do Windows](install-win10.md) ou [do Windows Server](install-on-server.md) instruções de instalação.</span><span class="sxs-lookup"><span data-stu-id="8e773-133">For instructions on how to install your downloaded distro(s), please refer to the [Windows Desktop](install-win10.md) or [Windows Server](install-on-server.md) installation instructions.</span></span>
