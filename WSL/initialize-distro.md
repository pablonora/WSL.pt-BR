---
title: Inicializar um novo WSL Linux distribuição
description: Depois de instalar um distribuição do Linux para o WSL, conclua a inicialização seguindo estas etapas simples
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122710"
---
# <a name="initializing-a-newly-installed-distro"></a>Inicializando um distribuição recentemente instalado
Depois que o distribuição tiver sido baixado e instalado, você precisará concluir a inicialização do novo distribuição:

## <a name="launch-a-distro"></a>Iniciar um distribuição
Para concluir a inicialização do seu distribuição recentemente instalado, inicie uma nova instância. Você pode fazer isso clicando no botão "Iniciar" no aplicativo Microsoft Store ou iniciando o distribuição no menu iniciar:

> Dica: Talvez você queira fixar o distribuições usado com mais frequência no menu iniciar e/ou na barra de tarefas!

![Iniciar o distribuições no menu iniciar](media/start-menu.png)

> No Windows Server, você pode iniciar o executável `<distro>.exe` do inicializador do distribuição na pasta de instalação do distribuição.

Na primeira vez em que um distribuição é executado recentemente, uma janela de console será aberta e você será solicitado a aguardar um minuto ou dois para que a instalação seja concluída.

> Durante esse estágio final da instalação, os arquivos do distribuição são descompactados e armazenados em seu computador, prontos para uso. Isso pode levar cerca de um minuto ou mais, dependendo do desempenho dos dispositivos de armazenamento do seu computador. Essa fase de instalação inicial só é necessária quando um distribuição é limpo-instalado – todas as futuras inicializações devem levar menos de um segundo.

## <a name="setting-up-a-new-linux-user-account"></a>Configurando uma nova conta de usuário do Linux

Quando a instalação for concluída, você será solicitado a criar uma nova conta de usuário (e sua senha). 

![Desempacotamento do Ubuntu no console do Windows](media/UbuntuInstall.png)

Essa conta de usuário é para o usuário não administrador normal no qual você fará logon por padrão ao iniciar um distribuição.

> Você pode escolher qualquer nome de usuário e senha que desejar-eles não têm nenhuma influência sobre seu nome de usuário do Windows. 

Quando você abrir uma nova instância do distribuição, não será solicitada sua senha, mas **se você elevar um processo usando `sudo`o, precisará inserir sua senha**, portanto, certifique-se de escolher uma senha que você possa lembrar facilmente! Consulte a página de [suporte ao usuário](user-support.md) para obter mais informações.

## <a name="update--upgrade-your-distros-packages"></a>Atualizar & atualizar os pacotes do seu distribuição

A maioria dos distribuiçõess são fornecidos com um catálogo de pacotes vazio/mínimo. É altamente recomendável atualizar regularmente seu catálogo de pacotes e atualizar seus pacotes instalados usando o Gerenciador de pacotes preferencial do distribuição. No Debian/Ubuntu, você usa apt:

```bash
sudo apt update && sudo apt upgrade
```

> O Windows não atualiza ou atualiza automaticamente suas distribuição (s) Linux: Essa é uma tarefa que os usuários do Linux preferem controlar.

Concluído! Aproveite o uso de seu novo distribuição Linux no WSL! Para saber mais sobre o WSL, examine os outros [documentos do WSL](https://aka.ms/wsldocs)ou a página de recursos do [WSL Learning](https://aka.ms/learnwsl).

![Aproveite o uso do Linux no WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Solução de problemas

Abaixo estão os erros relacionados e as correções sugeridas. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para obter outros erros comuns e suas soluções.

> **Falha na instalação com o erro 0x8007007E** Esse erro ocorre quando o sistema não dá suporte ao Linux na loja.  Certifique-se de que:
> * Você está executando o Windows Build 16215 ou posterior. [Verifique sua compilação](troubleshooting.md#check-your-build-number).
> * O componente opcional do subsistema do Windows para Linux está habilitado e o computador foi reiniciado.  [Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
