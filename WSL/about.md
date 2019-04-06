---
title: Saiba mais sobre o subsistema Windows para Linux
description: Saiba mais sobre como funciona o subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: a9c8d32f2b87319b45b1b757b4d71c0a4c41292c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063504"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="14db7-104">Subsistema do Windows para obter a documentação do Linux</span><span class="sxs-lookup"><span data-stu-id="14db7-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="14db7-105">O subsistema Windows para Linux permite que os desenvolvedores execute ambiente GNU/Linux – incluindo ferramentas, utilitários e aplicativos de linha de comando mais – diretamente no Windows, sem modificações, sem a sobrecarga de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="14db7-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="14db7-106">Você pode:</span><span class="sxs-lookup"><span data-stu-id="14db7-106">You can:</span></span>

1. <span data-ttu-id="14db7-107">Escolha suas distribuições favoritas do GNU/Linux [da Windows Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="14db7-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="14db7-108">Executar o software livre de linha de comando comuns, como `grep`, `sed`, `awk`, ou outros binários ELF-64.</span><span class="sxs-lookup"><span data-stu-id="14db7-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="14db7-109">Executar scripts de shell do Bash e aplicativos de linha de comando do GNU/Linux incluindo:</span><span class="sxs-lookup"><span data-stu-id="14db7-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="14db7-110">Ferramentas: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="14db7-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="14db7-111">Idiomas: JavaScript/Node.js, Ruby, Python, C/C++, C# & F#, confiar, Go, etc.</span><span class="sxs-lookup"><span data-stu-id="14db7-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="14db7-112">Services: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="14db7-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="14db7-113">Instale software adicional com o próprio Gerenciador de pacotes de distribuição de GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="14db7-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="14db7-114">Invocar aplicativos do Windows usando o shell de linha de comando Unix-like.</span><span class="sxs-lookup"><span data-stu-id="14db7-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="14db7-115">Chama aplicativos de GNU/Linux no Windows.</span><span class="sxs-lookup"><span data-stu-id="14db7-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="14db7-116">Introdução</span><span class="sxs-lookup"><span data-stu-id="14db7-116">Getting started</span></span>

* [<span data-ttu-id="14db7-117">Instalar o Linux no Windows</span><span class="sxs-lookup"><span data-stu-id="14db7-117">Install Linux on Windows</span></span>](install_guide.md)
* [<span data-ttu-id="14db7-118">Visite a referência de comando</span><span class="sxs-lookup"><span data-stu-id="14db7-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="14db7-119">Perguntas frequentes de leitura</span><span class="sxs-lookup"><span data-stu-id="14db7-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="14db7-120">Blogs da equipe</span><span class="sxs-lookup"><span data-stu-id="14db7-120">Team Blogs</span></span>
*  [<span data-ttu-id="14db7-121">Visão geral de post com uma coleção de vídeos e blogs</span><span class="sxs-lookup"><span data-stu-id="14db7-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="14db7-122">[Blog de linha de comando](https://blogs.msdn.microsoft.com/commandline/) (ativo)</span><span class="sxs-lookup"><span data-stu-id="14db7-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="14db7-123">[Subsistema do Windows para Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (históricas)</span><span class="sxs-lookup"><span data-stu-id="14db7-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="14db7-124">Postagens & artigos</span><span class="sxs-lookup"><span data-stu-id="14db7-124">Posts & Articles</span></span>
* [<span data-ttu-id="14db7-125">Executar Bash do Ubuntu no Windows</span><span class="sxs-lookup"><span data-stu-id="14db7-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="14db7-126">Os desenvolvedores pudessem executá Usermode Ubuntu Linux binários e Bash no Windows 10</span><span class="sxs-lookup"><span data-stu-id="14db7-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="14db7-127">Ubuntu no Windows – Userspace o Ubuntu para desenvolvedores do Windows</span><span class="sxs-lookup"><span data-stu-id="14db7-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="14db7-128">Envie comentários</span><span class="sxs-lookup"><span data-stu-id="14db7-128">Provide Feedback</span></span>
* [<span data-ttu-id="14db7-129">Rastreador de problemas do GitHub</span><span class="sxs-lookup"><span data-stu-id="14db7-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="14db7-130">Portal de linha de comando do UserVoice</span><span class="sxs-lookup"><span data-stu-id="14db7-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
