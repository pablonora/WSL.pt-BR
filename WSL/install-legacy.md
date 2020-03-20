---
title: Instalar ou remover na atualização de aniversário do Windows 10 ou na atualização de criadores
description: Instruções de instalação e desinstalação para a atualização da atualização de aniversário do Windows 10 ou do Creators
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10, herdado, beta, instalação, remoção, desinstalação, desinstalação, exclusão, preterido
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 416bed3ed3a0470da2eb5e6beb75e73eb6836200
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269767"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>Guia para instalar ou desinstalar o subsistema do Windows para Linux em atualização de aniversário do Windows 10 e o criador de atualizações 

Se você estiver executando a atualização do Windows 10 para criadores ou posterior, [siga as instruções de instalação do Windows 10](install-win10.md).

<strong><em><span style="color: #f28014">As instruções a seguir são para usuários que executam a atualização de aniversário do Windows 10 ou a atualização do Windows 10 para criadores</span></em></strong>

Antes da atualização do Windows 10 outono Creators (versão 1709), o WSL foi lançado como um recurso beta e instalou uma única instância do Ubuntu quando o "bash no Ubuntu no Windows" (ou bash. exe) foi executado pela primeira vez.

> Embora você possa usar o WSL em versões anteriores do Windows 10, essa versão beta "Legacy distribuição" agora é considerada obsoleta. É altamente recomendável que você execute a versão mais recente do Windows 10 disponível. Cada nova versão do Windows 10 inclui vários centenas de correções e melhorias no WSL sozinho, permitindo que mais ferramentas e aplicativos do Linux sejam executados corretamente no WSL.

Se você não puder atualizar para a atualização de criadores de outono ou posterior, siga as etapas abaixo para habilitar e usar o WSL:

1. Ativar o modo de desenvolvedor para executar o WSL na atualização de aniversário do Windows 10 ou na atualização de criadores, você deve habilitar o modo de desenvolvedor:

    Abrir **configurações** ->  -> de **atualização e segurança** **para desenvolvedores**

    Selecione o botão de opção modo de desenvolvedor  
    ![Habilitar o modo de desenvolvedor](media/updateAndSecurity.png)

    > A necessidade de habilitar o modo de desenvolvedor foi [removida na atualização dos criadores de outono do Windows 10](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. Abra um prompt de comando.  Digite `bash` e pressione Enter

    Na primeira vez que você executar o bash no Ubuntu no Windows, será solicitado que você aceite a licença do Canonical. Depois de aceito, o WSL baixará e instalará a instância do Ubuntu em seu computador e um atalho "bash no Ubuntu no Windows" será adicionado ao menu iniciar.

    ![Avisar para instalar o Ubuntu](media/bashShellInstall.png)

    Na primeira vez que você executar o bash no Ubuntu no Windows, será solicitado que você crie um nome de usuário e senha UNIX. Siga as [instruções da nova instância do distribuição](initialize-distro.md) para concluir a instalação

1. Inicie um novo shell do Ubuntu por meio de:
    * Executando `bash` de um prompt de comando
    * Clicando no atalho "bash no Ubuntu no Windows" do menu iniciar

    
## <a name="uninstallingremoving-the-legacy-distro"></a>Desinstalando/removendo o distribuição herdado
Se você atualizar para a atualização dos criadores de outono do Windows 10 de uma versão anterior do Windows 10 na qual você instalou o WSL, seu distribuição existente permanecerá intacto. No entanto, é altamente recomendável que você instale uma nova loja entregue distribuição ASAP e migre todos os arquivos, dados, etc. necessários do seu distribuição herdado para o novo distribuição.

Para remover o distribuição herdado de seu computador, execute o seguinte em uma linha de comando ou instância do PowerShell:

```console
wsl --unregister Legacy
```

Se você não estiver usando o Windows versão 1903 ou superior, talvez seja necessário executar `wslconfig /u Legacy` ou `lxrun /uninstall /full` em vez disso. 

### <a name="manually-deleting-the-legacy-distro"></a>Excluindo manualmente o distribuição herdado
Se desejar, você pode excluir manualmente sua instância herdada. Isso pode ser necessário se você encontrar problemas ao desinstalar o distribuição herdado usando `lxrun.exe`ou estiver executando a atualização do Windows 10 Spring 2018 (ou posterior) que não são fornecidos com o `lxrun.exe`.

Para excluir de forma forçada seu distribuição WSL herdado, exclua a pasta `%localappdata%\lxss\` (e todo o subconteúdo) usando o Windows ' Explorador de arquivos ou a linha de comando:

Uso do PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

Usando o cmd:
```console
DEL /S %localappdata%\lxss\
```
