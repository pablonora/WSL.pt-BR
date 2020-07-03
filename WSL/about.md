---
title: Uma visão geral do Subsistema do Windows para Linux
description: Saiba mais sobre o Subsistema do Windows para Linux, as diferentes versões e as maneiras pelas quais você pode usá-las.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 05/12/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 75da6389beec4af7ac684ec7ee2ef31431e14071
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336059"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a><span data-ttu-id="b231c-104">O que é o Subsistema do Windows para Linux?</span><span class="sxs-lookup"><span data-stu-id="b231c-104">What is the Windows Subsystem for Linux?</span></span>

<span data-ttu-id="b231c-105">O Subsistema do Windows para Linux permite que os desenvolvedores executem um ambiente GNU/Linux, incluindo a maioria das ferramentas de linha de comando, utilitários e aplicativos, diretamente no Windows, sem modificações e sem a sobrecarga de uma máquina virtual tradicional ou instalação dualboot.</span><span class="sxs-lookup"><span data-stu-id="b231c-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a traditional virtual machine or dualboot setup.</span></span>

<span data-ttu-id="b231c-106">Você pode:</span><span class="sxs-lookup"><span data-stu-id="b231c-106">You can:</span></span>

* <span data-ttu-id="b231c-107">Escolha sua distribuição do Linux/GNU favorita [na Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="b231c-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
* <span data-ttu-id="b231c-108">Execute as ferramentas de linha de comando comuns, como `grep`, `sed`, `awk` ou outros binários ELF-64.</span><span class="sxs-lookup"><span data-stu-id="b231c-108">Run common command-line tools such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span>
* <span data-ttu-id="b231c-109">Execute scripts de shell do Bash e aplicativos de linha de comando do GNU/Linux, incluindo:</span><span class="sxs-lookup"><span data-stu-id="b231c-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="b231c-110">Ferramentas: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="b231c-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="b231c-111">Linguagens: [Node.js](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go etc.</span><span class="sxs-lookup"><span data-stu-id="b231c-111">Languages: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="b231c-112">Serviços: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).</span><span class="sxs-lookup"><span data-stu-id="b231c-112">Services: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).</span></span>
* <span data-ttu-id="b231c-113">Instale o software adicional usando o gerenciador de pacotes de distribuição do GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="b231c-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
* <span data-ttu-id="b231c-114">Invoque aplicativos do Windows usando um shell de linha de comando do UNIX.</span><span class="sxs-lookup"><span data-stu-id="b231c-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
* <span data-ttu-id="b231c-115">Invoque aplicativos do GNU/Linux no Windows.</span><span class="sxs-lookup"><span data-stu-id="b231c-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="what-is-wsl-2"></a><span data-ttu-id="b231c-116">O que é o WSL 2?</span><span class="sxs-lookup"><span data-stu-id="b231c-116">What is WSL 2?</span></span>

<span data-ttu-id="b231c-117">O WSL 2 é uma nova versão da arquitetura do Subsistema do Windows para Linux que capacita o Subsistema do Windows para Linux a executar binários ELF64 Linux no Windows.</span><span class="sxs-lookup"><span data-stu-id="b231c-117">WSL 2 is a new version of the Windows Subsystem for Linux architecture that powers the Windows Subsystem for Linux to run ELF64 Linux binaries on Windows.</span></span> <span data-ttu-id="b231c-118">As metas principais dele são **aumentar o desempenho do sistema de arquivos** e adicionar **compatibilidade completa com a chamada do sistema**.</span><span class="sxs-lookup"><span data-stu-id="b231c-118">Its primary goals are to **increase file system performance**, as well as adding **full system call compatibility**.</span></span>

<span data-ttu-id="b231c-119">Essa nova arquitetura altera como esses binários do Linux interagem com o Windows e o hardware do computador, mas ainda fornece a mesma experiência do usuário que no WSL 1 (a versão atual amplamente disponível).</span><span class="sxs-lookup"><span data-stu-id="b231c-119">This new architecture changes how these Linux binaries interact with Windows and your computer's hardware, but still provides the same user experience as in WSL 1 (the current widely available version).</span></span>

<span data-ttu-id="b231c-120">As distribuições individuais do Linux podem ser executadas com a arquitetura do WSL 1 ou do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="b231c-120">Individual Linux distributions can be run with either the WSL 1 or WSL 2 architecture.</span></span> <span data-ttu-id="b231c-121">Cada distribuição pode passar por upgrade ou downgrade a qualquer momento e você pode executar distribuições do WSL 1 e do WSL 2 lado a lado.</span><span class="sxs-lookup"><span data-stu-id="b231c-121">Each distribution can be upgraded or downgraded at any time and you can run WSL 1 and WSL 2 distributions side by side.</span></span> <span data-ttu-id="b231c-122">O WSL 2 usa uma arquitetura totalmente nova que se beneficia do uso de um kernel Linux real.</span><span class="sxs-lookup"><span data-stu-id="b231c-122">WSL 2 uses an entirely new architecture that benefits from running a real Linux kernel.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b231c-123">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b231c-123">Next steps</span></span>

* [<span data-ttu-id="b231c-124">Instalar o WSL 1 e atualizar para o WSL 2</span><span class="sxs-lookup"><span data-stu-id="b231c-124">Install WSL 1 and update to WSL 2</span></span>](./install-win10.md)

* [<span data-ttu-id="b231c-125">Comparar o WSL 2 e o WSL 1</span><span class="sxs-lookup"><span data-stu-id="b231c-125">Compare WSL 2 and WSL 1</span></span>](./compare-versions.md)

* [<span data-ttu-id="b231c-126">Criar uma conta de usuário e uma senha para sua nova distribuição do Linux</span><span class="sxs-lookup"><span data-stu-id="b231c-126">Create a user account and password for your new Linux distribution</span></span>](./user-support.md)

* [<span data-ttu-id="b231c-127">Ler as perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="b231c-127">Read Frequently Asked Questions</span></span>](./faq.md)

* [<span data-ttu-id="b231c-128">Ler as perguntas frequentes sobre o WSL 2</span><span class="sxs-lookup"><span data-stu-id="b231c-128">Read Frequently Asked Questions about WSL 2</span></span>](./wsl2-faq.md)

* [<span data-ttu-id="b231c-129">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="b231c-129">Troubleshooting</span></span>](./troubleshooting.md)

* [<span data-ttu-id="b231c-130">Executar comandos de interoperabilidade entre o Windows e o Linux</span><span class="sxs-lookup"><span data-stu-id="b231c-130">Run interoperability commands between Windows and Linux</span></span>](./interop.md)

* [<span data-ttu-id="b231c-131">Executar comandos e configurações de inicialização</span><span class="sxs-lookup"><span data-stu-id="b231c-131">Run launch commands and configurations</span></span>](./wsl-config.md)

* [<span data-ttu-id="b231c-132">Configurar as permissões de arquivo</span><span class="sxs-lookup"><span data-stu-id="b231c-132">Set up file permissions</span></span>](./file-permissions.md)

* [<span data-ttu-id="b231c-133">Configurar o WSL para Empresas</span><span class="sxs-lookup"><span data-stu-id="b231c-133">Set up WSL for Enterprise</span></span>](./enterprise.md)

* [<span data-ttu-id="b231c-134">Comandos do WSL de referência</span><span class="sxs-lookup"><span data-stu-id="b231c-134">Reference WSL commands</span></span>](./reference.md)

* [<span data-ttu-id="b231c-135">Criar uma distribuição personalizada</span><span class="sxs-lookup"><span data-stu-id="b231c-135">Build a custom distributions</span></span>](./build-custom-distro.md)

* [<span data-ttu-id="b231c-136">Ler as notas sobre a versão do WSL</span><span class="sxs-lookup"><span data-stu-id="b231c-136">Read the WSL Release Notes</span></span>](./release-notes.md)
