---
title: Perguntas frequentes (FAQ)
description: Perguntas frequentes sobre o subsistema do Windows para Linux.
keywords: BashOnWindows, Bash, WSL, Windows, windowssubsystem, perguntas frequentes
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: e3376f8dff83262577bc52fb3ac368b70b21d922
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122761"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="66b99-104">Perguntas frequentes sobre o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="66b99-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="66b99-105">O que é o subsistema do Windows para Linux (WSL)?</span><span class="sxs-lookup"><span data-stu-id="66b99-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="66b99-106">O subsistema do Windows para Linux (WSL) é um novo recurso do Windows 10 que permite executar ferramentas de linha de comando nativas do Linux diretamente no Windows, juntamente com seus aplicativos tradicionais de área de trabalho do Windows e da loja moderna.</span><span class="sxs-lookup"><span data-stu-id="66b99-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="66b99-107">Consulte a [página sobre](./about.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="66b99-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="66b99-108">Quem é WSL?</span><span class="sxs-lookup"><span data-stu-id="66b99-108">Who is WSL for?</span></span>
<span data-ttu-id="66b99-109">Isso é basicamente uma ferramenta para desenvolvedores – especialmente desenvolvedores da Web e aqueles que trabalham em ou com projetos de software livre.</span><span class="sxs-lookup"><span data-stu-id="66b99-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="66b99-110">Isso permite que aqueles que desejam/precisem usar bash, ferramentas`sed`comuns `awk`do Linux (, etc.) e muitas ferramentas do Linux (Ruby, Python, etc.) para usar seus ferramentas no Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="66b99-111">O que posso fazer com o WSL?</span><span class="sxs-lookup"><span data-stu-id="66b99-111">What can I do with WSL?</span></span>
<span data-ttu-id="66b99-112">O WSL fornece um aplicativo chamado bash. exe que, quando iniciado, abre um console do Windows que executa o shell bash.</span><span class="sxs-lookup"><span data-stu-id="66b99-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="66b99-113">Usando o bash, você pode executar aplicativos e ferramentas de linha de comando do Linux.</span><span class="sxs-lookup"><span data-stu-id="66b99-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="66b99-114">Por exemplo, digite `lsb_release -a` e pressione Enter. você verá os detalhes do distribuição do Linux em execução no momento:</span><span class="sxs-lookup"><span data-stu-id="66b99-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![Captura de tela de detalhes do distribuição](media/distro.png)

<span data-ttu-id="66b99-116">Você também pode acessar o sistema de arquivos do computador local de dentro do shell do Linux bash – você encontrará as unidades locais `/mnt` montadas na pasta.</span><span class="sxs-lookup"><span data-stu-id="66b99-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="66b99-117">Por exemplo, sua `C:` unidade está montada `/mnt/c`em:</span><span class="sxs-lookup"><span data-stu-id="66b99-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![Captura de tela da unidade C montada](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="66b99-119">O que é bash?</span><span class="sxs-lookup"><span data-stu-id="66b99-119">What is Bash?</span></span>
<span data-ttu-id="66b99-120">O [bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) é um shell baseado em texto popular e linguagem de comando.</span><span class="sxs-lookup"><span data-stu-id="66b99-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="66b99-121">É o shell padrão incluído no Ubuntu e em outros distribuições do Linux e no macOS.</span><span class="sxs-lookup"><span data-stu-id="66b99-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="66b99-122">Os usuários digitam comandos em um shell para executar scripts e/ou executar comandos e ferramentas para realizar muitas tarefas.</span><span class="sxs-lookup"><span data-stu-id="66b99-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="66b99-123">Como isso funciona?</span><span class="sxs-lookup"><span data-stu-id="66b99-123">How does this work?</span></span>
<span data-ttu-id="66b99-124">Confira nosso [blog](https://blogs.msdn.microsoft.com/wsl/) onde entramos em detalhes sobre a tecnologia subjacente.</span><span class="sxs-lookup"><span data-stu-id="66b99-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="66b99-125">Por que usar WSL em vez do Linux em uma VM?</span><span class="sxs-lookup"><span data-stu-id="66b99-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="66b99-126">O WSL requer menos recursos (CPU, memória e armazenamento) do que uma máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="66b99-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="66b99-127">O WSL também permite que você execute aplicativos e ferramentas de linha de comando do Linux juntamente com os aplicativos de linha de comando, área de trabalho e da loja do Windows e para acessar os arquivos do Windows de dentro do Linux.</span><span class="sxs-lookup"><span data-stu-id="66b99-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="66b99-128">Isso permite que você use aplicativos do Windows e ferramentas de linha de comando do Linux no mesmo conjunto de arquivos, se desejar.</span><span class="sxs-lookup"><span data-stu-id="66b99-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="66b99-129">Por que eu usaria, por exemplo, Ruby no Linux em vez de no Windows?</span><span class="sxs-lookup"><span data-stu-id="66b99-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="66b99-130">Algumas ferramentas de plataforma cruzada foram criadas supondo que o ambiente no qual elas são executadas se comporta como o Linux.</span><span class="sxs-lookup"><span data-stu-id="66b99-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="66b99-131">Por exemplo, algumas ferramentas pressupõem que elas sejam capazes de acessar caminhos de arquivo muito longos ou que arquivos/pastas específicos existam.</span><span class="sxs-lookup"><span data-stu-id="66b99-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="66b99-132">Isso geralmente causa problemas no Windows que, com freqüência, se comporta de forma diferente do Linux.</span><span class="sxs-lookup"><span data-stu-id="66b99-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="66b99-133">Muitas linguagens, como Ruby e node, costumam ser modeladas e funcionam muito bem no Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="66b99-134">No entanto, nem todos os proprietários do gem Ruby ou do node/NPM library têm suas bibliotecas para dar suporte ao Windows e muitos têm dependências específicas do Linux.</span><span class="sxs-lookup"><span data-stu-id="66b99-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="66b99-135">Isso geralmente pode resultar em sistemas criados usando tais ferramentas e bibliotecas que estão sofrendo de compilação e, às vezes, erros de tempo de execução ou comportamentos indesejados no Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="66b99-136">Esses são apenas alguns dos problemas que fizeram com que muitas pessoas perguntassem à Microsoft para aprimorar as ferramentas de linha de comando do Windows e o que nos levou para fazer parcerias com o Canonical para habilitar as ferramentas de linha de comando do Linux e bash nativas para serem executadas no Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="66b99-137">O que isso significa para o PowerShell?</span><span class="sxs-lookup"><span data-stu-id="66b99-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="66b99-138">Ao trabalhar com projetos OSS, há inúmeros cenários em que é imensamente útil entrar em bash a partir de um prompt do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="66b99-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="66b99-139">O suporte para bash é complementar e fortalece o valor da linha de comando no Windows, permitindo que o PowerShell e a Comunidade do PowerShell aproveitem outras tecnologias populares.</span><span class="sxs-lookup"><span data-stu-id="66b99-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="66b99-140">Leia mais no blog da equipe do PowerShell – [bash para Windows: Por que é incrível e o que significa para o PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="66b99-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="66b99-141">Posso executar todos os aplicativos do Linux no WSL?</span><span class="sxs-lookup"><span data-stu-id="66b99-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="66b99-142">Não!</span><span class="sxs-lookup"><span data-stu-id="66b99-142">No!</span></span> <span data-ttu-id="66b99-143">WSL é uma ferramenta voltada para permitir que os usuários que precisam deles executem ferramentas de linha de comando bash e Core Linux no Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="66b99-144">O WSL não dá suporte a áreas de trabalho de GUI ou aplicativos (por exemplo, GNOME, KDE, etc.)</span><span class="sxs-lookup"><span data-stu-id="66b99-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="66b99-145">Além disso, embora você possa executar muitos aplicativos de servidor populares (por exemplo, Redis), não recomendamos o WSL para hospedar serviços de produção – a Microsoft oferece uma variedade de soluções para executar cargas de trabalho de produção do Linux no Azure, no Hyper-V e no Docker.</span><span class="sxs-lookup"><span data-stu-id="66b99-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="66b99-146">Em quais SKUs do Windows o WSL está incluído?</span><span class="sxs-lookup"><span data-stu-id="66b99-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="66b99-147">O subsistema do Windows para Linux está disponível na versão de área de trabalho do Windows para a atualização de aniversários e criadores do Windows 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="66b99-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="66b99-148">A partir dos criadores de outono, a atualização WSL estará disponível nas SKUs de desktop e de servidor do Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="66b99-149">A quais processadores o WSL dá suporte?</span><span class="sxs-lookup"><span data-stu-id="66b99-149">What processors does WSL support?</span></span>
<span data-ttu-id="66b99-150">O WSL dá suporte a CPUs x64 e ARM.</span><span class="sxs-lookup"><span data-stu-id="66b99-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="66b99-151">Como fazer acessar minha unidade C:?</span><span class="sxs-lookup"><span data-stu-id="66b99-151">How do I access my C: drive?</span></span>
<span data-ttu-id="66b99-152">Pontos de montagem para discos rígidos no computador local são criados automaticamente e fornecem acesso fácil ao sistema de arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="66b99-153">**letra\<da unidade/mnt/>/**</span><span class="sxs-lookup"><span data-stu-id="66b99-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="66b99-154">Exemplo `cd /mnt/c` de uso seria acessar c:</span><span class="sxs-lookup"><span data-stu-id="66b99-154">Example usage would be `cd /mnt/c` to access c:</span></span>\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="66b99-155">Como fazer usar um arquivo do Windows com um aplicativo do Linux?</span><span class="sxs-lookup"><span data-stu-id="66b99-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="66b99-156">Um dos benefícios do WSL é a capacidade de acessar seus arquivos por meio de aplicativos ou ferramentas do Windows e do Linux.</span><span class="sxs-lookup"><span data-stu-id="66b99-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="66b99-157">O WSL monta as unidades `/mnt/<drive>` fixas da máquina na pasta em seu distribuições do Linux.</span><span class="sxs-lookup"><span data-stu-id="66b99-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="66b99-158">Por exemplo, sua `C:` unidade está montada em`/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="66b99-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="66b99-159">Usando suas unidades montadas, você pode editar o código no, por `C:\dev\myproj\` exemplo, usando o [Visual Studio](https://visualstudio.microsoft.com/vs/) /ou [vs Code](https://code.visualstudio.com/), e criar/testar esse código no Linux acessando `/mnt/c/dev/myproj`os mesmos arquivos por meio do.</span><span class="sxs-lookup"><span data-stu-id="66b99-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="66b99-160">**OBSERVAÇÃO IMPORTANTE**: Uma das principais limitações do uso do WSL é que o acesso e a alteração direta de arquivos em seu sistema de arquivos do Linux distribuições usando aplicativos ou ferramentas do Windows não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="66b99-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="66b99-161">Consulte: [Não altere os arquivos do Linux usando ferramentas e aplicativos do Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="66b99-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="66b99-162">Os arquivos na unidade Linux são diferentes da unidade montada do Windows?</span><span class="sxs-lookup"><span data-stu-id="66b99-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="66b99-163">Os arquivos na raiz do Linux (ou `/`seja,) são controlados por WSL que imita o comportamento específico do Linux, incluindo, mas não se limitando a:</span><span class="sxs-lookup"><span data-stu-id="66b99-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="66b99-164">Arquivos que contêm caracteres de nome de arquivo do Windows inválidos</span><span class="sxs-lookup"><span data-stu-id="66b99-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="66b99-165">Symlinks criado para usuários não administradores</span><span class="sxs-lookup"><span data-stu-id="66b99-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="66b99-166">Alterando atributos de arquivo por meio de chmod e proprietário</span><span class="sxs-lookup"><span data-stu-id="66b99-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="66b99-167">Distinção entre maiúsculas e minúsculas de arquivo/pasta</span><span class="sxs-lookup"><span data-stu-id="66b99-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="66b99-168">Os arquivos em unidades montadas são controlados pelo Windows e têm os seguintes comportamentos:</span><span class="sxs-lookup"><span data-stu-id="66b99-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="66b99-169">Diferenciação do caso de suporte</span><span class="sxs-lookup"><span data-stu-id="66b99-169">Support case sensitivity</span></span>
   * <span data-ttu-id="66b99-170">Todas as permissões são definidas para refletir melhor as permissões do Windows</span><span class="sxs-lookup"><span data-stu-id="66b99-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="66b99-171">Por que há muitos erros quando executo apt-get upgrade?</span><span class="sxs-lookup"><span data-stu-id="66b99-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="66b99-172">Alguns pacotes usam recursos que ainda não implementamos.</span><span class="sxs-lookup"><span data-stu-id="66b99-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="66b99-173">`udev`, por exemplo, ainda não tem suporte e causa `apt-get upgrade` vários erros.</span><span class="sxs-lookup"><span data-stu-id="66b99-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="66b99-174">Para corrigir problemas relacionados ao `udev`, siga as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="66b99-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="66b99-175">Grave o seguinte no `/usr/sbin/policy-rc.d` e salve suas alterações.</span><span class="sxs-lookup"><span data-stu-id="66b99-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="66b99-176">Adicionar permissões de execução a`/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="66b99-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="66b99-177">Execute os seguintes comandos</span><span class="sxs-lookup"><span data-stu-id="66b99-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="66b99-178">Como fazer desinstalar uma distribuição WSL?</span><span class="sxs-lookup"><span data-stu-id="66b99-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="66b99-179">Em builds anteriores a 1709 (16299), abra um prompt de comando e execute:</span><span class="sxs-lookup"><span data-stu-id="66b99-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="66b99-180">As distribuições do WSL instaladas no repositório podem ser desinstaladas como qualquer outro aplicativo do Windows, clicando com o botão direito do mouse no bloco do aplicativo e clicando em desinstalar ou por meio do PowerShell usando o [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span><span class="sxs-lookup"><span data-stu-id="66b99-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="66b99-181">Por que o ping gera erros de permissão negada?</span><span class="sxs-lookup"><span data-stu-id="66b99-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="66b99-182">No WSL Builds < 14926, ping necessário WSL para executar por meio de um console elevado.</span><span class="sxs-lookup"><span data-stu-id="66b99-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="66b99-183">Esse problema foi corrigido no Build 14926 e posterior.</span><span class="sxs-lookup"><span data-stu-id="66b99-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="66b99-184">Como fazer executar um servidor OpenSSH?</span><span class="sxs-lookup"><span data-stu-id="66b99-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="66b99-185">São necessários privilégios de administrador no Windows para executar o OpenSSH no WSL.</span><span class="sxs-lookup"><span data-stu-id="66b99-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="66b99-186">Para executar um servidor OpenSSH, execute o bash no Ubuntu no Windows como administrador ou execute o bash. exe em um prompt do CMD/PowerShell com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="66b99-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="66b99-187">Por que obtenho "erro: 0x80040306 "quando tento instalar?</span><span class="sxs-lookup"><span data-stu-id="66b99-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="66b99-188">WSL não dá suporte à execução em um console herdado.</span><span class="sxs-lookup"><span data-stu-id="66b99-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="66b99-189">Para desativar o console herdado:</span><span class="sxs-lookup"><span data-stu-id="66b99-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="66b99-190">Abra o WSL, o PowerShell ou o cmd</span><span class="sxs-lookup"><span data-stu-id="66b99-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="66b99-191">Clique com o botão direito do mouse na barra de título-> Propriedades-> desmarque "usar o console herdado"</span><span class="sxs-lookup"><span data-stu-id="66b99-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="66b99-192">Clique em OK</span><span class="sxs-lookup"><span data-stu-id="66b99-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="66b99-193">Por que obtenho "erro: 0x80040154 "quando executo o bash. exe após a atualização do Windows?</span><span class="sxs-lookup"><span data-stu-id="66b99-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="66b99-194">O recurso "subsistema do Windows para Linux" pode ser desabilitado durante uma atualização do Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="66b99-195">Se isso acontecer, o recurso do Windows deverá ser habilitado novamente.</span><span class="sxs-lookup"><span data-stu-id="66b99-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="66b99-196">As instruções para habilitar o recurso "subsistema do Windows para Linux" podem ser encontradas no [Guia de instalação](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)do.</span><span class="sxs-lookup"><span data-stu-id="66b99-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="66b99-197">Como fazer alterar o idioma de exibição do WSL?</span><span class="sxs-lookup"><span data-stu-id="66b99-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="66b99-198">A instalação do WSL tentará alterar automaticamente a localidade do Ubuntu para corresponder à localidade da instalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="66b99-199">Se você não quiser esse comportamento, poderá executar esse comando para alterar a localidade do Ubuntu após a conclusão da instalação.</span><span class="sxs-lookup"><span data-stu-id="66b99-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="66b99-200">Você precisará reiniciar o bash. exe para que essa alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="66b99-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="66b99-201">O exemplo abaixo muda para a localidade para en-US:</span><span class="sxs-lookup"><span data-stu-id="66b99-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="66b99-202">Por que não tenho acesso à Internet do WSL?</span><span class="sxs-lookup"><span data-stu-id="66b99-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="66b99-203">Alguns usuários relataram problemas com aplicativos de firewall específicos que bloqueiam o acesso à Internet no WSL.</span><span class="sxs-lookup"><span data-stu-id="66b99-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="66b99-204">Os firewalls relatados são:</span><span class="sxs-lookup"><span data-stu-id="66b99-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="66b99-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="66b99-205">Kaspersky</span></span>
1. <span data-ttu-id="66b99-206">MÉDIA</span><span class="sxs-lookup"><span data-stu-id="66b99-206">AVG</span></span>
1. <span data-ttu-id="66b99-207">Avast</span><span class="sxs-lookup"><span data-stu-id="66b99-207">Avast</span></span>

<span data-ttu-id="66b99-208">Em alguns casos, a desativação do firewall permite o acesso.</span><span class="sxs-lookup"><span data-stu-id="66b99-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="66b99-209">Em alguns casos, simplesmente ter o firewall instalado procura bloquear o acesso.</span><span class="sxs-lookup"><span data-stu-id="66b99-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="66b99-210">Como fazer acessar uma porta do WSL no Windows?</span><span class="sxs-lookup"><span data-stu-id="66b99-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="66b99-211">WSL compartilha o endereço IP do Windows, pois ele é executado no Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="66b99-212">Como tal, você pode acessar qualquer porta no localhost, por exemplo, se você tivesse conteúdo da Web na https://localhost:1234 porta 1234, poderia no seu navegador do Windows.</span><span class="sxs-lookup"><span data-stu-id="66b99-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="66b99-213">Como posso fazer backup de meu WSL distribuições?</span><span class="sxs-lookup"><span data-stu-id="66b99-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="66b99-214">A melhor maneira de fazer backup de seu distribuições está disponível no Windows versão 1809 e posterior.</span><span class="sxs-lookup"><span data-stu-id="66b99-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="66b99-215">Você pode exportar toda a distribuição para um tarball usando o `wsl --export` comando.</span><span class="sxs-lookup"><span data-stu-id="66b99-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="66b99-216">Em seguida, você pode importar esse distribuição de volta para `wsl --import` o WSL usando o comando, permitindo que você faça backup e salve Estados de suas distribuições do WSL.</span><span class="sxs-lookup"><span data-stu-id="66b99-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="66b99-217">Observe que os serviços de backup tradicionais que os arquivos de backup em suas pastas AppData (como o backup do Windows) não corromperão os arquivos do Linux.</span><span class="sxs-lookup"><span data-stu-id="66b99-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="66b99-218">Onde posso fornecer comentários?</span><span class="sxs-lookup"><span data-stu-id="66b99-218">Where can I provide feedback?</span></span>

<span data-ttu-id="66b99-219">Você pode compartilhar comentários e fazer perguntas por meio de vários canais: Comentários e perguntas devem ser direcionados para:</span><span class="sxs-lookup"><span data-stu-id="66b99-219">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="66b99-220">Nosso [rastreador de problemas do GitHub](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="66b99-220">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="66b99-221">Nosso [portal de UserVoice de linha de comando](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="66b99-221">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="66b99-222">Nosso [blog da equipe de linha de comando](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="66b99-222">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="66b99-223">Por meio do Twitter.</span><span class="sxs-lookup"><span data-stu-id="66b99-223">Via Twitter.</span></span> <span data-ttu-id="66b99-224">Siga [@richturn_ms](https://twitter.com/richturn_MS) no Twitter para aprender sobre notícias, atualizações, etc.</span><span class="sxs-lookup"><span data-stu-id="66b99-224">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
