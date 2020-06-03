---
title: Instalar o WSL (Subsistema Windows para Linux) no Windows 10
description: Instruções de instalação para o Subsistema Windows para Linux no Windows 10.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, install
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6ed12ba9d63d3f4038b67489035e13113a372928
ms.sourcegitcommit: 9f12e168b80775cd967f22f97376e51043c3667e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "84301197"
---
# <a name="install-windows-subsystem-for-linux"></a>Instalar o Subsistema do Windows para Linux

O guia a seguir abordará as etapas necessárias para instalar o WSL (Subsistema do Windows para Linux) em um computador que executa o Windows 10.

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a>Habilitar o recurso opcional Subsistema do Windows para Linux

Antes de instalar uma distribuição do Linux, habilite o recurso opcional "Subsistema do Windows para Linux" no Windows 10:

1. Abra o PowerShell como administrador e insira este script:

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. Reinicie seu computador quando solicitado.

## <a name="install-a-linux-distribution"></a>Instalar uma distribuição do Linux

Há três maneiras de baixar e instalar suas distribuições preferidas do Linux:

- Baixe e instale usando a Microsoft Store (consulte abaixo)
- [Baixar e instalar a distribuição manualmente por meio da linha de comando](install-manual.md)
- [Instalar no Windows Server](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a>Instale usando a Microsoft Store

As distribuições do Linux podem ser instaladas por meio da Microsoft Store no Windows 10 (Build 16215 e posteriores).

> [!NOTE]
> Siga estas etapas para [verificar o número de build do Windows 10](troubleshooting.md#check-your-build-number).

1. Abra a Microsoft Store e escolha sua distribuição do Linux favorita.

    ![Exibição das distribuições do Linux na Microsoft Store](media/store.png)

    Os links a seguir abrirão a página da Microsoft Store para cada distribuição:

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix para WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. Selecione "Obter" e, depois que a distribuição for baixada, selecione "Iniciar".

    ![Exibição das distribuições do Linux na Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Conclua a inicialização de sua distribuição

Depois de iniciar a distribuição do Linux, siga as instruções na tela para inicializar a distribuição.

> [!NOTE]
> Para o Windows Server, inicie a distribuição usando o executável, `<distro>.exe`, na pasta de instalação.

Na primeira vez em que uma distribuição recém-instalada for executada, uma janela de console será aberta e você precisará aguardar alguns minutos para que a instalação seja concluída. Durante essa fase final da instalação, os arquivos da distribuição são descompactados e armazenados em seu computador, prontos para uso. Isso pode levar cerca de um minuto ou mais, dependendo do desempenho dos dispositivos de armazenamento de seu computador. Essa fase de instalação inicial só é necessária quando uma distribuição é instalada de modo limpo – todas as futuras inicializações deverão levar menos de um segundo.

## <a name="set-up-a-new-linux-user-account"></a>Configurar uma nova conta de usuário do Linux

Quando a instalação for concluída, você será solicitado a criar uma nova conta de usuário (e sua senha).

![Desempacotamento do Ubuntu no console do Windows](media/UbuntuInstall.png)

Essa conta de usuário destina-se ao usuário não administrador normal como o qual você estará conectado por padrão ao iniciar uma distribuição. Você pode escolher qualquer nome de usuário e senha que desejar – eles não têm nenhuma influência sobre seu nome de usuário do Windows.

Quando você abrir uma nova instância da distribuição, não será solicitada sua senha, mas **se você elevar um processo usando `sudo`, precisará inserir sua senha**, portanto, certifique-se de escolher uma senha que você possa lembrar facilmente! Consulte a página [Suporte ao usuário](user-support.md) para obter mais informações.

## <a name="update--upgrade-packages"></a>Atualizar pacotes e fazer upgrade deles

A maioria das distribuições é fornecida com um catálogo de pacotes vazio ou mínimo. Recomendamos expressamente que você atualize regularmente o catálogo de pacotes e faça upgrade dos pacotes instalados usando seu gerenciador de pacotes preferencial da distribuição. No Debian/Ubuntu, use apt:

```bash
sudo apt update && sudo apt upgrade
```

O Windows não atualiza as distribuições do Linux nem faz upgrade delas automaticamente. Essa é uma tarefa que a maioria dos usuários do Linux prefere controlar por conta própria.

Aproveite o uso de sua nova distribuição do Linux no WSL!

## <a name="troubleshooting"></a>Solução de problemas

Veja abaixo os erros de instalação relacionados e as correções sugeridas. Consulte a [página de solução de problemas do WSL](troubleshooting.md) para ver outros erros comuns e suas soluções.

### <a name="installation-failed-with-error-0x8007007e"></a>Falha na instalação com o erro 0x8007007e

Esse erro ocorre quando o sistema não dá suporte ao Linux por meio da loja.  Certifique-se de que:

- Você está executando o Windows Build 16215 ou posterior. [Verifique seu build](troubleshooting.md#check-your-build-number).
- O componente opcional do Subsistema Windows para Linux está habilitado e o computador foi reiniciado.  [Verifique se o WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).

### <a name="installation-failed-with-error-0x80070003"></a>Falha na instalação com o erro 0x80070003

O Subsistema Windows para Linux é executado somente na unidade do sistema (normalmente, a unidade `C:`). Verifique se as distribuições estão armazenadas na unidade do sistema:

- Abra **Configurações** -> **Armazenamento** -> **Mais configurações de armazenamento: Alterar o local em que o novo conteúdo é salvo**
  
    ![Imagem das configurações do sistema para instalar aplicativos na unidade C:](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a>Falha de WslRegisterDistribution com o erro 0x8007019e

O componente opcional do Subsistema Windows para Linux não está habilitado:

- Abra **Painel de Controle** -> **Programas e Recursos** -> **Ativar ou desativar recursos do Windows** -> marque **Subsistema Windows para Linux** ou use o cmdlet do PowerShell mencionado no início deste artigo.
