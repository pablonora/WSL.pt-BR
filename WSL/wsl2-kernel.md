---
title: Atualizar o kernel do WSL 2 Linux
description: Instruções sobre como atualizar o kernel do WSL 2 Linux manualmente
keywords: wsl, windows, linux kernel, windows subsystem for linux, kernel
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 1628bea2f1bae590928b055425413e5b085dffef
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153047"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Atualizar o kernel do WSL 2 Linux

Para atualizar manualmente o kernel do Linux dentro do WSL2, siga estas etapas.

> [!NOTE] 
> Se o instalador não conseguir encontrar a WSL 1, clique com o botão direito do mouse no instalador de atualização do kernel do Linux e pressione "Desinstalar", então execute novamente o instalador.

## <a name="download-the-linux-kernel-update-package"></a>Baixar o pacote de atualização do kernel do Linux

[Baixe o pacote de atualização do último kernel do Linux para o WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para computadores x64.

> [!NOTE]
> Se estiver usando um computador ARM64, baixe o [pacote ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).

## <a name="install-the-linux-kernel-update-package"></a>Instalar o pacote de atualização do kernel do Linux

Para instalar o pacote de atualização do kernel do Linux:

  1. Execute o pacote de atualização baixado na etapa anterior.

  2. Você receberá uma solicitação para fornecer permissões elevadas, selecione 'Sim' para aprovar essa instalação.

  3. Quando a instalação for concluída, você estará pronto para começar a usar o WSL2!

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Planos futuros para atualizar o kernel do WSL2 Linux

Para obter mais informações, leia o artigo [Alterações na atualização do kernel do Linux para o WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponível no [blog da linha de comando do Windows](https://aka.ms/cliblog).
