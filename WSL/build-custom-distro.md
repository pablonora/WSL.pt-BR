---
title: Criar uma distribuição do Linux personalizada para WSL
description: Saiba como criar uma distribuição do Linux personalizada para o subsistema do Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema do windows, distribuição, personalizado
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063254"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>Criando uma distribuição do Linux personalizada para WSL

Use a nossa amostra WSL do código-fonte aberto para criar pacotes de distribuição do WSL para o Microsoft Store e/ou para criar pacotes personalizados de distribuição do Linux para o sideload. Você pode encontrar o [repositório do iniciador de distribuição](https://github.com/Microsoft/WSL-DistroLauncher) no GitHub.

Este projeto permite:
* Mantenedores da distribuição Linux para empacotar e enviar uma distribuição do Linux como um appx que é executado no WSL
* Desenvolvedores criem distribuições do Linux personalizadas que podem ser carregado em seu computador de desenvolvimento

## <a name="background"></a>Histórico
Podemos distribuir distribuições do Linux para WSL como aplicativos de UWP por meio do Microsoft Store. Você pode instalar esses aplicativos que serão executados, em seguida, no WSL - subsistema que se encontra no kernel do Windows. Esse mecanismo de entrega traz muitos benefícios, conforme discutido em uma postagem de blog anterior.

## <a name="sideloading-a-custom-linux-distro-package"></a>Sideload de um pacote de distribuição do Linux personalizado
Você pode criar um pacote de distribuição do Linux personalizado como um aplicativo para fazer sideload em seu computador pessoal. Observe que seu pacote personalizado não seria distribuído por meio do Microsoft Store, a menos que você envia como um mantenedor de distribuição.
Para configurar seu computador para fazer sideload dos aplicativos, você precisará habilitar isso nas configurações do sistema sob "Para desenvolvedores".  Certifique-se de ter o modo de desenvolvedor ou fazer sideload dos aplicativos selecionados

## <a name="for-linux-distro-maintainers"></a>Para os mantenedores da distribuição do Linux
Para enviar para a Store, você precisará trabalhar para receber a aprovação para publicação. Se você for um proprietário de distribuição de Linux interessado em Adicionar sua distribuição para a Microsoft Store, entre em contato com wslpartners@microsoft.com.

## <a name="getting-started"></a>Introdução
Siga as instruções sobre o [repositório GitHub do iniciador de distribuição](https://github.com/Microsoft/WSL-DistroLauncher) para criar um pacote de distribuição do Linux personalizado.

 
## <a name="team-blogs"></a>Blogs da equipe
*  [Abra o fornecimento de uma amostra do WSL para mantenedores da distribuição de Linux e distribuições do Linux personalizada de Sideload](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [Blog de linha de comando](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Envie comentários
* [Repositório de distribuição iniciador Gitub](https://github.com/Microsoft/WSL-DistroLauncher)
* [Rastreador de problemas do GitHub para WSL](https://github.com/Microsoft/BashOnWindows/issues)
* [Portal de linha de comando do UserVoice](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
