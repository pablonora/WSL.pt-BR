---
title: Instalar o subsistema Linux no Windows Server
description: Instruções de instalação para o subsistema Linux no Windows Server.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Windows Server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269781"
---
# <a name="windows-server-installation-guide"></a>Guia de instalação do Windows Server

> Aplica-se ao Windows Server 2019 e posterior

Na//Build2017, a Microsoft anunciou que o subsistema do Windows para Linux estará [disponível no Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Estas instruções demonstram como executar o subsistema do Windows para Linux no Windows Server 1709 e posterior.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Habilitar o subsistema do Windows para Linux (WSL)

Para poder executar o Linux distribuições no Windows, você deve habilitar o recurso opcional "subsistema do Windows para Linux" e reinicializar.

1. Abra o PowerShell como administrador e execute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie o computador quando solicitado. **Essa reinicialização é necessária** para garantir que o WSL possa iniciar um ambiente de execução confiável.

## <a name="download-a-linux-distro"></a>Baixar um distribuição do Linux

Siga [estas instruções](install-manual.md) para baixar sua distribuição do Linux favorita.

## <a name="extract-and-install-a-linux-distro"></a>Extrair e instalar um distribuição do Linux
Agora que você baixou um distribuição, Extraia seu conteúdo e instalou manualmente o distribuição:

1. Extraia `<distro>.appx` o conteúdo do pacote, por exemplo, usando o PowerShell:

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. Execute o iniciador distribuição para concluir a instalação, execute o aplicativo iniciador distribuição na pasta de `<distro>.exe`destino, denominada. Por exemplo: `ubuntu.exe`, etc.

    ![Expansão do Ubuntu distribuição no Windows Server](media/server-appx-expand.png)

    > **Solução de problemas**
    > * **A instalação falhou com o erro 0x8007007E**: Esse erro ocorre quando o sistema não dá suporte a WSL. Certifique-se de que:
    >   * Você está executando o Windows Build 16215 ou posterior. [Verifique sua compilação](troubleshooting.md#check-your-build-number).
    >   * O componente opcional do subsistema do Windows para Linux está habilitado e o computador foi reiniciado.  [Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Adicione o caminho distribuição ao caminho do ambiente do Windows`C:\Users\Administrator\Ubuntu` (neste exemplo), por exemplo, usando o PowerShell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    Agora você pode iniciar o distribuição a partir de qualquer caminho `<distro>.exe`digitando. Por exemplo: `ubuntu.exe`

Agora que seu distribuição do Linux está instalado, você deve [inicializar sua nova instância do distribuição](initialize-distro.md) antes de usar o distribuição.
