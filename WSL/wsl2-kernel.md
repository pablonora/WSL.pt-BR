---
title: Atualizando o kernel do Linux WSL 2
description: Instruções sobre como atualizar o kernel do WSL 2 Linux manualmente
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138185"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Atualizando o kernel do Linux WSL 2

Para atualizar manualmente o kernel do Linux dentro do WSL 2, siga estas etapas. 

## <a name="download-the-linux-kernel-update-package"></a>Baixar o pacote de atualização do kernel do Linux

Clique neste [link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para baixar o pacote de atualização do kernel WSL2 Linux mais recente para computadores AMD64.

> [!NOTE] Se você estiver usando um computador ARM64, baixe [esse pacote](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) em vez disso.

## <a name="install-the-linux-kernel-update-package"></a>Instalar o pacote de atualização do kernel do Linux

Para instalar o pacote de atualização do kernel do Linux:
    1. Execute o pacote de atualização baixado na etapa anterior.
    2. Você será solicitado a fornecer permissões elevadas, selecione ' Sim ' para aprovar esta instalação.
    3. Quando a instalação for concluída, você estará pronto para começar a usar o WSL2!

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Planos futuros para atualizar o kernel do Linux WSL2

Para obter mais informações sobre essas alterações, leia [esta postagem do blog](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) no [blog da linha de comando do Windows](https://aka.ms/cliblog).