---
title: Instalar o WSL (Subsistema Windows para Linux) no Windows 10
description: Instruções de instalação para o Subsistema Windows para Linux no Windows 10.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, install, enable, WSL2, version 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ec24bbe6ed3ecc4413e623d12d12f9a92c6db9e6
ms.sourcegitcommit: f0b33cdd1ce7b461e7f657d44e9798094ef55b55
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/20/2020
ms.locfileid: "83683034"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guia de instalação do Subsistema Windows para Linux para Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Instalar o Subsistema Windows para Linux

Antes de instalar as distribuições do Linux no Windows, você deverá habilitar o recurso opcional "Subsistema do Windows para Linux".

Abra o PowerShell como administrador e execute:

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

Para instalar apenas o WSL 1, você deve reiniciar o computador e passar para [Instalar a distribuição do Linux de sua escolha](./install-win10.md#install-your-linux-distribution-of-choice), caso contrário, espere para reiniciar e passar para a atualização para o WSL 2. Leia mais sobre a [Comparação entre o WSL 2 e o WSL 1](./compare-versions.md).

## <a name="update-to-wsl-2"></a>Atualizar para o WSL 2

Para atualizar para o WSL 2, você deve atender aos seguintes critérios:

- Executar o Windows 10, [atualizado para a versão 2004](ms-settings:windowsupdate), **Build 19041** ou superiores.

> [!IMPORTANT]
> Atualmente, para fazer a atualização para o Windows 10, versão 2004 (Build 19041), você precisará [ingressar no Programa Windows Insider](https://insider.windows.com/insidersigninboth/) e selecionar o anel "Versão Prévia". A versão pública deverá ser disponibilizada até o final de maio.

- Verifique sua versão do Windows selecionando a **tecla do logotipo do Windows + R**, digite **winver**, selecione **OK**. (Ou digite o comando `ver` no prompt de comando do Windows). [Faça a atualização para a última versão do Windows](ms-settings:windowsupdate) se o build for anterior ao 19041. [Obtenha o Assistente do Windows Update](https://www.microsoft.com/software-download/windows10).

### <a name="enable-the-virtual-machine-platform-optional-component"></a>Habilite o componente opcional "Plataforma de máquina virtual"

Antes de instalar o WSL 2, você deve habilitar o recurso opcional "Plataforma de Máquina Virtual".

Abra o PowerShell como administrador e execute:

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

**Reinicie** o computador para concluir a instalação do WSL e a atualização para o WSL 2.

### <a name="set-wsl-2-as-your-default-version"></a>Definir o WSL 2 como sua versão padrão

Execute o seguinte comando no PowerShell para definir o WSL 2 como a versão padrão ao instalar uma nova distribuição do Linux:

```powershell
wsl --set-default-version 2
```

## <a name="install-your-linux-distribution-of-choice"></a>Instalar a distribuição do Linux de sua escolha

1. Abra a [Microsoft Store](https://aka.ms/wslstore) e escolha sua distribuição do Linux favorita.

    ![Exibição das distribuições do Linux na Microsoft Store](media/store.png)

    Os links a seguir abrirão a página da Microsoft Store para cada distribuição:

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [OpenSUSE Leap 15.1](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [SUSE Linux Enterprise Server 12 SP5](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [SUSE Linux Enterprise Server 15 SP1](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix para WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

2. Na página da distribuição, selecione "Obter".

    ![Distribuições do Linux na Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a>Configurar uma nova distribuição

Na primeira vez que você iniciar uma distribuição do Linux recém-instalada, uma janela de console será aberta e será solicitado que você aguarde um ou dois minutos para que os arquivos sejam descompactados e armazenados em seu PC. Todas as futuras inicializações deverão levar menos de um segundo.

Em seguida, você precisará [criar uma conta de usuário e uma senha para sua nova distribuição do Linux](./user-support.md).

![Desempacotamento do Ubuntu no console do Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>Definir a versão de distribuição para WSL 1 ou WSL 2

Verifique a versão do WSL atribuída a cada uma das distribuições do Linux instaladas abrindo a linha de comando do PowerShell e inserindo o comando (disponível somente no [Windows Build 19041 ou superiores](ms-settings:windowsupdate)): `wsl -l -v`

```powershell
wsl --list --verbose
```

Para definir uma distribuição para ter suporte de qualquer versão do WSL, execute:

```powershell
wsl --set-version <distribution name> <versionNumber>
```

Assegure-se de substituir `<distribution name>` pelo nome real da sua distribuição e `<versionNumber>` pelo número '1' ou '2'. Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.

Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:

```powershell
wsl --set-default-version 2
```

Isso definirá a versão de qualquer nova distribuição instalada no WSL 2.

## <a name="troubleshooting-installation"></a>Como solucionar problemas de instalação

Veja abaixo erros relacionados e correções sugeridas. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros comuns e suas soluções.

- **Falha na instalação com o erro 0x80070003**
  - O Subsistema Windows para Linux é executado somente na unidade do sistema (normalmente, a unidade `C:`). Verifique se as distribuições estão armazenadas na unidade do sistema:  
  - Abra **Configurações** -> **Armazenamento** -> **Mais Configurações de Armazenamento: Altere onde o novo conteúdo é salvo**
    ![Imagem das configurações do sistema para instalar aplicativos na unidade C:](media/AppStorage.png)

- **WslRegisterDistribution falhou com o erro 0x8007019e**
  - O componente opcional do Subsistema Windows para Linux não está habilitado:
  - Abra **Painel de Controle** -> **Programas e Recursos** -> **Ativar ou desativar recursos do Windows** -> marque **Subsistema Windows para Linux** ou use o cmdlet do PowerShell mencionado no início deste artigo.

- **Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**
  - Verifique se a virtualização está habilitada dentro do BIOS do seu computador. As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.

- **Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**
  - Verifique se você tem o Subsistema do Windows para Linux habilitado e se está usando o Windows, versão de Build 19041 ou superior. Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).

- **A operação solicitada não pôde ser concluída devido a uma limitação do sistema de disco virtual. Os arquivos do disco rígido virtual devem ser descompactados e descriptografados e não devem ser esparsos.**
  - Verifique o [thread 4103 do GitHub no WSL](https://github.com/microsoft/WSL/issues/4103) em que esse problema está sendo acompanhado para obter informações atualizadas.

- **O termo 'wsl' não é reconhecido como nome de um cmdlet, uma função, um arquivo de script ou um programa operável.**
  - Verifique se o [componente opcional do Subsistema do Windows para Linux está instalado](./install-win10.md#enable-the-virtual-machine-platform-optional-component). Além disso, se você estiver usando um dispositivo Arm64 e executar esse comando do PowerShell, receberá esse erro. Em vez disso, execute `wsl.exe` no [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) ou no prompt de comando.
