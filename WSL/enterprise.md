---
title: Subsistema do Windows para Linux for Enterprise
description: Recursos e instruções sobre como usar melhor o subsistema do Windows para Linux em um ambiente corporativo.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10, Enterprise, implantação, offline, empacotamento, armazenamento, distribuição, instalação, instalar
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: c32d62267c77d87fb200cfe43b8e6f43b4e3a56d
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269856"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Subsistema do Windows para Linux for Enterprise

O Microsoft Store for Business oferece uma variedade de soluções para empresas que desejam implantar o WSL em sua empresa. Os [documentos online](https://docs.microsoft.com/en-us/microsoft-store/) do Microsoft Store for Business são um excelente recurso para descobrir informações gerais sobre a experiência de armazenamento.

Se você é uma empresa que está apenas procurando ser configurada para iniciar a implantação do WSL, você pode seguir estas etapas, que são explicadas dentro do Microsoft Store docs:

* [Inscreva-se no Microsoft Store for Business e comece](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Gerencie seus produtos e serviços (incluindo quem pode acessar quais aplicativos em seu armazenamento privado)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). Aqui você pode adicionar WSL distribuições ao seu armazenamento e controlar quem pode instalá-los
* [Use um método de distribuição de sua escolha para implantar o software em sua empresa](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Comunique-se aos usuários que têm acesso ao WSL distribuições de que eles podem [usar essas etapas](https://docs.microsoft.com/en-us/windows/wsl/install-win10) para instalar o distribuição ou o distribuições de sua escolha 

## <a name="how-to-distribute-a-distro-offline"></a>Como distribuir um distribuição offline

Se os computadores em sua empresa não tiverem acesso ao Microsoft Store ou ao Microsoft Store for Business, você poderá baixar o instalador de um distribuição do Linux que tenha uma licença offline seguindo estas etapas. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Configurar uma conta do Azure Active Directory (AD) 

Você precisa ter uma conta do Azure AD e ser o administrador global da sua organização para obter o instalador de aplicativos Microsoft Store. Se você já tiver uma conta, poderá ignorar esta etapa.

As instruções para registrar uma conta podem ser encontradas aqui: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>Entre na loja para empresas e vá para a Home Page
Entre aqui: www.microsoft.com/business-store

![home page da MS Store para empresas](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>Vá para configurações de gerenciamento-> e habilite ' Mostrar aplicativos offline '

![Página de configurações da MS Store para empresas](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>Volte para a página principal clicando em ' comprar para o meu grupo '

![home page da MS Store para empresas](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>Pesquise o distribuição desejado e selecione-o

![home page MS Store para empresas com a pesquisa ativa](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>Selecione uma licença ' offline ' no menu suspenso tipo de licença e clique em ' obter o aplicativo '

![Página de produtos da MS Store para empresas Ubuntu](media/offlineinstallscreens/4-screen.png)

Observação: algumas distribuições podem optar por não ter uma licença offline

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>Clique no botão ' Gerenciar ' para acessar a página do produto do aplicativo

![Página de produtos da MS Store para empresas Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>Selecione sua arquitetura e baixe o pacote para uso offline

![Página de detalhes do produto MS Store para empresas Ubuntu](media/offlineinstallscreens/6-screen.png)

Esse instalador pode ser distribuído para qualquer computador em que você queira instalar o WSL.