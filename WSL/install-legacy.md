---
title: Instalar ou remover em atualização de aniversário do Windows 10 ou atualização para criadores
description: Instruções de instalação e desinstalação para o herdado, a distribuição beta em atualização de aniversário do Windows 10 ou atualização para criadores
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, herdado, beta, instalar, remover, desinstalar, desinstalar, delete, preterido
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: fbb5bdc401a013b0853774cff6ad2dc84a36e412
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040842"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="cc25c-104">Guia para instalar ou desinstalar o subsistema do Windows para Linux em atualização de aniversário do Windows 10 e atualização para criadores</span><span class="sxs-lookup"><span data-stu-id="cc25c-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="cc25c-105">Se você estiver executando o Windows 10 Creators Update ou posterior, por favor [siga as instruções de instalação do Windows 10](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="cc25c-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="cc25c-106"><strong><em><span style="color: #f28014">As instruções a seguir são para usuários que executam a atualização de aniversário do Windows 10 ou Windows 10 Creators Update</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="cc25c-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="cc25c-107">Antes do Windows 10 Fall Creators Update (versão 1709), o WSL foi lançado como um recurso beta e instalado uma única instância do Ubuntu, quando o "Bash no Ubuntu no Windows" (ou Bash.exe) foi executado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="cc25c-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="cc25c-108">Embora você possa usar o WSL em versões anteriores do Windows 10, essa versão beta "distribuição herdada" é considerada obsoleta.</span><span class="sxs-lookup"><span data-stu-id="cc25c-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="cc25c-109">Recomendamos que você execute a versão mais recente do Windows 10 disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cc25c-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="cc25c-110">Cada nova versão do Windows 10 inclui várias centenas de correções e aprimoramentos no WSL sozinho, permitindo que o tornam cada vez mais ferramentas do Linux e aplicativos sejam executados corretamente no WSL.</span><span class="sxs-lookup"><span data-stu-id="cc25c-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="cc25c-111">Se você não pode atualizar para o Fall Creators Update ou posterior, siga as etapas abaixo para habilitar e usar WSL:</span><span class="sxs-lookup"><span data-stu-id="cc25c-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="cc25c-112">Ativar o desenvolvedor modo para execução WSL em atualização de aniversário do Windows 10 ou atualização para criadores, você deve habilitar o modo de desenvolvedor:</span><span class="sxs-lookup"><span data-stu-id="cc25c-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="cc25c-113">Abra **as configurações** -> **atualização e segurança** -> **para desenvolvedores**</span><span class="sxs-lookup"><span data-stu-id="cc25c-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="cc25c-114">Selecione o botão de opção de modo de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="cc25c-114">Select the Developer Mode radio button</span></span>  
    ![Habilitar o modo de desenvolvedor](media/updateAndSecurity.png)

    > <span data-ttu-id="cc25c-116">O requisito para habilitar o modo de desenvolvedor foi [removido no Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="cc25c-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="cc25c-117">Abra um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="cc25c-117">Open a command prompt.</span></span>  <span data-ttu-id="cc25c-118">Tipo `bash` e pressione enter</span><span class="sxs-lookup"><span data-stu-id="cc25c-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="cc25c-119">Na primeira vez que você executar o Bash no Ubuntu no Windows, você será solicitado a aceitar a licença da Canonical.</span><span class="sxs-lookup"><span data-stu-id="cc25c-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="cc25c-120">Depois de aceita, WSL baixará e instalará a instância do Ubuntu em seu computador e um atalho "Bash no Ubuntu no Windows" será adicionado ao menu Iniciar.</span><span class="sxs-lookup"><span data-stu-id="cc25c-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Solicitar a instalação do Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="cc25c-122">Na primeira vez que você executar o Bash no Ubuntu no Windows, você será solicitado a criar um nome de usuário do UNIX e uma senha.</span><span class="sxs-lookup"><span data-stu-id="cc25c-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="cc25c-123">Siga as [novas instruções de instância de distribuição](initialize-distro.md) para concluir a instalação</span><span class="sxs-lookup"><span data-stu-id="cc25c-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="cc25c-124">Inicie um novo shell do Ubuntu, qualquer um:</span><span class="sxs-lookup"><span data-stu-id="cc25c-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="cc25c-125">Executando `bash` em um prompt de comando</span><span class="sxs-lookup"><span data-stu-id="cc25c-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="cc25c-126">Clicar o atalho "Bash no Ubuntu no Windows" do menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="cc25c-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="cc25c-127">Desinstalando/remoção da distribuição herdada</span><span class="sxs-lookup"><span data-stu-id="cc25c-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="cc25c-128">Se você atualizar para o Windows 10 Fall Creators Update de uma versão anterior do Windows 10 que você instalou o WSL, sua distribuição existente permanecerão intacta.</span><span class="sxs-lookup"><span data-stu-id="cc25c-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="cc25c-129">No entanto, podemos FORTEMENTE encorajá-lo a instalar uma distribuição de nova entregues pelo Store urgente e migrar quaisquer arquivos necessários, dados, etc. de sua distribuição herdada para sua nova distribuição.</span><span class="sxs-lookup"><span data-stu-id="cc25c-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="cc25c-130">Para remover da distribuição herdada do seu computador, execute o seguinte de uma instância de linha de comando ou o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="cc25c-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="cc25c-131">A exclusão manual de distribuição herdada</span><span class="sxs-lookup"><span data-stu-id="cc25c-131">Manually deleting the legacy distro</span></span>
<span data-ttu-id="cc25c-132">Se desejar, você poderá excluir manualmente sua instância herdada.</span><span class="sxs-lookup"><span data-stu-id="cc25c-132">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="cc25c-133">Isso pode ser necessário se você encontrar problemas ao desinstalar usando a distribuição herdada `lxrun.exe`, ou estiver executando a atualização do Windows 10 primavera 2018 (ou posterior) que não são fornecidos com `lxrun.exe`.</span><span class="sxs-lookup"><span data-stu-id="cc25c-133">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="cc25c-134">Para forçar a exclusão de sua distribuição WSL herdada, exclua o `%localappdata%\lxss\` pasta (e todos os é um subdiretório de conteúdo) usando o Explorador de arquivos dos Windows ou da linha de comando:</span><span class="sxs-lookup"><span data-stu-id="cc25c-134">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="cc25c-135">Usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="cc25c-135">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="cc25c-136">Usando o Cmd:</span><span class="sxs-lookup"><span data-stu-id="cc25c-136">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
