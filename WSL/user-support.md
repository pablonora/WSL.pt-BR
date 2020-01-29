---
title: Criar e atualizar contas de usuário para distribuições do WSL
description: Referência para contas de usuário e gerenciamento de permissões com o Subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, user accounts
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 85bd8f05d041181c2cfb16f6fb55aaeea15b332c
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520575"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a><span data-ttu-id="2dc9f-104">Criar e atualizar contas de usuário para distribuições do WSL</span><span class="sxs-lookup"><span data-stu-id="2dc9f-104">Create and update user accounts for WSL distributions</span></span>

<span data-ttu-id="2dc9f-105">Depois que você habilitar o WSL e instalar uma distribuição do Linux da Microsoft Store, a primeira etapa que será solicitada ao abrir sua distribuição do Linux recém-instalada será a criação de uma conta, incluindo um **nome de usuário** e **senha**.</span><span class="sxs-lookup"><span data-stu-id="2dc9f-105">Once you have enabled WSL and installed a Linux distribution from the Microsoft Store, the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="2dc9f-106">O **nome de usuário** e a **senha** são específicos da sua distribuição do Linux e não têm nenhuma influência sobre seu nome de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="2dc9f-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="2dc9f-107">Depois de criar o **nome de usuário** e a **senha**, a conta será o usuário padrão para a distribuição e entrará automaticamente na inicialização.</span><span class="sxs-lookup"><span data-stu-id="2dc9f-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="2dc9f-108">Essa conta será considerada o administrador do Linux, com a capacidade de executar comandos administrativos `sudo` (Super User Do).</span><span class="sxs-lookup"><span data-stu-id="2dc9f-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="2dc9f-109">Cada distribuição do Linux em execução no Subsistema Windows para Linux tem suas próprias contas de usuário e senhas do Linux.</span><span class="sxs-lookup"><span data-stu-id="2dc9f-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="2dc9f-110">Você precisará configurar uma conta de usuário do Linux sempre que adicionar uma distribuição, reinstalação ou redefinição.</span><span class="sxs-lookup"><span data-stu-id="2dc9f-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="2dc9f-111">Redefinir sua senha do Linux</span><span class="sxs-lookup"><span data-stu-id="2dc9f-111">Reset your Linux password</span></span>

<span data-ttu-id="2dc9f-112">Para alterar sua senha, abra a distribuição do Linux (Ubuntu, por exemplo) e insira o comando: `passwd`</span><span class="sxs-lookup"><span data-stu-id="2dc9f-112">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="2dc9f-113">Você será solicitado a inserir a senha atual, inserir a nova senha e, em seguida, confirmar a nova senha.</span><span class="sxs-lookup"><span data-stu-id="2dc9f-113">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

### <a name="forgot-your-password"></a><span data-ttu-id="2dc9f-114">Esqueceu sua senha</span><span class="sxs-lookup"><span data-stu-id="2dc9f-114">Forgot your password</span></span>

<span data-ttu-id="2dc9f-115">Se você esqueceu a senha da sua distribuição do Linux:</span><span class="sxs-lookup"><span data-stu-id="2dc9f-115">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="2dc9f-116">Abra o PowerShell e insira a raiz da distribuição do WSL padrão usando o comando: `wsl -u root`</span><span class="sxs-lookup"><span data-stu-id="2dc9f-116">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

<span data-ttu-id="2dc9f-117">Se você precisa atualizar a senha que foi esquecida em uma distribuição que não seja a padrão, use o comando: `wsl -d Debian -u root`, substituindo `Debian` pelo nome da sua distribuição de destino.</span><span class="sxs-lookup"><span data-stu-id="2dc9f-117">-- If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="2dc9f-118">Depois que a distribuição do WSL tiver sido aberta no nível raiz dentro do PowerShell, você poderá usar esse comando para atualizar a senha: `passwd`</span><span class="sxs-lookup"><span data-stu-id="2dc9f-118">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="2dc9f-119">Você será solicitado a inserir uma nova senha do UNIX e, em seguida, confirmar essa senha.</span><span class="sxs-lookup"><span data-stu-id="2dc9f-119">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="2dc9f-120">Depois da informação de que a senha foi atualizada com êxito, feche o WSL dentro do PowerShell usando o comando: `exit`</span><span class="sxs-lookup"><span data-stu-id="2dc9f-120">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="2dc9f-121">Se você está executando uma versão anterior do sistema operacional Windows, como a 1703 (Atualização do Windows 10 para Criadores) ou a 1709 (Windows 10 Fall Creators Update), consulte a [versão arquivada deste documento de atualização de conta de usuário](./user-support-archived.md).</span><span class="sxs-lookup"><span data-stu-id="2dc9f-121">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
