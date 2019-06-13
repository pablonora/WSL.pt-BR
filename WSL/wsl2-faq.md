---
title: Perguntas frequentes sobre o WSL 2
description: Perguntas frequentes sobre o subsistema Windows para Linux 2
keywords: Instalar o BashOnWindows, bash, wsl, wsl2, windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10,
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 84805278abaeb6334c662e1dfab1bced3e0ddb0b
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038086"
---
# <a name="wsl-2-faq"></a>PERGUNTAS FREQUENTES SOBRE O WSL 2

Abaixo está uma lista de perguntas frequentes (FAQ) sobre o subsistema Windows para Linux 2.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>O WSL 2 usa o Hyper-V? Ele estará disponível no Windows 10 Home?

2 WSL estará disponível em todos os SKUs onde WSL está disponível no momento, incluindo Windows 10 Home.

A versão mais recente do WSL usa arquitetura Hyper-V para habilitar sua virtualização. Essa arquitetura estará disponível em um componente opcional que é um subconjunto do recurso do Hyper-V. Este componente opcional estará disponível em todas as SKUs. Você pode esperar ver mais detalhes sobre essa experiência assim que nos aproximarmos para a versão 2 do WSL.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>O que acontecerá com WSL 1? Ele será ser abandonado?

No momento, não temos planos para substituir o WSL 1. Você pode executar WSL 1 e 2 WSL distribuições lado a lado e pode atualizar e fazer o downgrade de qualquer distribuição a qualquer momento. Adicionando o WSL 2 como uma nova arquitetura apresenta uma plataforma melhor para a equipe do WSL oferecer recursos que tornam o WSL uma maneira incrível para executar um ambiente Linux no Windows.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>Será possível executar WSL 2 e outras ferramentas de virtualização de terceiros 3ª como VirtualBox ou VMware?

Alguns aplicativos de terceiros 3ª não funcionam quando o Hyper-V está em uso, o que significa que não será capazes de executar quando o WSL 2 está habilitado. Infelizmente, isso inclui o VMware e em versões do VirtualBox antes do VirtualBox 6 (6.0.0 lançado em dezembro de 2018 do VirtualBox [agora dá suporte ao Hyper-V como um núcleo de execução de fallback em um host do Windows] [ 1]!)

Estamos investigando maneiras para ajudar a resolver esse problema. Por exemplo, vamos expor um conjunto de APIs chamados [plataforma de hipervisor] [ 2] que provedores de virtualização de terceiros podem usar para tornar o seu software compatíveis com o Hyper-V Isso permite que aplicativos usado como a arquitetura do Hyper-V seu emulação [o Google Android Emulator][3], e o VirtualBox, 6 e acima do qual são agora compatíveis com Hyper-V.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>Para acessar a GPU no WSL 2? Há planos para aumentar o suporte de hardware?

Nas versões iniciais do acesso ao hardware WSL 2 suporte será limitado, por exemplo: não será possível acessar a GPU, serial ou USBs. No entanto, adicionar um melhor suporte de dispositivo é alto em nossa lista de pendências, pois isso abre muitos mais casos de uso para os desenvolvedores que desejarem para interagir com esses dispositivos. Enquanto isso, você sempre pode usar 1 WSL que tem acesso USB e porta serial. Por favor, fique ligado neste blog e os membros da equipe WSL no Twitter para ficar informado sobre os recursos mais recentes, chegando ao insider compila e em contato para fornecer comentários sobre a quais dispositivos você gostaria de interagir com!

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>2 WSL poderão usar aplicativos de rede?

Sim, em geral a aplicativos de rede serão mais rápido e funcionam melhor, já que temos completa do sistema chamada compatibilidade. No entanto, a nova arquitetura usa componentes de rede virtualizados. Isso significa que, no modo de visualização inicial, compilações WSL 2 se comportarão de forma mais semelhante a uma máquina virtual, por exemplo: 2 WSL terá um endereço IP diferente no computador host. Estamos empenhados em fazer com que o WSL 2 se sinta o mesmo que 1 WSL e que inclui a melhorar nossa história de rede. Esperamos adicionar melhorias mais rápido possível, como acessar todos os aplicativos de rede do Linux ou Windows usando localhost. Publicaremos mais detalhes sobre nossa história e melhorias de rede quando nos aproximarmos do lançamento do WSL 2.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>Pode executar o WSL 2 em uma máquina virtual?

Sim! Você precisará certificar-se de que a máquina virtual tem aninhada virtualização habilitada. Isso pode ser habilitado no Hyper-V, executando o seguinte comando em uma janela do PowerShell com privilégios de administrador:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

Certifique-se de substituir '&lt;VMName&gt;' com o nome de sua máquina virtual.

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/