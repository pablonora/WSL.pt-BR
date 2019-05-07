---
title: Instalar o subsistema do Windows para Linux (WSL) no Windows 10
description: Instruções de instalação para o subsistema Windows para Linux no Windows 10.
keywords: Instalar o BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10,
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063284"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Subsistema do Windows para o guia de instalação do Linux para Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Instale o subsistema do Windows para Linux

Antes de instalar qualquer distribuições do Linux para WSL, você deve garantir que o "Windows subsistema para Linux" recurso opcional está habilitado:

1. Abra o PowerShell como administrador e execute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie o computador quando solicitado.

## <a name="install-your-linux-distribution-of-choice"></a>Instalar sua distribuição do Linux de escolha
Para baixar e instalar seu distro(s) preferencial, você tem três opções:
1. Baixe e instale o Store do Windows (veja abaixo)
1. Baixe e instale o comando-linha/Script ([leia as instruções de instalação manual](install-manual.md))
1. Baixe e descompacte e instalar manualmente (para o Windows Server - [as instruções aqui](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update e posterior: Instalar a partir do Microsoft Store

> Esta seção destina-se a compilação 16215 ou posterior do Windows.  Siga estas etapas para [verificar seu build](troubleshooting.md#check-your-build-number). 

1. Abra o Microsoft Store e escolha sua distribuição do Linux favorita.

    ![Modo de exibição de distribuições do Linux no armazenamento do Windows](media/store.png)

    Os links a seguir abrirá a página de armazenamento do Windows para cada distribuição:

    * [Ubuntu](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [OpenSUSE](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SLES](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. Página a distribuição, selecione "Obter"

    ![Modo de exibição de distribuições do Linux no armazenamento do Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Concluir a inicialização de sua distribuição
Agora que sua distribuição do Linux é instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) uma vez, antes que ele pode ser usado.

## <a name="troubleshooting"></a>Solução de problemas: 

Abaixo estão os erros relacionados e correções sugeridas. Consulte a [página de solução de problemas de WSL](troubleshooting.md) para outros erros comuns e suas soluções.

* **Instalação falhou com erro 0x80070003**
    * O subsistema Windows para Linux é executado somente na unidade do sistema (geralmente, isso é seu `C:` unidade). Certifique-se de que as distribuições são armazenadas na unidade do sistema:  
    * Abra **as configurações** -> **armazenamento** -> **mais configurações de armazenamento: Alterar onde o novo conteúdo é salvo**
    ![imagem das configurações do sistema para instalar aplicativos na unidade c:](media/AppStorage.png)
