---
title: Atualizar o kernel do WSL 2 Linux
description: Instruções sobre como atualizar o kernel do WSL 2 Linux manualmente
keywords: wsl, windows, linux kernel, windows subsystem for linux, kernel
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 1628bea2f1bae590928b055425413e5b085dffef
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153047"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="1eb99-104">Atualizar o kernel do WSL 2 Linux</span><span class="sxs-lookup"><span data-stu-id="1eb99-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="1eb99-105">Para atualizar manualmente o kernel do Linux dentro do WSL2, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="1eb99-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="1eb99-106">Se o instalador não conseguir encontrar a WSL 1, clique com o botão direito do mouse no instalador de atualização do kernel do Linux e pressione "Desinstalar", então execute novamente o instalador.</span><span class="sxs-lookup"><span data-stu-id="1eb99-106">If the installer can't find WSL 1, right-click the Linux kernel update installer and press "Uninstall", then rerun the installer.</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="1eb99-107">Baixar o pacote de atualização do kernel do Linux</span><span class="sxs-lookup"><span data-stu-id="1eb99-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="1eb99-108">[Baixe o pacote de atualização do último kernel do Linux para o WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para computadores x64.</span><span class="sxs-lookup"><span data-stu-id="1eb99-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="1eb99-109">Se estiver usando um computador ARM64, baixe o [pacote ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).</span><span class="sxs-lookup"><span data-stu-id="1eb99-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="1eb99-110">Instalar o pacote de atualização do kernel do Linux</span><span class="sxs-lookup"><span data-stu-id="1eb99-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="1eb99-111">Para instalar o pacote de atualização do kernel do Linux:</span><span class="sxs-lookup"><span data-stu-id="1eb99-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="1eb99-112">Execute o pacote de atualização baixado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="1eb99-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="1eb99-113">Você receberá uma solicitação para fornecer permissões elevadas, selecione 'Sim' para aprovar essa instalação.</span><span class="sxs-lookup"><span data-stu-id="1eb99-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="1eb99-114">Quando a instalação for concluída, você estará pronto para começar a usar o WSL2!</span><span class="sxs-lookup"><span data-stu-id="1eb99-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="1eb99-115">Planos futuros para atualizar o kernel do WSL2 Linux</span><span class="sxs-lookup"><span data-stu-id="1eb99-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="1eb99-116">Para obter mais informações, leia o artigo [Alterações na atualização do kernel do Linux para o WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponível no [blog da linha de comando do Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="1eb99-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
