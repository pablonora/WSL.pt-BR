---
title: Criar uma distribuição do Linux personalizada para WSL
description: Saiba como criar uma distribuição do Linux personalizada para o subsistema do Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema do windows, distribuição, personalizado
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063254"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="e956d-104">Criando uma distribuição do Linux personalizada para WSL</span><span class="sxs-lookup"><span data-stu-id="e956d-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="e956d-105">Use a nossa amostra WSL do código-fonte aberto para criar pacotes de distribuição do WSL para o Microsoft Store e/ou para criar pacotes personalizados de distribuição do Linux para o sideload.</span><span class="sxs-lookup"><span data-stu-id="e956d-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="e956d-106">Você pode encontrar o [repositório do iniciador de distribuição](https://github.com/Microsoft/WSL-DistroLauncher) no GitHub.</span><span class="sxs-lookup"><span data-stu-id="e956d-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="e956d-107">Este projeto permite:</span><span class="sxs-lookup"><span data-stu-id="e956d-107">This project enables:</span></span>
* <span data-ttu-id="e956d-108">Mantenedores da distribuição Linux para empacotar e enviar uma distribuição do Linux como um appx que é executado no WSL</span><span class="sxs-lookup"><span data-stu-id="e956d-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="e956d-109">Desenvolvedores criem distribuições do Linux personalizadas que podem ser carregado em seu computador de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="e956d-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="e956d-110">Histórico</span><span class="sxs-lookup"><span data-stu-id="e956d-110">Background</span></span>
<span data-ttu-id="e956d-111">Podemos distribuir distribuições do Linux para WSL como aplicativos de UWP por meio do Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="e956d-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="e956d-112">Você pode instalar esses aplicativos que serão executados, em seguida, no WSL - subsistema que se encontra no kernel do Windows.</span><span class="sxs-lookup"><span data-stu-id="e956d-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="e956d-113">Esse mecanismo de entrega traz muitos benefícios, conforme discutido em uma postagem de blog anterior.</span><span class="sxs-lookup"><span data-stu-id="e956d-113">This delivery mechanism has many benefits as discussed in an earlier blog post.</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="e956d-114">Sideload de um pacote de distribuição do Linux personalizado</span><span class="sxs-lookup"><span data-stu-id="e956d-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="e956d-115">Você pode criar um pacote de distribuição do Linux personalizado como um aplicativo para fazer sideload em seu computador pessoal.</span><span class="sxs-lookup"><span data-stu-id="e956d-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="e956d-116">Observe que seu pacote personalizado não seria distribuído por meio do Microsoft Store, a menos que você envia como um mantenedor de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e956d-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="e956d-117">Para configurar seu computador para fazer sideload dos aplicativos, você precisará habilitar isso nas configurações do sistema sob "Para desenvolvedores".</span><span class="sxs-lookup"><span data-stu-id="e956d-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="e956d-118">Certifique-se de ter o modo de desenvolvedor ou fazer sideload dos aplicativos selecionados</span><span class="sxs-lookup"><span data-stu-id="e956d-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="e956d-119">Para os mantenedores da distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="e956d-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="e956d-120">Para enviar para a Store, você precisará trabalhar para receber a aprovação para publicação.</span><span class="sxs-lookup"><span data-stu-id="e956d-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="e956d-121">Se você for um proprietário de distribuição de Linux interessado em Adicionar sua distribuição para a Microsoft Store, entre em contato com wslpartners@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e956d-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="e956d-122">Introdução</span><span class="sxs-lookup"><span data-stu-id="e956d-122">Getting Started</span></span>
<span data-ttu-id="e956d-123">Siga as instruções sobre o [repositório GitHub do iniciador de distribuição](https://github.com/Microsoft/WSL-DistroLauncher) para criar um pacote de distribuição do Linux personalizado.</span><span class="sxs-lookup"><span data-stu-id="e956d-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="e956d-124">Blogs da equipe</span><span class="sxs-lookup"><span data-stu-id="e956d-124">Team Blogs</span></span>
*  [<span data-ttu-id="e956d-125">Abra o fornecimento de uma amostra do WSL para mantenedores da distribuição de Linux e distribuições do Linux personalizada de Sideload</span><span class="sxs-lookup"><span data-stu-id="e956d-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="e956d-126">Blog de linha de comando</span><span class="sxs-lookup"><span data-stu-id="e956d-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="e956d-127">Envie comentários</span><span class="sxs-lookup"><span data-stu-id="e956d-127">Provide Feedback</span></span>
* [<span data-ttu-id="e956d-128">Repositório de distribuição iniciador Gitub</span><span class="sxs-lookup"><span data-stu-id="e956d-128">Distro Launcher Gitub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="e956d-129">Rastreador de problemas do GitHub para WSL</span><span class="sxs-lookup"><span data-stu-id="e956d-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="e956d-130">Portal de linha de comando do UserVoice</span><span class="sxs-lookup"><span data-stu-id="e956d-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
