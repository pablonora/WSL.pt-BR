---
title: Alterações de experiência do usuário entre WSL 1 e WSL 2
description: Alterações de experiência do usuário entre WSL 1 e WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 1965a22a2e290777b207d9ded099ce4a79e1ed38
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256329"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>Alterações de experiência do usuário entre WSL 1 e WSL 2

Esta página aborda as diferenças de experiência do usuário entre o WSL 1 e a versão prévia do WSL 2. As principais alterações a serem observadas são:

- Coloque os arquivos que seus aplicativos Linux acessarão no sistema de arquivos raiz do Linux para agilizar a velocidade de desempenho do arquivo
- Em builds iniciais de versão prévia do WSL 2, você precisará acessar aplicativos de rede usando um endereço IP e não um localhost

Abaixo está a lista completa de outras alterações que você poderá observar:

- O WSL 2 usa um VHD [(Disco de Hardware Virtual)](https://en.wikipedia.org/wiki/VHD_(file_format)) para armazenar seus arquivos e, se você atingir o tamanho máximo, talvez seja necessário expandi-lo
- Ao iniciar, o WSL 2 usará uma pequena proporção de memória
- A velocidade cruzada de acesso ao arquivo do sistema operacional será mais lenta em builds iniciais de versão prévia

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Colocar os arquivos do Linux no sistema de arquivos raiz do Linux
Coloque os arquivos que serão acessados com frequência com aplicativos Linux dentro do seu sistema de arquivos raiz do Linux para aproveitar os benefícios de desempenho do arquivo. Esses arquivos precisam estar dentro do sistema de arquivos raiz do Linux para terem acesso mais rápido ao sistema de arquivos. Também possibilitamos que os aplicativos do Windows acessassem o sistema de arquivos raiz do Linux (como o Explorador de Arquivos! Tente executar: `explorer.exe .` no diretório base de sua distribuição do Linux e veja o que acontece), o que tornará essa transição significativamente mais fácil. 

## <a name="accessing-network-applications"></a>Acessar aplicativos de rede
Nos builds iniciais de versão prévia do WSL 2, você precisará acessar um servidor Windows no Linux usando o endereço IP do seu computador host.

### <a name="accessing-windows-applications-from-linux"></a>Acessar aplicativos do Windows no Linux
Para acessar um aplicativo de rede do Windows, você precisará usar o endereço IP do seu computador host. Você pode fazer isso com estas etapas:

- Obtenha o endereço IP do seu computador host executando o comando `cat /etc/resolv.conf` e copiando o endereço IP após o termo `nameserver`. 
- Conecte-se a qualquer servidor Windows usando o endereço IP copiado.

A imagem abaixo mostra um exemplo disso por meio da conexão com um servidor Node.js em execução no Windows via curl. 

![Acessar aplicativos de rede do Linux usando o Windows](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a>Acessar aplicativos do Linux usando o Windows

Dependendo da versão do Windows que você está usando, talvez seja necessário recuperar o endereço IP da máquina virtual. Se seu build for o 18945 ou superior, você poderá usar o `localhost` normalmente. 

#### <a name="accessing-linux-on-builds-lower-than-18945"></a>Acessar o Linux em builds anteriores a [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)

Se você tiver um servidor em uma distribuição do WSL, precisará encontrar o endereço IP da máquina virtual que está acionando sua distribuição e conectar-se a ela. Você pode fazer isso seguindo estas etapas:

- Obtenha o endereço IP da sua distribuição executando o comando `ip addr` dentro da distribuição do WSL e encontrando-o sob o valor `inet` da interface `eth0`.
   - Você pode encontrar isso mais facilmente filtrando a saída do comando usando grep da seguinte maneira: `ip addr | grep eth0`.
- Conecte-se ao seu servidor Linux usando o IP encontrado acima.

A imagem abaixo mostra um exemplo disso por meio da conexão com um servidor Node.js usando o navegador Edge.

![Acessar aplicativos de rede do Linux usando o Windows](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a>Outras considerações de rede

#### <a name="connecting-via-remote-ip-addresses"></a>Conectar-se via endereços IP remotos

Ao usar endereços IP remotos para se conectar aos seus aplicativos, eles serão tratados como conexões de LAN (rede local). Isso significa que você precisará verificar se seu aplicativo pode aceitar conexões de LAN, ou seja: talvez seja necessário associar seu aplicativo a `0.0.0.0` em vez de `127.0.0.1`. Por exemplo, no Python usando Flask, isso pode ser feito com o comando: `app.run(host='0.0.0.0')`. Tenha em mente a segurança ao fazer essas alterações, pois isso permitirá conexões de sua LAN. 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>Acessar uma distribuição do WSL2 usando a LAN (rede local)

Ao usar uma distribuição do WSL 1, se o computador tiver sido configurado para ser acessado pela sua LAN, os aplicativos executados no WSL também poderão ser acessados em sua LAN. Esse não é o caso padrão no WSL2, pois o WSL2 tem um adaptador Ethernet virtualizado com o próprio endereço IP. No momento, para habilitar esse fluxo de trabalho, será necessário percorrer as mesmas etapas que você faria para uma máquina virtual normal. Estamos analisando maneiras de aprimorar essa experiência!

#### <a name="ipv6-access"></a>Acesso IPv6

Atualmente, as distribuições do WSL 2 não conseguem acessar endereços IPv6. Estamos trabalhando para adicionar esse recurso.

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Entender como o WSL 2 usa um VHD e o que fazer se você atingir o tamanho máximo
O WSL 2 armazena todos os arquivos do Linux dentro de um VHD que usa o sistema de arquivos ext4. Esse VHD é redimensionado automaticamente para atender às suas necessidades de armazenamento. O VHD também tem um tamanho máximo inicial de 256 GB. Se sua distribuição aumentar de tamanho para exceder 256 GB, você verá erros informando que você ficou sem espaço em disco. Você pode corrigir isso expandindo o tamanho do VHD. Instruções sobre como fazer isto podem ser vistas abaixo:

1. Termine todas as instâncias WSL usando o comando `wsl --shutdown`
2. Localize o nome do pacote de instalação da distribuição, 'PackageFamilyName'
   - Em um prompt do PowerShell (em que 'distro' é o nome da distribuição), digite:
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. Localize o caminho completo do arquivo VHD usado pela sua instalação do WSL 2, que será o seu 'pathToVHD':
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. Redimensione o VHD do WSL 2 concluindo os seguintes comandos
   - Abra um prompt de comando com privilégios de administrador do Windows e execute os seguintes comandos:
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. Inicie a distribuição do WSL
6. Faça com que o WSL saiba que ele pode expandir o tamanho do sistema de arquivos
   - Execute estes comandos em sua distribuição do WSL:
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copie o nome dessa entrada, que terá a seguinte aparência: /dev/sdXX (com o X representando qualquer outro caractere)
      - `sudo resize2fs /dev/sdXX`
         - Use o valor copiado anteriormente. Talvez seja necessário usar: `apt install resize2fs`.

Observe: em geral, não modifique, mova ou acesse os arquivos relacionados ao WSL localizados dentro da sua pasta AppData usando as ferramentas ou os editores do Windows. Isso pode fazer com que a distribuição do Linux fique corrompida.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>O WSL 2 usará um pouco da memória na inicialização
O WSL 2 usa uma VM de utilitário leve em um kernel real do Linux para fornecer excelente desempenho do sistema de arquivos e compatibilidade completa de chamada do sistema, enquanto ainda é tão leve, rápido, integrado e responsivo quanto o WSL 1. Essa VM do utilitário tem um pequeno volume de memória e alocará memória com suporte de endereço virtual na inicialização. Ela é configurada para começar com uma pequena proporção da memória total.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>A velocidade cruzada do arquivo do sistema operacional será mais lenta em builds iniciais de versão prévia
Você perceberá velocidades de arquivo mais lentas em comparação com o WSL 1 ao acessar arquivos do Windows em um aplicativo do Linux ou acessar arquivos do Linux em aplicativos do Windows. Isso é resultado das alterações de arquitetura no WSL 2. A equipe do WSL está investigando ativamente como podemos aprimorar essa experiência.
