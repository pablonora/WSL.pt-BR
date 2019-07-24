---
title: Referência de comando do subsistema do Windows para Linux
description: Lista de comandos que gerenciam o subsistema do Windows para Linux
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307651"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Referência de comando para o subsistema do Windows para Linux

A melhor maneira de interagir com o subsistema do Windows para Linux é usar o `wsl.exe` comando. 

## `wsl.exe` 

Abaixo está uma lista que contém todas as opções `wsl.exe` ao usar o da versão 1903 do Windows.

* Argumentos para executar binários do Linux:

    * Se nenhuma linha de comando for fornecida, o WSL. exe iniciará o shell padrão.

    * --Exec,-e<CommandLine>
        * Execute o comando especificado sem usar o Shell do Linux padrão.

    * --
        * Passe a linha de comando restante como está.

* Opções:
    * --Distribution,-d<Distro>
        * Execute a distribuição especificada.

    * --usuário,-u<UserName>
        * Executar como o usuário especificado.

* Argumentos para gerenciar o subsistema do Windows para Linux:

    * --exportar <Distro><FileName>
        * Exporta a distribuição para um arquivo tar.
        O nome de arquivo pode ser-para saída padrão.

    * --Import <Distro> <InstallLocation>[opções <FileName> ]
        * Importa o arquivo tar especificado como uma nova distribuição.
        O nome de arquivo pode ser-para entrada padrão.

        * Opções:
            * --Version <Version> especifica a versão a ser usada para a nova distribuição.

    * --List,-l [opções]
        * Lista distribuições.

        * Opções:
            * --todos
                * Listar todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.

            * --executando
                * Lista somente as distribuições que estão em execução no momento.

    * --Set-Default,-s<Distro>
        * Define a distribuição como o padrão.

    * --Set-padrão-versão<Version>
        * Altera a versão de instalação padrão para novas distribuições.

    * --Set-Version <Distro><Version>
        * Altera a versão da distribuição especificada.

    * --Terminate,-t<Distro>
        * Encerra a distribuição especificada.

    * --cancelar registro<Distro>
        * Cancela o registro da distribuição.

    * --help
        * Exibir informações de uso.

## <a name="additional-commands"></a>Comandos adicionais

Também há comandos históricos para interagir com o subsistema do Windows para Linux. Sua funcionalidade é englobada no `wsl.exe`, mas ainda estão disponíveis para uso. 

### `wslconfig.exe`

Esse comando permite que você configure a distribuição do WSL. Abaixo está uma lista de suas opções.

* /l,/List [opção]
    * Lista as distribuições registradas.
        * /All – opcionalmente, liste todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.

        * /Running-lista somente as distribuições que estão em execução no momento.

* /s,/SetDefault<DistributionName>
    * Define a distribuição como o padrão.

* /t,/Terminate<DistributionName>
    * Encerra a distribuição.

* /u,/Unregister<DistributionName>
    * Cancela o registro da distribuição.

### `bash.exe`

Esse comando é usado para iniciar um shell bash. Abaixo estão as opções que você pode usar com este comando.

* Nenhuma opção fornecida
    * Inicia o shell bash no diretório atual. Se o shell bash não for instalado automaticamente`lxrun /install`

* bash ~
    * Inicia o shell bash no diretório base do usuário.  Semelhante à execução `cd ~`.

* bash-c "&lt;comando&gt;"
    * Executa o comando, imprime a saída e sai de volta para o prompt de comando do Windows. <br/> <br/> Exemplo`bash -c "ls"`

## <a name="deprecated-commands"></a>Comandos preteridos

O `lxrun.exe` foi o primeiro comando usado para instalar e gerenciar o subsistema do Windows para Linux. Ele foi preterido a partir do Windows 10 1803 e posterior.

O comando `lxrun.exe` pode ser usado para interagir diretamente com o subsistema do [Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .  Esses comandos são instalados no `\Windows\System32` diretório e podem ser executados em um prompt de comando do Windows ou no PowerShell.

| Comando                     | Descrição                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | O comando lxrun é usado para gerenciar a instância WSL. |
| `lxrun /install`            | Inicia o processo de download e instalação. <br/> **/y** pode ser adicionado para ignorar todos os prompts.  O prompt de confirmação é automaticamente aceito e o usuário padrão é definido como raiz.          |
| `lxrun /uninstall`          | Desinstala e exclui a imagem do Ubuntu.  Por padrão, isso não remove o diretório inicial do Ubuntu do usuário. <br/> **/y** pode ser adicionado para aceitar automaticamente o prompt de confirmação <br/>**/Full** desinstala e exclui o diretório inicial do Ubuntu do usuário         |
| `lxrun /setdefaultuser <userName>`     | Define o bash padrão no usuário do Ubuntu. Solicitará uma senha se o usuário especificado não existir.  Para obter mais informações, https://aka.ms/wslusers visite:. <br/> **/y** Ignora promping para a senha.  O usuário será criado sem uma senha.|
| `lxrun /update`            | Atualiza o índice do pacote do subsistema          |
