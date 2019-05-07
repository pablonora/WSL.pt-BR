---
title: Gerenciar as distribuições do Linux
description: Fazer referência a listagem e configuração de várias distribuições do Linux em execução no subsistema do Windows para Linux.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063494"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Gerenciar e configurar o subsistema do Windows para Linux

> Aplica-se ao Windows 10 Fall Creators Update e versões posteriores.  Consulte nossa atualizada [guia de instalação](./install_guide.md) Experimente os novos recursos de gerenciamento e inicie a execução de várias distribuições do Linux da Windows Store.

## <a name="ways-to-run-wsl"></a>Maneiras de executar o WSL

Há muitas maneiras de executar o Linux com o subsistema Windows para Linux.

1. `[distro]` IE `ubuntu`
1. `wsl.exe` ou `bash.exe`
1. `wsl [command]` ou `bash -c [command]`

Qual método você deve usar depende do que você está fazendo.

### <a name="launch-wsl-by-distribution"></a>Inicie o WSL por distribuição

Executando uma distribuição usando o aplicativo do específica de distribuição dessa distribuição na sua própria janela de console é iniciado.

![Inicie o WSL do menu Iniciar](media/start-launch.png)

É o mesmo que clicar em "Iniciar" na Windows Store.

![Inicie o WSL da Windows Store](media/store-launch.png)

Você também pode executar a distribuição da linha de comando executando `[distribution].exe`.

A desvantagem de usar uma distribuição da linha de comando dessa maneira é que ele será alterado automaticamente seu diretório de trabalho do diretório atual para o diretório de base da distribuição.

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

### <a name="wsl-and-wsl-command"></a>wsl e wsl [comando]

A melhor maneira de executar o WSL da linha de comando está usando `wsl.exe`.

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

Não apenas `wsl` manter o diretório de trabalho atual no lugar, ele permite que você execute um único comando ao longo de comandos do Windows de lado.

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

### <a name="windows-10-version-1903-and-later"></a>Windows 10, versão 1903 e posterior

Você pode usar `wsl.exe` para gerenciar suas distribuições no subsistema Windows para Linux (WSL), incluindo listagem distribuições disponíveis, definindo uma distribuição padrão e distribuições de desinstalação.

Independentemente, cada distribuição Linux gerencia suas próprias configurações. Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.  Por exemplo `ubuntu /?`.

#### <a name="list-distributions"></a>Lista de distribuições

`wsl -l` , `wsl --list`  
Lista de distribuições do Linux disponíveis disponíveis para WSL.  Se uma distribuição estiver listada, ele é instalado e pronto para ser usado.

`wsl --list --all`   
Lista todas as distribuições, incluindo aqueles que não podem ser usados no momento.  Eles podem estar no processo de instalação, desinstalação, ou estiverem em um estado interrompido.  

`wsl --list --running`   
Lista todas as distribuições que estão sendo executados.

#### <a name="set-a-default-distribution"></a>Defina uma distribuição padrão

A distribuição de WSL padrão é o que é executado quando você executar `wsl` em uma linha de comando.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Define a distribuição padrão para `<DistributionName>`.

**Exemplo:**  
`wsl -s Ubuntu` definiria meu distribuição padrão para o Ubuntu.  Agora quando executo `wsl npm init` ele será executado no Ubuntu.  Se eu executar `wsl` ela será aberta uma sessão do Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Cancelar o registro e reinstalar uma distribuição

Ao Linux distribuições podem ser instaladas por meio do Windows, armazenamento, eles não podem ser desinstalados por meio da loja.  WSL Config permite distribuições ser desinstalado/desregistrado.

O cancelamento do registro também permite que distribuições ser reinstalado.

> **Cuidado:** Depois que o registro cancelado, todos os dados, configurações e software associado a essa distribuição serão permanentemente perdidas.  Reinstalar da loja instalará uma cópia limpa da distribuição.

`wsl --unregister <DistributionName>`  
Cancela o registro a distribuição do WSL para que possa ser reinstalado ou limpos.

Por exemplo: `wsl -unregister Ubuntu` removeria Ubuntu das distribuições disponíveis no WSL.  Quando executo `wsl --list` não serão listado.

Para reinstalar, localize a distribuição em que a Windows Store e selecione "Iniciar".

#### <a name="run-as-a-specific-user"></a>Executar como um usuário específico

`wsl -u <Username>`, `wsl --user <Username>`

Execute o WSL como o usuário especificado. Observe que o usuário deve existir dentro distribuição WSL.

#### <a name="run-a-specific-distribution"></a>Executar uma distribuição específica

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

Executar uma distribuição especificada de WSL, pode ser usado para enviar comandos para uma distribuição específica sem precisar alterar o padrão.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versões anteriores ao Windows 10, versão 1903

Configuração de WSL (`wslconfig.exe`) é uma ferramenta de linha de comando para gerenciar as distribuições do Linux em execução no subsistema do Windows para Linux (WSL).  Ele permite listar distribuições disponíveis, defina uma distribuição padrão e desinstalar as distribuições.

Enquanto o WSL configuração é útil para as configurações que abrangem ou coordenam as distribuições, cada distribuição Linux independentemente gerencia suas próprias configurações.  Para ver comandos específicos de distribuição, execute `[distro.exe] /?`.  Por exemplo `ubuntu /?`.

Para ver todas as opções disponíveis para wslconfig, execute:  `wslconfig /?`

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

#### <a name="list-distributions"></a>Lista de distribuições

`wslconfig /list`  
Lista de distribuições do Linux disponíveis disponíveis para WSL.  Se uma distribuição estiver listada, ele é instalado e pronto para ser usado.

`wslconfig /list /all`  
Lista todas as distribuições, incluindo aqueles que não podem ser usados no momento.  Eles podem estar no processo de instalação, desinstalação, ou estiverem em um estado interrompido.  

#### <a name="set-a-default-distribution"></a>Defina uma distribuição padrão

A distribuição de WSL padrão é o que é executado quando você executar `wsl` em uma linha de comando.

`wslconfig /setdefault <DistributionName>`

Define a distribuição padrão para `<DistributionName>`.

**Exemplo:**  
`wslconfig /setdefault Ubuntu` definiria meu distribuição padrão para o Ubuntu.  Agora quando executo `wsl npm init` ele será executado no Ubuntu.  Se eu executar `wsl` ela será aberta uma sessão do Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Cancelar o registro e reinstalar uma distribuição

Ao Linux distribuições podem ser instaladas por meio do Windows, armazenamento, eles não podem ser desinstalados por meio da loja.  WSL Config permite distribuições ser desinstalado/desregistrado.

O cancelamento do registro também permite que distribuições ser reinstalado.

> **Cuidado:** Depois que o registro cancelado, todos os dados, configurações e software associado a essa distribuição serão permanentemente perdidas.  Reinstalar da loja instalará uma cópia limpa da distribuição.

`wslconfig /unregister <DistributionName>`  
Cancela o registro a distribuição do WSL para que possa ser reinstalado ou limpos.

Por exemplo: `wslconfig /unregister Ubuntu` removeria Ubuntu das distribuições disponíveis no WSL.  Quando executo `wslconfig /list` não serão listado.

Para reinstalar, localize a distribuição em que a Windows Store e selecione "Iniciar".

## <a name="set-wsl-launch-settings"></a>Definir configurações de inicialização WSL

> **Disponível no Windows Insider Build 17093 e posterior**

Configure automaticamente algumas funcionalidades em WSL que será aplicada sempre que iniciar o subsistema usando `wsl.conf`. 

Direita agora, isso inclui opções de montagem automática e configuração de rede.

`wsl.conf` está localizado em cada distribuição do Linux em `/etc/wsl.conf`. Se o arquivo não estiver lá, você pode criá-lo. WSL detectará a existência do arquivo e irá ler seu conteúdo. Se o arquivo está ausente ou malformado (ou seja, inadequada marcação formatação), WSL continuará iniciar como normal.

Aqui está um exemplo `wsl.conf` arquivo você pode adicionar em suas distribuições:

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

WSL dá suporte a duas seções: `automount` e `network`.

#### <a name="automount"></a>Montagem automática

Seção: `[automount]`


| key        | value                          | padrão      | Notas                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | verdadeiro         | `true` causas (isto é, de unidades fixas `C:/` ou `D:/`) deve ser montado automaticamente com DrvFs em `/mnt`.  `false` significa que unidades não ser montadas automaticamente, mas você ainda pode montá-los manualmente ou por meio de `fstab`.                                                                                                             |
| mountFsTab | boolean                        | verdadeiro         | `true` define `/etc/fstab` a ser processada no início WSL. /etc/fstab é um arquivo em que você pode declarar outros sistemas de arquivos, como um compartilhamento SMB. Assim, você pode montar esses sistemas de arquivos automaticamente em WSL no início do backup.                                                                                                                |
| Raiz       | String                         | `/mnt/`      | Define o diretório em que unidades fixas serão montadas automaticamente. Por exemplo, se você tiver um diretório no WSL em `/windir/` e você especificar que como a raiz, você esperaria ver suas unidades fixas montadas em `/windir/c`                                                                                              |
| opções    | lista separada por vírgulas de valores | Cadeia de caracteres vazia | Esse valor é acrescentado à cadeia de opções de montagem padrão DrvFs. **Somente as opções de DrvFs específicas podem ser especificadas.** Não há suporte para as opções que a montagem binária normalmente analisaria em um sinalizador. Se você quiser especificar explicitamente essas opções, você deve incluir cada unidade para o qual você deseja fazer isso em /etc/fstab. |

Por padrão, o WSL define o uid e gid como o valor do usuário padrão (distribuição do Ubuntu, o usuário padrão é criado com o uid = 1000, gid = 1000). Se o usuário especificar uma opção gid ou uid explicitamente por meio dessa chave, o valor associado será substituído. Caso contrário, o valor padrão sempre será acrescentado.

**Observação:** Essas opções são aplicadas como as opções de montagem para todas as unidades montadas automaticamente. Para alterar as opções para apenas uma unidade específica, use o /etc/fstab em vez disso.

#### <a name="network"></a>rede

Rótulo de seção: `[network]`

| key | value | padrão | Notas|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` Define o WSL para gerar `/etc/hosts`. O `hosts` arquivo contém um mapa estático do endereço IP correspondente de nomes de host. |
| generateResolvConf | boolean | `true` | `true` Definir WSL para gerar `/etc/resolv.conf`. O `resolv.conf` contém uma lista DNS que são capazes de resolver um determinado nome de host para seu endereço IP. | 

#### <a name="interop"></a>Interoperabilidade

Rótulo de seção: `[interop]`

Essas opções estão disponíveis no Insider Build 17713 e posterior.

| key | value | padrão | Notas|
|:----|:----|:----|:----|
| enabled | boolean | `true` | Configuração de chave nesse determinará se WSL oferece suporte a processos do Windows iniciar. |
| appendWindowsPath | boolean | `true` | Configuração de chave nesse determinará se WSL adicionará os elementos de caminho do Windows para a variável de ambiente $PATH. | 
