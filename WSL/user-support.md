---
title: Permissões e a conta de usuário do Linux
description: Referência para contas de usuário e gerenciamento de permissões com o subsistema do Windows para Linux.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, contas de usuário
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063594"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Contas de usuário e as permissões de subsistema Windows para Linux

Criação de seu usuário do Linux é a primeira etapa na configuração de uma nova distribuição do Linux no WSL.  A primeira conta de usuário criada é configurada automaticamente com alguns atributos especiais:

1. É o usuário padrão, ele entrar automaticamente na inicialização.
1. É administrador do Linux (um membro do grupo sudo) por padrão.

Cada distribuição do Linux em execução no subsistema do Windows para Linux tem seu próprio Linux contas de usuário e senhas.  Você precisará configurar uma conta de usuário do Linux sempre que você adicionar uma distribuição, reinstale ou redefinir.  Contas de usuário do Linux não são apenas independentes por distribuição, eles também são independentes da sua conta de usuário do Windows.

## <a name="resetting-your-linux-password"></a>Redefinir sua senha do Linux

Se você tiver acesso à sua conta de usuário do Linux e sabe sua senha atual, alterá-lo usando o Linux de redefinição de senha ferramentas dessa distribuição – provavelmente `passwd`.

Se isso for não é uma opção, dependendo da distribuição, você poderá redefinir sua senha, redefinindo o usuário padrão.

WSL oferece logs de uma marca de usuário padrão para identificar qual conta de usuário automaticamente no, quando você inicia um WSL.  Como várias distribuições incluem comandos para definir o usuário padrão como raiz e também um usuário raiz com nenhuma senha definida, alterar o usuário padrão para a raiz é uma ferramenta útil para coisas como a redefinição de senha.

### <a name="for-creators-update-and-earlier"></a>Para a atualização para criadores e versões anteriores
Se você estiver executando o Windows 10 Creators update ou versões anteriores, você pode alterar o usuário de Bash padrão executando os comandos a seguir:

1. Alterar o usuário padrão para `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Execute `bash.exe` fazer logon agora como `root`:

    ```console
    C:\> bash.exe
    ```

1. Redefinir sua senha usando o comando de senha de distribuição e feche o Console do Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. No Windows CMD, redefina seu usuário padrão para sua conta de usuário normal do Linux:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Para o Fall Creators Update e posterior
Para ver quais comandos estão disponíveis para uma distribuição específica, execute `[distro.exe] /?`.
    
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

Etapa de instruções passo a passo usando o Ubuntu:

1. Abra o CMD
1. Defina o usuário padrão do Linux como `root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Inicie sua distribuição do Linux (`ubuntu`).  Você será automaticamente fazer logon como `root`:

1. Redefinir sua senha usando o `passwd` comando:

    ```BASH
    $ passwd username
    ```

1. No Windows CMD, redefina seu usuário padrão para sua conta de usuário normal do Linux.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Permissões

Há dois conceitos importantes para ter em mente quando se trata de permissões no WSL:

1. O modelo de permissão do Windows controla os direitos de um processo para recursos do Windows
2. O modelo de permissão de Linux controla os direitos de um processo de recursos do Linux

Ao executar o Linux em WSL, Linux terão as mesmas permissões do Windows que o processo que inicia a ele. Linux pode ser iniciado em um dos dois níveis de permissão:

* Normal (não elevada): Executa o Linux com as permissões do usuário conectado
* Administrador/privilégios elevados: Executa o Linux com as permissões do administrador com privilégios elevados/Windows

> Porque que elevados processos podem alterar/danos dados e configurações do sistema e podem acesso/Modificar protegidos de arquivos e pastas, **Evite** iniciando elevados processos, a menos que você tenha que absolutamente - se eles estão Windows ou Linux aplicativos/tools/shells!

As permissões do Windows acima são independentes das permissões dentro de uma instância do Linux: Linux "privilégios de raiz" afetam apenas os direitos do usuário dentro do ambiente Linux & sistema de arquivos; eles não têm impacto sobre os privilégios do Windows concedidos. Assim, executar um processo de Linux como raiz (por exemplo, via `sudo`) apenas concede que processam os direitos de administrador no ambiente do Linux.

**Exemplo:**    
Uma sessão de Bash com privilégios de administrador do Windows pode acessar `cd /mnt/c/Users/Administrator` enquanto uma sessão Bash sem privilégios de administrador vê um erro "Permissão negada".

No Linux, digitando `sudo cd /mnt/c/Users/Administrator` não concederá acesso ao diretório do administrador, pois as permissões no Windows são gerenciadas pelo Windows.

O modelo de permissão do Linux é importante quando se está dentro do ambiente do Linux no qual o usuário tem permissões com base no usuário Linux atual.

**Exemplo:**  
Pode ser executado por um usuário no grupo sudo `sudo apt update`.
