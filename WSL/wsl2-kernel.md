---
title: Atualizando o kernel do Linux WSL 2
description: Instruções sobre como atualizar o kernel do WSL 2 Linux manualmente
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138185"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="de709-104">Atualizando o kernel do Linux WSL 2</span><span class="sxs-lookup"><span data-stu-id="de709-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="de709-105">Para atualizar manualmente o kernel do Linux dentro do WSL 2, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="de709-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="de709-106">Baixar o pacote de atualização do kernel do Linux</span><span class="sxs-lookup"><span data-stu-id="de709-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="de709-107">Clique neste [link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para baixar o pacote de atualização do kernel WSL2 Linux mais recente para computadores AMD64.</span><span class="sxs-lookup"><span data-stu-id="de709-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for AMD64 machines.</span></span>

> [!NOTE] <span data-ttu-id="de709-108">Se você estiver usando um computador ARM64, baixe [esse pacote](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="de709-108">if you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="de709-109">Instalar o pacote de atualização do kernel do Linux</span><span class="sxs-lookup"><span data-stu-id="de709-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="de709-110">Para instalar o pacote de atualização do kernel do Linux:</span><span class="sxs-lookup"><span data-stu-id="de709-110">To install the Linux kernel update package:</span></span>
    1. <span data-ttu-id="de709-111">Execute o pacote de atualização baixado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="de709-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="de709-112">Você será solicitado a fornecer permissões elevadas, selecione ' Sim ' para aprovar esta instalação.</span><span class="sxs-lookup"><span data-stu-id="de709-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="de709-113">Quando a instalação for concluída, você estará pronto para começar a usar o WSL2!</span><span class="sxs-lookup"><span data-stu-id="de709-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="de709-114">Planos futuros para atualizar o kernel do Linux WSL2</span><span class="sxs-lookup"><span data-stu-id="de709-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="de709-115">Para obter mais informações sobre essas alterações, leia [esta postagem do blog](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) no [blog da linha de comando do Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="de709-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>