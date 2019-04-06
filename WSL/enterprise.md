---
title: Subsistema do Windows para Linux para a empresa
description: Recursos e instruções sobre como fazer o melhor usam o subsistema Windows para Linux em um ambiente corporativo.
keywords: Instalar o BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, enterprise, implantação, offline, empacotamento, armazenamento, distribuição, instalação,
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063274"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Subsistema do Windows para Linux para a empresa

A Microsoft Store para empresas oferece uma variedade de soluções para empresas que desejam implantar WSL em sua empresa. O [documentos online](https://docs.microsoft.com/en-us/microsoft-store/) para a Microsoft Store para empresas são um ótimo recurso para obter informações gerais sobre a experiência de Store.

Se você é uma empresa que está apenas procurando para obter backup para iniciar a implantação WSL você pode seguir estas etapas, que são explicadas dentro de documentos do Microsoft Store:

* [Inscreva-se para a Microsoft Store para empresas e começar](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Gerenciar seus produtos e serviços (incluindo quem pode acessar quais aplicativos no seu repositório privado)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). Aqui você pode adicionar WSL distribuições para seu repositório e controlar quem pode instalá-los
* [Usar um método de distribuição de sua escolha para implantar o software em sua empresa](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Comunicar-se aos usuários que têm acesso a distribuições WSL que eles podem [usar estas etapas](https://docs.microsoft.com/en-us/windows/wsl/install-win10) para instalar a distribuição ou distribuições de sua preferência 

## <a name="how-to-distribute-a-distro-offline"></a>Como distribuir uma distribuição Offline

Se os computadores em sua empresa não tiverem acesso para a Microsoft Store ou o Microsoft Store para empresas, em seguida, você pode baixar o instalador de uma distribuição do Linux que tenha uma licença offline seguindo estas etapas. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Configurar uma conta do Azure Active Directory (AD) 

Você precisa ter uma conta do AD do Azure e ser o administrador global para sua organização para obter o instalador de aplicativos da Microsoft Store. Se você já tiver uma conta, você pode ignorar esta etapa.

As instruções para registrar uma conta podem ser encontradas aqui: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>Entre na Store para empresas e vá para a home page
Entre aqui: www.microsoft.com/business-store

![MS Store para a home page comercial](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>Vá para gerenciar -> configurações e habilitar 'Mostrar aplicativos offline'

![MS Store para a página de configurações de negócios](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>Volte à página principal, clicando em 'Comprar meu grupo'

![MS Store para a home page comercial](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>Pesquisar sua distribuição desejada e selecioná-lo

![MS Store para a home page comercial, com a pesquisa do Active Directory](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>Selecione uma licença de 'Offline' no menu de lista suspensa de tipo de licença e clique em 'Obter o aplicativo'

![MS Store para a página de produto do Ubuntu de negócios](media/offlineinstallscreens/4-screen.png)

Observação: algumas distribuições podem optar por não ter uma licença offline

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>Clique no botão 'Gerenciar' para chegar à página de produto do aplicativo

![MS Store para a página de produto do Ubuntu de negócios](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>Selecione sua arquitetura e baixe o pacote para uso offline

![MS Store para a página de detalhes do produto comercial Ubuntu](media/offlineinstallscreens/6-screen.png)

Esse instalador, em seguida, pode ser distribuído em qualquer computador onde você deseja instalar o WSL.