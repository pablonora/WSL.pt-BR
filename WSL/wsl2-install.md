---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91bd479e922fc29bf11b89dcfe06fa381632c4fa
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520545"
---
# <a name="installation-instructions-for-wsl-2"></a>Instruções de instalação do WSL 2

Você pode assistir ao vídeo abaixo ou ler este artigo para saber como instalar o WSL2. 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:

> O WSL 2 só está disponível no Windows 10 builds 18917 ou superiores

- Verifique se você tem o WSL instalado (você pode encontrar instruções para fazer isso [aqui](./install-win10.md)) e se está executando o Windows 10 **build 18917** ou superior
   - Para verificar se você está usando o build 18917 ou superior, ingresse [no Programa Windows Insider](https://insider.windows.com/en-us/) e selecione o anel modo Rápido ou Lento. 
   - Você pode verificar a versão do Windows abrindo o prompt de comando e executando o comando `ver`.
- Habilite o componente opcional "Plataforma de máquina virtual"
- Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando
- Verifique quais versões do WSL suas distribuições estão usando

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Habilite o componente opcional "Plataforma de máquina virtual" e verifique se o WSL está habilitado

Você precisará verificar se tem os componentes opcionais do Subsistema do Windows para Linux e da Plataforma de Máquina Virtual instalados. Você pode fazer isso executando o seguinte comando no PowerShell: 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Reinicie o computador para concluir a instalação dos dois componentes.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando

Se você não tiver uma distribuição do Linux instalada, consulte a página de documentação [Instalar no Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) para obter instruções sobre a instalação. 

Para definir uma distribuição, execute: 

```
wsl --set-version <Distro> 2
```

e substitua `<Distro>` pelo nome real da sua distribuição. (Você pode encontrá-lo com o comando: `wsl -l`). Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.

Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:

```
wsl --set-default-version 2
```

Isso fará com que qualquer nova distribuição instalada seja inicializada como uma distribuição do WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Termine verificando quais versões do WSL suas distribuições estão usando

Para verificar quais versões do WSL cada distribuição está usando, execute o seguinte comando (somente disponível no Windows Build 18917 ou superior):

`wsl --list --verbose` ou `wsl -l -v`

A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão". Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2. 

## <a name="troubleshooting"></a>Solução de problemas: 

Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.

* **Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**
    * Verifique se a virtualização está habilitada dentro do BIOS do seu computador. As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.
   
* **Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente. Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).

* **A operação solicitada não pôde ser concluída devido a uma limitação do sistema de disco virtual. Os arquivos do disco rígido virtual devem ser descompactados e descriptografados e não devem ser esparsos.**
    * Verifique o [thread 4103 do GitHub no WSL](https://github.com/microsoft/WSL/issues/4103) em que esse problema está sendo acompanhado para obter informações atualizadas.

* **O termo 'wsl' não é reconhecido como nome de um cmdlet, uma função, um arquivo de script ou um programa operável.** 
    * Verifique se o [componente opcional do Subsistema do Windows para Linux está instalado](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> Além disso, se você estiver usando um dispositivo Arm64 e executar esse comando do PowerShell, receberá esse erro. Em vez disso, execute `wsl.exe` no [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) ou no prompt de comando. 
