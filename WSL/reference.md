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
ms.openlocfilehash: 018b02b43e859476f7ee38f54df8efa0ca0e652b
ms.sourcegitcommit: 62c49d435a91f2e390c3c495f3e09e62b5ada13c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2019
ms.locfileid: "69578839"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Referência de comando para o subsistema do Windows para Linux

A melhor maneira de interagir com o subsistema do Windows para Linux é usar o `wsl.exe` comando. 


## `wsl.exe`

Abaixo está uma lista que contém todas as opções `wsl.exe` ao usar o da versão 1903 do Windows.

Usando`wsl [Argument] [Options...] [CommandLine]`

### <a name="arguments-for-running-linux-binaries"></a>Argumentos para executar binários do Linux

* **Sem argumentos**

  Se nenhuma linha de comando for fornecida, o WSL. exe iniciará o shell padrão.

* **--Exec,-e \<linha de comando >**
  
  Execute o comando especificado sem usar o Shell do Linux padrão.

* **--**
  
  Passe a linha de comando restante como está.

Os comandos acima também aceitam as seguintes opções:

* **--Distribution,-d \<distribuição >**

  Execute a distribuição especificada.

* **--User,-u \<nome de usuário >**

  Executar como o usuário especificado.

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a>Argumentos para gerenciar o subsistema do Windows para Linux

* **--exportar \<distribuição > \<nome do arquivo >**
  
  Exporta a distribuição para um arquivo tar. O nome de arquivo pode ser-para saída padrão.

* **--Import \<distribuição > \<InstallLocation > \<filename >**
  
  Importa o arquivo tar especificado como uma nova distribuição. O nome de arquivo pode ser-para entrada padrão.

* **--List,-l [opções]**
  
  Lista distribuições.

  Opções:
  * **--todos**
      
    Listar todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.

  * **--executando**
      
    Lista somente as distribuições que estão em execução no momento.

* **--Set-Default,-s \<distribuição >**
  
  Define a distribuição como o padrão.

* **--Terminate,-t \<distribuição >**
  
  Encerra a distribuição especificada.

* **--cancelar registro \<de distribuição >**
  
  Cancela o registro da distribuição.
   
* **--ajuda** Exibir informações de uso.

## <a name="additional-commands"></a>Comandos adicionais

Também há comandos históricos para interagir com o subsistema do Windows para Linux. Sua funcionalidade é englobada no `wsl.exe`, mas ainda estão disponíveis para uso. 

### `wslconfig.exe`

Esse comando permite que você configure a distribuição do WSL. Abaixo está uma lista de suas opções.

Usando`wslconfig [Argument] [Options...]`

#### <a name="arguments"></a>Argumentos
* **/l,/List [opções]**
  
  Lista as distribuições registradas.
  
  Opções:
    * **/All**
    
      Opcionalmente, liste todas as distribuições, incluindo distribuições que estão sendo instaladas ou desinstaladas no momento.

    * **/running**
      
      Lista somente as distribuições que estão em execução no momento.

* **/s,/SetDefault \<distribuição >**
  
  Define a distribuição como o padrão.

* **/t,/Terminate \<distribuição >**
  
  Encerra a distribuição.

* **/u,/Unregister \<distribuição >**
  
  Cancela o registro da distribuição.
   
* **> \</upgrade distribuição**
  
  Atualiza a distribuição para o formato do sistema de arquivos WslFs.

### `bash.exe`

Esse comando é usado para iniciar um shell bash. Abaixo estão as opções que você pode usar com este comando.

Usando`bash [Options...]`

* **Nenhuma opção fornecida**
  
  Inicia o shell bash no diretório atual. Se o shell bash não for instalado automaticamente`lxrun /install`

* **~**
  
  `bash ~`inicia o shell bash no diretório base do usuário.  Semelhante à execução `cd ~`.

* **-c "\<> de comando"**
  
  Executa o comando, imprime a saída e sai de volta para o prompt de comando do Windows.
    
  Exemplo: `bash -c "ls"`.

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
