---
title: Saiba mais sobre o subsistema do Windows para Linux
description: Saiba mais sobre como funciona o subsistema do Windows para Linux.
keywords: BashOnWindows, Bash, WSL, Windows, windowssubsystem, GNU, Linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: edff78b1447aa382253417d27df52fe497c58b08
ms.sourcegitcommit: e17038c166b69f73e593ae3ac351c9d66e2ba64b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67694622"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="89627-104">Documentação do subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="89627-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="89627-105">O subsistema do Windows para Linux permite que os desenvolvedores executem um ambiente GNU/Linux, incluindo a maioria das ferramentas de linha de comando, utilitários e aplicativos, diretamente no Windows, sem a sobrecarga de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="89627-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="89627-106">Você pode:</span><span class="sxs-lookup"><span data-stu-id="89627-106">You can:</span></span>

1. <span data-ttu-id="89627-107">Escolha suas distribuições do GNU/Linux favoritas [no Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="89627-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="89627-108">Execute software de linha de comando comum gratuito, `grep`como `sed` `awk`,, ou outros binários ELF-64.</span><span class="sxs-lookup"><span data-stu-id="89627-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="89627-109">Execute scripts de shell bash e aplicativos de linha de comando GNU/Linux, incluindo:</span><span class="sxs-lookup"><span data-stu-id="89627-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="89627-110">Ferramentas: vim, Emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="89627-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="89627-111">Idiomas: JavaScript/node. js, Ruby, Python, C/C++, C# & F#, Rust, go, etc.</span><span class="sxs-lookup"><span data-stu-id="89627-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="89627-112">Serviços: sshd, MySQL, Apache, Lighttpd</span><span class="sxs-lookup"><span data-stu-id="89627-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="89627-113">Instale o software adicional usando o Gerenciador de pacotes de distribuição GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="89627-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="89627-114">Invocar aplicativos do Windows usando um shell de linha de comando do UNIX.</span><span class="sxs-lookup"><span data-stu-id="89627-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="89627-115">Invocar aplicativos GNU/Linux no Windows.</span><span class="sxs-lookup"><span data-stu-id="89627-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="89627-116">Guia de Introdução</span><span class="sxs-lookup"><span data-stu-id="89627-116">Getting Started</span></span>

* [<span data-ttu-id="89627-117">Instalar o Linux no Windows 10</span><span class="sxs-lookup"><span data-stu-id="89627-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="89627-118">Visite a referência de comando</span><span class="sxs-lookup"><span data-stu-id="89627-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="89627-119">Leia as perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="89627-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="89627-120">Blogs da equipe</span><span class="sxs-lookup"><span data-stu-id="89627-120">Team Blogs</span></span>
*  [<span data-ttu-id="89627-121">Postagem de visão geral com uma coleção de vídeos e Blogs</span><span class="sxs-lookup"><span data-stu-id="89627-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="89627-122">[Blog de linha de comando](https://blogs.msdn.microsoft.com/commandline/) Activo</span><span class="sxs-lookup"><span data-stu-id="89627-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="89627-123">[Blog do subsistema do Windows para Linux](https://blogs.msdn.microsoft.com/wsl/) Histórico</span><span class="sxs-lookup"><span data-stu-id="89627-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="89627-124">Posta & artigos</span><span class="sxs-lookup"><span data-stu-id="89627-124">Posts & Articles</span></span>
* [<span data-ttu-id="89627-125">Execute o bash no Ubuntu no Windows</span><span class="sxs-lookup"><span data-stu-id="89627-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="89627-126">Os desenvolvedores podem executar os binários bash e UserMode Ubuntu Linux no Windows 10</span><span class="sxs-lookup"><span data-stu-id="89627-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="89627-127">Ubuntu no Windows – o espaço de logon do Ubuntu para desenvolvedores do Windows</span><span class="sxs-lookup"><span data-stu-id="89627-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="89627-128">Envie comentários</span><span class="sxs-lookup"><span data-stu-id="89627-128">Provide Feedback</span></span>
* [<span data-ttu-id="89627-129">Rastreador de problemas do GitHub</span><span class="sxs-lookup"><span data-stu-id="89627-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="89627-130">Portal do UserVoice de linha de comando</span><span class="sxs-lookup"><span data-stu-id="89627-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
