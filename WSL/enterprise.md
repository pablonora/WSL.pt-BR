---
title: Subsistema do Windows para Linux for Enterprise
description: Recursos e instruções sobre como fazer o melhor usam o subsistema Windows para Linux em um ambiente corporativo.
keywords: Instalar o BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, enterprise, implantação, offline, empacotamento, armazenamento, distribuição, instalação,
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063274"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="e3c06-104">Subsistema do Windows para Linux for Enterprise</span><span class="sxs-lookup"><span data-stu-id="e3c06-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="e3c06-105">A Microsoft Store para empresas oferece uma variedade de soluções para empresas que desejam implantar WSL em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="e3c06-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="e3c06-106">O [documentos online](https://docs.microsoft.com/en-us/microsoft-store/) para a Microsoft Store para empresas são um ótimo recurso para obter informações gerais sobre a experiência de Store.</span><span class="sxs-lookup"><span data-stu-id="e3c06-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="e3c06-107">Se você é uma empresa que está apenas procurando para obter backup para iniciar a implantação WSL você pode seguir estas etapas, que são explicadas dentro de documentos do Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="e3c06-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="e3c06-108">Inscreva-se para a Microsoft Store para empresas e começar</span><span class="sxs-lookup"><span data-stu-id="e3c06-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="e3c06-109">[Gerenciar seus produtos e serviços (incluindo quem pode acessar quais aplicativos no seu repositório privado)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="e3c06-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="e3c06-110">Aqui você pode adicionar WSL distribuições para seu repositório e controlar quem pode instalá-los</span><span class="sxs-lookup"><span data-stu-id="e3c06-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="e3c06-111">Usar um método de distribuição de sua escolha para implantar o software em sua empresa</span><span class="sxs-lookup"><span data-stu-id="e3c06-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="e3c06-112">Comunicar-se aos usuários que têm acesso a distribuições WSL que eles podem [usar estas etapas](https://docs.microsoft.com/en-us/windows/wsl/install-win10) para instalar a distribuição ou distribuições de sua preferência</span><span class="sxs-lookup"><span data-stu-id="e3c06-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="e3c06-113">Como distribuir uma distribuição Offline</span><span class="sxs-lookup"><span data-stu-id="e3c06-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="e3c06-114">Se os computadores em sua empresa não tiverem acesso para a Microsoft Store ou o Microsoft Store para empresas, em seguida, você pode baixar o instalador de uma distribuição do Linux que tenha uma licença offline seguindo estas etapas.</span><span class="sxs-lookup"><span data-stu-id="e3c06-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="e3c06-115">Configurar uma conta do Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="e3c06-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="e3c06-116">Você precisa ter uma conta do AD do Azure e ser o administrador global para sua organização para obter o instalador de aplicativos da Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="e3c06-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="e3c06-117">Se você já tiver uma conta, você pode ignorar esta etapa.</span><span class="sxs-lookup"><span data-stu-id="e3c06-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="e3c06-118">As instruções para registrar uma conta podem ser encontradas aqui: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="e3c06-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="e3c06-119">Entre na Store para empresas e vá para a home page</span><span class="sxs-lookup"><span data-stu-id="e3c06-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="e3c06-120">Entre aqui: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="e3c06-120">Sign in here: www.microsoft.com/business-store</span></span>

![MS Store para a home page comercial](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="e3c06-122">Vá para gerenciar -> configurações e habilitar 'Mostrar aplicativos offline'</span><span class="sxs-lookup"><span data-stu-id="e3c06-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![MS Store para a página de configurações de negócios](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="e3c06-124">Volte à página principal, clicando em 'Comprar meu grupo'</span><span class="sxs-lookup"><span data-stu-id="e3c06-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![MS Store para a home page comercial](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="e3c06-126">Pesquisar sua distribuição desejada e selecioná-lo</span><span class="sxs-lookup"><span data-stu-id="e3c06-126">Search for your desired distro and select it</span></span>

![MS Store para a home page comercial, com a pesquisa do Active Directory](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="e3c06-128">Selecione uma licença de 'Offline' no menu de lista suspensa de tipo de licença e clique em 'Obter o aplicativo'</span><span class="sxs-lookup"><span data-stu-id="e3c06-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![MS Store para a página de produto do Ubuntu de negócios](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="e3c06-130">Observação: algumas distribuições podem optar por não ter uma licença offline</span><span class="sxs-lookup"><span data-stu-id="e3c06-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="e3c06-131">Clique no botão 'Gerenciar' para chegar à página de produto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3c06-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![MS Store para a página de produto do Ubuntu de negócios](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="e3c06-133">Selecione sua arquitetura e baixe o pacote para uso offline</span><span class="sxs-lookup"><span data-stu-id="e3c06-133">Select your architecture and download the package for offline use</span></span>

![MS Store para a página de detalhes do produto comercial Ubuntu](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="e3c06-135">Esse instalador, em seguida, pode ser distribuído em qualquer computador onde você deseja instalar o WSL.</span><span class="sxs-lookup"><span data-stu-id="e3c06-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>