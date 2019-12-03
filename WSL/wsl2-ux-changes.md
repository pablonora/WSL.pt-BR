---
title: Alterações de UX entre WSL 1 e WSL 2
description: Alterações de experiência do usuário entre WSL 1 e WSL 2
keywords: BashOnWindows, Bash, WSL, wsl2, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 635e4335bd3fe5dd1629faba0168ec4fa331e190
ms.sourcegitcommit: 6f6b7b67dd35b5fc7b582bb7ac27b9936dedb23d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/02/2019
ms.locfileid: "74681641"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>Alterações de experiência do usuário entre WSL 1 e WSL 2

Esta página passa pelas diferenças de experiência do usuário entre o WSL 1 e a versão prévia do WSL 2. As principais alterações a serem observadas são:

- Coloque os arquivos que seus aplicativos Linux acessarão no sistema de arquivos raiz do Linux para uma velocidade de desempenho de arquivo mais rápida
- Em compilações iniciais da visualização do WSL 2, você precisará acessar aplicativos de rede usando um endereço IP e não usando localhost

E abaixo está a lista completa de outras alterações que você pode observar:

- O WSL 2 usa um [disco de hardware virtual](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) para armazenar seus arquivos e, se você atingir seu tamanho máximo, talvez seja necessário expandi-lo
- Ao iniciar, o WSL 2 agora usará uma pequena proporção de memória
- A velocidade de acesso ao arquivo do sistema operacional será mais lenta em compilações iniciais de visualização

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Coloque os arquivos do Linux no sistema de arquivos raiz do Linux
Certifique-se de colocar os arquivos que serão acessados com frequência com aplicativos Linux dentro do seu sistema de arquivos raiz Linux para aproveitar os benefícios de desempenho do arquivo. Esses arquivos precisam estar dentro do sistema de arquivos raiz do Linux para ter acesso mais rápido ao sistema de arquivos. Também tornamos possível que os aplicativos do Windows acessem o sistema de arquivos raiz do Linux (como o explorador de arquivos! Tente executar: `explorer.exe .` no diretório base de seu distribuição do Linux e veja o que acontece), o que tornará essa transição significativamente mais fácil. 

## <a name="accessing-network-applications"></a>Acessando aplicativos de rede
Nas compilações iniciais da versão prévia do WSL 2, você precisará acessar qualquer Windows Server do Linux usando o endereço IP do seu computador host.

### <a name="accessing-windows-applications-from-linux"></a>Acessando aplicativos do Windows no Linux
Para acessar um aplicativo de rede do Windows, você precisará usar o endereço IP do seu computador host. Você pode fazer isso com estas etapas:

- Obtenha o endereço IP do seu computador host executando o comando `cat /etc/resolv.conf` e copiando o endereço IP após o termo `nameserver`. 
- Conecte-se a qualquer servidor Windows usando o endereço IP copiado.

A figura abaixo mostra um exemplo disso conectando-se a um servidor node. js em execução no Windows via ondulação. 

![Acessando aplicativos de rede Linux do Windows](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows-only-in-builds-lower-than-18945"></a>Acessando aplicativos Linux do Windows (somente em compilações inferiores a 18945)
Se você tiver um servidor em um WSL distribuição, precisará encontrar o endereço IP da máquina virtual que está ligando seu distribuição e conectar-se a ele com esse endereço IP. Você pode fazer isso seguindo estas etapas:

- Obtenha o endereço IP do seu distribuição executando o comando `ip addr` dentro de seu WSL distribuição e encontrando-o sob o valor `inet` da interface `eth0`.
   - Você pode encontrar isso mais facilmente filtrando a saída do comando usando grep da seguinte maneira: `ip addr | grep eth0`.
- Conecte-se ao seu servidor Linux usando o IP encontrado acima.

A figura abaixo mostra um exemplo disso conectando-se a um servidor node. js usando o navegador Edge.

![Acessando aplicativos de rede Linux do Windows](media/wsl2-network-w2l.jpg)

Se sua compilação for 18945 ou superior, você poderá usar localhost da mesma forma que o normal. 

### <a name="other-networking-considerations"></a>Outras considerações de rede

#### <a name="connecting-via-remote-ip-addresses"></a>Conectando por meio de endereços IP remotos

Ao usar endereços IP remotos para se conectar aos seus aplicativos, eles serão tratados como conexões da LAN (rede local). Isso significa que você precisará certificar-se de que seu aplicativo pode aceitar conexões de LAN, ou seja, talvez seja necessário associar seu aplicativo a `0.0.0.0` em vez de `127.0.0.1`. Por exemplo, no Python usando Flask, isso pode ser feito com o comando: `app.run(host='0.0.0.0')`. Tenha em mente a segurança ao fazer essas alterações, pois isso permitirá conexões de sua LAN. 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>Acessando um WSL2 distribuição da rede local (LAN)

Ao usar um WSL1 distribuição, se o computador tiver sido configurado para ser acessado pelo em sua LAN, os aplicativos executados no WSL também poderão ser acessados em sua LAN. Esse não é o caso padrão em WSL2, pois WSL2 tem um adaptador Ethernet virtualizado com seu próprio endereço IP. No momento, para habilitar esse fluxo de trabalho, será necessário percorrer as mesmas etapas que você faria para uma máquina virtual normal. Estamos analisando maneiras de melhorar essa experiência!

#### <a name="ipv6-access"></a>Acesso IPv6

WSL2 distribuições atualmente não pode acessar endereços IPv6. Estamos trabalhando para adicionar esse recurso.

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Entender o WSL 2 usa um VHD e o que fazer se você atingir seu tamanho máximo
O WSL 2 armazena todos os arquivos do Linux dentro de um VHD que usa o sistema de arquivos EXT4. Esse VHD é redimensionado automaticamente para atender às suas necessidades de armazenamento. Esse VHD também tem um tamanho máximo inicial de 256 GB. Se seu distribuição aumentar de tamanho para ser maior que 256 GB, você verá erros informando que você ficou sem espaço em disco. Você pode corrigi-los expandindo o tamanho do VHD. As instruções sobre como fazer isso estão abaixo:

1. Encerrar todas as instâncias de WSL usando o comando `wsl --shutdown`
2. Localize o nome do pacote de instalação do distribuição ' PackageFamilyName '
   - Em um prompt do PowerShell (em que ' distribuição ' é o seu nome de distribuição), digite:
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. Localize o arquivo VHD FullPath usado pela sua instalação do WSL 2, que será o seu ' pathToVHD ':
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. Redimensione o VHD do WSL 2 concluindo os seguintes comandos
   - Abra uma janela de prompt de comando com privilégios de administrador e execute os seguintes comandos:
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. Inicie o WSL distribuição
6. Faça com que o WSL saiba que ele pode expandir o tamanho do seu sistema de arquivos
   - Execute estes comandos em seu WSL distribuição:
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copie o nome dessa entrada, que terá a seguinte aparência:/dev/sdXX (com o X representando qualquer outro caractere)
      - `sudo resize2fs /dev/sdXX`
         - Certifique-se de usar o valor copiado anteriormente e talvez seja necessário usar: `apt install resize2fs`.

Observação: em geral, não modifique, mova ou acesse os arquivos relacionados ao WSL localizados dentro da sua pasta AppData usando as ferramentas ou os editores do Windows. Isso pode fazer com que o distribuição do Linux fique corrompido.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 usará alguma memória na inicialização
O WSL 2 usa uma VM de utilitário leve em um kernel Linux real para fornecer excelente desempenho do sistema de arquivos e compatibilidade completa de chamada do sistema, enquanto ainda está sendo tão leve, rápido, integrado e responsivo como WSL 1. Essa VM do utilitário tem uma pequena superfície de memória e alocará memória com suporte de endereço virtual na inicialização. Ele é configurado para começar com uma pequena proporção da memória total.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>A velocidade do arquivo entre OS sistemas operacionais será mais lenta nas compilações iniciais de visualização
Você perceberá velocidades de arquivo mais lentas em comparação com WSL 1 ao acessar arquivos do Windows de um aplicativo Linux ou acessar arquivos do Linux de um aplicativo do Windows. Isso é resultado das alterações de arquitetura no WSL 2 e é algo que a equipe de WSL está investigando ativamente sobre como podemos melhorar essa experiência.
