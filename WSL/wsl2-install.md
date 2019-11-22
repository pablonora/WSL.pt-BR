---
title: Instalar o WSL 2
description: Instruções de instalação do WSL 2
keywords: BashOnWindows, Bash, WSL, WSL 2, Windows, subsistema do Windows para Linux, subsistema do Windows, Ubuntu, Debian, Suse, Windows 10, instalar
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a53e6a986813809d0c355b80b3fe3028adb21375
ms.sourcegitcommit: 73f4cc6ac9482ea9727f3cda0ec5c3572e164256
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/21/2019
ms.locfileid: "74309053"
---
# <a name="installation-instructions-for-wsl-2"></a>Instruções de instalação do WSL 2

Para instalar e começar a usar o WSL 2, conclua as etapas a seguir:

> WSL 2 is only available in Windows 10 builds 18917 or higher

- Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher
   - To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring. 
   - You can check your Windows version by opening Command Prompt and running the `ver` command.
- Habilite o componente opcional "Plataforma de máquina virtual"
- Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando
- Verifique quais versões do WSL suas distribuições estão usando

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled

You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed. You can do that by running the following command in PowerShell: 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Please restart your machine to finish installing both components.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Defina uma distribuição para ser apoiada pelo WSL 2 usando a linha de comando

If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one. 

To set a distro please run: 

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

To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):

`wsl --list --verbose` ou `wsl -l -v`

A distribuição que você escolheu acima agora deve exibir um "2" na coluna "versão". Agora que você terminou, sinta-se à vontade para começar a usar sua distribuição do WSL 2. 

## <a name="troubleshooting"></a>Solução de problemas: 

Veja abaixo erros relacionados e correções sugeridas ao instalar o WSL 2. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros gerais do WSL e suas soluções.

* **Ocorreu falha na instalação com o erro 0x80070003 ou 0x80370102**
    * Verifique se a virtualização está habilitada dentro do BIOS do seu computador. As instruções para fazer isso variam de um computador para o outro e muito provavelmente estarão sob opções relacionadas à CPU.
   
* **Erro ao tentar fazer upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Verifique se você tem o subsistema do Windows para Linux habilitado e se está usando o Build do Windows versão 18917 ou mais recente. Para habilitar o WSL, execute este comando em um prompt do PowerShell com privilégios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Você pode encontrar as instruções de instalação completas do WSL [aqui](./install-win10.md).

* **The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**
    * Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.

* **The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.** 
    * Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error. Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt. 
