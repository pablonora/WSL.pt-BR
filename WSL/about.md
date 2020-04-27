---
title: Saiba mais sobre o Subsistema Windows para Linux
description: Saiba mais sobre como o Subsistema Windows para Linux funciona.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: fbb1ce5cf5d5c83e25d0a6a0cece7b70537a44a1
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "74200198"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="b0255-104">Documentação do Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="b0255-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="b0255-105">O Subsistema Windows para Linux permite que os desenvolvedores executem um ambiente GNU/Linux, incluindo a maioria das ferramentas de linha de comando, utilitários e aplicativos, diretamente no Windows, sem modificações e sem a sobrecarga de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0255-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="b0255-106">Você pode:</span><span class="sxs-lookup"><span data-stu-id="b0255-106">You can:</span></span>

1. <span data-ttu-id="b0255-107">Escolha sua distribuição do Linux/GNU favorita [na Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="b0255-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="b0255-108">Execute o software de linha de comando comum gratuito, como `grep`, `sed`, `awk` ou outros binários ELF-64.</span><span class="sxs-lookup"><span data-stu-id="b0255-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="b0255-109">Execute scripts de shell do Bash e aplicativos de linha de comando do GNU/Linux, incluindo:</span><span class="sxs-lookup"><span data-stu-id="b0255-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="b0255-110">Ferramentas: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="b0255-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="b0255-111">Linguagens: Javascript/Node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span><span class="sxs-lookup"><span data-stu-id="b0255-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="b0255-112">Serviços: SSHD, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="b0255-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="b0255-113">Instale o software adicional usando o gerenciador de pacotes de distribuição do GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="b0255-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="b0255-114">Invoque aplicativos do Windows usando um shell de linha de comando do UNIX.</span><span class="sxs-lookup"><span data-stu-id="b0255-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="b0255-115">Invoque aplicativos do GNU/Linux no Windows.</span><span class="sxs-lookup"><span data-stu-id="b0255-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="b0255-116">Introdução</span><span class="sxs-lookup"><span data-stu-id="b0255-116">Getting Started</span></span>

* [<span data-ttu-id="b0255-117">Instale o Linux no Windows 10</span><span class="sxs-lookup"><span data-stu-id="b0255-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="b0255-118">Visite a referência de comandos</span><span class="sxs-lookup"><span data-stu-id="b0255-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="b0255-119">Leia as perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="b0255-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="b0255-120">Blogs da equipe</span><span class="sxs-lookup"><span data-stu-id="b0255-120">Team Blogs</span></span>
*  [<span data-ttu-id="b0255-121">Postagem de visão geral com uma coleção de vídeos e blogs</span><span class="sxs-lookup"><span data-stu-id="b0255-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="b0255-122">[Blog de linha de comando](https://blogs.msdn.microsoft.com/commandline/) (ativo)</span><span class="sxs-lookup"><span data-stu-id="b0255-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="b0255-123">[Blog do Subsistema Windows para Linux](https://blogs.msdn.microsoft.com/wsl/) (histórico)</span><span class="sxs-lookup"><span data-stu-id="b0255-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="b0255-124">Postagens e artigos</span><span class="sxs-lookup"><span data-stu-id="b0255-124">Posts & Articles</span></span>
* [<span data-ttu-id="b0255-125">Execute o Bash do Ubuntu no Windows</span><span class="sxs-lookup"><span data-stu-id="b0255-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="b0255-126">Os desenvolvedores podem executar os binários do Bash e do UserMode do Ubuntu Linux no Windows 10</span><span class="sxs-lookup"><span data-stu-id="b0255-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="b0255-127">Ubuntu no Windows – o espaço do usuário do Ubuntu para desenvolvedores Windows</span><span class="sxs-lookup"><span data-stu-id="b0255-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="b0255-128">Envie comentários</span><span class="sxs-lookup"><span data-stu-id="b0255-128">Provide Feedback</span></span>
* [<span data-ttu-id="b0255-129">Rastreador de problemas do GitHub</span><span class="sxs-lookup"><span data-stu-id="b0255-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

