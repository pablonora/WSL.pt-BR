---
title: Instalar o Subsistema Linux no Windows Server
description: Instruções de instalação para o Subsistema Linux no Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema do windows para linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ebcd7f6b10d2b734b1f2a66f64a5e3292855bcf4
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671013"
---
# <a name="windows-server-installation-guide"></a>Guia de instalação do Windows Server

O Subsistema do Windows para Linux está disponível para instalação no Windows Server 2019 (versão 1709) e posterior. Este guia explicará as etapas de habilitação do WSL em seu computador.

## <a name="enable-the-windows-subsystem-for-linux"></a>Habilitar o Subsistema do Windows para Linux

Para poder executar as distribuições do Linux no Windows, você deverá habilitar o recurso opcional "Subsistema do Windows para Linux" e reiniciar.

Abra o PowerShell como administrador e execute:

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a>Baixar uma distribuição do Linux

Siga [estas instruções](install-manual.md) para baixar sua distribuição favorita do Linux.

## <a name="extract-and-install-a-linux-distribution"></a>Extrair e instalar uma distribuição do Linux

Agora que você baixou uma distribuição do Linux, para extrair o conteúdo e instalá-lo manualmente, siga estas etapas:

1. Extraia o conteúdo do pacote `<distro>.appx` usando o PowerShell:

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. Execute o aplicativo inicializador de distribuição na pasta de destino. O inicializador normalmente é chamado de `<distro>.exe` (por exemplo, `ubuntu.exe`).

    ![Expansão da distribuição do Ubuntu no Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> **Falha na instalação com o erro 0x8007007e**: Esse erro ocorre quando o sistema não é compatível com o WSL. Garanta que você está executando o Windows Build 16215 ou posterior. [Verifique seu build](troubleshooting.md#check-your-build-number). Certifique-se também de [confirmar se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled) e se o computador foi reiniciado após a habilitação do recurso.  

3. Adicione o caminho da distribuição ao caminho do ambiente do Windows (`C:\Users\Administrator\Ubuntu`, neste exemplo) usando o PowerShell:

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

Agora você pode iniciar sua distribuição em qualquer caminho digitando `<distro>.exe`. Por exemplo: `ubuntu.exe`.

Agora que a distribuição está instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) antes de usar a distribuição.
