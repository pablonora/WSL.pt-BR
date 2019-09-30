---
title: Inicializar uma nova distribuição do Linux no WSL
description: Depois de instalar uma distribuição do Linux para o WSL, conclua a inicialização seguindo estas etapas simples
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122710"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="a9ea3-104">Como iniciar uma distribuição recentemente instalada</span><span class="sxs-lookup"><span data-stu-id="a9ea3-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="a9ea3-105">Depois que a distribuição tiver sido baixada e instalada, você precisará concluir a inicialização da nova distribuição:</span><span class="sxs-lookup"><span data-stu-id="a9ea3-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="a9ea3-106">Iniciar uma distribuição</span><span class="sxs-lookup"><span data-stu-id="a9ea3-106">Launch a distro</span></span>
<span data-ttu-id="a9ea3-107">Para concluir a inicialização de sua distribuição recentemente instalada, inicie uma nova instância.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="a9ea3-108">Você pode fazer isso clicando no botão "Iniciar" no aplicativo Microsoft Store ou iniciando a distribuição no menu Iniciar:</span><span class="sxs-lookup"><span data-stu-id="a9ea3-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="a9ea3-109">Dica: Talvez você queira fixar as distribuições usadas com mais frequência no menu Iniciar e/ou na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Iniciar distribuições no menu Iniciar](media/start-menu.png)

> <span data-ttu-id="a9ea3-111">No Windows Server, você pode iniciar o executável do inicializador da distribuição `<distro>.exe` na pasta de instalação da distribuição.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="a9ea3-112">Na primeira vez em que uma distribuição for executada, uma janela de console será aberta e você será solicitado a aguardar um minuto ou dois para que a instalação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="a9ea3-113">Durante essa fase final da instalação, os arquivos da distribuição são descompactados e armazenados em seu computador, prontos para uso.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="a9ea3-114">Isso pode levar cerca de um minuto ou mais, dependendo do desempenho dos dispositivos de armazenamento de seu computador.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="a9ea3-115">Essa fase de instalação inicial só é necessária quando uma distribuição é instalada de modo limpo – todas as futuras inicializações deverão levar menos de um segundo.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="a9ea3-116">Como configurar uma nova conta de usuário do Linux</span><span class="sxs-lookup"><span data-stu-id="a9ea3-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="a9ea3-117">Quando a instalação for concluída, você será solicitado a criar uma nova conta de usuário (e sua senha).</span><span class="sxs-lookup"><span data-stu-id="a9ea3-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Desempacotamento do Ubuntu no console do Windows](media/UbuntuInstall.png)

<span data-ttu-id="a9ea3-119">Essa conta de usuário é para o usuário não administrador normal na qual você fará logon por padrão ao iniciar uma distribuição.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="a9ea3-120">Você pode escolher qualquer nome de usuário e senha que desejar – eles não têm nenhuma influência sobre seu nome de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="a9ea3-121">Quando você abrir uma nova instância da distribuição, não será solicitada sua senha, mas **se você elevar um processo usando `sudo`, precisará inserir sua senha**, portanto, certifique-se de escolher uma senha que você possa lembrar facilmente!</span><span class="sxs-lookup"><span data-stu-id="a9ea3-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="a9ea3-122">Consulte a página [Suporte ao usuário](user-support.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="a9ea3-123">Atualização e upgrade dos pacotes de sua distribuição</span><span class="sxs-lookup"><span data-stu-id="a9ea3-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="a9ea3-124">A maioria das distribuições é fornecida com um catálogo de pacotes vazio/mínimo.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="a9ea3-125">É altamente recomendável atualizar regularmente seu catálogo de pacotes e fazer upgrade de seus pacotes instalados usando o gerenciador de pacotes preferencial da distribuição.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="a9ea3-126">No Debian/Ubuntu, você usa apt:</span><span class="sxs-lookup"><span data-stu-id="a9ea3-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="a9ea3-127">O Windows não atualiza ou faz upgrade automaticamente de suas distribuições do Linux: Essa é uma tarefa que os usuários do Linux preferem controlar por conta própria.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="a9ea3-128">Concluído!</span><span class="sxs-lookup"><span data-stu-id="a9ea3-128">You're done!</span></span> <span data-ttu-id="a9ea3-129">Aproveite o uso de sua nova distribuição do Linux no WSL!</span><span class="sxs-lookup"><span data-stu-id="a9ea3-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="a9ea3-130">Para saber mais sobre o WSL, examine os outros [documentos do WSL](https://aka.ms/wsldocs) ou a [página de recursos de aprendizagem do WSL](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="a9ea3-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Aproveite o uso do Linux no WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="a9ea3-132">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="a9ea3-132">Troubleshooting</span></span>

<span data-ttu-id="a9ea3-133">Veja abaixo erros relacionados e correções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="a9ea3-134">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros comuns e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="a9ea3-135">**Falha na instalação com o erro 0x8007007e** Esse erro ocorre quando o sistema não é compatível com o Linux na loja.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="a9ea3-136">Certifique-se de que:</span><span class="sxs-lookup"><span data-stu-id="a9ea3-136">Make sure that:</span></span>
> * <span data-ttu-id="a9ea3-137">Você está executando o Windows Build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="a9ea3-138">[Verifique seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="a9ea3-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="a9ea3-139">O componente opcional do Subsistema Windows para Linux está habilitado e o computador foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="a9ea3-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="a9ea3-140">[Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="a9ea3-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
