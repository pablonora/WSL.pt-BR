---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: Instalar o BashOnWindows, bash, wsl, wsl2, windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10,
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038076"
---
# <a name="installation-instructions-for-wsl-2"></a>Instruções de instalação do WSL 2

Para instalar e começar a usar o WSL 2 conclua as seguintes etapas:

- Ativar o componente opcional de 'Platform da máquina Virtual'
- Defina uma distribuição que passarão por 2 WSL usando a linha de comando
- Verifique se o que estão usando versões do WSL suas distribuições

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Ativar o componente opcional de 'Platform da máquina Virtual'

Abra o PowerShell como administrador e execute:

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

Depois que essas alterações são habilitadas, você precisará reiniciar o computador.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Defina uma distribuição que passarão por 2 WSL usando a linha de comando

Na execução do PowerShell:

`wsl --set-version <Distro> 2`

e lembre-se de substituir `<Distro>` com o nome real da sua distribuição. (Você pode encontrá-las com o comando: `wsl -l`). Você pode alterar para 1 WSL na qualquer momento, executando o mesmo comando como mostrado acima, mas substituindo ' 2' com um ' 1'.

Além disso, se você quiser fazer WSL 2 a arquitetura padrão pode fazer isso com este comando:

`wsl --set-default-version 2`

Isso fará com que qualquer nova distribuição que você instale ser inicializada como uma distribuição WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Concluir com verificando o que estão usando versões do WSL sua distribuição

Para verificar quais versões do WSL cada distribuição está usando usam o seguinte comando:

`wsl --list --verbose` ou `wsl -l -v`

A distribuição que você escolheu acima agora deve exibir um '2' na coluna 'version'. Agora que você terminou fique à vontade começar a usar sua distribuição WSL 2! 