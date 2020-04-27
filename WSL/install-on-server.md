---
title: Instalar o Subsistema Linux no Windows Server
description: Instruções de instalação para o Subsistema Linux no Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema do windows para linux, windowssubsystem, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256389"
---
# <a name="windows-server-installation-guide"></a>Guia de instalação do Windows Server

> Aplica-se ao Windows Server 2019 e posteriores

No //Build2017, a Microsoft anunciou que o Subsistema do Windows para Linux estará [disponível no Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Essas instruções demonstram como executar o Subsistema do Windows para Linux no Windows Server 1709 e versões posteriores.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Habilitar o WSL (Subsistema do Windows para Linux)

Para poder executar as distribuições do Linux no Windows, você deverá habilitar o recurso opcional "Subsistema do Windows para Linux" e reiniciar.

1. Abra o PowerShell como administrador e execute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie seu computador quando solicitado. **Essa reinicialização é necessária** para que o WSL possa ser iniciado em um ambiente de execução confiável.

## <a name="download-a-linux-distro"></a>Baixar uma distribuição do Linux

Siga [estas instruções](install-manual.md) para baixar sua distribuição favorita do Linux.

## <a name="extract-and-install-a-linux-distro"></a>Extrair e instalar uma distribuição do Linux
Agora que você baixou uma distribuição, extraia o conteúdo dela e instale-a manualmente:

1. Extraia o conteúdo `<distro>.appx` do pacote, por exemplo, usando o PowerShell:

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. Execute o inicializador da distribuição para concluir a instalação e execute o aplicativo inicializador da distribuição na pasta de destino, denominada `<distro>.exe`. Por exemplo: `ubuntu.exe` etc.

    ![Expansão da distribuição do Ubuntu no Windows Server](media/server-appx-expand.png)

    > **Solução de problemas**
    > * **Falha na instalação com o erro 0x8007007e**: Esse erro ocorre quando o sistema não é compatível com o WSL. Certifique-se de que:
    >   * Você está executando o Windows Build 16215 ou posterior. [Verifique seu build](troubleshooting.md#check-your-build-number).
    >   * O componente opcional do Subsistema Windows para Linux está habilitado e o computador foi reiniciado.  [Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Adicione o caminho da distribuição ao caminho do ambiente do Windows (`C:\Users\Administrator\Ubuntu`, neste exemplo), por exemplo, usando o PowerShell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    Agora você pode iniciar a distribuição em qualquer caminho digitando `<distro>.exe`. Por exemplo: `ubuntu.exe`

Agora que a distribuição do Linux está instalada, você deve [inicializar a nova instância de distribuição](initialize-distro.md) antes de usar sua distribuição.
