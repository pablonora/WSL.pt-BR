---
title: Sobre o WSL 2
description: Sobre o WSL 2 a nova arquitetura para o subsistema do Windows para Linux
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 983699c26a21af7b81ba31067316ba3bbf1601af
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020929"
---
# <a name="about-wsl-2"></a>Sobre o WSL 2

WSL 2 é uma nova versão da arquitetura que capacita o subsistema do Windows para Linux a executar binários do ELF64 Linux no Windows. Suas metas principais são aumentar o desempenho do sistema de arquivos, bem como adicionar compatibilidade completa com a chamada do sistema. Essa nova arquitetura altera como esses binários do Linux interagem com o Windows e o hardware do computador, mas ainda fornece a mesma experiência do usuário que no WSL 1 (a versão atual amplamente disponível). Os distribuições individuais do Linux podem ser executados como um WSL 1 distribuição, ou como um WSL 2 distribuição, podem ser atualizados ou rebaixados a qualquer momento, e você pode executar WSL 1 e WSL 2 distribuições lado a lado. O WSL 2 usa uma arquitetura totalmente nova que usa um kernel Linux real.

## <a name="linux-kernel-in-wsl-2"></a>Kernel do Linux no WSL 2

O kernel do Linux no WSL 2 é criado internamente a partir da ramificação estável mais recente, com base na origem disponível em kernel.org. Esse kernel foi especialmente ajustado para WSL 2. Ele foi otimizado quanto ao tamanho e ao desempenho para fornecer uma experiência incrível do Linux no Windows e será atendido por meio de atualizações do Windows, o que significa que você obterá as correções de segurança e melhorias de kernel mais recentes sem precisar gerenciá-las por conta própria.

Além disso, esse kernel será de código aberto. Você pode encontrar o código-fonte completo para o kernel do Linux [aqui](https://github.com/microsoft/WSL2-Linux-Kernel). Se você quiser ler mais sobre esse kernel, poderá conferir [esta postagem de blog](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) escrita pela equipe que a criou.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Visão geral resumida da arquitetura WSL 2

O WSL 2 usa a mais recente e mais alta tecnologia de virtualização para executar seu kernel do Linux dentro de uma VM (máquina virtual) do utilitário leve. No entanto, o WSL 2 não será uma experiência de VM tradicional. Uma experiência de VM tradicional pode ser lenta para inicializar, é isolada, consome muitos recursos e requer seu tempo para gerenciá-lo. WSL 2 não tem esses atributos. Ele ainda fornecerá os benefícios notáveis do WSL 1: Altos níveis de integração entre o Windows e o Linux, tempos de inicialização extremamente rápidos, superfície de recursos pequenos e o melhor de tudo não exigirão nenhuma configuração ou gerenciamento de VM. Embora o WSL 2 Use uma VM, ele será gerenciado e executado nos bastidores, deixando você com a mesma experiência do usuário que o WSL 1.

## <a name="increased-file-io-performance"></a>Desempenho de e/s de arquivo aumentado

Operações intensivas de arquivos, como git clone, instalação NPM, atualização de apt, atualização de apt e muito mais serão visivelmente mais rápidas. O aumento da velocidade real dependerá de qual aplicativo você está executando e de como ele está interagindo com o sistema de arquivos. As versões iniciais do WSL 2 executam até 20x mais rápidas em comparação com WSL 1 ao desempacotar um tarball compactado e cerca de 2 vezes mais rápido ao usar o git clone, NPM install e CMake em vários projetos.

## <a name="full-system-call-compatibility"></a>Compatibilidade total com a chamada do sistema

Os binários do Linux usam chamadas do sistema para executar muitas funções, como acessar arquivos, solicitar memória, criar processos e muito mais. Enquanto o WSL 1 usava uma camada de conversão criada pela equipe do WSL, o WSL 2 inclui seu próprio kernel do Linux com compatibilidade total com a chamada do sistema. Isso introduz um conjunto totalmente novo de aplicativos que você pode executar dentro do WSL, como o Docker e muito mais. Além disso, todas as atualizações para o kernel do Linux podem estar imediatamente prontas para serem adicionadas ao seu computador, em vez de esperar que a equipe do WSL implemente as alterações e, em seguida, as tenha adicionado.