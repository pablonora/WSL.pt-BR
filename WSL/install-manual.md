---
title: Baixar manualmente o subsistema do Windows para distribuições do Linux (WSL)
description: Instruções sobre como baixar manualmente o subsistema do Windows para distribuições do Linux.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, WSL, subsistema do windows, distribuição, ubuntu, openSUSE, kali SLES, debian,
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063564"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Baixar manualmente o subsistema do Windows para pacotes de distribuição do Linux

Há vários cenários em que você pode não ser capaz de (ou deseja) para instalar as distribuições de Linux WSL por meio do Microsoft Store. Especificamente, você pode estar executando um SKU de sistema operacional que não oferece suporte a Microsoft Store, ou suas políticas de rede corporativa e/ou administradores para não permitir o uso da Microsoft Store em seu ambiente de desktop manutenção de longo prazo (LTSB/LTSC) ou o Windows Server.

Nesses casos, enquanto WSL em si estiver disponível, como você baixar e instalar distribuições do Linux no WSL se você não pode acessar o armazenamento?

> Observação: **Ambientes de shell de linha de comando, incluindo distribuições de Linux/SWL, PowerShell e Cmd não têm permissão para executar no modo do Windows 10 S**. Essa restrição existe para garantir que as metas de integridade e segurança de modo S oferece: Leia [esta postagem](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obter mais informações.

## <a name="downloading-distros"></a>Baixando distribuições

Se o aplicativo Microsoft Store não estiver disponível, você pode baixar e instalar manualmente as distribuições de Linux clicando estes links:
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE](https://aka.ms/wsl-opensuse-42)
* [SLES](https://aka.ms/wsl-sles-12)

Isso fará com que o `<distro>.appx` pacotes para baixar uma pasta de sua escolha. Siga as [instruções de instalação](#installing-your-distro) para instalar seu distro(s) baixado.

## <a name="downloading-distros-via-the-command-line"></a>Download de Distribuições por meio da linha de comando
Se você preferir, você também pode baixar o distro(s) preferido por meio da linha de comando:

 ### <a name="download-using-powershell"></a>Baixe usando o PowerShell
 Para baixar as distribuições usando o PowerShell, use o [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet. Aqui está um exemplo de instrução para baixar o Ubuntu 16.04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Se o download estiver demorando muito tempo, desativar a barra de progresso, definindo `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Baixe usando o curl
Atualização do Windows 10 primavera 2018 (ou posterior) inclui a popular [curl do utilitário de linha de comando](https://curl.haxx.se/) com a qual você pode invocar as solicitações da web (ou seja, HTTP GET, POST, PUT, comandos etc.) na linha de comando. Você pode usar `curl.exe` para baixar as distribuições acima:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

No exemplo acima, `curl.exe` é executado (não apenas `curl`) garantir que, no PowerShell, o executável real curl invocado, não a rotação do PowerShell para o alias [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> Observação: Usando o `curl` pode ser preferível se você precisar invocar/script as etapas de download usando o shell de Cmd e/ou `.bat`  /  `.cmd` scripts.

## <a name="installing-your-distro"></a>Instalando sua distribuição
Para obter instruções sobre como instalar seu distro(s) baixado, consulte o [área de trabalho do Windows](install-win10.md) ou [do Windows Server](install-on-server.md) instruções de instalação.
