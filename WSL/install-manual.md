---
title: Baixar manualmente o subsistema do Windows para Linux (WSL) distribuições
description: Instruções sobre como baixar manualmente o subsistema do Windows para distribuições do Linux.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema do Windows para Linux, WSL, subsistema do Windows, distribuição, Ubuntu, openSUSE, SLES, Debian, Kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: aa0b42748115045105bb4e6eae91493bfee11d09
ms.sourcegitcommit: 467b6c8e9716d1a60dbf9f7658fd9579da365b58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2020
ms.locfileid: "77624920"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Baixar manualmente os pacotes do subsistema do Windows para Linux distribuição

Há vários cenários nos quais você pode não ser possível (ou deseja) instalar o WSL Linux distribuições por meio do Microsoft Store. Especificamente, você pode estar executando um SKU de sistema operacional de área de trabalho do Windows Server ou de LTSC (manutenção de longo prazo) que não dá suporte a Microsoft Store, ou suas políticas de rede corporativa e/ou administradores para não permitir o uso de Microsoft Store em seu ambiente.

Nesses casos, embora o WSL em si esteja disponível, como baixar e instalar o Linux distribuições no WSL se você não puder acessar o armazenamento?

> Observação: os **ambientes de Shell de linha de comando, incluindo cmd, PowerShell e Linux/WSL distribuições, não têm permissão para serem executados no modo Windows 10 S**. Essa restrição existe para garantir a integridade e os objetivos de segurança que o modo S fornece: leia [esta postagem](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obter mais informações.

## <a name="downloading-distros"></a>Baixando o distribuições

Se o aplicativo Microsoft Store não estiver disponível, você poderá baixar e instalar manualmente o distribuições do Linux clicando nestes links:
<!-- * [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm) -->
* Ubuntu 18.04
* Ubuntu 18, 4 ARM
* [Ubuntu 16, 4](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix para WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Isso fará com que os pacotes de `<distro>.appx` sejam baixados em uma pasta de sua escolha. Siga as [instruções de instalação](#installing-your-distro) para instalar suas distribuiçãos baixadas.

## <a name="downloading-distros-via-the-command-line"></a>Baixando o distribuições por meio da linha de comando
Se preferir, você também pode baixar seus distribuição (s) preferenciais por meio da linha de comando:

 ### <a name="download-using-powershell"></a>Baixar usando o PowerShell
 Para baixar o distribuições usando o PowerShell, use o cmdlet [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) . Aqui está um exemplo de instrução para baixar o Ubuntu 16, 4.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Se o download estiver demorando muito, desative a barra de progresso definindo `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Baixar usando ondulação
A atualização do Windows 10 Spring 2018 (ou posterior) inclui o [Utilitário de linha de comando de ondulação](https://curl.haxx.se/) popular com o qual você pode invocar solicitações da Web (ou seja, comandos http Get, post, put, etc.) da linha de comando. Você pode usar `curl.exe` para baixar o distribuições acima:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

No exemplo acima, `curl.exe` é executado (não apenas `curl`) para garantir que, no PowerShell, o executável de ondulação real seja invocado, não o alias de ondulação do PowerShell para [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> Observação: o uso de `curl` pode ser preferível se você precisar invocar/gerar script de etapas de download usando o shell cmd e/ou `.bat` / scripts `.cmd`.

## <a name="installing-your-distro"></a>Instalando seu distribuição
Se você estiver usando o Windows 10, poderá instalar o distribuição com o PowerShell. Basta navegar para a pasta que contém o distribuição baixado acima e, nesse diretório, execute o comando a seguir, em que `app_name` é o nome do seu arquivo distribuição. Appx.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Se você estiver usando o Windows Server, poderá encontrar as instruções de instalação na página de documentação do [Windows Server](install-on-server.md) .

Depois de instalar o distribuição, consulte a página [etapas de inicialização](initialize-distro.md) para inicializar o novo distribuição.
