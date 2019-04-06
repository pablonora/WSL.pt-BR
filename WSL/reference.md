---
title: Subsistema do Windows para referência de comando do Linux
description: Lista de comandos que gerenciam o subsistema Windows para Linux
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063574"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Referência de comandos do subsistema do Windows para Linux

> `lxrun.exe` é preterido a partir do Windows 10 1803 e posterior.

O comando `lxrun.exe` pode ser usado para interagir com o [subsistema Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) diretamente.  Esses comandos são instalados no `\Windows\System32` diretório e pode ser executado dentro de um prompt de comando do Windows ou no PowerShell.

* `lxrun.exe` é usado para gerenciar o WSL.  Esse comando pode ser usado para instalar ou desinstalar a imagem do Ubuntu.


| Comando                     | Descrição                     |
|:----------------------------|:---------------------------|
| `bash`                      | Inicia o shell do Bash no diretório atual.  Se o shell Bash não é instalado automaticamente será executado `lxrun /install` |
| `bash ~`                    | O shell bash é iniciado no diretório base do Ubuntu do usuário.  Semelhante à execução de cd ~            |
| `bash -c "<command>"`       | Executa o comando, imprime a saída e sai de volta para o prompt de comando do Windows. <br/> <br/> Exemplo: **bash -c "ls"** |

<p>

| Comando                     | Descrição                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | O comando lxrun é usado para gerenciar a instância WSL. |
| `lxrun /install`            | Inicia o download e o processo de instalação. <br/> **/y** podem ser adicionados para ignorar todos os prompts.  O prompt de confirmação é aceito automaticamente e o usuário padrão é definido como raiz.          |
| `lxrun /uninstall`          | Desinstala e exclui a imagem do Ubuntu.  Por padrão isso não remove o diretório base do Ubuntu do usuário. <br/> **/y** podem ser adicionados ao aceitar automaticamente o prompt de confirmação <br/>**completas** desinstala e exclui o diretório base do Ubuntu do usuário         |
| `lxrun /setdefaultuser <userName>`     | Define o padrão do Bash no Ubuntu usuário. Solicitará uma senha se o usuário especificado não existe.  Para obter mais informações, visite: https://aka.ms/wslusers. <br/> **/y** promping ignora a senha.  O usuário será criado sem uma senha.|
| `lxrun /update`            | Atualiza o índice do pacote do subsistema          |
