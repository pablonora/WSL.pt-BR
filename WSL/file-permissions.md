---
title: Permissões de arquivo
description: Compreendendo como o WSL determina as permissões de arquivo no Windows
keywords: BashOnWindows, Bash, WSL, wsl2, Windows, subsistema do Windows para Linux, windowssubsystem, Ubuntu, Debian, Suse, Windows 10, arquivo, permissões
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520855"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="daf75-104">Permissões de arquivo para WSL</span><span class="sxs-lookup"><span data-stu-id="daf75-104">File Permissions for WSL</span></span>

<span data-ttu-id="daf75-105">Esta página detalha como as permissões de arquivo do Linux são interpretadas no subsistema do Windows para Linux, especialmente ao acessar recursos dentro do Windows no sistema de arquivos NT.</span><span class="sxs-lookup"><span data-stu-id="daf75-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="daf75-106">Esta documentação pressupõe uma compreensão básica da [estrutura de permissões do sistema de arquivos do Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span><span class="sxs-lookup"><span data-stu-id="daf75-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span></span> <!--TODO: Double check that it's okay to add these links--> <span data-ttu-id="daf75-107">e o [comando umask](https://en.wikipedia.org/wiki/Umask).</span><span class="sxs-lookup"><span data-stu-id="daf75-107">and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="daf75-108">Ao acessar arquivos do Windows do WSL, as permissões de arquivo são calculadas a partir de permissões do Windows ou são lidas de metadados que foram adicionados ao arquivo pelo WSL.</span><span class="sxs-lookup"><span data-stu-id="daf75-108">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="daf75-109">Esses metadados não são habilitados por padrão.</span><span class="sxs-lookup"><span data-stu-id="daf75-109">This metadata is not enabled by default.</span></span> 

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="daf75-110">Metadados do WSL em arquivos do Windows</span><span class="sxs-lookup"><span data-stu-id="daf75-110">WSL metadata on Windows files</span></span>

<span data-ttu-id="daf75-111">Quando os metadados são habilitados como uma opção de montagem no WSL, os atributos estendidos em arquivos do Windows NT podem ser adicionados e interpretados para fornecer permissões do sistema de arquivos do Linux.</span><span class="sxs-lookup"><span data-stu-id="daf75-111">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span> 

<span data-ttu-id="daf75-112">WSL pode adicionar quatro atributos estendidos NTFS:</span><span class="sxs-lookup"><span data-stu-id="daf75-112">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="daf75-113">Nome do Atributo</span><span class="sxs-lookup"><span data-stu-id="daf75-113">Attribute Name</span></span> | <span data-ttu-id="daf75-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="daf75-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="daf75-115">$LXUID</span><span class="sxs-lookup"><span data-stu-id="daf75-115">$LXUID</span></span> | <span data-ttu-id="daf75-116">ID do proprietário do usuário</span><span class="sxs-lookup"><span data-stu-id="daf75-116">User Owner ID</span></span> |
| <span data-ttu-id="daf75-117">$LXGID</span><span class="sxs-lookup"><span data-stu-id="daf75-117">$LXGID</span></span> | <span data-ttu-id="daf75-118">ID do proprietário do grupo</span><span class="sxs-lookup"><span data-stu-id="daf75-118">Group Owner ID</span></span> |
| <span data-ttu-id="daf75-119">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="daf75-119">$LXMOD</span></span> | <span data-ttu-id="daf75-120">Modo de arquivo (a permissão de sistemas de arquivos é octal e o tipo, por exemplo: 0777)</span><span class="sxs-lookup"><span data-stu-id="daf75-120">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="daf75-121">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="daf75-121">$LXDEV</span></span> | <span data-ttu-id="daf75-122">Dispositivo, se for um arquivo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="daf75-122">Device, if it is a device file</span></span> |

<span data-ttu-id="daf75-123">Além disso, qualquer arquivo que não seja um arquivo ou diretório regular (por exemplo: symlinks, FIFOs, dispositivos de bloco, soquetes UNIX e dispositivos de caracteres) também tem um [ponto de nova análise](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)de NTFS.</span><span class="sxs-lookup"><span data-stu-id="daf75-123">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="daf75-124">Isso torna muito mais rápido determinar o tipo de arquivo em um determinado diretório sem precisar consultar seus atributos estendidos.</span><span class="sxs-lookup"><span data-stu-id="daf75-124">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span> 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a><span data-ttu-id="daf75-125">Cenários de acesso a arquivos</span><span class="sxs-lookup"><span data-stu-id="daf75-125">File Access Scenarios</span></span>

<span data-ttu-id="daf75-126">Abaixo está uma descrição de como as permissões são determinadas ao acessar arquivos de diferentes maneiras usando o subsistema do Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="daf75-126">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="daf75-127">Acessando arquivos no sistema de arquivos da unidade do Windows (DrvFS) do Linux</span><span class="sxs-lookup"><span data-stu-id="daf75-127">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="daf75-128">Esses cenários ocorrem quando você está acessando os arquivos do Windows do WSL, provavelmente por meio de `/mnt/c`.</span><span class="sxs-lookup"><span data-stu-id="daf75-128">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span> 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="daf75-129">Lendo permissões de arquivo de um arquivo existente do Windows</span><span class="sxs-lookup"><span data-stu-id="daf75-129">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="daf75-130">O resultado depende de se o arquivo já tem metadados existentes.</span><span class="sxs-lookup"><span data-stu-id="daf75-130">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="daf75-131">**O arquivo não tem metadados (padrão)**</span><span class="sxs-lookup"><span data-stu-id="daf75-131">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="daf75-132">Se o arquivo não tiver nenhum metadado associado a ele, converteremos as permissões efetivas do usuário do Windows para ler/gravar/executar bits e defini-los como o mesmo valor para usuário, grupo e outros.</span><span class="sxs-lookup"><span data-stu-id="daf75-132">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="daf75-133">Por exemplo, se sua conta de usuário do Windows tiver acesso de leitura e execução, mas sem acesso de gravação ao arquivo, isso será mostrado como `r-x` para usuário, grupo e outros.</span><span class="sxs-lookup"><span data-stu-id="daf75-133">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="daf75-134">Se o arquivo tiver o atributo ' somente leitura ' definido no Windows, não concederemos acesso de gravação no Linux.</span><span class="sxs-lookup"><span data-stu-id="daf75-134">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="daf75-135">O arquivo tem metadados</span><span class="sxs-lookup"><span data-stu-id="daf75-135">The file has metadata</span></span>

<span data-ttu-id="daf75-136">Se o arquivo tiver metadados presentes, basta usar esses valores de metadados em vez de converter as permissões efetivas do usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="daf75-136">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="daf75-137">Alterando permissões de arquivo em um arquivo existente do Windows usando chmod</span><span class="sxs-lookup"><span data-stu-id="daf75-137">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="daf75-138">O resultado depende de se o arquivo já tem metadados existentes.</span><span class="sxs-lookup"><span data-stu-id="daf75-138">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="daf75-139">**O arquivo não tem metadados (padrão)**</span><span class="sxs-lookup"><span data-stu-id="daf75-139">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="daf75-140">O chmod terá apenas um efeito, se você remover todos os atributos de gravação de um arquivo, o atributo ' somente leitura ' no arquivo do Windows será definido, pois esse é o mesmo comportamento que o CIFS (Common Internet File System), que é o cliente SMB (Server Message Block) no Linux.</span><span class="sxs-lookup"><span data-stu-id="daf75-140">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="daf75-141">O arquivo tem metadados</span><span class="sxs-lookup"><span data-stu-id="daf75-141">The file has metadata</span></span>

<span data-ttu-id="daf75-142">O chmod será alterado ou adicionará metadados dependendo dos metadados existentes do arquivo.</span><span class="sxs-lookup"><span data-stu-id="daf75-142">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="daf75-143">Tenha em mente que você não pode dar a si mesmo mais acesso do que o que tem no Windows, mesmo que os metadados indiquem que é o caso.</span><span class="sxs-lookup"><span data-stu-id="daf75-143">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="daf75-144">Por exemplo, você pode definir os metadados para exibir que você tem permissões de gravação em um arquivo usando `chmod 777`, mas se você tentou acessar esse arquivo, ainda não conseguiria gravar nele.</span><span class="sxs-lookup"><span data-stu-id="daf75-144">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="daf75-145">Isso é graças à interoperabilidade, pois qualquer comando de leitura ou gravação para arquivos do Windows é roteado por meio de suas permissões de usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="daf75-145">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="daf75-146">Criando um arquivo no DriveFS</span><span class="sxs-lookup"><span data-stu-id="daf75-146">Creating a file in DriveFS</span></span>

<span data-ttu-id="daf75-147">O resultado depende de se os metadados estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="daf75-147">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="daf75-148">Os metadados não estão habilitados (padrão)</span><span class="sxs-lookup"><span data-stu-id="daf75-148">Metadata is not enabled (default)</span></span>

<span data-ttu-id="daf75-149">As permissões do Windows do arquivo recém-criado serão as mesmas que se você criou o arquivo no Windows sem um descritor de segurança específico, ele herdará as permissões do pai.</span><span class="sxs-lookup"><span data-stu-id="daf75-149">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span> 

##### <a name="metadata-is-enabled"></a><span data-ttu-id="daf75-150">Os metadados estão habilitados</span><span class="sxs-lookup"><span data-stu-id="daf75-150">Metadata is enabled</span></span>

<span data-ttu-id="daf75-151">Os bits de permissão do arquivo são definidos para seguir o umask do Linux e o arquivo será salvo com metadados.</span><span class="sxs-lookup"><span data-stu-id="daf75-151">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="daf75-152">Qual usuário do Linux e grupo do Linux possui o arquivo?</span><span class="sxs-lookup"><span data-stu-id="daf75-152">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="daf75-153">O resultado depende de se o arquivo já tem metadados existentes.</span><span class="sxs-lookup"><span data-stu-id="daf75-153">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="daf75-154">**O arquivo não tem metadados (padrão)**</span><span class="sxs-lookup"><span data-stu-id="daf75-154">**The file does not have metadata (default)**</span></span>
<span data-ttu-id="daf75-155">No cenário padrão, ao montar as unidades do Windows, especificamos que a ID de usuário (UID) de qualquer arquivo está definida como a ID de usuário do usuário WSL e a ID do grupo (GID) é definida como a ID do grupo principal do usuário do WSL.</span><span class="sxs-lookup"><span data-stu-id="daf75-155">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span> 

##### <a name="the-file-has-metadata"></a><span data-ttu-id="daf75-156">O arquivo tem metadados</span><span class="sxs-lookup"><span data-stu-id="daf75-156">The file has metadata</span></span>

<span data-ttu-id="daf75-157">O UID e o GID especificados nos metadados são aplicados como o proprietário do usuário e o proprietário do grupo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="daf75-157">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span> 

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="daf75-158">Acessando arquivos do Linux do Windows usando o `\\wsl$`</span><span class="sxs-lookup"><span data-stu-id="daf75-158">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="daf75-159">O acesso a arquivos do Linux via `\\wsl$` usará o usuário padrão de seu WSL distribuição.</span><span class="sxs-lookup"><span data-stu-id="daf75-159">Accessing Linux files via `\\wsl$` will use the default user of your WSL distro.</span></span> <span data-ttu-id="daf75-160">Portanto, qualquer aplicativo do Windows que esteja acessando os arquivos do Linux terá as mesmas permissões que o usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="daf75-160">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="daf75-161">Criando um novo arquivo</span><span class="sxs-lookup"><span data-stu-id="daf75-161">Creating a new file</span></span>

<span data-ttu-id="daf75-162">O umask padrão é aplicado ao criar um novo arquivo dentro de um WSL distribuição do Windows.</span><span class="sxs-lookup"><span data-stu-id="daf75-162">The default umask is applied when creating a new file inside of a WSL distro from Windows.</span></span> <span data-ttu-id="daf75-163">O umask padrão é `022`ou, em outras palavras, ele permite todas as permissões, exceto permissões de gravação para grupos e outros.</span><span class="sxs-lookup"><span data-stu-id="daf75-163">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="daf75-164">Acessando arquivos no sistema de arquivos raiz Linux do Linux</span><span class="sxs-lookup"><span data-stu-id="daf75-164">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="daf75-165">Todos os arquivos criados, modificados ou acessados no sistema de arquivos raiz do Linux seguem convenções padrão do Linux, como aplicar o umask a um arquivo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="daf75-165">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="daf75-166">Configurando permissões de arquivo</span><span class="sxs-lookup"><span data-stu-id="daf75-166">Configuring file permissions</span></span>

<span data-ttu-id="daf75-167">Você pode configurar suas permissões de arquivo dentro de suas unidades do Windows usando as opções de montagem em WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="daf75-167">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="daf75-168">As opções de montagem permitem que você defina as máscaras de permissões `umask`, `dmask` e `fmask`.</span><span class="sxs-lookup"><span data-stu-id="daf75-168">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="daf75-169">A `umask` é aplicada a todos os arquivos, a `dmask` é aplicada apenas aos diretórios e a `fmask` é aplicada apenas aos arquivos.</span><span class="sxs-lookup"><span data-stu-id="daf75-169">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="daf75-170">Essas máscaras de permissão são então colocadas por meio de uma operação OR lógica quando são aplicadas a arquivos, por exemplo: se você tiver um valor `umask` de `023` e um valor `fmask` de `022`, a máscara de permissões resultante para os arquivos será `023`.</span><span class="sxs-lookup"><span data-stu-id="daf75-170">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span> 

<span data-ttu-id="daf75-171">Consulte a página do documento [' gerenciar distribuições do Linux '](./wsl-config.md) para obter instruções sobre como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="daf75-171">Please see the ['Manage Linux Distributions'](./wsl-config.md) document page for instructions on how to do this.</span></span>
<!-- TODO: Add # to the link-->

