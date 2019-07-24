---
title: Subsistema do Windows para Linux for Enterprise
description: Recursos e instruções sobre como usar melhor o subsistema do Windows para Linux em um ambiente corporativo.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10, Enterprise, implantação, offline, empacotamento, armazenamento, distribuição, instalação, instalar
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2019
ms.locfileid: "59063274"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="ac6a3-104">Subsistema do Windows para Linux for Enterprise</span><span class="sxs-lookup"><span data-stu-id="ac6a3-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="ac6a3-105">O Microsoft Store for Business oferece uma variedade de soluções para empresas que desejam implantar o WSL em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="ac6a3-106">Os [documentos online](https://docs.microsoft.com/en-us/microsoft-store/) do Microsoft Store for Business são um excelente recurso para descobrir informações gerais sobre a experiência de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="ac6a3-107">Se você é uma empresa que está apenas procurando ser configurada para iniciar a implantação do WSL, você pode seguir estas etapas, que são explicadas dentro do Microsoft Store docs:</span><span class="sxs-lookup"><span data-stu-id="ac6a3-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="ac6a3-108">Inscreva-se no Microsoft Store for Business e comece</span><span class="sxs-lookup"><span data-stu-id="ac6a3-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="ac6a3-109">[Gerencie seus produtos e serviços (incluindo quem pode acessar quais aplicativos em seu armazenamento privado)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="ac6a3-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="ac6a3-110">Aqui você pode adicionar WSL distribuições ao seu armazenamento e controlar quem pode instalá-los</span><span class="sxs-lookup"><span data-stu-id="ac6a3-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="ac6a3-111">Use um método de distribuição de sua escolha para implantar o software em sua empresa</span><span class="sxs-lookup"><span data-stu-id="ac6a3-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="ac6a3-112">Comunique-se aos usuários que têm acesso ao WSL distribuições de que eles podem [usar essas etapas](https://docs.microsoft.com/en-us/windows/wsl/install-win10) para instalar o distribuição ou o distribuições de sua escolha</span><span class="sxs-lookup"><span data-stu-id="ac6a3-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="ac6a3-113">Como distribuir um distribuição offline</span><span class="sxs-lookup"><span data-stu-id="ac6a3-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="ac6a3-114">Se os computadores em sua empresa não tiverem acesso ao Microsoft Store ou ao Microsoft Store for Business, você poderá baixar o instalador de um distribuição do Linux que tenha uma licença offline seguindo estas etapas.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="ac6a3-115">Configurar uma conta do Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="ac6a3-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="ac6a3-116">Você precisa ter uma conta do Azure AD e ser o administrador global da sua organização para obter o instalador de aplicativos Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="ac6a3-117">Se você já tiver uma conta, poderá ignorar esta etapa.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="ac6a3-118">As instruções para registrar uma conta podem ser encontradas aqui: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="ac6a3-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="ac6a3-119">Entre na loja para empresas e vá para a Home Page</span><span class="sxs-lookup"><span data-stu-id="ac6a3-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="ac6a3-120">Entre aqui: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="ac6a3-120">Sign in here: www.microsoft.com/business-store</span></span>

![home page da MS Store para empresas](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="ac6a3-122">Vá para configurações de gerenciamento-> e habilite ' Mostrar aplicativos offline '</span><span class="sxs-lookup"><span data-stu-id="ac6a3-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![Página de configurações da MS Store para empresas](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="ac6a3-124">Volte para a página principal clicando em ' comprar para o meu grupo '</span><span class="sxs-lookup"><span data-stu-id="ac6a3-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![home page da MS Store para empresas](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="ac6a3-126">Pesquise o distribuição desejado e selecione-o</span><span class="sxs-lookup"><span data-stu-id="ac6a3-126">Search for your desired distro and select it</span></span>

![home page MS Store para empresas com a pesquisa ativa](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="ac6a3-128">Selecione uma licença ' offline ' no menu suspenso tipo de licença e clique em ' obter o aplicativo '</span><span class="sxs-lookup"><span data-stu-id="ac6a3-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![Página de produtos da MS Store para empresas Ubuntu](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="ac6a3-130">Observação: algumas distribuições podem optar por não ter uma licença offline</span><span class="sxs-lookup"><span data-stu-id="ac6a3-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="ac6a3-131">Clique no botão ' Gerenciar ' para acessar a página do produto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="ac6a3-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![Página de produtos da MS Store para empresas Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="ac6a3-133">Selecione sua arquitetura e baixe o pacote para uso offline</span><span class="sxs-lookup"><span data-stu-id="ac6a3-133">Select your architecture and download the package for offline use</span></span>

![Página de detalhes do produto MS Store para empresas Ubuntu](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="ac6a3-135">Esse instalador pode ser distribuído para qualquer computador em que você queira instalar o WSL.</span><span class="sxs-lookup"><span data-stu-id="ac6a3-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>