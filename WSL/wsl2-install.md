---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: Instalar o BashOnWindows, bash, wsl, wsl2, windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10,
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038076"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="d12dc-104">Instruções de instalação do WSL 2</span><span class="sxs-lookup"><span data-stu-id="d12dc-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="d12dc-105">Para instalar e começar a usar o WSL 2 conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d12dc-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="d12dc-106">Ativar o componente opcional de 'Platform da máquina Virtual'</span><span class="sxs-lookup"><span data-stu-id="d12dc-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="d12dc-107">Defina uma distribuição que passarão por 2 WSL usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="d12dc-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="d12dc-108">Verifique se o que estão usando versões do WSL suas distribuições</span><span class="sxs-lookup"><span data-stu-id="d12dc-108">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="d12dc-109">Ativar o componente opcional de 'Platform da máquina Virtual'</span><span class="sxs-lookup"><span data-stu-id="d12dc-109">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="d12dc-110">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="d12dc-110">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="d12dc-111">Depois que essas alterações são habilitadas, você precisará reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="d12dc-111">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="d12dc-112">Defina uma distribuição que passarão por 2 WSL usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="d12dc-112">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="d12dc-113">Na execução do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d12dc-113">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="d12dc-114">e lembre-se de substituir `<Distro>` com o nome real da sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="d12dc-114">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="d12dc-115">(Você pode encontrá-las com o comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="d12dc-115">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="d12dc-116">Você pode alterar para 1 WSL na qualquer momento, executando o mesmo comando como mostrado acima, mas substituindo ' 2' com um ' 1'.</span><span class="sxs-lookup"><span data-stu-id="d12dc-116">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="d12dc-117">Além disso, se você quiser fazer WSL 2 a arquitetura padrão pode fazer isso com este comando:</span><span class="sxs-lookup"><span data-stu-id="d12dc-117">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="d12dc-118">Isso fará com que qualquer nova distribuição que você instale ser inicializada como uma distribuição WSL 2.</span><span class="sxs-lookup"><span data-stu-id="d12dc-118">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="d12dc-119">Concluir com verificando o que estão usando versões do WSL sua distribuição</span><span class="sxs-lookup"><span data-stu-id="d12dc-119">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="d12dc-120">Para verificar quais versões do WSL cada distribuição está usando usam o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d12dc-120">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="d12dc-121">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="d12dc-121">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="d12dc-122">A distribuição que você escolheu acima agora deve exibir um '2' na coluna 'version'.</span><span class="sxs-lookup"><span data-stu-id="d12dc-122">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="d12dc-123">Agora que você terminou fique à vontade começar a usar sua distribuição WSL 2!</span><span class="sxs-lookup"><span data-stu-id="d12dc-123">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 