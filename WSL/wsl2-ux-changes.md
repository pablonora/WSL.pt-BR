---
title: Alterações UX entre WSL 1 e 2 do WSL
description: Mudanças na experiência do usuário entre WSL 1 e 2 do WSL
keywords: BashOnWindows, bash, wsl, wsl2, windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038096"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>Mudanças na experiência do usuário entre WSL 1 e 2 do WSL

Esta página ultrapassar as diferenças de experiência do usuário entre WSL 1 e a visualização de WSL 2. As principais alterações a serem consideradas são:

- Colocar arquivos de que seus aplicativos Linux acessará no seu sistema de arquivos de raiz do Linux para velocidade de desempenho mais rápido do arquivo
- Em compilações inicias da visualização 2 WSL você precisará acessar a aplicativos de rede usando um endereço IP e não usar localhost

E, abaixo está a lista completa de outras alterações que podem ser observados:

- WSL 2 usa um VHD para armazenar seus arquivos e se você atingir seu tamanho máximo que você pode precisar para expandi-lo
- Ao iniciar, WSL 2 agora usarão uma pequena proporção de memória
- Entre o sistema operacional, velocidade de acesso de arquivo será mais lenta em compilações de visualização inicial

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Coloque os arquivos do Linux em seu sistema de arquivos de raiz do Linux
Certifique-se de colocar os arquivos que você acessará frequentemente com o Linux aplicativos dentro de seu Linux raiz do sistema de arquivos para aproveitar os benefícios de desempenho do arquivo. Esses arquivos precisam estar dentro do sistema de arquivos raiz Linux para ter acesso de sistema de arquivos mais rápido. Podemos também tornam possível para aplicativos do Windows acessar o sistema de arquivos do Linux raiz (como o Explorador de arquivos! Tente executar: `explorer.exe /` em seu shell bash e veja o que acontece) que irá facilitar essa transição. 

## <a name="accessing-network-applications"></a>Acesso a aplicativos de rede
Nas compilações do preview 2 WSL inicias, você precisará acessar qualquer servidor do Linux do Windows usando o endereço IP de sua distribuição do Linux e qualquer servidor Windows do Linux usando o endereço IP do seu computador host. Isso é algo que é temporária e muito alta em nossa lista de prioridade para corrigir.

### <a name="accessing-linux-applications-from-windows"></a>Acesso a aplicativos do Linux do Windows
Se você tiver um servidor em uma distribuição WSL, você precisará localizar o endereço IP da máquina virtual capacitar sua distribuição e conectá-lo com esse endereço IP. Você pode fazer isso seguindo estas etapas:

- Obter o endereço IP da sua distribuição, executando o comando `ip addr` dentro de sua distribuição WSL e localizá-lo sob o `inet` valor o `eth0` interface.
   - Você pode encontrá-lo mais facilmente por meio da filtragem de saída do comando usando grep da seguinte forma: `ip addr | grep eth0`.
- Conecte-se ao seu servidor Linux usando o IP encontrado acima.

A figura abaixo mostra um exemplo ao se conectar a um servidor de nodeJS usando o navegador Edge.

![Acesso a aplicativos de rede do Linux do Windows](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>Acesso a aplicativos do Windows do Linux
Para acessar um aplicativo de rede do Windows, você precisará usar o endereço IP do seu computador host. Você pode fazer isso com estas etapas:

- Obter o endereço IP do seu computador host executando o comando `cat /etc/resolv.conf` e copiar o endereço IP após o termo `nameserver`. 
- Conecte-se a qualquer servidor do Windows usando o endereço IP copiado.

A figura abaixo mostra um exemplo ao se conectar a um servidor de python em execução no Windows por meio de rotação. 

![Acesso a aplicativos de rede do Linux do Windows](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Noções básicas sobre o WSL 2 usa um VHD e o que fazer se você atingir seu tamanho máximo
2 de WSL armazena todos os arquivos do Linux dentro de um VHD que usa o sistema de arquivos ext4. Esse VHD é redimensionado automaticamente para atender às suas necessidades de armazenamento. Esse VHD também tem um tamanho inicial máximo de 256GB. Se a sua distribuição aumenta de tamanho seja maior que 256GB, você verá erros informando que você executou sem espaço em disco. Você pode corrigi-los expandindo o tamanho do VHD. As instruções sobre como fazer isso estão abaixo:

1. Encerrar todas as instâncias WSL usando o `wsl --shutdown` comando
2. Redimensionar o VHD de 2 WSL executando os comandos a seguir
   - Abra um janela de prompt de comando com privilégios de administrador e execute os seguintes comandos:
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. Inicie sua distribuição WSL
4. Verifique o WSL ciente de que ele pode expandir o tamanho do seu sistema de arquivos
   - Execute estes comandos em sua distribuição WSL:
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copie o nome desta entrada, que se parecerá com: / DES/sdXX (com o X que representa qualquer outro caractere)
      - `sudo resize2fs /dev/sdXX`
         - Certifique-se de usar o valor copiado anteriormente, e você talvez precise usar: `apt install resize2fs`.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>2 WSL usará alguma memória na inicialização
WSL 2 usa um utilitário leve de VM em um kernel do Linux real para fornecer o desempenho do sistema de arquivo grande e completa do sistema chamada compatibilidade enquanto ainda estar assim como a luz, rápida, integrada e ágeis como 1 WSL. Esse utilitário VM tem uma pegada pequena de memória e alocará memória de endereço Virtual feito na inicialização. Ele é configurado para iniciar com uma pequena proporção do total de memória.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>Entre o sistema operacional, velocidade do arquivo será mais lenta em compilações de visualização inicial
Você observará que as velocidades de arquivo mais lentas em comparação com WSL 1 ao acessar arquivos do Windows de um aplicativo do Linux, ou acessar arquivos do Linux de um aplicativo do Windows. Isso é um resultado das alterações na arquitetura em WSL 2 e é algo que a equipe WSL ativamente está investigando nos como podemos melhorar essa experiência.