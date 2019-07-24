---
title: Instalar ou remover na atualização de aniversário do Windows 10 ou na atualização de criadores
description: Instruções de instalação e desinstalação para a atualização da atualização de aniversário do Windows 10 ou do Creators
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10, herdado, beta, instalação, remoção, desinstalação, desinstalação, exclusão, preterido
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0d8fdabd61fadbfc58549a220ead23585a3d3656
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499267"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="fce9f-104">Guia para instalar ou desinstalar o subsistema do Windows para Linux em atualização de aniversário do Windows 10 e o criador de atualizações</span><span class="sxs-lookup"><span data-stu-id="fce9f-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="fce9f-105">Se você estiver executando a atualização do Windows 10 para criadores ou posterior, [siga as instruções de instalação do Windows 10](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="fce9f-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="fce9f-106"><strong><em><span style="color: #f28014">As instruções a seguir são para usuários que executam a atualização de aniversário do Windows 10 ou a atualização do Windows 10 para criadores</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="fce9f-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="fce9f-107">Antes da atualização do Windows 10 outono Creators (versão 1709), o WSL foi lançado como um recurso beta e instalou uma única instância do Ubuntu quando o "bash no Ubuntu no Windows" (ou bash. exe) foi executado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fce9f-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="fce9f-108">Embora você possa usar o WSL em versões anteriores do Windows 10, essa versão beta "Legacy distribuição" agora é considerada obsoleta.</span><span class="sxs-lookup"><span data-stu-id="fce9f-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="fce9f-109">É altamente recomendável que você execute a versão mais recente do Windows 10 disponível.</span><span class="sxs-lookup"><span data-stu-id="fce9f-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="fce9f-110">Cada nova versão do Windows 10 inclui vários centenas de correções e melhorias no WSL sozinho, permitindo que mais ferramentas e aplicativos do Linux sejam executados corretamente no WSL.</span><span class="sxs-lookup"><span data-stu-id="fce9f-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="fce9f-111">Se você não puder atualizar para a atualização de criadores de outono ou posterior, siga as etapas abaixo para habilitar e usar o WSL:</span><span class="sxs-lookup"><span data-stu-id="fce9f-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="fce9f-112">Ativar o modo de desenvolvedor para executar o WSL na atualização de aniversário do Windows 10 ou na atualização de criadores, você deve habilitar o modo de desenvolvedor:</span><span class="sxs-lookup"><span data-stu-id="fce9f-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="fce9f-113">Abrir **configurações** -> **atualização e segurança** -> **para desenvolvedores**</span><span class="sxs-lookup"><span data-stu-id="fce9f-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="fce9f-114">Selecione o botão de opção modo de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="fce9f-114">Select the Developer Mode radio button</span></span>  
    ![Habilitar o modo de desenvolvedor](media/updateAndSecurity.png)

    > <span data-ttu-id="fce9f-116">A necessidade de habilitar o modo de desenvolvedor foi [removida na atualização dos criadores de outono do Windows 10](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="fce9f-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="fce9f-117">Abra um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="fce9f-117">Open a command prompt.</span></span>  <span data-ttu-id="fce9f-118">Digite `bash` e pressione Enter</span><span class="sxs-lookup"><span data-stu-id="fce9f-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="fce9f-119">Na primeira vez que você executar o bash no Ubuntu no Windows, será solicitado que você aceite a licença do Canonical.</span><span class="sxs-lookup"><span data-stu-id="fce9f-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="fce9f-120">Depois de aceito, o WSL baixará e instalará a instância do Ubuntu em seu computador e um atalho "bash no Ubuntu no Windows" será adicionado ao menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="fce9f-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Avisar para instalar o Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="fce9f-122">Na primeira vez que você executar o bash no Ubuntu no Windows, será solicitado que você crie um nome de usuário e senha UNIX.</span><span class="sxs-lookup"><span data-stu-id="fce9f-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="fce9f-123">Siga as [instruções da nova instância do distribuição](initialize-distro.md) para concluir a instalação</span><span class="sxs-lookup"><span data-stu-id="fce9f-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="fce9f-124">Inicie um novo shell do Ubuntu por meio de:</span><span class="sxs-lookup"><span data-stu-id="fce9f-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="fce9f-125">Executando `bash` a partir de um prompt de comando</span><span class="sxs-lookup"><span data-stu-id="fce9f-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="fce9f-126">Clicando no atalho "bash no Ubuntu no Windows" do menu iniciar</span><span class="sxs-lookup"><span data-stu-id="fce9f-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="fce9f-127">Desinstalando/removendo o distribuição herdado</span><span class="sxs-lookup"><span data-stu-id="fce9f-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="fce9f-128">Se você atualizar para a atualização dos criadores de outono do Windows 10 de uma versão anterior do Windows 10 na qual você instalou o WSL, seu distribuição existente permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="fce9f-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="fce9f-129">No entanto, é altamente recomendável que você instale uma nova loja entregue distribuição ASAP e migre todos os arquivos, dados, etc. necessários do seu distribuição herdado para o novo distribuição.</span><span class="sxs-lookup"><span data-stu-id="fce9f-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="fce9f-130">Para remover o distribuição herdado de seu computador, execute o seguinte em uma linha de comando ou instância do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fce9f-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
wsl --unregister Legacy
```

<span data-ttu-id="fce9f-131">Se você não estiver usando o Windows versão 1903 ou superior, talvez seja necessário executar `wslconfig /u Legacy` ou `lxrun /uninstall /full` em vez disso.</span><span class="sxs-lookup"><span data-stu-id="fce9f-131">If you are not using Windows Version 1903 or higher, you may need to run `wslconfig /u Legacy` or `lxrun /uninstall /full` instead.</span></span> 

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="fce9f-132">Excluindo manualmente o distribuição herdado</span><span class="sxs-lookup"><span data-stu-id="fce9f-132">Manually deleting the legacy distro</span></span>
<span data-ttu-id="fce9f-133">Se desejar, você pode excluir manualmente sua instância herdada.</span><span class="sxs-lookup"><span data-stu-id="fce9f-133">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="fce9f-134">Isso pode ser necessário se você encontrar problemas ao desinstalar o distribuição herdado usando `lxrun.exe`ou estiver executando a atualização do Windows 10 Spring 2018 (ou posterior) que não são fornecidos `lxrun.exe`com o.</span><span class="sxs-lookup"><span data-stu-id="fce9f-134">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="fce9f-135">Para excluir de modo forçado seu distribuição WSL herdado, `%localappdata%\lxss\` exclua a pasta (e o seu subconteúdo) usando o Windows ' Explorador de arquivos ou a linha de comando:</span><span class="sxs-lookup"><span data-stu-id="fce9f-135">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="fce9f-136">Usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="fce9f-136">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="fce9f-137">Usando o cmd:</span><span class="sxs-lookup"><span data-stu-id="fce9f-137">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
