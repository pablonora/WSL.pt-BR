---
title: Inicializar um novo WSL Linux distribuição
description: Depois de instalar um distribuição do Linux para o WSL, conclua a inicialização seguindo estas etapas simples
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122710"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="32d00-104">Inicializando um distribuição recentemente instalado</span><span class="sxs-lookup"><span data-stu-id="32d00-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="32d00-105">Depois que o distribuição tiver sido baixado e instalado, você precisará concluir a inicialização do novo distribuição:</span><span class="sxs-lookup"><span data-stu-id="32d00-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="32d00-106">Iniciar um distribuição</span><span class="sxs-lookup"><span data-stu-id="32d00-106">Launch a distro</span></span>
<span data-ttu-id="32d00-107">Para concluir a inicialização do seu distribuição recentemente instalado, inicie uma nova instância.</span><span class="sxs-lookup"><span data-stu-id="32d00-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="32d00-108">Você pode fazer isso clicando no botão "Iniciar" no aplicativo Microsoft Store ou iniciando o distribuição no menu iniciar:</span><span class="sxs-lookup"><span data-stu-id="32d00-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="32d00-109">Dica: Talvez você queira fixar o distribuições usado com mais frequência no menu iniciar e/ou na barra de tarefas!</span><span class="sxs-lookup"><span data-stu-id="32d00-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Iniciar o distribuições no menu iniciar](media/start-menu.png)

> <span data-ttu-id="32d00-111">No Windows Server, você pode iniciar o executável `<distro>.exe` do inicializador do distribuição na pasta de instalação do distribuição.</span><span class="sxs-lookup"><span data-stu-id="32d00-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="32d00-112">Na primeira vez em que um distribuição é executado recentemente, uma janela de console será aberta e você será solicitado a aguardar um minuto ou dois para que a instalação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="32d00-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="32d00-113">Durante esse estágio final da instalação, os arquivos do distribuição são descompactados e armazenados em seu computador, prontos para uso.</span><span class="sxs-lookup"><span data-stu-id="32d00-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="32d00-114">Isso pode levar cerca de um minuto ou mais, dependendo do desempenho dos dispositivos de armazenamento do seu computador.</span><span class="sxs-lookup"><span data-stu-id="32d00-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="32d00-115">Essa fase de instalação inicial só é necessária quando um distribuição é limpo-instalado – todas as futuras inicializações devem levar menos de um segundo.</span><span class="sxs-lookup"><span data-stu-id="32d00-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="32d00-116">Configurando uma nova conta de usuário do Linux</span><span class="sxs-lookup"><span data-stu-id="32d00-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="32d00-117">Quando a instalação for concluída, você será solicitado a criar uma nova conta de usuário (e sua senha).</span><span class="sxs-lookup"><span data-stu-id="32d00-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Desempacotamento do Ubuntu no console do Windows](media/UbuntuInstall.png)

<span data-ttu-id="32d00-119">Essa conta de usuário é para o usuário não administrador normal no qual você fará logon por padrão ao iniciar um distribuição.</span><span class="sxs-lookup"><span data-stu-id="32d00-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="32d00-120">Você pode escolher qualquer nome de usuário e senha que desejar-eles não têm nenhuma influência sobre seu nome de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="32d00-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="32d00-121">Quando você abrir uma nova instância do distribuição, não será solicitada sua senha, mas **se você elevar um processo usando `sudo`o, precisará inserir sua senha**, portanto, certifique-se de escolher uma senha que você possa lembrar facilmente!</span><span class="sxs-lookup"><span data-stu-id="32d00-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="32d00-122">Consulte a página de [suporte ao usuário](user-support.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="32d00-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="32d00-123">Atualizar & atualizar os pacotes do seu distribuição</span><span class="sxs-lookup"><span data-stu-id="32d00-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="32d00-124">A maioria dos distribuiçõess são fornecidos com um catálogo de pacotes vazio/mínimo.</span><span class="sxs-lookup"><span data-stu-id="32d00-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="32d00-125">É altamente recomendável atualizar regularmente seu catálogo de pacotes e atualizar seus pacotes instalados usando o Gerenciador de pacotes preferencial do distribuição.</span><span class="sxs-lookup"><span data-stu-id="32d00-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="32d00-126">No Debian/Ubuntu, você usa apt:</span><span class="sxs-lookup"><span data-stu-id="32d00-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="32d00-127">O Windows não atualiza ou atualiza automaticamente suas distribuição (s) Linux: Essa é uma tarefa que os usuários do Linux preferem controlar.</span><span class="sxs-lookup"><span data-stu-id="32d00-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="32d00-128">Concluído!</span><span class="sxs-lookup"><span data-stu-id="32d00-128">You're done!</span></span> <span data-ttu-id="32d00-129">Aproveite o uso de seu novo distribuição Linux no WSL!</span><span class="sxs-lookup"><span data-stu-id="32d00-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="32d00-130">Para saber mais sobre o WSL, examine os outros [documentos do WSL](https://aka.ms/wsldocs)ou a página de recursos do [WSL Learning](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="32d00-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Aproveite o uso do Linux no WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="32d00-132">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="32d00-132">Troubleshooting</span></span>

<span data-ttu-id="32d00-133">Abaixo estão os erros relacionados e as correções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="32d00-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="32d00-134">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para obter outros erros comuns e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="32d00-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="32d00-135">**Falha na instalação com o erro 0x8007007E** Esse erro ocorre quando o sistema não dá suporte ao Linux na loja.</span><span class="sxs-lookup"><span data-stu-id="32d00-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="32d00-136">Certifique-se de que:</span><span class="sxs-lookup"><span data-stu-id="32d00-136">Make sure that:</span></span>
> * <span data-ttu-id="32d00-137">Você está executando o Windows Build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="32d00-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="32d00-138">[Verifique sua compilação](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="32d00-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="32d00-139">O componente opcional do subsistema do Windows para Linux está habilitado e o computador foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="32d00-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="32d00-140">[Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="32d00-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
