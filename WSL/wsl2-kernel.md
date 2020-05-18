---
title: Atualizar o kernel do WSL 2 Linux
description: Instruções sobre como atualizar o kernel do WSL 2 Linux manualmente
keywords: wsl, windows, linux kernel, windows subsystem for linux, kernel
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 89e5755699938b7797aa65a5f3131f93e3e31796
ms.sourcegitcommit: e6e888f2b88a2d9c105cee46e5ab5b70aa43dd80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83343828"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Atualizar o kernel do WSL 2 Linux

Para atualizar manualmente o kernel do Linux dentro do WSL2, siga estas etapas.

> [!NOTE] 
> Se o instalador não conseguir encontrar o WSL 1, clique com o botão direito do mouse no instalador de atualização do kernel do Linux e selecione Desinstalar e execute o instalador novamente

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
