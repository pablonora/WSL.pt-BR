---
title: Conta de usuário e permissões do Linux
description: Referência para contas de usuário e gerenciamento de permissões com o subsistema do Windows para Linux.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema do Windows para Linux, windowssubsystem, Ubuntu, contas de usuário
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040828"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Contas de usuário e permissões para o subsistema do Windows para Linux

A criação de seu usuário do Linux é a primeira etapa na configuração de uma nova distribuição do Linux no WSL.  A primeira conta de usuário criada é automaticamente configurada com alguns atributos especiais:

1. É o usuário padrão--ele entra automaticamente na inicialização.
1. É administrador do Linux (um membro do grupo sudo) por padrão.

Cada distribuição do Linux em execução no subsistema do Windows para Linux tem suas próprias contas de usuário e senhas do Linux.  Você precisará configurar uma conta de usuário do Linux sempre que adicionar uma distribuição, reinstalação ou redefinição.  As contas de usuário do Linux não são apenas independentes por distribuição, elas também são independentes da sua conta de usuário do Windows.

## <a name="resetting-your-linux-password"></a>Redefinindo sua senha do Linux

Se você tiver acesso à sua conta de usuário do Linux e souber sua senha atual, altere-a usando as ferramentas de redefinição de senha do `passwd`Linux dessa distribuição-provavelmente.

Se essa não for uma opção, dependendo da distribuição, talvez seja possível redefinir sua senha redefinindo o usuário padrão.

O WSL oferece uma marca de usuário padrão para identificar qual conta de usuário faz logon automaticamente quando você inicia um WSL.  Como muitas distribuições incluem comandos para definir o usuário padrão como root e também um usuário raiz sem senha definida, alterar o usuário padrão para root é uma ferramenta útil para coisas como a redefinição de senha.

### <a name="for-creators-update-and-earlier"></a>Para a atualização do Creators e anterior
Se você estiver executando a atualização do Windows 10 para criadores ou anterior, poderá alterar o usuário bash padrão executando os seguintes comandos:

1. Altere o usuário padrão para `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Executar `bash.exe` agora fazer logon como `root`:

    ```console
    C:\> bash.exe
    ```

1. Redefina sua senha usando o comando de senha da distribuição e feche o console do Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. No Windows CMD, redefina o usuário padrão de volta para sua conta de usuário Linux normal:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Para a atualização de criadores de outono e posterior
Para ver quais comandos estão disponíveis para uma determinada distribuição, execute `[distro.exe] /?`.
    
Por exemplo, com o Ubuntu instalado:

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

Instruções passo a passo usando o Ubuntu:

1. Abrir CMD
1. Defina o usuário padrão do Linux `root`como:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Inicie sua distribuição do Linux`ubuntu`().  Você fará logon automaticamente como `root`:

1. Redefina sua senha usando `passwd` o comando:

    ```BASH
    $ passwd username
    ```

1. No Windows CMD, redefina o usuário padrão de volta para sua conta de usuário normal do Linux.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Permissões

Há dois conceitos importantes a ter em mente quando se trata de permissões em WSL:

1. O modelo de permissão do Windows governa os direitos de um processo para recursos do Windows
2. O modelo de permissão do Linux controla os direitos de um processo para recursos do Linux

Ao executar o Linux no WSL, o Linux terá as mesmas permissões do Windows que o processo que o inicia. O Linux pode ser iniciado em um dos dois níveis de permissão:

* Normal (não elevado): O Linux é executado com as permissões do usuário conectado
* Elevado/administrador: O Linux é executado com permissões elevadas/administrativas do Windows

> Como processos elevados podem acessar/modificar (e, portanto, danificar) configurações de todo o sistema e dados protegidos em todo o sistema, **Evite** iniciar processos elevados, a menos que você tenha certeza de que eles são aplicativos/ferramentas do Windows ou Linux/ concha!

As permissões acima do Windows são independentes das permissões em uma instância do Linux: Os "privilégios raiz" do Linux só afetam os direitos do usuário no ambiente Linux & FileSystem; Eles não têm nenhum impacto sobre os privilégios do Windows concedidos. Portanto, a execução de um processo do Linux como raiz ( `sudo`por exemplo, via) concede apenas os direitos de administrador do processo no ambiente Linux.

**Exemplo:**     
Uma sessão de bash com privilégios de administrador do `cd /mnt/c/Users/Administrator` Windows pode acessar enquanto uma sessão de bash sem privilégios de administrador veria um erro de "permissão negada".

No Linux, a `sudo cd /mnt/c/Users/Administrator` digitação não concederá acesso ao diretório do administrador, pois as permissões no Windows são gerenciadas pelo Windows.

O modelo de permissão do Linux é importante quando estiver dentro do ambiente Linux em que o usuário tem permissões baseadas no usuário atual do Linux.

**Exemplo:**  
Um usuário no grupo sudo pode ser executado `sudo apt update`.
