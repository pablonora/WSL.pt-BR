---
title: Instalar o WSL (Subsistema Windows para Linux) no Windows 10
description: Instruções de instalação para o Subsistema Windows para Linux no Windows 10.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, install, enable, WSL2, version 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 73e3b982cd29558fdc86bd499f9a4c51a9d22e83
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948690"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="116dc-104">Guia de instalação do Subsistema Windows para Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="116dc-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="116dc-105">Instalar o Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="116dc-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="116dc-106">Antes de instalar as distribuições do Linux no Windows, você deverá habilitar o recurso opcional "Subsistema do Windows para Linux".</span><span class="sxs-lookup"><span data-stu-id="116dc-106">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="116dc-107">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="116dc-107">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="116dc-108">Para instalar apenas o WSL 1, você deve reiniciar o computador e passar para [Instalar a distribuição do Linux de sua escolha](./install-win10.md#install-your-linux-distribution-of-choice), caso contrário, espere para reiniciar e passar para a atualização para o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="116dc-108">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="116dc-109">Leia mais sobre a [Comparação entre o WSL 2 e o WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="116dc-109">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="116dc-110">Atualizar para o WSL 2</span><span class="sxs-lookup"><span data-stu-id="116dc-110">Update to WSL 2</span></span>

<span data-ttu-id="116dc-111">Para atualizar para o WSL 2, você deve atender aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="116dc-111">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="116dc-112">Executar o Windows 10, [atualizado para a versão 2004](ms-settings:windowsupdate), **Build 19041** ou superiores.</span><span class="sxs-lookup"><span data-stu-id="116dc-112">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>

- <span data-ttu-id="116dc-113">Verifique sua versão do Windows selecionando a **tecla do logotipo do Windows + R**, digite **winver**, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="116dc-113">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="116dc-114">(Ou digite o comando `ver` no prompt de comando do Windows).</span><span class="sxs-lookup"><span data-stu-id="116dc-114">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="116dc-115">[Faça a atualização para a última versão do Windows](ms-settings:windowsupdate) se o build for anterior ao 19041.</span><span class="sxs-lookup"><span data-stu-id="116dc-115">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 19041.</span></span> <span data-ttu-id="116dc-116">[Obtenha o Assistente do Windows Update](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="116dc-116">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="116dc-117">Habilite o componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="116dc-117">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="116dc-118">Antes de instalar o WSL 2, você deve habilitar o recurso opcional "Plataforma de Máquina Virtual".</span><span class="sxs-lookup"><span data-stu-id="116dc-118">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="116dc-119">Abra o PowerShell como administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="116dc-119">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="116dc-120">**Reinicie** o computador para concluir a instalação do WSL e a atualização para o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="116dc-120">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="116dc-121">Definir o WSL 2 como sua versão padrão</span><span class="sxs-lookup"><span data-stu-id="116dc-121">Set WSL 2 as your default version</span></span>

<span data-ttu-id="116dc-122">Abra o PowerShell como administrador e execute este comando para definir o WSL 2 como a versão padrão ao instalar uma nova distribuição do Linux:</span><span class="sxs-lookup"><span data-stu-id="116dc-122">Open PowerShell as Administrator and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="116dc-123">Você poderá ver esta mensagem depois de executar esse comando: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="116dc-123">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="116dc-124">Siga o link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) e instale o MSI dessa página em nossa documentação para instalar um kernel do Linux em seu computador para o WSL 2 usar.</span><span class="sxs-lookup"><span data-stu-id="116dc-124">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="116dc-125">Depois de instalar o kernel, execute o comando novamente e ele deverá ser concluído com êxito sem mostrar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="116dc-125">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="116dc-126">A atualização da WSL 1 para a WSL 2 pode levar vários minutos para ser concluída, dependendo do tamanho da sua distribuição alvo.</span><span class="sxs-lookup"><span data-stu-id="116dc-126">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="116dc-127">Se você estiver executando uma instalação mais antiga (herdada) do WSL 1 da Atualização para Criadores ou da Atualização de Aniversário do Windows 10, poderá encontrar um erro de atualização.</span><span class="sxs-lookup"><span data-stu-id="116dc-127">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="116dc-128">Siga estas instruções para [desinstalar e remover as distribuições herdadas](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="116dc-128">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span> 
>
> <span data-ttu-id="116dc-129">Se `wsl --set-default-version` resultar como um comando inválido, insira `wsl --help`.</span><span class="sxs-lookup"><span data-stu-id="116dc-129">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="116dc-130">Se `--set-default-version` não está listado, isso significa que o sistema operacional não é compatível com ele, e você precisa atualizar para a versão 2004, Build 19041 ou superior.</span><span class="sxs-lookup"><span data-stu-id="116dc-130">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 2004, Build 19041 or higher.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="116dc-131">Instalar a distribuição do Linux de sua escolha</span><span class="sxs-lookup"><span data-stu-id="116dc-131">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="116dc-132">Abra a [Microsoft Store](https://aka.ms/wslstore) e escolha sua distribuição do Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="116dc-132">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Exibição das distribuições do Linux na Microsoft Store](media/store.png)

    <span data-ttu-id="116dc-134">Os links a seguir abrirão a página da Microsoft Store para cada distribuição:</span><span class="sxs-lookup"><span data-stu-id="116dc-134">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="116dc-135">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="116dc-135">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="116dc-136">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="116dc-136">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="116dc-137">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="116dc-137">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="116dc-138">OpenSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="116dc-138">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="116dc-139">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="116dc-139">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="116dc-140">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="116dc-140">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="116dc-141">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="116dc-141">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="116dc-142">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="116dc-142">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="116dc-143">Fedora Remix para WSL</span><span class="sxs-lookup"><span data-stu-id="116dc-143">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="116dc-144">Pengwin</span><span class="sxs-lookup"><span data-stu-id="116dc-144">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="116dc-145">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="116dc-145">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="116dc-146">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="116dc-146">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="116dc-147">Na página da distribuição, selecione "Obter".</span><span class="sxs-lookup"><span data-stu-id="116dc-147">From the distribution's page, select "Get".</span></span>

    ![Distribuições do Linux na Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="116dc-149">Configurar uma nova distribuição</span><span class="sxs-lookup"><span data-stu-id="116dc-149">Set up a new distribution</span></span>

<span data-ttu-id="116dc-150">Na primeira vez que você iniciar uma distribuição do Linux recém-instalada, uma janela de console será aberta e será solicitado que você aguarde um ou dois minutos para que os arquivos sejam descompactados e armazenados em seu PC.</span><span class="sxs-lookup"><span data-stu-id="116dc-150">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="116dc-151">Todas as futuras inicializações deverão levar menos de um segundo.</span><span class="sxs-lookup"><span data-stu-id="116dc-151">All future launches should take less than a second.</span></span>

<span data-ttu-id="116dc-152">Em seguida, você precisará [criar uma conta de usuário e uma senha para sua nova distribuição do Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="116dc-152">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Desempacotamento do Ubuntu no console do Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="116dc-154">Definir a versão de distribuição para WSL 1 ou WSL 2</span><span class="sxs-lookup"><span data-stu-id="116dc-154">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="116dc-155">Verifique a versão do WSL atribuída a cada uma das distribuições do Linux instaladas abrindo a linha de comando do PowerShell e inserindo o comando (disponível somente no [Windows Build 19041 ou superiores](ms-settings:windowsupdate)): `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="116dc-155">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="116dc-156">Para definir uma distribuição para ter suporte de qualquer versão do WSL, execute:</span><span class="sxs-lookup"><span data-stu-id="116dc-156">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="116dc-157">Assegure-se de substituir `<distribution name>` pelo nome real da sua distribuição e `<versionNumber>` pelo número '1' ou '2'.</span><span class="sxs-lookup"><span data-stu-id="116dc-157">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="116dc-158">Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.</span><span class="sxs-lookup"><span data-stu-id="116dc-158">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="116dc-159">Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:</span><span class="sxs-lookup"><span data-stu-id="116dc-159">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="116dc-160">Isso definirá a versão de qualquer nova distribuição instalada no WSL 2.</span><span class="sxs-lookup"><span data-stu-id="116dc-160">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="116dc-161">Como solucionar problemas de instalação</span><span class="sxs-lookup"><span data-stu-id="116dc-161">Troubleshooting installation</span></span>

<span data-ttu-id="116dc-162">Veja abaixo erros relacionados e correções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="116dc-162">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="116dc-163">Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros comuns e suas soluções.</span><span class="sxs-lookup"><span data-stu-id="116dc-163">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="116dc-164">**Falha na instalação com o erro 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="116dc-164">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="116dc-165">O Subsistema Windows para Linux é executado somente na unidade do sistema (normalmente, a unidade `C:`).</span><span class="sxs-lookup"><span data-stu-id="116dc-165">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="116dc-166">Verifique se as distribuições estão armazenadas na unidade do sistema:</span><span class="sxs-lookup"><span data-stu-id="116dc-166">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="116dc-167">Abra **Configurações** -> **Armazenamento** -> **Mais Configurações de Armazenamento: Altere onde o novo conteúdo é salvo**
    ![Imagem das configurações do sistema para instalar aplicativos na unidade C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="116dc-167">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="116dc-168">**WslRegisterDistribution falhou com o erro 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="116dc-168">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="116dc-169">O componente opcional do Subsistema Windows para Linux não está habilitado:</span><span class="sxs-lookup"><span data-stu-id="116dc-169">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="116dc-170">Abra **Painel de Controle** -> **Programas e Recursos** -> **Ativar ou Desativar Recursos do Windows** -> Selecione **Subsistema do Windows para Linux** ou use o cmdlet PowerShell mencionado no início deste artigo.</span><span class="sxs-lookup"><span data-stu-id="116dc-170">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="116dc-171">**Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="116dc-171">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="116dc-172">Verifique se a virtualização está habilitada dentro do BIOS do seu computador.</span><span class="sxs-lookup"><span data-stu-id="116dc-172">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="116dc-173">As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.</span><span class="sxs-lookup"><span data-stu-id="116dc-173">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="116dc-174">**Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="116dc-174">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="116dc-175">Verifique se você tem o Subsistema do Windows para Linux habilitado e se está usando o Windows, versão de Build 19041 ou superior.</span><span class="sxs-lookup"><span data-stu-id="116dc-175">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 19041 or higher.</span></span> <span data-ttu-id="116dc-176">Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="116dc-176">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="116dc-177">Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="116dc-177">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

- <span data-ttu-id="116dc-178">**A operação solicitada não pôde ser concluída devido a uma limitação do sistema de disco virtual. Os arquivos do disco rígido virtual devem ser descompactados e descriptografados e não devem ser esparsos.**</span><span class="sxs-lookup"><span data-stu-id="116dc-178">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="116dc-179">Para obter informações atualizadas, verifique o [thread 4103 do GitHub no WSL](https://github.com/microsoft/WSL/issues/4103) em que esse problema está sendo acompanhado.</span><span class="sxs-lookup"><span data-stu-id="116dc-179">Please check [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="116dc-180">**O termo 'wsl' não é reconhecido como nome de um cmdlet, uma função, um arquivo de script ou um programa operável.**</span><span class="sxs-lookup"><span data-stu-id="116dc-180">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="116dc-181">Verifique se o [componente opcional do Subsistema do Windows para Linux está instalado](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="116dc-181">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="116dc-182">Além disso, se você estiver usando um dispositivo ARM64 e executar esse comando no PowerShell, receberá esse erro.</span><span class="sxs-lookup"><span data-stu-id="116dc-182">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="116dc-183">Em vez disso, execute `wsl.exe` no [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) ou no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="116dc-183">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
