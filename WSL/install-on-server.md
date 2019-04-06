---
title: Instale o subsistema do Linux no Windows Server
description: Instruções de instalação para o subsistema do Linux no Windows Server.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, do windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063614"
---
# <a name="windows-server-installation-guide"></a>Guia de instalação do Windows Server

> Aplica-se ao Windows Server 2019 e posterior

No / / Build2017, a Microsoft anunciou que o subsistema do Windows para Linux serão [disponível no Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Estas instruções explicam executando o subsistema Windows para Linux no Windows Server 1709 e posterior.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Permitir que o subsistema Windows para Linux (WSL)

Antes de executar distribuições do Linux no Windows, você deve habilitar o recurso opcional de "Subsistema Windows para Linux" e reinicialize.

1. Abra o PowerShell como administrador e execute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie o computador quando solicitado. **Essa reinicialização é necessária** para garantir que o WSL pode iniciar um ambiente de execução confiável.

## <a name="download-a-linux-distro"></a>Baixe uma distribuição do Linux

Siga [estas instruções](install-manual.md) para baixar sua distribuição do Linux favorita.

## <a name="extract-and-install-a-linux-distro"></a>Extrair e instalar uma distribuição do Linux
Agora que você baixou uma distribuição, extraia seu conteúdo e instalar manualmente a distribuição:

1. Extrair o `<distro>.appx` conteúdo do pacote, por exemplo, usando o PowerShell:

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. Execute o iniciador de distribuição para concluir a instalação, execute o aplicativo de iniciador de distribuição na pasta de destino, denominado `<distro>.exe`. Por exemplo: `ubuntu.exe`, etc.

    ![Distribuição expandida do Ubuntu no Windows Server](media/server-appx-expand.png)

    > **Solução de problemas**
    > * **Falha na instalação com o erro 0x8007007e**: Esse erro ocorre quando o sistema não dá suporte a WSL. Certifique-se de que:
    >   * Você está executando o Windows build 16215 ou posterior. [Verificar seu build](troubleshooting.md#check-your-build-number).
    >   * O subsistema do Windows para o componente opcional do Linux está habilitado e o computador for reiniciado.  [Verifique se WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Adicionar seu caminho de distribuição para o caminho de ambiente do Windows (`C:\Users\Administrator\Ubuntu` neste exemplo), por exemplo, usando o Powershell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    Agora você pode iniciar sua distribuição a partir de qualquer caminho digitando `<distro>.exe`. Por exemplo:  `ubuntu.exe`

Agora que sua distribuição do Linux é instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) antes de usar sua distribuição.
