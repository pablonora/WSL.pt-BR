---
title: Sobre WSL 2
description: Sobre o WSL 2 a nova arquitetura para o subsistema Windows para Linux
keywords: Instalar o BashOnWindows, bash, wsl, wsl2, windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10,
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b3b0b1ce0f55fed0b4cf223ccc18a509dcf81788
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038126"
---
WSL 2 é uma nova versão da arquitetura que alimenta o subsistema do Windows para Linux executar binários ELF64 Linux no Windows. Seus objetivos principais são aumentar o desempenho do sistema de arquivos, bem como a adição de compatibilidade de chamadas completa do sistema. Essa nova arquitetura altera como esses binários de Linux interagem com o Windows e o hardware do computador, mas ainda fornece a mesma experiência de usuário como no WSL 1 (a versão atual amplamente disponível). Linux individual distribuições podem ser executadas como uma distribuição WSL 1, ou como uma distribuição WSL 2, pode ser atualizado ou desatualizado a qualquer momento, e você pode executar o WSL 1 e 2 WSL distribuições lado a lado. WSL 2 usa uma arquitetura totalmente nova que usa um kernel do Linux real.

## <a name="linux-kernel-in-wsl-2"></a>Kernel do Linux no WSL 2

O kernel do Linux no WSL 2 é criado internamente a partir da ramificação estável mais recente, com base no código-fonte disponível em kernel.org. Esse kernel foi ajustado especialmente para 2 WSL. Ele foi otimizado para o tamanho e desempenho para fornecer uma experiência incrível do Linux no Windows e será atendido por meio de atualizações do Windows, o que significa que você obterá as correções de segurança mais recentes e aprimoramentos do kernel sem a necessidade de gerenciá-lo.

Além disso, este kernel estará livre. Você pode encontrar o código-fonte completo para o kernel do Linux [aqui](https://thirdpartysource.microsoft.com/download/Windows%20Subsystem%20for%20Linux%20v2/May%202019/WSLv2-Linux-Kernel-master.zip). Se você quiser ler mais sobre esse kernel, você pode fazer check-out [esta postagem de blog](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) escrito pela equipe que criou.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Uma breve visão geral da arquitetura do WSL 2

WSL 2 usa o melhor e mais recente na tecnologia de virtualização para executar o kernel do Linux dentro de uma máquina virtual de utilitário leve (VM). No entanto, o WSL 2 não será uma experiência VM tradicional. Uma experiência tradicional de VM pode ser lenta inicializado, é isolada, consome muitos recursos e requer que seu tempo para gerenciá-lo. WSL 2 não tem esses atributos. Ele ainda fornecerá benefícios incríveis de WSL 1: Altos níveis de integração entre o Windows e Linux, tempos de inicialização extremamente rápidas, consumo de recursos pequeno e o melhor de tudo não exigirá nenhuma configuração de VM ou gerenciamento. Enquanto WSL 2 usa uma VM, ele será gerenciado e executar em segundo plano, deixando você com a mesma experiência de usuário que WSL 1.

## <a name="increased-file-io-performance"></a>Arquivo de maior desempenho de e/s

Operações com uso intensivo de arquivo, como o clone do git, npm install, apt atualização, atualização apt e muito mais tudo será notavelmente mais rápidas. O aumento de velocidade real dependerá de qual aplicativo você está em execução e como ele está interagindo com o sistema de arquivos. Versões iniciais do WSL 2 executam até 20 vezes mais rápido em comparação com o WSL 1, ao descompactar um tarball compactado e, em torno de 2 a 5 vezes mais rápido de ao usar o clone do git, npm install e cmake em diversos projetos.

## <a name="full-system-call-compatibility"></a>Compatibilidade de chamadas completa do sistema

Binários do Linux usam chamadas do sistema para executar várias funções, como acessar arquivos, solicitando a memória, criação de processos e muito mais. 1 WSL usado uma camada de conversão que foi criada pela equipe do WSL, o WSL 2 inclui seu próprio kernel do Linux com a compatibilidade de chamadas completa do sistema. Isso apresenta um novo conjunto de aplicativos que podem ser executados dentro de WSL, como Docker e muito mais. Além disso, todas as atualizações para o kernel do Linux podem ser imediatamente prontas para ser adicionado ao seu computador, em vez de aguardar a equipe WSL implementar as alterações e, então, eles adicionado.