---
title: Inicializar uma nova distribuição do Linux de WSL
description: Depois de instalar uma distribuição do Linux para WSL, concluir a inicialização, seguindo estas etapas simples
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063604"
---
# <a name="initializing-a-newly-installed-distro"></a>Inicializando uma distribuição recém-instalado
Depois que sua distribuição foi baixada e instalada, você precisará concluir a inicialização da nova distribuição:

## <a name="launch-a-distro"></a>Iniciar uma distribuição
Para concluir a inicialização de sua distribuição recém-instalado, inicie uma nova instância. Você pode fazer isso clicando no botão "Iniciar" no aplicativo da Windows Store, ou iniciando a distribuição do menu Iniciar:

> Dica: Pode ser que você deseja fixar seu distribuições usadas com mais frequência ao menu Iniciar e/ou à barra de tarefas!

![Inicie as distribuições do menu Iniciar](media/start-menu.png)

> No Windows Server, você pode iniciar o inicializador do sua distribuição executável `<distro>.exe` da pasta de instalação de distribuição.

Na primeira vez em uma distribuição recém-instalado é executado, um Console do janela será aberta, e você terá que aguardar um minuto ou dois concluir a instalação.

> Durante esse estágio final da instalação, os arquivos da distribuição são desprovisionar compactados e armazenados no seu PC, pronto para uso. Isso pode levar ao redor de um minuto ou mais conforme o desempenho do seu PC dispositivos de armazenamento. Fase de instalação inicial, só é necessário quando uma distribuição é limpo instalado - todas as inicializações futuras devem levar menos de um segundo.

## <a name="setting-up-a-new-linux-user-account"></a>Como configurar uma nova conta de usuário do Linux

Depois que a instalação for concluída, você precisará criar uma nova conta de usuário (e sua senha). 

![Ubuntu desempacotar no console do Windows](media/UbuntuInstall.png)

Essa conta de usuário é para o usuário normal não-administrador que você vai estar conectado como por padrão ao iniciar uma distribuição.

> Você pode escolher qualquer nome de usuário e senha que você deseja – eles terem nenhuma influência sobre seu nome de usuário do Windows. 

Quando você abre uma nova instância de distribuição, não serão solicitados a senha, mas **se você elevar um processo usando `sudo`, você precisará inserir sua senha**, portanto, certifique-se de que você escolher uma senha que você se lembre facilmente! Consulte a [suporte ao usuário](user-support.md) página para obter mais informações.

## <a name="update--upgrade-your-distros-packages"></a>Atualizar & pacotes da sua distribuição de atualização

A maioria das distribuições são fornecidos com um catálogo de pacote vazio/mínimo. É altamente recomendável atualizar regularmente seu catálogo de pacote e atualizar seus pacotes instalados usando o Gerenciador de pacotes preferido da sua distribuição. No Debian/Ubuntu, use apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows automaticamente atualização ou upgrade distro(s) seu Linux: Essa é uma tarefa que preferir controlar se os usuários do Linux.

Concluído! Aproveite usando sua nova distribuição do Linux no WSL. Para saber mais sobre o WSL, examine a outra [docs WSL](https://aka.ms/wsldocs), ou o [WSL página de recursos de aprendizado](https://aka.ms/learnwsl).

![Aproveite a usando o Linux no WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Solução de problemas

Abaixo estão os erros relacionados e correções sugeridas. Consulte a [página de solução de problemas de WSL](troubleshooting.md) para outros erros comuns e suas soluções.

> **Falha na instalação com o erro 0x8007007e** esse erro ocorre quando o sistema não dá suporte a Linux da loja.  Certifique-se de que:
> * Você está executando o Windows build 16215 ou posterior. [Verificar seu build](troubleshooting.md#check-your-build-number).
> * O subsistema do Windows para o componente opcional do Linux está habilitado e o computador for reiniciado.  [Verifique se WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
