---
title: Instalar o WSL (Subsistema Windows para Linux) no Windows 10
description: Instruções de instalação para o Subsistema Windows para Linux no Windows 10.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, install
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200240"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guia de instalação do Subsistema Windows para Linux para Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Instalar o Subsistema Windows para Linux

Antes de instalar distribuições do Linux para WSL, você deve garantir que o recurso opcional "Subsistema Windows para Linux" esteja habilitado:

1. Abra o PowerShell como administrador e execute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie seu computador quando solicitado.

## <a name="install-your-linux-distribution-of-choice"></a>Instale a distribuição do Linux de sua escolha
Para baixar e instalar suas distribuições preferenciais, há três opções:
* Baixe e instale usando a Microsoft Store (consulte abaixo)
* Baixe e instale usando a linha de comando/script ([leia as instruções de instalação no manual](install-manual.md))
* Baixe e descompacte e instale manualmente (for Windows Server – [instruções aqui](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update e posteriores: Instale usando a Microsoft Store

> Esta seção destina-se ao Windows build 16215 ou posterior.  Siga estas etapas para [verificar seu build](troubleshooting.md#check-your-build-number). 

1. Abra a Microsoft Store e escolha sua distribuição do Linux favorita.

    ![Exibição das distribuições do Linux na Microsoft Store](media/store.png)

    Os links a seguir abrirão a página da Microsoft Store para cada distribuição:

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix para WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. Na página da distribuição, selecione "Obter"

    ![Exibição das distribuições do Linux na Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Conclua a inicialização de sua distribuição
Agora que a distribuição do Linux está instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) uma vez, antes que possa ser usada.

## <a name="troubleshooting"></a>Solução de problemas: 

Veja abaixo erros relacionados e correções sugeridas. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros comuns e suas soluções.

* **Falha na instalação com o erro 0x80070003**
    * O Subsistema Windows para Linux é executado somente na unidade do sistema (normalmente, a unidade `C:`). Verifique se as distribuições estão armazenadas na unidade do sistema:  
    * Abra **Configurações** -> **Armazenamento** -> **Mais configurações de armazenamento: Altere onde o novo conteúdo é salvo**
    ![Imagem das configurações do sistema para instalar aplicativos na unidade C:](media/AppStorage.png)
    
    
 * **WslRegisterDistribution falhou com o erro 0x8007019e**   
  * O componente opcional do Subsistema Windows para Linux não está habilitado: 
   * Abra **Painel de Controle** -> **Programas e Recursos** -> **Ativar ou desativar recursos do Windows** -> marque **Subsistema Windows para Linux** ou use o cmdlet do PowerShell mencionado no início deste artigo.
