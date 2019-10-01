---
title: Conta de usuário e permissões do Linux
description: Referência para contas de usuário e gerenciamento de permissões com o Subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, user accounts
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d8434283e459ae25637fac0c0b1877ca07d9a255
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269708"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Contas de usuário e permissões para o Subsistema Windows para Linux

A criação de seu usuário do Linux é a primeira etapa na configuração de uma nova distribuição do Linux no WSL.  A primeira conta de usuário criada é automaticamente configurada com alguns atributos especiais:

1. É o usuário padrão – ele se conecta automaticamente na inicialização.
1. É o administrador do Linux (um membro do grupo sudo) por padrão.

Cada distribuição do Linux em execução no Subsistema Windows para Linux tem suas próprias contas de usuário e senhas do Linux.  Você precisará configurar uma conta de usuário do Linux sempre que adicionar uma distribuição, reinstalação ou redefinição.  As contas de usuário do Linux não são apenas independentes por distribuição, elas também são independentes da sua conta de usuário do Windows.

## <a name="resetting-your-linux-password"></a>Como redefinir sua senha do Linux

Se você tiver acesso à sua conta de usuário do Linux e souber sua senha atual, altere-a usando as ferramentas de redefinição de senha do Linux dessa distribuição – provavelmente, `passwd`.

Se essa não for uma opção, dependendo da distribuição, talvez seja possível redefinir sua senha redefinindo o usuário padrão.

O WSL oferece uma tag de usuário padrão para identificar qual conta de usuário faz logon automaticamente quando você inicia um WSL.  Como muitas distribuições incluem comandos para definir o usuário padrão como raiz e também um usuário raiz sem senha definida, alterar o usuário padrão para raiz é uma ferramenta útil para ações como uma redefinição de senha.

### <a name="for-creators-update-and-earlier"></a>Para a Atualização para Criadores e anteriores
Se você estiver executando a Atualização do Windows 10 para Criadores ou anterior, poderá alterar o usuário Bash padrão executando os seguintes comandos:

1. Altere o usuário padrão para `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Execute `bash.exe` para agora fazer logon como `root`:

    ```console
    C:\> bash.exe
    ```

1. Redefina sua senha usando o comando de senha da distribuição e feche o console do Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. No CMD do Windows, redefina o usuário padrão de volta para sua conta de usuário Linux normal:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Para o Fall Creators Update e posteriores
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

1. Abra o CMD
1. Defina o usuário padrão do Linux como `root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Inicie sua distribuição do Linux (`ubuntu`).  Você fará logon automaticamente como `root`:

1. Redefina sua senha usando o comando `passwd`:

    ```BASH
    $ passwd username
    ```

1. No CMD do Windows, redefina o usuário padrão de volta para sua conta de usuário Linux normal.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Permissões

Há dois conceitos importantes a ter em mente quando se trata de permissões no WSL:

1. O modelo de permissão do Windows rege os direitos de um processo para recursos do Windows
2. O modelo de permissão do Linux rege os direitos de um processo para recursos do Linux

Ao executar o Linux no WSL, o Linux terá as mesmas permissões do Windows que o processo que o inicia. O Linux pode ser iniciado em um dos dois níveis de permissão:

* Normal (não elevado): O Linux é executado com as permissões do usuário conectado
* Elevado/administrador: O Linux é executado com permissões elevadas/de administrador do Windows

> Como processos elevados podem acessar/modificar (e, portanto, danificar) as configurações de todo o sistema e dados protegidos, **EVITE** iniciar processos elevados a menos que seja absolutamente necessário – sejam eles aplicativos/ferramentas/shells do Windows ou Linux!

As permissões do Windows acima são independentes das permissões em uma instância do Linux: Os "privilégios raiz" do Linux só afetam os direitos do usuário no ambiente do Linux e no sistema de arquivos. Eles não têm nenhum impacto sobre os privilégios do Windows concedidos. Portanto, a execução de um processo do Linux como raiz (por exemplo, via `sudo`) concede apenas os direitos de administrador do processo no ambiente do Linux.

**Exemplo:**     
Uma sessão do Bash com privilégios de administrador do Windows pode acessar `cd /mnt/c/Users/Administrator` enquanto uma sessão do Bash sem privilégios de administrador veria um erro de "Permissão negada".

No Linux, digitar `sudo cd /mnt/c/Users/Administrator` não permitirá acesso ao diretório do administrador, pois as permissões no Windows são gerenciadas pelo Windows.

O modelo de permissão do Linux é importante quando estiver dentro do ambiente Linux em que o usuário tem permissões baseadas no usuário atual do Linux.

**Exemplo:**  
Um usuário no grupo sudo pode executar `sudo apt update`.
