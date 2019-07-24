---
title: Gerenciar distribuições do Linux
description: Listagem de referência e configuração de várias distribuições do Linux em execução no subsistema do Windows para Linux.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, WSL. conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: 0c9f9315b17d5156aa111e7619ee25534653b27e
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499273"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Gerenciar e configurar o subsistema do Windows para Linux

> Aplica-se à atualização dos criadores de outono do Windows 10 e posterior.  Consulte nosso [Guia de instalação](./install_guide.md) atualizado para experimentar novos recursos de gerenciamento e iniciar a execução de várias distribuições do Linux na Microsoft Store.

## <a name="ways-to-run-wsl"></a>Maneiras de executar o WSL

Há várias maneiras de executar o Linux com o subsistema do Windows para Linux.

1. `[distro]`, por exemplo`ubuntu`
1. `wsl.exe` ou `bash.exe`
1. `wsl [command]` ou `bash -c [command]`

Qual método deve ser usado depende do que você está fazendo.

### <a name="launch-wsl-by-distribution"></a>Iniciar o WSL por distribuição

A execução de uma distribuição usando o aplicativo específico do distribuição inicia essa distribuição na própria janela do console.

![Iniciar o WSL no menu iniciar](media/start-launch.png)

É o mesmo que clicar em "Launch" na Microsoft Store.

![Inicie o WSL da Microsoft Store](media/store-launch.png)

Você também pode executar a distribuição na linha de comando executando `[distribution].exe`.

A desvantagem de executar uma distribuição da linha de comando dessa forma é que ela alterará automaticamente seu diretório de trabalho do diretório atual para o diretório base da distribuição.

**Exemplo:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a>WSL e WSL [comando]

A melhor maneira de executar o WSL na linha de comando é `wsl.exe`usar o.

**Exemplo:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

Não apenas `wsl` mantém o diretório de trabalho atual em vigor, ele permite que você execute um único comando ao longo dos comandos do Windows.

**Exemplo:**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

**Exemplo:**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a>Gerenciando várias distribuições do Linux

### <a name="windows-10-version-1903-and-later"></a>Windows 10 versão 1903 e posterior

Você pode usar `wsl.exe` o para gerenciar suas distribuições no subsistema do Windows para Linux (WSL), incluindo a listagem de distribuições disponíveis, a definição de uma distribuição padrão e a desinstalação de distribuições.

Cada distribuição do Linux gerencia de forma independente suas próprias configurações. Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.  Por exemplo `ubuntu /?`.

#### <a name="list-distributions"></a>Listar distribuições

`wsl -l`,`wsl --list`  
Lista as distribuições disponíveis do Linux disponíveis para WSL.  Se uma distribuição estiver listada, ela será instalada e estará pronta para uso.

`wsl --list --all`   
Lista todas as distribuições, incluindo aquelas que não são utilizáveis no momento.  Eles podem estar no processo de instalação, desinstalação ou em um estado desfeito.  

`wsl --list --running`   
Lista todas as distribuições que estão em execução no momento.

#### <a name="set-a-default-distribution"></a>Definir uma distribuição padrão

A distribuição WSL padrão é aquela que é executada quando você executa `wsl` em uma linha de comando.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Define a distribuição padrão como `<DistributionName>`.

**Exemplo:**  
`wsl -s Ubuntu`definirei minha distribuição padrão como Ubuntu.  Agora, quando eu `wsl npm init` o executo, ele será executado no Ubuntu.  Se eu executá `wsl` -lo, abrirá uma sessão do Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Cancelar o registro e reinstalar uma distribuição

Embora as distribuições do Linux possam ser instaladas por meio da Microsoft Store, elas não podem ser desinstaladas por meio da loja.  WSL config permite que as distribuições sejam canceladas/desinstaladas.

O cancelamento do registro também permite que as distribuições sejam reinstaladas.

> **Cuidado:** Após o registro, todos os dados, as configurações e os softwares associados a essa distribuição serão permanentemente perdidos.  A reinstalação do repositório instalará uma cópia limpa da distribuição.

`wsl --unregister <DistributionName>`  
Cancela o registro da distribuição do WSL para que possa ser reinstalado ou limpo.

Por exemplo: `wsl --unregister Ubuntu` removeria o Ubuntu das distribuições disponíveis no WSL.  Quando eu executo `wsl --list` , ele não será listado.

Para reinstalar o, localize a distribuição na Microsoft Store e selecione "Iniciar".

#### <a name="run-as-a-specific-user"></a>Executar como um usuário específico

`wsl -u <Username>`, `wsl --user <Username>`

Execute WSL como o usuário especificado. Observe que o usuário deve existir dentro da distribuição WSL.

#### <a name="run-a-specific-distribution"></a>Executar uma distribuição específica

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

Executar uma distribuição especificada de WSL, pode ser usado para enviar comandos para uma distribuição específica sem precisar alterar o padrão.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versões anteriores ao Windows 10 versão 1903

WSL config (`wslconfig.exe`) é uma ferramenta de linha de comando para gerenciar distribuições do Linux em execução no subsistema do Windows para Linux (WSL).  Ele permite que você liste as distribuições disponíveis, defina uma distribuição padrão e desinstale as distribuições.

Embora a configuração do WSL seja útil para configurações que abrangem ou coordenam distribuições, cada distribuição do Linux gerencia de forma independente suas próprias configurações.  Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.  Por exemplo `ubuntu /?`.

Para ver todas as opções disponíveis para wslconfig, execute:`wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a>Listar distribuições

`wslconfig /list`  
Lista as distribuições disponíveis do Linux disponíveis para WSL.  Se uma distribuição estiver listada, ela será instalada e estará pronta para uso.

`wslconfig /list /all`  
Lista todas as distribuições, incluindo aquelas que não são utilizáveis no momento.  Eles podem estar no processo de instalação, desinstalação ou em um estado desfeito.  

#### <a name="set-a-default-distribution"></a>Definir uma distribuição padrão

A distribuição WSL padrão é aquela que é executada quando você executa `wsl` em uma linha de comando.

`wslconfig /setdefault <DistributionName>`

Define a distribuição padrão como `<DistributionName>`.

**Exemplo:**  
`wslconfig /setdefault Ubuntu`definirei minha distribuição padrão como Ubuntu.  Agora, quando eu `wsl npm init` o executo, ele será executado no Ubuntu.  Se eu executá `wsl` -lo, abrirá uma sessão do Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Cancelar o registro e reinstalar uma distribuição

Embora as distribuições do Linux possam ser instaladas por meio da Microsoft Store, elas não podem ser desinstaladas por meio da loja.  WSL config permite que as distribuições sejam canceladas/desinstaladas.

O cancelamento do registro também permite que as distribuições sejam reinstaladas.

> **Cuidado:** Após o registro, todos os dados, as configurações e os softwares associados a essa distribuição serão permanentemente perdidos.  A reinstalação do repositório instalará uma cópia limpa da distribuição.

`wslconfig /unregister <DistributionName>`  
Cancela o registro da distribuição do WSL para que possa ser reinstalado ou limpo.

Por exemplo: `wslconfig /unregister Ubuntu` removeria o Ubuntu das distribuições disponíveis no WSL.  Quando eu executo `wslconfig /list` , ele não será listado.

Para reinstalar o, localize a distribuição na Microsoft Store e selecione "Iniciar".

## <a name="set-wsl-launch-settings"></a>Definir configurações de inicialização WSL

> **Disponível no Windows Insider Build 17093 e posterior**

Configure automaticamente determinadas funcionalidades no WSL que serão aplicadas toda vez que você iniciar o subsistema usando `wsl.conf`. 

No momento, isso inclui opções de montagem automática e configuração de rede.

`wsl.conf`está localizado em cada distribuição do Linux `/etc/wsl.conf`no. Se o arquivo não estiver lá, você mesmo poderá criá-lo. O WSL detectará a existência do arquivo e lerá seu conteúdo. Se o arquivo estiver ausente ou malformado (ou seja, formatação de marcação inadequada), o WSL continuará a ser iniciado normalmente.

Aqui está um arquivo `wsl.conf` de exemplo que você pode adicionar ao seu distribuições:

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>Opções de configuração

Para manter as convenções. ini, as chaves são declaradas em uma seção. 

O WSL dá suporte a `automount` duas `network`seções: e.

#### <a name="automount"></a>montagem automática

Section`[automount]`


| key        | value                          | default      | registra                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true`causa unidades fixas (ou seja, `C:/`ou `D:/`) a ser montado automaticamente com DrvFs em `/mnt`.  `false`significa que as unidades não serão montadas automaticamente, mas você ainda poderá montá- `fstab`las manualmente ou por meio do.                                                                                                             |
| mountFsTab | boolean                        | true         | `true`conjuntos `/etc/fstab` a serem processados no início do WSL. /etc/fstab é um arquivo no qual você pode declarar outros sistemas de arquivos, como um compartilhamento SMB. Assim, você pode montar esses sistemas de fileautomaticamente no WSL na inicialização.                                                                                                                |
| básica       | String                         | `/mnt/`      | Define o diretório em que as unidades fixas serão montadas automaticamente. Por exemplo, se você tiver um diretório em WSL em `/windir/` e especificar que, como a raiz, esperaria ver suas unidades fixas montadas em`/windir/c`                                                                                              |
| opções    | lista de valores separados por vírgulas | Cadeia de caracteres vazia | Esse valor é acrescentado à cadeia de opções padrão de montagem DrvFs. **Somente opções específicas de DrvFs podem ser especificadas.** As opções que o binário de montagem normalmente analisam em um sinalizador não são suportadas. Se você quiser especificar explicitamente essas opções, deverá incluir todas as unidades para as quais deseja fazer isso no/etc/fstab. |

Por padrão, WSL define o UID e o GID como o valor do usuário padrão (no Ubuntu distribuição, o usuário padrão é criado com UID = 1000, GID = 1000). Se o usuário especificar uma opção GID ou uid explicitamente por meio dessa chave, o valor associado será substituído. Caso contrário, o valor padrão será sempre acrescentado.

**Observação:** Essas opções são aplicadas como opções de montagem para todas as unidades montadas automaticamente. Para alterar as opções somente para uma unidade específica, use/etc/fstab em vez disso.

#### <a name="network"></a>rede

Rótulo da seção:`[network]`

| key | value | default | registra|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true`define WSL para gerar `/etc/hosts`. O `hosts` arquivo contém um mapa estático do endereço IP correspondente de nomes de host. |
| generateResolvConf | boolean | `true` | `true`Defina WSL para gerar `/etc/resolv.conf`. O `resolv.conf` contém uma lista DNS que é capaz de resolver um determinado nome de host para seu endereço IP. | 

#### <a name="interop"></a>interoperabilidade

Rótulo da seção:`[interop]`

Essas opções estão disponíveis no Insider Build 17713 e posterior.

| key | value | default | registra|
|:----|:----|:----|:----|
| enabled | boolean | `true` | Definir essa chave determinará se o WSL dará suporte à inicialização de processos do Windows. |
| appendWindowsPath | boolean | `true` | Definir essa chave determinará se WSL adicionará elementos de caminho do Windows à variável de ambiente $PATH. | 
