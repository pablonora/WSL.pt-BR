---
title: Sobre o WSL 2
description: Sobre o WSL 2, a nova arquitetura para o Subsistema do Windows para Linux
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: f11aed3a5583d1a68f4a0e095103eb0315ca2c45
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256379"
---
# <a name="about-wsl-2"></a>Sobre o WSL 2

O WSL 2 é uma nova versão da arquitetura que capacita o Subsistema do Windows para Linux a executar binários ELF64 Linux no Windows. As metas principais dele são aumentar o desempenho do sistema de arquivos e adicionar compatibilidade completa com a chamada do sistema. Essa nova arquitetura altera como esses binários do Linux interagem com o Windows e o hardware do computador, mas ainda fornece a mesma experiência do usuário que no WSL 1 (a versão atual amplamente disponível). As distribuições individuais do Linux podem ser executadas como uma distribuição do WSL 1 ou do WSL 2, podem ser atualizadas ou passar por downgrade a qualquer momento, e você pode executar as distribuições do WSL 1 e do WSL 2 lado a lado. O WSL 2 usa uma arquitetura totalmente nova que usa um kernel Linux real.

## <a name="linux-kernel-in-wsl-2"></a>Kernel Linux no WSL 2

O kernel Linux no WSL 2 é criado internamente usando a ramificação estável mais recente, com base na origem disponível em kernel.org. Esse kernel foi especialmente ajustado para o WSL 2. Ele foi otimizado quanto ao tamanho e ao desempenho para fornecer uma experiência incrível do Linux no Windows e a manutenção será realizada por meio de atualizações do Windows, o que significa que você obterá as correções de segurança e as melhorias de kernel mais recentes sem precisar gerenciá-las por conta própria.

Além disso, esse kernel será de software livre. Você pode encontrar o código-fonte completo para o kernel Linux [aqui](https://github.com/microsoft/WSL2-Linux-Kernel). Se você quiser ler mais sobre esse kernel, poderá conferir [esta postagem no blog](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) escrita pela equipe que o criou.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Visão geral resumida da arquitetura WSL 2

O WSL 2 usa a mais recente e melhor tecnologia de virtualização para executar o kernel Linux dentro de uma VM (máquina virtual) do utilitário leve. No entanto, o WSL 2 NÃO será uma experiência de VM tradicional. Uma experiência de VM tradicional poderá ter inicialização lenta, ser isolada, consumir muitos recursos e requerer seu tempo para gerenciá-la. O WSL 2 não tem esses atributos. Ele ainda fornecerá os benefícios notáveis do WSL 1: Altos níveis de integração entre o Windows e o Linux, tempos de inicialização extremamente rápidos, volume de recursos pequeno e, o melhor de tudo, não exigirá nenhuma configuração ou gerenciamento de VM. Embora o WSL 2 use uma VM, ele será gerenciado e executado nos bastidores, deixando você com a mesma experiência do usuário que o WSL 1.

## <a name="increased-file-io-performance"></a>Maior desempenho de E/S de arquivo

Operações com uso intensivo de arquivos, como `git clone`, `npm install`, `apt update`, `apt upgrade` e muito mais, serão visivelmente mais rápidas. O aumento da velocidade real dependerá de qual aplicativo você está executando e de como ele está interagindo com o sistema de arquivos. As versões iniciais do WSL 2 são executadas até 20 vezes mais rapidamente em comparação com o WSL 1 ao desempacotar um tarball compactado e cerca de duas a cinco vezes mais rapidamente ao usar `git clone`, `npm install` e `cmake` em vários projetos.

## <a name="full-system-call-compatibility"></a>Compatibilidade total com a chamada do sistema

Os binários do Linux usam chamadas do sistema para executar muitas funções, como acessar arquivos, solicitar memória, criar processos e muito mais. Enquanto o WSL 1 usava uma camada de conversão criada pela equipe do WSL, o WSL 2 inclui o próprio kernel Linux com compatibilidade total com a chamada do sistema. Ele introduz um conjunto totalmente novo de aplicativos que você pode executar dentro do WSL, como o Docker e muito mais. Além disso, todas as atualizações para o kernel Linux podem estar imediatamente prontas para serem adicionadas ao seu computador, em vez de esperar que a equipe do WSL implemente as alterações e, em seguida, as adicione.