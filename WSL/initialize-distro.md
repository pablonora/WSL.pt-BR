---
title: Inicializar uma nova distribuição do Linux de WSL
description: Depois de instalar uma distribuição do Linux para WSL, concluir a inicialização, seguindo estas etapas simples
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063604"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="d693b-104">Inicializando uma distribuição recém-instalado</span><span class="sxs-lookup"><span data-stu-id="d693b-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="d693b-105">Depois que sua distribuição foi baixada e instalada, você precisará concluir a inicialização da nova distribuição:</span><span class="sxs-lookup"><span data-stu-id="d693b-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="d693b-106">Iniciar uma distribuição</span><span class="sxs-lookup"><span data-stu-id="d693b-106">Launch a distro</span></span>
<span data-ttu-id="d693b-107">Para concluir a inicialização de sua distribuição recém-instalado, inicie uma nova instância.</span><span class="sxs-lookup"><span data-stu-id="d693b-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="d693b-108">Você pode fazer isso clicando no botão "Iniciar" no aplicativo da Windows Store, ou iniciando a distribuição do menu Iniciar:</span><span class="sxs-lookup"><span data-stu-id="d693b-108">You can do this by clicking the "launch" button in the Windows Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="d693b-109">Dica: Pode ser que você deseja fixar seu distribuições usadas com mais frequência ao menu Iniciar e/ou à barra de tarefas!</span><span class="sxs-lookup"><span data-stu-id="d693b-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Inicie as distribuições do menu Iniciar](media/start-menu.png)

> <span data-ttu-id="d693b-111">No Windows Server, você pode iniciar o inicializador do sua distribuição executável `<distro>.exe` da pasta de instalação de distribuição.</span><span class="sxs-lookup"><span data-stu-id="d693b-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="d693b-112">Na primeira vez em uma distribuição recém-instalado é executado, um Console do janela será aberta, e você terá que aguardar um minuto ou dois concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="d693b-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="d693b-113">Durante esse estágio final da instalação, os arquivos da distribuição são desprovisionar compactados e armazenados no seu PC, pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="d693b-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="d693b-114">Isso pode levar ao redor de um minuto ou mais conforme o desempenho do seu PC dispositivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d693b-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="d693b-115">Fase de instalação inicial, só é necessário quando uma distribuição é limpo instalado - todas as inicializações futuras devem levar menos de um segundo.</span><span class="sxs-lookup"><span data-stu-id="d693b-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="d693b-116">Como configurar uma nova conta de usuário do Linux</span><span class="sxs-lookup"><span data-stu-id="d693b-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="d693b-117">Depois que a instalação for concluída, você precisará criar uma nova conta de usuário (e sua senha).</span><span class="sxs-lookup"><span data-stu-id="d693b-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Ubuntu desempacotar no console do Windows](media/UbuntuInstall.png)

<span data-ttu-id="d693b-119">Essa conta de usuário é para o usuário normal não-administrador que você vai estar conectado como por padrão ao iniciar uma distribuição.</span><span class="sxs-lookup"><span data-stu-id="d693b-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="d693b-120">Você pode escolher qualquer nome de usuário e senha que você deseja – eles terem nenhuma influência sobre seu nome de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="d693b-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="d693b-121">Quando você abre uma nova instância de distribuição, não serão solicitados a senha, mas **se você elevar um processo usando `sudo`, você precisará inserir sua senha**, portanto, certifique-se de que você escolher uma senha que você se lembre facilmente!</span><span class="sxs-lookup"><span data-stu-id="d693b-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="d693b-122">Consulte a [suporte ao usuário](user-support.md) página para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d693b-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="d693b-123">Atualizar & pacotes da sua distribuição de atualização</span><span class="sxs-lookup"><span data-stu-id="d693b-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="d693b-124">A maioria das distribuições são fornecidos com um catálogo de pacote vazio/mínimo.</span><span class="sxs-lookup"><span data-stu-id="d693b-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="d693b-125">É altamente recomendável atualizar regularmente seu catálogo de pacote e atualizar seus pacotes instalados usando o Gerenciador de pacotes preferido da sua distribuição.</span><span class="sxs-lookup"><span data-stu-id="d693b-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="d693b-126">No Debian/Ubuntu, use apt:</span><span class="sxs-lookup"><span data-stu-id="d693b-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="d693b-127">Windows automaticamente atualização ou upgrade distro(s) seu Linux: Essa é uma tarefa que preferir controlar se os usuários do Linux.</span><span class="sxs-lookup"><span data-stu-id="d693b-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="d693b-128">Concluído!</span><span class="sxs-lookup"><span data-stu-id="d693b-128">You're done!</span></span> <span data-ttu-id="d693b-129">Aproveite usando sua nova distribuição do Linux no WSL.</span><span class="sxs-lookup"><span data-stu-id="d693b-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="d693b-130">Para saber mais sobre o WSL, examine a outra [docs WSL](https://aka.ms/wsldocs), ou o [WSL página de recursos de aprendizado](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="d693b-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Aproveite a usando o Linux no WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="d693b-132">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="d693b-132">Troubleshooting</span></span>

<span data-ttu-id="d693b-133">Abaixo estão os erros relacionados e correções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="d693b-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="d693b-134">Consulte a [página de solução de problemas de WSL](troubleshooting.md) para outros erros comuns e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="d693b-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="d693b-135">**Falha na instalação com o erro 0x8007007e** esse erro ocorre quando o sistema não dá suporte a Linux da loja.</span><span class="sxs-lookup"><span data-stu-id="d693b-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="d693b-136">Certifique-se de que:</span><span class="sxs-lookup"><span data-stu-id="d693b-136">Make sure that:</span></span>
> * <span data-ttu-id="d693b-137">Você está executando o Windows build 16215 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d693b-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="d693b-138">[Verificar seu build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="d693b-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="d693b-139">O subsistema do Windows para o componente opcional do Linux está habilitado e o computador for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="d693b-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="d693b-140">[Verifique se WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="d693b-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
