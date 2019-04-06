---
title: Permissões e a conta de usuário do Linux
description: Referência para contas de usuário e gerenciamento de permissões com o subsistema do Windows para Linux.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu, contas de usuário
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063594"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="2548b-104">Contas de usuário e as permissões de subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="2548b-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="2548b-105">Criação de seu usuário do Linux é a primeira etapa na configuração de uma nova distribuição do Linux no WSL.</span><span class="sxs-lookup"><span data-stu-id="2548b-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="2548b-106">A primeira conta de usuário criada é configurada automaticamente com alguns atributos especiais:</span><span class="sxs-lookup"><span data-stu-id="2548b-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="2548b-107">É o usuário padrão, ele entrar automaticamente na inicialização.</span><span class="sxs-lookup"><span data-stu-id="2548b-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="2548b-108">É administrador do Linux (um membro do grupo sudo) por padrão.</span><span class="sxs-lookup"><span data-stu-id="2548b-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="2548b-109">Cada distribuição do Linux em execução no subsistema do Windows para Linux tem seu próprio Linux contas de usuário e senhas.</span><span class="sxs-lookup"><span data-stu-id="2548b-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="2548b-110">Você precisará configurar uma conta de usuário do Linux sempre que você adicionar uma distribuição, reinstale ou redefinir.</span><span class="sxs-lookup"><span data-stu-id="2548b-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="2548b-111">Contas de usuário do Linux não são apenas independentes por distribuição, eles também são independentes da sua conta de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="2548b-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="2548b-112">Redefinir sua senha do Linux</span><span class="sxs-lookup"><span data-stu-id="2548b-112">Resetting your Linux password</span></span>

<span data-ttu-id="2548b-113">Se você tiver acesso à sua conta de usuário do Linux e sabe sua senha atual, alterá-lo usando o Linux de redefinição de senha ferramentas dessa distribuição – provavelmente `passwd`.</span><span class="sxs-lookup"><span data-stu-id="2548b-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="2548b-114">Se isso for não é uma opção, dependendo da distribuição, você poderá redefinir sua senha, redefinindo o usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="2548b-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="2548b-115">WSL oferece logs de uma marca de usuário padrão para identificar qual conta de usuário automaticamente no, quando você inicia um WSL.</span><span class="sxs-lookup"><span data-stu-id="2548b-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="2548b-116">Como várias distribuições incluem comandos para definir o usuário padrão como raiz e também um usuário raiz com nenhuma senha definida, alterar o usuário padrão para a raiz é uma ferramenta útil para coisas como a redefinição de senha.</span><span class="sxs-lookup"><span data-stu-id="2548b-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="2548b-117">Para a atualização para criadores e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="2548b-117">For Creators Update and earlier</span></span>
<span data-ttu-id="2548b-118">Se você estiver executando o Windows 10 Creators update ou versões anteriores, você pode alterar o usuário de Bash padrão executando os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="2548b-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="2548b-119">Alterar o usuário padrão para `root`:</span><span class="sxs-lookup"><span data-stu-id="2548b-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="2548b-120">Execute `bash.exe` fazer logon agora como `root`:</span><span class="sxs-lookup"><span data-stu-id="2548b-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="2548b-121">Redefinir sua senha usando o comando de senha de distribuição e feche o Console do Linux:</span><span class="sxs-lookup"><span data-stu-id="2548b-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="2548b-122">No Windows CMD, redefina seu usuário padrão para sua conta de usuário normal do Linux:</span><span class="sxs-lookup"><span data-stu-id="2548b-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="2548b-123">Para o Fall Creators Update e posterior</span><span class="sxs-lookup"><span data-stu-id="2548b-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="2548b-124">Para ver quais comandos estão disponíveis para uma distribuição específica, execute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="2548b-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="2548b-125">Por exemplo, com o Ubuntu instalado:</span><span class="sxs-lookup"><span data-stu-id="2548b-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="2548b-126">Etapa de instruções passo a passo usando o Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="2548b-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="2548b-127">Abra o CMD</span><span class="sxs-lookup"><span data-stu-id="2548b-127">Open CMD</span></span>
1. <span data-ttu-id="2548b-128">Defina o usuário padrão do Linux como `root`:</span><span class="sxs-lookup"><span data-stu-id="2548b-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="2548b-129">Inicie sua distribuição do Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="2548b-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="2548b-130">Você será automaticamente fazer logon como `root`:</span><span class="sxs-lookup"><span data-stu-id="2548b-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="2548b-131">Redefinir sua senha usando o `passwd` comando:</span><span class="sxs-lookup"><span data-stu-id="2548b-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="2548b-132">No Windows CMD, redefina seu usuário padrão para sua conta de usuário normal do Linux.</span><span class="sxs-lookup"><span data-stu-id="2548b-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="2548b-133">Permissões</span><span class="sxs-lookup"><span data-stu-id="2548b-133">Permissions</span></span>

<span data-ttu-id="2548b-134">Há dois conceitos importantes para ter em mente quando se trata de permissões no WSL:</span><span class="sxs-lookup"><span data-stu-id="2548b-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="2548b-135">O modelo de permissão do Windows controla os direitos de um processo para recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="2548b-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="2548b-136">O modelo de permissão de Linux controla os direitos de um processo de recursos do Linux</span><span class="sxs-lookup"><span data-stu-id="2548b-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="2548b-137">Ao executar o Linux em WSL, Linux terão as mesmas permissões do Windows que o processo que inicia a ele.</span><span class="sxs-lookup"><span data-stu-id="2548b-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="2548b-138">Linux pode ser iniciado em um dos dois níveis de permissão:</span><span class="sxs-lookup"><span data-stu-id="2548b-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="2548b-139">Normal (não elevada): Executa o Linux com as permissões do usuário conectado</span><span class="sxs-lookup"><span data-stu-id="2548b-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="2548b-140">Administrador/privilégios elevados: Executa o Linux com as permissões do administrador com privilégios elevados/Windows</span><span class="sxs-lookup"><span data-stu-id="2548b-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="2548b-141">Porque que elevados processos podem alterar/danos dados e configurações do sistema e podem acesso/Modificar protegidos de arquivos e pastas, **Evite** iniciando elevados processos, a menos que você tenha que absolutamente - se eles estão Windows ou Linux aplicativos/tools/shells!</span><span class="sxs-lookup"><span data-stu-id="2548b-141">Because that elevated processes can change/damage system-wide settings and data, and can access/modify protected files and folders, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="2548b-142">As permissões do Windows acima são independentes das permissões dentro de uma instância do Linux: Linux "privilégios de raiz" afetam apenas os direitos do usuário dentro do ambiente Linux & sistema de arquivos; eles não têm impacto sobre os privilégios do Windows concedidos.</span><span class="sxs-lookup"><span data-stu-id="2548b-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="2548b-143">Assim, executar um processo de Linux como raiz (por exemplo, via `sudo`) apenas concede que processam os direitos de administrador no ambiente do Linux.</span><span class="sxs-lookup"><span data-stu-id="2548b-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

**<span data-ttu-id="2548b-144">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="2548b-144">Example:</span></span>**    
<span data-ttu-id="2548b-145">Uma sessão de Bash com privilégios de administrador do Windows pode acessar `cd /mnt/c/Users/Administrator` enquanto uma sessão Bash sem privilégios de administrador vê um erro "Permissão negada".</span><span class="sxs-lookup"><span data-stu-id="2548b-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="2548b-146">No Linux, digitando `sudo cd /mnt/c/Users/Administrator` não concederá acesso ao diretório do administrador, pois as permissões no Windows são gerenciadas pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="2548b-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="2548b-147">O modelo de permissão do Linux é importante quando se está dentro do ambiente do Linux no qual o usuário tem permissões com base no usuário Linux atual.</span><span class="sxs-lookup"><span data-stu-id="2548b-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

**<span data-ttu-id="2548b-148">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="2548b-148">Example:</span></span>**  
<span data-ttu-id="2548b-149">Pode ser executado por um usuário no grupo sudo `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="2548b-149">A user in the sudo group may run `sudo apt update`.</span></span>
