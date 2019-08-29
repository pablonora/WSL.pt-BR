---
title: Perguntas frequentes (FAQ)
description: Perguntas frequentes sobre o subsistema do Windows para Linux.
keywords: BashOnWindows, Bash, WSL, Windows, windowssubsystem, perguntas frequentes
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: e3376f8dff83262577bc52fb3ac368b70b21d922
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122761"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Perguntas frequentes sobre o subsistema do Windows para Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>O que é o subsistema do Windows para Linux (WSL)?
O subsistema do Windows para Linux (WSL) é um novo recurso do Windows 10 que permite executar ferramentas de linha de comando nativas do Linux diretamente no Windows, juntamente com seus aplicativos tradicionais de área de trabalho do Windows e da loja moderna.

Consulte a [página sobre](./about.md) para obter mais detalhes.

## <a name="who-is-wsl-for"></a>Quem é WSL?
Isso é basicamente uma ferramenta para desenvolvedores – especialmente desenvolvedores da Web e aqueles que trabalham em ou com projetos de software livre. Isso permite que aqueles que desejam/precisem usar bash, ferramentas`sed`comuns `awk`do Linux (, etc.) e muitas ferramentas do Linux (Ruby, Python, etc.) para usar seus ferramentas no Windows.

## <a name="what-can-i-do-with-wsl"></a>O que posso fazer com o WSL?
O WSL fornece um aplicativo chamado bash. exe que, quando iniciado, abre um console do Windows que executa o shell bash. Usando o bash, você pode executar aplicativos e ferramentas de linha de comando do Linux. Por exemplo, digite `lsb_release -a` e pressione Enter. você verá os detalhes do distribuição do Linux em execução no momento:

![Captura de tela de detalhes do distribuição](media/distro.png)

Você também pode acessar o sistema de arquivos do computador local de dentro do shell do Linux bash – você encontrará as unidades locais `/mnt` montadas na pasta. Por exemplo, sua `C:` unidade está montada `/mnt/c`em:  

![Captura de tela da unidade C montada](media/ls.png)

## <a name="what-is-bash"></a>O que é bash?
O [bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) é um shell baseado em texto popular e linguagem de comando. É o shell padrão incluído no Ubuntu e em outros distribuições do Linux e no macOS. Os usuários digitam comandos em um shell para executar scripts e/ou executar comandos e ferramentas para realizar muitas tarefas.

## <a name="how-does-this-work"></a>Como isso funciona?
Confira nosso [blog](https://blogs.msdn.microsoft.com/wsl/) onde entramos em detalhes sobre a tecnologia subjacente.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>Por que usar WSL em vez do Linux em uma VM?
O WSL requer menos recursos (CPU, memória e armazenamento) do que uma máquina virtual completa. O WSL também permite que você execute aplicativos e ferramentas de linha de comando do Linux juntamente com os aplicativos de linha de comando, área de trabalho e da loja do Windows e para acessar os arquivos do Windows de dentro do Linux. Isso permite que você use aplicativos do Windows e ferramentas de linha de comando do Linux no mesmo conjunto de arquivos, se desejar.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>Por que eu usaria, por exemplo, Ruby no Linux em vez de no Windows?
Algumas ferramentas de plataforma cruzada foram criadas supondo que o ambiente no qual elas são executadas se comporta como o Linux. Por exemplo, algumas ferramentas pressupõem que elas sejam capazes de acessar caminhos de arquivo muito longos ou que arquivos/pastas específicos existam. Isso geralmente causa problemas no Windows que, com freqüência, se comporta de forma diferente do Linux.

Muitas linguagens, como Ruby e node, costumam ser modeladas e funcionam muito bem no Windows. No entanto, nem todos os proprietários do gem Ruby ou do node/NPM library têm suas bibliotecas para dar suporte ao Windows e muitos têm dependências específicas do Linux. Isso geralmente pode resultar em sistemas criados usando tais ferramentas e bibliotecas que estão sofrendo de compilação e, às vezes, erros de tempo de execução ou comportamentos indesejados no Windows.

Esses são apenas alguns dos problemas que fizeram com que muitas pessoas perguntassem à Microsoft para aprimorar as ferramentas de linha de comando do Windows e o que nos levou para fazer parcerias com o Canonical para habilitar as ferramentas de linha de comando do Linux e bash nativas para serem executadas no Windows.

## <a name="what-does-this-mean-for-powershell"></a>O que isso significa para o PowerShell?
Ao trabalhar com projetos OSS, há inúmeros cenários em que é imensamente útil entrar em bash a partir de um prompt do PowerShell. O suporte para bash é complementar e fortalece o valor da linha de comando no Windows, permitindo que o PowerShell e a Comunidade do PowerShell aproveitem outras tecnologias populares.

Leia mais no blog da equipe do PowerShell – [bash para Windows: Por que é incrível e o que significa para o PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>Posso executar todos os aplicativos do Linux no WSL?
Não! WSL é uma ferramenta voltada para permitir que os usuários que precisam deles executem ferramentas de linha de comando bash e Core Linux no Windows. 

O WSL não dá suporte a áreas de trabalho de GUI ou aplicativos (por exemplo, GNOME, KDE, etc.)  

Além disso, embora você possa executar muitos aplicativos de servidor populares (por exemplo, Redis), não recomendamos o WSL para hospedar serviços de produção – a Microsoft oferece uma variedade de soluções para executar cargas de trabalho de produção do Linux no Azure, no Hyper-V e no Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>Em quais SKUs do Windows o WSL está incluído?
O subsistema do Windows para Linux está disponível na versão de área de trabalho do Windows para a atualização de aniversários e criadores do Windows 10 ou posterior.

A partir dos criadores de outono, a atualização WSL estará disponível nas SKUs de desktop e de servidor do Windows.

## <a name="what-processors-does-wsl-support"></a>A quais processadores o WSL dá suporte?
O WSL dá suporte a CPUs x64 e ARM.

## <a name="how-do-i-access-my-c-drive"></a>Como fazer acessar minha unidade C:?
Pontos de montagem para discos rígidos no computador local são criados automaticamente e fornecem acesso fácil ao sistema de arquivos do Windows. 
 
**letra\<da unidade/mnt/>/**
 
Exemplo `cd /mnt/c` de uso seria acessar c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Como fazer usar um arquivo do Windows com um aplicativo do Linux?

Um dos benefícios do WSL é a capacidade de acessar seus arquivos por meio de aplicativos ou ferramentas do Windows e do Linux. 

O WSL monta as unidades `/mnt/<drive>` fixas da máquina na pasta em seu distribuições do Linux. Por exemplo, sua `C:` unidade está montada em`/mnt/c/` 

Usando suas unidades montadas, você pode editar o código no, por `C:\dev\myproj\` exemplo, usando o [Visual Studio](https://visualstudio.microsoft.com/vs/) /ou [vs Code](https://code.visualstudio.com/), e criar/testar esse código no Linux acessando `/mnt/c/dev/myproj`os mesmos arquivos por meio do.

> **OBSERVAÇÃO IMPORTANTE**: Uma das principais limitações do uso do WSL é que o acesso e a alteração direta de arquivos em seu sistema de arquivos do Linux distribuições usando aplicativos ou ferramentas do Windows não tem suporte. Consulte: [Não altere os arquivos do Linux usando ferramentas e aplicativos do Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Os arquivos na unidade Linux são diferentes da unidade montada do Windows?

1. Os arquivos na raiz do Linux (ou `/`seja,) são controlados por WSL que imita o comportamento específico do Linux, incluindo, mas não se limitando a:
   * Arquivos que contêm caracteres de nome de arquivo do Windows inválidos
   * Symlinks criado para usuários não administradores
   * Alterando atributos de arquivo por meio de chmod e proprietário
   * Distinção entre maiúsculas e minúsculas de arquivo/pasta

2. Os arquivos em unidades montadas são controlados pelo Windows e têm os seguintes comportamentos:
   * Diferenciação do caso de suporte
   * Todas as permissões são definidas para refletir melhor as permissões do Windows

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>Por que há muitos erros quando executo apt-get upgrade?
Alguns pacotes usam recursos que ainda não implementamos. `udev`, por exemplo, ainda não tem suporte e causa `apt-get upgrade` vários erros.

Para corrigir problemas relacionados ao `udev`, siga as seguintes etapas:

1. Grave o seguinte no `/usr/sbin/policy-rc.d` e salve suas alterações.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Adicionar permissões de execução a`/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. Execute os seguintes comandos

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>Como fazer desinstalar uma distribuição WSL?

Em builds anteriores a 1709 (16299), abra um prompt de comando e execute:
  ```batchfile
  lxrun /uninstall /full
  ```
  
As distribuições do WSL instaladas no repositório podem ser desinstaladas como qualquer outro aplicativo do Windows, clicando com o botão direito do mouse no bloco do aplicativo e clicando em desinstalar ou por meio do PowerShell usando o [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).

## <a name="why-does-ping-generate-permission-denied-errors"></a>Por que o ping gera erros de permissão negada?
No WSL Builds < 14926, ping necessário WSL para executar por meio de um console elevado. Esse problema foi corrigido no Build 14926 e posterior.

## <a name="how-do-i-run-an-openssh-server"></a>Como fazer executar um servidor OpenSSH?
São necessários privilégios de administrador no Windows para executar o OpenSSH no WSL. Para executar um servidor OpenSSH, execute o bash no Ubuntu no Windows como administrador ou execute o bash. exe em um prompt do CMD/PowerShell com privilégios de administrador.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>Por que obtenho "erro: 0x80040306 "quando tento instalar?
WSL não dá suporte à execução em um console herdado. Para desativar o console herdado:

1. Abra o WSL, o PowerShell ou o cmd
1. Clique com o botão direito do mouse na barra de título-> Propriedades-> desmarque "usar o console herdado"
1. Clique em OK

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>Por que obtenho "erro: 0x80040154 "quando executo o bash. exe após a atualização do Windows?
O recurso "subsistema do Windows para Linux" pode ser desabilitado durante uma atualização do Windows. Se isso acontecer, o recurso do Windows deverá ser habilitado novamente. As instruções para habilitar o recurso "subsistema do Windows para Linux" podem ser encontradas no [Guia de instalação](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)do.

## <a name="how-do-i-change-the-display-language-of-wsl"></a>Como fazer alterar o idioma de exibição do WSL?
A instalação do WSL tentará alterar automaticamente a localidade do Ubuntu para corresponder à localidade da instalação do Windows. Se você não quiser esse comportamento, poderá executar esse comando para alterar a localidade do Ubuntu após a conclusão da instalação. Você precisará reiniciar o bash. exe para que essa alteração entre em vigor.

O exemplo abaixo muda para a localidade para en-US:
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>Por que não tenho acesso à Internet do WSL?
Alguns usuários relataram problemas com aplicativos de firewall específicos que bloqueiam o acesso à Internet no WSL. Os firewalls relatados são:

1. Kaspersky
1. MÉDIA
1. Avast

Em alguns casos, a desativação do firewall permite o acesso. Em alguns casos, simplesmente ter o firewall instalado procura bloquear o acesso.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Como fazer acessar uma porta do WSL no Windows?
WSL compartilha o endereço IP do Windows, pois ele é executado no Windows. Como tal, você pode acessar qualquer porta no localhost, por exemplo, se você tivesse conteúdo da Web na https://localhost:1234 porta 1234, poderia no seu navegador do Windows.

## <a name="how-can-i-back-up-my-wsl-distros"></a>Como posso fazer backup de meu WSL distribuições?

A melhor maneira de fazer backup de seu distribuições está disponível no Windows versão 1809 e posterior. Você pode exportar toda a distribuição para um tarball usando o `wsl --export` comando. Em seguida, você pode importar esse distribuição de volta para `wsl --import` o WSL usando o comando, permitindo que você faça backup e salve Estados de suas distribuições do WSL. 

Observe que os serviços de backup tradicionais que os arquivos de backup em suas pastas AppData (como o backup do Windows) não corromperão os arquivos do Linux. 



## <a name="where-can-i-provide-feedback"></a>Onde posso fornecer comentários?

Você pode compartilhar comentários e fazer perguntas por meio de vários canais: Comentários e perguntas devem ser direcionados para:
* Nosso [rastreador de problemas do GitHub](https://github.com/Microsoft/BashOnWindows/issues)
* Nosso [portal de UserVoice de linha de comando](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Nosso [blog da equipe de linha de comando](https://blogs.msdn.microsoft.com/commandline/)
* Por meio do Twitter. Siga [@richturn_ms](https://twitter.com/richturn_MS) no Twitter para aprender sobre notícias, atualizações, etc.
