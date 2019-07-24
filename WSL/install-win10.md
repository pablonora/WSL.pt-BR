---
title: Instalar o subsistema do Windows para Linux (WSL) no Windows 10
description: Instruções de instalação para o subsistema do Windows para Linux no Windows 10.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10, instalar
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499288"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guia de instalação do subsistema do Windows para Linux para Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Instalar o subsistema do Windows para Linux

Antes de instalar qualquer distribuições do Linux para WSL, você deve garantir que o recurso opcional "subsistema do Windows para Linux" esteja habilitado:

1. Abra o PowerShell como administrador e execute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie o computador quando solicitado.

## <a name="install-your-linux-distribution-of-choice"></a>Instale sua distribuição do Linux de sua escolha
Para baixar e instalar seus distribuição (s) preferenciais, você tem três opções:
1. Baixar e instalar do Microsoft Store (veja abaixo)
1. Baixar e instalar a partir da linha de comando/script ([Leia as instruções de instalação manual](install-manual.md))
1. Baixe e descompacte e instale manualmente (para Windows Server- [instruções aqui](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Atualização dos criadores de outono do Windows 10 e posterior: Instalar do Microsoft Store

> Esta seção destina-se ao Windows Build 16215 ou posterior.  Siga estas etapas para [verificar sua compilação](troubleshooting.md#check-your-build-number). 

1. Abra o Microsoft Store e escolha sua distribuição do Linux favorita.

    ![Exibição de distribuições do Linux no Microsoft Store](media/store.png)

    Os links a seguir abrirão a página da Microsoft Store para cada distribuição:

    * [Ubuntu 16, 4 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18, 4 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
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

1. Na página do distribuição, selecione "obter"

    ![Exibição de distribuições do Linux na Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Concluir a inicialização do seu distribuição
Agora que o distribuição do Linux está instalado, você deve [inicializar a nova instância do distribuição](initialize-distro.md) uma vez, antes que possa ser usada.

## <a name="troubleshooting"></a>Solução de problemas: 

Abaixo estão os erros relacionados e as correções sugeridas. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para obter outros erros comuns e suas soluções.

* **Falha na instalação com o erro 0x80070003**
    * O subsistema do Windows para Linux é executado somente na unidade do sistema (normalmente, `C:` essa é a unidade). Verifique se os distribuições estão armazenados na unidade do sistema:  
    * Abra **configurações** ->  armazenamento -> mais configurações de armazenamento: ** Alterar onde o novo conteúdo é**salvo
    ![imagem das configurações do sistema para instalar aplicativos na unidade C:](media/AppStorage.png)
    
    
 * **WslRegisterDistribution falhou com o erro 0x8007019e**   
  * O componente opcional do subsistema do Windows para Linux não está habilitado: 
   * Abra o **painel** -> de controle**programas e recursos** -> * * ativar ou desativar o recurso do Windows * *-> verificar o subsistema **do Windows para Linux** ou usar o cmdlet do PowerShell mencionado no início deste artigo.
