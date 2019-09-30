---
title: Inicializar uma nova distribuição do Linux no WSL
description: Depois de instalar uma distribuição do Linux para o WSL, conclua a inicialização seguindo estas etapas simples
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122710"
---
# <a name="initializing-a-newly-installed-distro"></a>Como iniciar uma distribuição recentemente instalada
Depois que a distribuição tiver sido baixada e instalada, você precisará concluir a inicialização da nova distribuição:

## <a name="launch-a-distro"></a>Iniciar uma distribuição
Para concluir a inicialização de sua distribuição recentemente instalada, inicie uma nova instância. Você pode fazer isso clicando no botão "Iniciar" no aplicativo Microsoft Store ou iniciando a distribuição no menu Iniciar:

> Dica: Talvez você queira fixar as distribuições usadas com mais frequência no menu Iniciar e/ou na barra de tarefas.

![Iniciar distribuições no menu Iniciar](media/start-menu.png)

> No Windows Server, você pode iniciar o executável do inicializador da distribuição `<distro>.exe` na pasta de instalação da distribuição.

Na primeira vez em que uma distribuição for executada, uma janela de console será aberta e você será solicitado a aguardar um minuto ou dois para que a instalação seja concluída.

> Durante essa fase final da instalação, os arquivos da distribuição são descompactados e armazenados em seu computador, prontos para uso. Isso pode levar cerca de um minuto ou mais, dependendo do desempenho dos dispositivos de armazenamento de seu computador. Essa fase de instalação inicial só é necessária quando uma distribuição é instalada de modo limpo – todas as futuras inicializações deverão levar menos de um segundo.

## <a name="setting-up-a-new-linux-user-account"></a>Como configurar uma nova conta de usuário do Linux

Quando a instalação for concluída, você será solicitado a criar uma nova conta de usuário (e sua senha). 

![Desempacotamento do Ubuntu no console do Windows](media/UbuntuInstall.png)

Essa conta de usuário é para o usuário não administrador normal na qual você fará logon por padrão ao iniciar uma distribuição.

> Você pode escolher qualquer nome de usuário e senha que desejar – eles não têm nenhuma influência sobre seu nome de usuário do Windows. 

Quando você abrir uma nova instância da distribuição, não será solicitada sua senha, mas **se você elevar um processo usando `sudo`, precisará inserir sua senha**, portanto, certifique-se de escolher uma senha que você possa lembrar facilmente! Consulte a página [Suporte ao usuário](user-support.md) para obter mais informações.

## <a name="update--upgrade-your-distros-packages"></a>Atualização e upgrade dos pacotes de sua distribuição

A maioria das distribuições é fornecida com um catálogo de pacotes vazio/mínimo. É altamente recomendável atualizar regularmente seu catálogo de pacotes e fazer upgrade de seus pacotes instalados usando o gerenciador de pacotes preferencial da distribuição. No Debian/Ubuntu, você usa apt:

```bash
sudo apt update && sudo apt upgrade
```

> O Windows não atualiza ou faz upgrade automaticamente de suas distribuições do Linux: Essa é uma tarefa que os usuários do Linux preferem controlar por conta própria.

Concluído! Aproveite o uso de sua nova distribuição do Linux no WSL! Para saber mais sobre o WSL, examine os outros [documentos do WSL](https://aka.ms/wsldocs) ou a [página de recursos de aprendizagem do WSL](https://aka.ms/learnwsl).

![Aproveite o uso do Linux no WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Solução de problemas

Veja abaixo erros relacionados e correções sugeridas. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros comuns e suas soluções.

> **Falha na instalação com o erro 0x8007007e** Esse erro ocorre quando o sistema não é compatível com o Linux na loja.  Certifique-se de que:
> * Você está executando o Windows Build 16215 ou posterior. [Verifique seu build](troubleshooting.md#check-your-build-number).
> * O componente opcional do Subsistema Windows para Linux está habilitado e o computador foi reiniciado.  [Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
