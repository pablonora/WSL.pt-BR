---
title: Perguntas frequentes (FAQ)
description: Perguntas frequentes sobre o subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063264"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Perguntas frequentes sobre o subsistema do Windows para Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>O que é o subsistema do Windows para Linux (WSL)?
O subsistema Windows para Linux (WSL) é um novo recurso do Windows 10 que permite que você execute ferramentas de linha de comando Linux nativas diretamente no Windows, juntamente com sua área de trabalho do Windows tradicional e moderno de aplicativos da store.

Consulte a [sobre a página](./about.md) para obter mais detalhes.

## <a name="who-is-wsl-for"></a>Quem é o WSL para?
Isso é principalmente uma ferramenta para desenvolvedores – especialmente os desenvolvedores da web e aqueles que trabalham no ou com projetos de software livre. Isso permite que aqueles que desejar/precisar usar o Bash, ferramentas comuns do Linux (`sed`, `awk`, etc.) e muitas ferramentas de primeira Linux (Ruby, Python, etc.) para usar sua cadeia de ferramentas no Windows.

## <a name="what-can-i-do-with-wsl"></a>O que pode fazer com o WSL?
WSL fornece que um aplicativo chamado Bash.exe que, quando iniciado, abre um console do Windows executando o shell Bash. Como usar o Bash, você pode executar aplicativos e ferramentas de linha de comando do Linux. Por exemplo, digite `lsb_release -a` e pressione enter; você verá os detalhes da distribuição do Linux em execução no momento:

![Captura de tela de detalhes de distribuição](media/distro.png)

Você também pode acessar o sistema de arquivos do seu computador local de dentro do shell Bash do Linux – você encontrará suas unidades locais montadas sob o `/mnt` pasta. Por exemplo, sua `C:` unidade é montada em `/mnt/c`:  

![Captura de tela da unidade montada do C](media/ls.png)

## <a name="what-is-bash"></a>O que é o Bash?
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) é um popular shell baseado em texto e a linguagem de comandos. É o shell padrão incluído no Ubuntu e outras distribuições de Linux e no macOS. Os usuários digitar comandos em um shell para executar scripts e/ou executar comandos e ferramentas para realizar muitas tarefas.

## <a name="how-does-this-work"></a>Como isso funciona?
Confira nossos [blog](https://blogs.msdn.microsoft.com/wsl/) onde podemos entrar em detalhes sobre a tecnologia subjacente.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>Por que eu usaria WSL em vez de Linux em uma VM?
WSL requer menos recursos (CPU, memória e armazenamento) que uma máquina virtual completo. WSL também permite que você executar ferramentas de linha de comando do Linux e aplicativos, juntamente com seus aplicativos de área de trabalho e repositório de linha de comando do Windows e acessar seus arquivos do Windows de dentro do Linux. Isso permite que você use ferramentas de linha de comando do Linux e de aplicativos do Windows no mesmo conjunto de arquivos, se desejar.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>Por que usar, por exemplo, Ruby no Linux, em vez de no Windows?
Algumas ferramentas de plataforma cruzada foram criadas, supondo que o ambiente em que são executadas se comporta como o Linux. Por exemplo, algumas ferramentas pressupõem que eles sejam capazes de acessar os caminhos de arquivo muito longo ou a existência de arquivos/pastas específicas. Com frequência isso causa problemas no Windows, que geralmente se comporta de forma diferente do Linux.

Muitas linguagens como Ruby e nó são geralmente transportados para o e perfeitamente, executados no Windows. No entanto, nem todos os proprietários da biblioteca de nó/NPM ou Gem Ruby portar suas bibliotecas para dar suporte a Windows, e muitas têm dependências específicas do Linux. Geralmente, isso pode resultar em sistemas criados usando essas ferramentas e bibliotecas apresentando problemas de compilação e, às vezes, erros de tempo de execução ou comportamentos indesejados no Windows.

Esses são apenas alguns dos problemas que causaram a várias pessoas pergunte à Microsoft para melhorar as ferramentas de linha de comando dos Windows e o que nos levou a parceria com a Canonical para habilitar o Bash e Linux da linha de comando ferramentas nativas ser executado no Windows.

## <a name="what-does-this-mean-for-powershell"></a>O que isso significa para o PowerShell?
Enquanto estiver trabalhando com projetos de software livre, há várias situações em que é extremamente útil descartar em Bash do PowerShell do prompt. Suporte de bash é complementar e reforça o valor da linha de comando no Windows, permitindo que o PowerShell e a comunidade do PowerShell para aproveitamento de outras tecnologias populares.

Leia mais sobre o blog da equipe do PowerShell – [Bash para Windows: Por que é impressionante e o que significa para o PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>Pode executar o Linux todos os aplicativos no WSL?
Não! WSL é uma ferramenta que permitem que os usuários que precisam delas, execute o Bash e as principais ferramentas de linha de comando do Linux no Windows. 

WSL faz **não** tem como objetivo para dar suporte a desktops de GUI ou aplicativos (por exemplo, Gnome, KDE, etc.)  

Além disso, mesmo que você poderá executar muitos aplicativos populares de servidor (por exemplo, Redis), não recomendamos WSL para hospedar os serviços de produção – a Microsoft oferece uma variedade de soluções para executar cargas de trabalho do Linux de produção no Azure, Hyper-V e o Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>Quais SKUs do Windows WSL está incluído?
Subsistema do Windows para Linux está disponível na versão da área de trabalho de atualização do Windows para o aniversário do Windows 10 e os criadores ou posterior.

A partir do Fall Creators update WSL estará disponível na área de trabalho e servidor SKUs do Windows.

## <a name="what-processors-does-wsl-support"></a>Quais processadores WSL dá suporte?
WSL dá suporte a x64 e ARM CPUs.

## <a name="how-do-i-access-my-c-drive"></a>Como fazer para acessar a unidade c:
Pontos de montagem de disco rígido no computador local são criados automaticamente e fornecem acesso fácil para o sistema de arquivos do Windows. 
 
**/mnt/\<letra da unidade > /**
 
Exemplo de uso seria `cd /mnt/c` acessar c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Como posso usar um arquivo do Windows com um aplicativo do Linux?

Um dos benefícios de WSL está sendo capaz de acessar seus arquivos por meio de ferramentas ou aplicativos do Windows e Linux. 

WSL monta a unidades fixas do seu computador sob o `/mnt/<drive>` pasta no seu distribuições do Linux. Por exemplo, seu `C:` unidade é montada em `/mnt/c/` 

Usando suas unidades montadas, você pode editar o código, por exemplo, `C:\dev\myproj\` usando [Visual Studio](https://visualstudio.microsoft.com/vs/) / ou [VS Code](https://code.visualstudio.com/)e a compilação e teste desse código em Linux, acessando os mesmos arquivos por meio de `\mnt\c\dev\myproj`.

> **OBSERVAÇÃO IMPORTANTE**: Uma das principais limitações do uso de WSL é que não é suportado diretamente acessar/alterando arquivos no sistema de arquivos de suas distribuições do Linux usando aplicativos do Windows ou ferramentas. Consulte: [Não altere os arquivos do Linux usando ferramentas e aplicativos do Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Arquivos na unidade de Linux são diferentes da unidade montada do Windows?

1. Arquivos na raiz do Linux (ou seja, `/`) são controladas pela WSL que imita o comportamento específico do Linux, incluindo mas não limitado a:
   * Arquivos que contêm caracteres de nome de arquivo inválidos do Windows
   * Links simbólicos criados para usuários não administradores
   * Alterando atributos de arquivo por meio de chmod e alterar o proprietário
   * Diferenciação de arquivo/pasta

2. Arquivos em unidades montadas são controlados pelo Windows e tem os seguintes comportamentos:
   * Suporte a diferenciação de maiusculas
   * Todas as permissões são definidas para refletir melhor as permissões do Windows

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>Por que existem muitos erros quando eu executo o apt-get atualização?
Alguns pacotes usam recursos que ainda não implementamos ainda. `udev`, por exemplo, ainda não tem suporte e faz com que diversos `apt-get upgrade` erros.

Para corrigir problemas relacionados à `udev`, siga as etapas a seguir:

1. Escreva o seguinte para `/usr/sbin/policy-rc.d` e salve suas alterações.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Adicionar permissões de execução ao `/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. Execute os seguintes comandos

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>Como desinstalar uma distribuição WSL?

Em compilações antes 1709 (16299) abra um prompt de comando e execute:
  ```batchfile
  lxrun /uninstall /full
  ```
  
Distribuições de WSL instaladas da loja podem ser desinstaladas como qualquer outro aplicativo do Windows, clicando duas vezes no bloco do aplicativo e clicando em desinstalação, ou por meio do PowerShell usando o [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).

## <a name="why-does-ping-generate-permission-denied-errors"></a>Por que o ping gerar erros de permissão negada?
Em WSL builds < 14926, ping necessárias WSL para execução por meio de um Console com privilégios elevados. Esse problema foi corrigido no Build 14926 e versões posteriores.

## <a name="how-do-i-run-an-openssh-server"></a>Como fazer para executar um OpenSSH server?
São necessários privilégios de administrador no Windows para executar o OpenSSH no WSL. Para executar um OpenSSH server, execute o Bash no Ubuntu no Windows como administrador ou execute bash.exe em um prompt do PowerShell/CMD com privilégios de administrador.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>Por que recebo "Erro: 0x80040306 "quando tento instalar?
WSL não oferece suporte à execução em um console herdado. Para desativar o console herdado:

1. Abra Cmd, PowerShell ou WSL
1. Clique com botão direito no título da barra -> Propriedades -> desmarque "Usar console herdado"
1. Clique em OK

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>Por que recebo "Erro: 0x80040154 "ao executar bash.exe após a atualização do Windows?
O recurso de "Subsistema Windows para Linux" pode ser desabilitado durante uma atualização do Windows. Se isso acontecer, o recurso do Windows deve ser habilitado novamente. Instruções para habilitar o recurso de "Subsistema Windows para Linux" podem ser encontradas na [guia de instalação](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

## <a name="how-do-i-change-the-display-language-of-wsl"></a>Como altero o idioma de exibição de WSL?
Instalação do WSL tentará alterar automaticamente a localidade do Ubuntu para coincidir com a localidade de sua instalação do Windows. Se você não quiser esse comportamento, você pode executar este comando para alterar a localidade do Ubuntu, após a conclusão da instalação. Você precisará reiniciar bash.exe para que essa alteração tenha efeito.

A seguir o exemplo altera a localidade en-US:
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>Por que eu não tenho acesso à internet de WSL?
Alguns usuários relataram problemas com aplicativos específicos de firewall bloqueando o acesso à internet no WSL. Os firewalls relatados são:

1. Kaspersky
1. AVG
1. Avast

Em alguns casos permite desativar o firewall para acesso. Em alguns casos a simples presença do firewall instalado procura para bloquear o acesso.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Como acessar uma porta de WSL no Windows?
WSL compartilha o endereço IP do Windows, pois ele está em execução no Windows. Como tal, você pode acessar todas as portas no localhost, por exemplo, se você tivesse o conteúdo da web na porta 1234, você poderia https://localhost:1234 no seu navegador do Windows.

## <a name="where-can-i-provide-feedback"></a>Onde posso fornecer comentários?

Você pode compartilhar suas opiniões e fazer perguntas por meio de vários canais: Comentários e perguntas devem ser direcionadas para:
* Nosso [rastreador de problemas do GitHub](https://github.com/Microsoft/BashOnWindows/issues)
* Nosso [portal de linha de comando do UserVoice](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Nosso [blog da equipe de linha de comando](https://blogs.msdn.microsoft.com/commandline/)
* Por meio do Twitter. Siga [ @richturn_ms ](https://twitter.com/richturn_MS) no Twitter para saber de notícias, atualizações, etc.
