---
title: Instalar ou remover em atualização de aniversário do Windows 10 ou atualização para criadores
description: Instruções de instalação e desinstalação para o herdado, a distribuição beta em atualização de aniversário do Windows 10 ou atualização para criadores
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, herdado, beta, instalar, remover, desinstalar, desinstalar, delete, preterido
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b31bb3a542b8481c723df42292e20e364680722d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063584"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>Guia para instalar ou desinstalar o subsistema do Windows para Linux em atualização de aniversário do Windows 10 e atualização para criadores 

Se você estiver executando o Windows 10 Creators Update ou posterior, por favor [siga as instruções de instalação do Windows 10](install-win10.md).

<strong><em><span style="color: #f28014">As instruções a seguir são para usuários que executam a atualização de aniversário do Windows 10 ou Windows 10 Creators Update</span></em></strong>

Antes do Windows 10 Fall Creators Update (versão 1709), o WSL foi lançado como um recurso beta e instalado uma única instância do Ubuntu, quando o "Bash no Ubuntu no Windows" (ou Bash.exe) foi executado pela primeira vez.

> Embora você possa usar o WSL em versões anteriores do Windows 10, essa versão beta "distribuição herdada" é considerada obsoleta. Recomendamos que você execute a versão mais recente do Windows 10 disponíveis. Cada nova versão do Windows 10 inclui várias centenas de correções e aprimoramentos no WSL sozinho, permitindo que o tornam cada vez mais ferramentas do Linux e aplicativos sejam executados corretamente no WSL.

Se você não pode atualizar para o Fall Creators Update ou posterior, siga as etapas abaixo para habilitar e usar WSL:

1. Ativar o desenvolvedor modo para execução WSL em atualização de aniversário do Windows 10 ou atualização para criadores, você deve habilitar o modo de desenvolvedor:

    Abra **as configurações** -> **atualização e segurança** -> **para desenvolvedores**

    Selecione o botão de opção de modo de desenvolvedor  
    ![Habilitar o modo de desenvolvedor](media/updateAndSecurity.png)

    > O requisito para habilitar o modo de desenvolvedor foi [removido no Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. Abra um prompt de comando.  Tipo `bash` e pressione enter

    Na primeira vez que você executar o Bash no Ubuntu no Windows, você será solicitado a aceitar a licença da Canonical. Quando accpted, WSL baixará e instalará a instância do Ubuntu em seu computador, e um atalho "Bash no Ubuntu no Windows" será adicionado ao menu Iniciar.

    ![Solicitar a instalação do Ubuntu](media/bashShellInstall.png)

    Na primeira vez que você executar o Bash no Ubuntu no Windows, você será solicitado a criar um nome de usuário do UNIX e uma senha. Siga as [novas instruções de instância de distribuição](initialize-distro.md) para concluir a instalação

1. Inicie um novo shell do Ubuntu, qualquer um:
    * Executando `bash` em um prompt de comando
    * Clicar o atalho "Bash no Ubuntu no Windows" do menu Iniciar

    
## <a name="uninstallingremoving-the-legacy-distro"></a>Desinstalando/remoção da distribuição herdada
Se você atualizar para o Windows 10 Fall Creators Update de uma versão anterior do Windows 10 que você instalou o WSL, sua distribuição existente permanecerão intacta. No entanto, podemos FORTEMENTE encorajá-lo a instalar uma distribuição de nova entregues pelo Store urgente e migrar quaisquer arquivos necessários, dados, etc. de sua distribuição herdada para sua nova distribuição.

Para remover da distribuição herdada do seu computador, execute o seguinte de uma instância de linha de comando ou o PowerShell:

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a>A exclusão manual de distribuição herdada
Se desejar, você poderá excluir manualmente sua instância herdada. Isso pode ser necessário se você encontrar problemas ao desinstalar usando a distribuição herdada `lxrun.exe`, ou estiver executando a atualização do Windows 10 primavera 2018 (ou posterior) que não são fornecidos com `lxrun.exe`.

Para forçar a exclusão de sua distribuição WSL herdada, exclua o `%localappdata%\lxss\` pasta (e todos os é um subdiretório de conteúdo) usando o Explorador de arquivos dos Windows ou da linha de comando:

Usando o PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

Usando o Cmd:
```console
DEL /S %localappdata%\lxss\
```
