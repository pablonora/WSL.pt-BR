---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91994f3a075436c022acb9dadeea072142687b72
ms.sourcegitcommit: cf6d8e277ed3102f8f879b9f39ba0966d4ea6135
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2019
ms.locfileid: "74164336"
---
# <a name="installation-instructions-for-wsl-2"></a>Instruções de instalação do WSL 2

Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:

> O WSL 2 só está disponível no Windows 10 Builds 18917 ou superior

- Verifique se você tem o WSL instalado (você pode encontrar instruções para fazer isso [aqui](./install-win10.md)) e se está executando o Windows 10 **Build 18917** ou superior
   - Para verificar se você está usando o Build 18917 ou superior, ingresse [no programa Windows Insider](https://insider.windows.com/en-us/) e selecione o anel "rápido". 
   - Você pode verificar a versão do Windows abrindo o prompt de comando e executando o comando `ver`.
- Habilite o componente opcional "Plataforma de máquina virtual"
- Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando
- Verifique quais versões do WSL suas distribuições estão usando

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Habilite o componente opcional ' plataforma de máquina virtual ' e verifique se o WSL está habilitado

Para habilitar o componente ' plataforma de máquina virtual ', abra o PowerShell como administrador e execute o comando a seguir. Se você estiver instalando o WSL pela primeira vez, selecione ' não ' quando for solicitada uma reinicialização, pois será necessário reiniciar o computador assim mesmo após instalar o componente opcional ' subsistema do Windows para Linux '.

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

Você também precisará certificar-se de que o componente opcional do subsistema do Windows para Linux esteja habilitado. Você pode fazer isso executando o seguinte comando em uma janela do PowerShell com privilégios de administrador: 

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

Reinicie o computador para concluir a instalação dos dois componentes.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando

Se você não tiver um distribuição do Linux instalado, consulte a página [instalar no Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs para obter instruções sobre como instalar um. 

No PowerShell, execute:

`wsl --set-version <Distro> 2`

e substitua `<Distro>` pelo nome real da sua distribuição. (Você pode encontrá-lo com o comando: `wsl -l`). Você pode retornar ao WSL 1 a qualquer momento executando o mesmo comando acima, mas substituindo “2” por “1”.

Além disso, se quiser tornar o WSL 2 sua arquitetura padrão, você poderá fazê-lo com este comando:

`wsl --set-default-version 2`

Isso fará com que qualquer nova distribuição instalada seja inicializada como uma distribuição do WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Termine verificando quais versões do WSL suas distribuições estão usando

Para verificar quais versões do WSL cada distribuição está usando, use o seguinte comando (disponível somente no Windows Build 18917 ou superior):

`wsl --list --verbose` ou `wsl -l -v`

A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão". Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2. 

## <a name="troubleshooting"></a>Solução de problemas: 

Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.

* **Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**
    * Verifique se a virtualização está habilitada dentro do BIOS do seu computador. As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.
   
* **Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente. Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).

* **A operação solicitada não pôde ser concluída devido a uma limitação do sistema de disco virtual. Os arquivos do disco rígido virtual devem ser descompactados e descriptografados e não devem ser esparsos.**
    * Verifique o [thread do GitHub WSL #4103](https://github.com/microsoft/WSL/issues/4103) onde esse problema está sendo acompanhado para obter informações atualizadas.