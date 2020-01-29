---
title: Criar e atualizar contas de usuário para distribuições do WSL
description: Referência para contas de usuário e gerenciamento de permissões com o Subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, user accounts
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 85bd8f05d041181c2cfb16f6fb55aaeea15b332c
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520575"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a>Criar e atualizar contas de usuário para distribuições do WSL

Depois que você habilitar o WSL e instalar uma distribuição do Linux da Microsoft Store, a primeira etapa que será solicitada ao abrir sua distribuição do Linux recém-instalada será a criação de uma conta, incluindo um **nome de usuário** e **senha**.

- O **nome de usuário** e a **senha** são específicos da sua distribuição do Linux e não têm nenhuma influência sobre seu nome de usuário do Windows.

- Depois de criar o **nome de usuário** e a **senha**, a conta será o usuário padrão para a distribuição e entrará automaticamente na inicialização.

- Essa conta será considerada o administrador do Linux, com a capacidade de executar comandos administrativos `sudo` (Super User Do).

- Cada distribuição do Linux em execução no Subsistema Windows para Linux tem suas próprias contas de usuário e senhas do Linux.  Você precisará configurar uma conta de usuário do Linux sempre que adicionar uma distribuição, reinstalação ou redefinição.

## <a name="reset-your-linux-password"></a>Redefinir sua senha do Linux

Para alterar sua senha, abra a distribuição do Linux (Ubuntu, por exemplo) e insira o comando: `passwd`

Você será solicitado a inserir a senha atual, inserir a nova senha e, em seguida, confirmar a nova senha.

### <a name="forgot-your-password"></a>Esqueceu sua senha

Se você esqueceu a senha da sua distribuição do Linux:

1. Abra o PowerShell e insira a raiz da distribuição do WSL padrão usando o comando: `wsl -u root`

Se você precisa atualizar a senha que foi esquecida em uma distribuição que não seja a padrão, use o comando: `wsl -d Debian -u root`, substituindo `Debian` pelo nome da sua distribuição de destino.

2. Depois que a distribuição do WSL tiver sido aberta no nível raiz dentro do PowerShell, você poderá usar esse comando para atualizar a senha: `passwd`

3. Você será solicitado a inserir uma nova senha do UNIX e, em seguida, confirmar essa senha. Depois da informação de que a senha foi atualizada com êxito, feche o WSL dentro do PowerShell usando o comando: `exit`

> [!NOTE]
> Se você está executando uma versão anterior do sistema operacional Windows, como a 1703 (Atualização do Windows 10 para Criadores) ou a 1709 (Windows 10 Fall Creators Update), consulte a [versão arquivada deste documento de atualização de conta de usuário](./user-support-archived.md).
