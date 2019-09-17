---
title: WSL 2 perguntas frequentes
description: Perguntas frequentes sobre o subsistema do Windows para Linux 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: ea6a1e4fc813ec80393a0c4e2beb89e9a40fb68e
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020920"
---
# <a name="wsl-2-faq"></a>PERGUNTAS FREQUENTES SOBRE O WSL 2

Veja abaixo uma lista de perguntas frequentes sobre o subsistema do Windows para Linux 2.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>O WSL 2 usa o Hyper-V? Ele estará disponível no Windows 10 Home?

O WSL 2 estará disponível em todos os SKUs nos quais o WSL está disponível no momento, incluindo o Windows 10 Home.

A versão mais recente do WSL usa a arquitetura do Hyper-V para habilitar sua virtualização. Essa arquitetura estará disponível no componente opcional ' plataforma de máquina virtual '. Esse componente opcional estará disponível em todos os SKUs. Você pode esperar ver mais detalhes sobre essa experiência logo que se aproximarmos da versão WSL 2.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>O que acontecerá com o WSL 1? Ela será abandonada?

No momento, não temos planos para substituir WSL 1. Você pode executar o WSL 1 e o WSL 2 distribuições lado a lado e pode atualizar e fazer downgrade de qualquer distribuição a qualquer momento. Adicionar o WSL 2 como uma nova arquitetura apresenta uma plataforma melhor para a equipe de WSL fornecer recursos que tornam o WSL uma maneira incrível de executar um ambiente Linux no Windows.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>Poderei executar o WSL 2 e outras ferramentas de virtualização de terceiros, como VMware ou VirtualBox?

Alguns aplicativos de terceiros não podem funcionar quando o Hyper-V está em uso, o que significa que eles não poderão ser executados quando o WSL 2 estiver habilitado. Infelizmente, isso inclui o VMware e as versões do VirtualBox antes do VirtualBox 6 (VirtualBox 6.0.0 lançado em dezembro de 2018 [agora dá suporte ao Hyper-V como um núcleo de execução de fallback em um host do Windows][1]!)

Estamos investigando maneiras de ajudar a resolver esse problema. Por exemplo, exponhamos um conjunto de APIs chamado [plataforma de hipervisor][2] que os provedores de virtualização de terceiros podem usar para tornar seu software compatível com o Hyper-V. Isso permite que os aplicativos usem a arquitetura do Hyper-V para sua emulação, como [o Google Android Emulator e o][3]VirtualBox 6 e superior, que agora são compatíveis com o Hyper-V.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>Posso acessar a GPU no WSL 2? Há planos para aumentar o suporte a hardware?

Nas versões iniciais do suporte ao acesso ao hardware do WSL 2 será limitado, por exemplo: você não poderá acessar a GPU, a serial ou a USBs. No entanto, adicionar melhor suporte a dispositivos é alto em nossa pendência, pois isso abre muitos outros casos de uso para os desenvolvedores que desejam interagir com esses dispositivos. Enquanto isso, você sempre pode usar WSL 1 que tem acesso USB e porta serial. Fique atento a este blog e WSL os membros da equipe no Twitter para se manter informado sobre os recursos mais recentes que estão chegando às compilações internas e entrar em contato para nos enviar comentários sobre quais dispositivos você gostaria de interagir!

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>O WSL 2 será capaz de usar aplicativos de rede?

Sim, em geral, os aplicativos de rede serão mais rápidos e funcionarão melhor, pois temos compatibilidade total com a chamada do sistema. No entanto, a nova arquitetura usa componentes de rede virtualizados. Isso significa que, em builds de visualização inicial, o WSL 2 se comportará de forma semelhante a uma máquina virtual, por exemplo: WSL 2 terá um endereço IP diferente do computador host. Estamos comprometidos em fazer com que o WSL 2 tenha a mesma aparência do WSL 1 e que inclui melhorar nossa história de rede. Esperamos adicionar melhorias o mais rápido possível, como acessar todos os aplicativos de rede do Linux ou do Windows usando localhost. Lançaremos mais detalhes sobre nossa história de rede e aprimoramentos conforme abordamos o lançamento do WSL 2.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>Posso executar o WSL 2 em uma máquina virtual?

Sim! Você precisa certificar-se de que a máquina virtual tenha a virtualização aninhada habilitada. Isso pode ser habilitado em seu host do Hyper-V pai executando o seguinte comando em uma janela do PowerShell com privilégios de administrador:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

Certifique-se de substituir&lt;'&gt;VMName ' pelo nome da sua máquina virtual.

## <a name="can-i-use-wslconf-in-wsl-2"></a>Posso usar WSL. conf no WSL 2?

WSL 2 dá suporte ao mesmo arquivo WSL. conf que o WSL 1 usa. Isso significa que todas as opções de configuração que você definiu em um WSL 1 distribuição, como a montagem automática de unidades do Windows, a habilitação ou desabilitação da interoperabilidade, a alteração do diretório em que as unidades do Windows serão montadas, etc. funcionará dentro do WSL 2. Você pode saber mais sobre as opções de configuração em WSL na página de [Gerenciamento do distribuição](./wsl-config.md) . 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
