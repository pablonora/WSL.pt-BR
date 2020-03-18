---
title: Atualizar o kernel do WSL 2 Linux
description: Instruções sobre como atualizar o kernel do WSL 2 Linux manualmente
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: f7fce13c2acc65e3afa2cc56873e40bc55a460bc
ms.sourcegitcommit: 506272bd7fc1cbda7e32146d54a8bdd02af3e0c4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2020
ms.locfileid: "79319706"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Atualizar o kernel do WSL 2 Linux

Para atualizar manualmente o kernel do Linux dentro do WSL2, siga estas etapas. 

## <a name="download-the-linux-kernel-update-package"></a>Baixar o pacote de atualização do kernel do Linux

Clique [neste link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para baixar o pacote de atualização do kernel do WSL2 Linux mais recente para computadores AMD64.

> [!NOTE] 
> Se você estiver usando um computador ARM64, baixe [este pacote](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).

## <a name="install-the-linux-kernel-update-package"></a>Instalar o pacote de atualização do kernel do Linux

Para instalar o pacote de atualização do kernel do Linux:

    1. Execute o pacote de atualização baixado na etapa anterior.
    2. Você receberá uma solicitação para fornecer permissões elevadas, selecione 'Sim' para aprovar essa instalação.
    3. Quando a instalação for concluída, você estará pronto para começar a usar o WSL2!

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Planos futuros para atualizar o kernel do WSL2 Linux

Para obter mais informações sobre essas alterações, leia [esta postagem](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) no [Blog da Linha de Comando do Windows](https://aka.ms/cliblog).
