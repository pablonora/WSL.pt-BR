---
title: Conta de usuário e permissões do Linux
description: Referência para contas de usuário e gerenciamento de permissões com o subsistema do Windows para Linux.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema do Windows para Linux, windowssubsystem, Ubuntu, contas de usuário
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040828"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="4df6b-104">Contas de usuário e permissões para o subsistema do Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="4df6b-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="4df6b-105">A criação de seu usuário do Linux é a primeira etapa na configuração de uma nova distribuição do Linux no WSL.</span><span class="sxs-lookup"><span data-stu-id="4df6b-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="4df6b-106">A primeira conta de usuário criada é automaticamente configurada com alguns atributos especiais:</span><span class="sxs-lookup"><span data-stu-id="4df6b-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="4df6b-107">É o usuário padrão--ele entra automaticamente na inicialização.</span><span class="sxs-lookup"><span data-stu-id="4df6b-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="4df6b-108">É administrador do Linux (um membro do grupo sudo) por padrão.</span><span class="sxs-lookup"><span data-stu-id="4df6b-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="4df6b-109">Cada distribuição do Linux em execução no subsistema do Windows para Linux tem suas próprias contas de usuário e senhas do Linux.</span><span class="sxs-lookup"><span data-stu-id="4df6b-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="4df6b-110">Você precisará configurar uma conta de usuário do Linux sempre que adicionar uma distribuição, reinstalação ou redefinição.</span><span class="sxs-lookup"><span data-stu-id="4df6b-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="4df6b-111">As contas de usuário do Linux não são apenas independentes por distribuição, elas também são independentes da sua conta de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="4df6b-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="4df6b-112">Redefinindo sua senha do Linux</span><span class="sxs-lookup"><span data-stu-id="4df6b-112">Resetting your Linux password</span></span>

<span data-ttu-id="4df6b-113">Se você tiver acesso à sua conta de usuário do Linux e souber sua senha atual, altere-a usando as ferramentas de redefinição de senha do `passwd`Linux dessa distribuição-provavelmente.</span><span class="sxs-lookup"><span data-stu-id="4df6b-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="4df6b-114">Se essa não for uma opção, dependendo da distribuição, talvez seja possível redefinir sua senha redefinindo o usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="4df6b-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="4df6b-115">O WSL oferece uma marca de usuário padrão para identificar qual conta de usuário faz logon automaticamente quando você inicia um WSL.</span><span class="sxs-lookup"><span data-stu-id="4df6b-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="4df6b-116">Como muitas distribuições incluem comandos para definir o usuário padrão como root e também um usuário raiz sem senha definida, alterar o usuário padrão para root é uma ferramenta útil para coisas como a redefinição de senha.</span><span class="sxs-lookup"><span data-stu-id="4df6b-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="4df6b-117">Para a atualização do Creators e anterior</span><span class="sxs-lookup"><span data-stu-id="4df6b-117">For Creators Update and earlier</span></span>
<span data-ttu-id="4df6b-118">Se você estiver executando a atualização do Windows 10 para criadores ou anterior, poderá alterar o usuário bash padrão executando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="4df6b-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="4df6b-119">Altere o usuário padrão para `root`:</span><span class="sxs-lookup"><span data-stu-id="4df6b-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="4df6b-120">Executar `bash.exe` agora fazer logon como `root`:</span><span class="sxs-lookup"><span data-stu-id="4df6b-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="4df6b-121">Redefina sua senha usando o comando de senha da distribuição e feche o console do Linux:</span><span class="sxs-lookup"><span data-stu-id="4df6b-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="4df6b-122">No Windows CMD, redefina o usuário padrão de volta para sua conta de usuário Linux normal:</span><span class="sxs-lookup"><span data-stu-id="4df6b-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="4df6b-123">Para a atualização de criadores de outono e posterior</span><span class="sxs-lookup"><span data-stu-id="4df6b-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="4df6b-124">Para ver quais comandos estão disponíveis para uma determinada distribuição, execute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="4df6b-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="4df6b-125">Por exemplo, com o Ubuntu instalado:</span><span class="sxs-lookup"><span data-stu-id="4df6b-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="4df6b-126">Instruções passo a passo usando o Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="4df6b-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="4df6b-127">Abrir CMD</span><span class="sxs-lookup"><span data-stu-id="4df6b-127">Open CMD</span></span>
1. <span data-ttu-id="4df6b-128">Defina o usuário padrão do Linux `root`como:</span><span class="sxs-lookup"><span data-stu-id="4df6b-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="4df6b-129">Inicie sua distribuição do Linux`ubuntu`().</span><span class="sxs-lookup"><span data-stu-id="4df6b-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="4df6b-130">Você fará logon automaticamente como `root`:</span><span class="sxs-lookup"><span data-stu-id="4df6b-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="4df6b-131">Redefina sua senha usando `passwd` o comando:</span><span class="sxs-lookup"><span data-stu-id="4df6b-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="4df6b-132">No Windows CMD, redefina o usuário padrão de volta para sua conta de usuário normal do Linux.</span><span class="sxs-lookup"><span data-stu-id="4df6b-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="4df6b-133">Permissões</span><span class="sxs-lookup"><span data-stu-id="4df6b-133">Permissions</span></span>

<span data-ttu-id="4df6b-134">Há dois conceitos importantes a ter em mente quando se trata de permissões em WSL:</span><span class="sxs-lookup"><span data-stu-id="4df6b-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="4df6b-135">O modelo de permissão do Windows governa os direitos de um processo para recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="4df6b-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="4df6b-136">O modelo de permissão do Linux controla os direitos de um processo para recursos do Linux</span><span class="sxs-lookup"><span data-stu-id="4df6b-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="4df6b-137">Ao executar o Linux no WSL, o Linux terá as mesmas permissões do Windows que o processo que o inicia.</span><span class="sxs-lookup"><span data-stu-id="4df6b-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="4df6b-138">O Linux pode ser iniciado em um dos dois níveis de permissão:</span><span class="sxs-lookup"><span data-stu-id="4df6b-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="4df6b-139">Normal (não elevado): O Linux é executado com as permissões do usuário conectado</span><span class="sxs-lookup"><span data-stu-id="4df6b-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="4df6b-140">Elevado/administrador: O Linux é executado com permissões elevadas/administrativas do Windows</span><span class="sxs-lookup"><span data-stu-id="4df6b-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="4df6b-141">Como processos elevados podem acessar/modificar (e, portanto, danificar) configurações de todo o sistema e dados protegidos em todo o sistema, **Evite** iniciar processos elevados, a menos que você tenha certeza de que eles são aplicativos/ferramentas do Windows ou Linux/ concha!</span><span class="sxs-lookup"><span data-stu-id="4df6b-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="4df6b-142">As permissões acima do Windows são independentes das permissões em uma instância do Linux: Os "privilégios raiz" do Linux só afetam os direitos do usuário no ambiente Linux & FileSystem; Eles não têm nenhum impacto sobre os privilégios do Windows concedidos.</span><span class="sxs-lookup"><span data-stu-id="4df6b-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="4df6b-143">Portanto, a execução de um processo do Linux como raiz ( `sudo`por exemplo, via) concede apenas os direitos de administrador do processo no ambiente Linux.</span><span class="sxs-lookup"><span data-stu-id="4df6b-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="4df6b-144">**Exemplo:**   </span><span class="sxs-lookup"><span data-stu-id="4df6b-144">**Example:**  </span></span>  
<span data-ttu-id="4df6b-145">Uma sessão de bash com privilégios de administrador do `cd /mnt/c/Users/Administrator` Windows pode acessar enquanto uma sessão de bash sem privilégios de administrador veria um erro de "permissão negada".</span><span class="sxs-lookup"><span data-stu-id="4df6b-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="4df6b-146">No Linux, a `sudo cd /mnt/c/Users/Administrator` digitação não concederá acesso ao diretório do administrador, pois as permissões no Windows são gerenciadas pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="4df6b-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="4df6b-147">O modelo de permissão do Linux é importante quando estiver dentro do ambiente Linux em que o usuário tem permissões baseadas no usuário atual do Linux.</span><span class="sxs-lookup"><span data-stu-id="4df6b-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="4df6b-148">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="4df6b-148">**Example:**</span></span>  
<span data-ttu-id="4df6b-149">Um usuário no grupo sudo pode ser executado `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="4df6b-149">A user in the sudo group may run `sudo apt update`.</span></span>
