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
# <a name="file-permissions-for-wsl"></a>Permissões de arquivo para WSL

Esta página detalha como as permissões de arquivo do Linux são interpretadas no subsistema do Windows para Linux, especialmente ao acessar recursos dentro do Windows no sistema de arquivos NT. Esta documentação pressupõe uma compreensão básica da [estrutura de permissões do sistema de arquivos do Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) <!--TODO: Double check that it's okay to add these links--> e o [comando umask](https://en.wikipedia.org/wiki/Umask).

Ao acessar arquivos do Windows do WSL, as permissões de arquivo são calculadas a partir de permissões do Windows ou são lidas de metadados que foram adicionados ao arquivo pelo WSL. Esses metadados não são habilitados por padrão. 

## <a name="wsl-metadata-on-windows-files"></a>Metadados do WSL em arquivos do Windows

Quando os metadados são habilitados como uma opção de montagem no WSL, os atributos estendidos em arquivos do Windows NT podem ser adicionados e interpretados para fornecer permissões do sistema de arquivos do Linux. 

WSL pode adicionar quatro atributos estendidos NTFS:

| Nome do Atributo | Descrição |
| --- | --- |
| $LXUID | ID do proprietário do usuário |
| $LXGID | ID do proprietário do grupo |
| $LXMOD | Modo de arquivo (a permissão de sistemas de arquivos é octal e o tipo, por exemplo: 0777) |
| $LXDEV | Dispositivo, se for um arquivo de dispositivo |

Além disso, qualquer arquivo que não seja um arquivo ou diretório regular (por exemplo: symlinks, FIFOs, dispositivos de bloco, soquetes UNIX e dispositivos de caracteres) também tem um [ponto de nova análise](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)de NTFS. Isso torna muito mais rápido determinar o tipo de arquivo em um determinado diretório sem precisar consultar seus atributos estendidos. 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a>Cenários de acesso a arquivos

Abaixo está uma descrição de como as permissões são determinadas ao acessar arquivos de diferentes maneiras usando o subsistema do Windows para Linux.

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Acessando arquivos no sistema de arquivos da unidade do Windows (DrvFS) do Linux

Esses cenários ocorrem quando você está acessando os arquivos do Windows do WSL, provavelmente por meio de `/mnt/c`. 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>Lendo permissões de arquivo de um arquivo existente do Windows

O resultado depende de se o arquivo já tem metadados existentes.

##### <a name="the-file-does-not-have-metadata-default"></a>**O arquivo não tem metadados (padrão)**

Se o arquivo não tiver nenhum metadado associado a ele, converteremos as permissões efetivas do usuário do Windows para ler/gravar/executar bits e defini-los como o mesmo valor para usuário, grupo e outros. Por exemplo, se sua conta de usuário do Windows tiver acesso de leitura e execução, mas sem acesso de gravação ao arquivo, isso será mostrado como `r-x` para usuário, grupo e outros. Se o arquivo tiver o atributo ' somente leitura ' definido no Windows, não concederemos acesso de gravação no Linux.

##### <a name="the-file-has-metadata"></a>O arquivo tem metadados

Se o arquivo tiver metadados presentes, basta usar esses valores de metadados em vez de converter as permissões efetivas do usuário do Windows.

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>Alterando permissões de arquivo em um arquivo existente do Windows usando chmod

O resultado depende de se o arquivo já tem metadados existentes.

##### <a name="the-file-does-not-have-metadata-default"></a>**O arquivo não tem metadados (padrão)**

O chmod terá apenas um efeito, se você remover todos os atributos de gravação de um arquivo, o atributo ' somente leitura ' no arquivo do Windows será definido, pois esse é o mesmo comportamento que o CIFS (Common Internet File System), que é o cliente SMB (Server Message Block) no Linux.

##### <a name="the-file-has-metadata"></a>O arquivo tem metadados

O chmod será alterado ou adicionará metadados dependendo dos metadados existentes do arquivo. 

Tenha em mente que você não pode dar a si mesmo mais acesso do que o que tem no Windows, mesmo que os metadados indiquem que é o caso. Por exemplo, você pode definir os metadados para exibir que você tem permissões de gravação em um arquivo usando `chmod 777`, mas se você tentou acessar esse arquivo, ainda não conseguiria gravar nele. Isso é graças à interoperabilidade, pois qualquer comando de leitura ou gravação para arquivos do Windows é roteado por meio de suas permissões de usuário do Windows.

#### <a name="creating-a-file-in-drivefs"></a>Criando um arquivo no DriveFS

O resultado depende de se os metadados estão habilitados.

##### <a name="metadata-is-not-enabled-default"></a>Os metadados não estão habilitados (padrão)

As permissões do Windows do arquivo recém-criado serão as mesmas que se você criou o arquivo no Windows sem um descritor de segurança específico, ele herdará as permissões do pai. 

##### <a name="metadata-is-enabled"></a>Os metadados estão habilitados

Os bits de permissão do arquivo são definidos para seguir o umask do Linux e o arquivo será salvo com metadados.

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>Qual usuário do Linux e grupo do Linux possui o arquivo? 

O resultado depende de se o arquivo já tem metadados existentes.

##### <a name="the-file-does-not-have-metadata-default"></a>**O arquivo não tem metadados (padrão)**
No cenário padrão, ao montar as unidades do Windows, especificamos que a ID de usuário (UID) de qualquer arquivo está definida como a ID de usuário do usuário WSL e a ID do grupo (GID) é definida como a ID do grupo principal do usuário do WSL. 

##### <a name="the-file-has-metadata"></a>O arquivo tem metadados

O UID e o GID especificados nos metadados são aplicados como o proprietário do usuário e o proprietário do grupo do arquivo. 

### <a name="accessing-linux-files-from-windows-using-wsl"></a>Acessando arquivos do Linux do Windows usando o `\\wsl$`

O acesso a arquivos do Linux via `\\wsl$` usará o usuário padrão de seu WSL distribuição. Portanto, qualquer aplicativo do Windows que esteja acessando os arquivos do Linux terá as mesmas permissões que o usuário padrão.

#### <a name="creating-a-new-file"></a>Criando um novo arquivo

O umask padrão é aplicado ao criar um novo arquivo dentro de um WSL distribuição do Windows. O umask padrão é `022`ou, em outras palavras, ele permite todas as permissões, exceto permissões de gravação para grupos e outros. 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Acessando arquivos no sistema de arquivos raiz Linux do Linux

Todos os arquivos criados, modificados ou acessados no sistema de arquivos raiz do Linux seguem convenções padrão do Linux, como aplicar o umask a um arquivo recém-criado.

## <a name="configuring-file-permissions"></a>Configurando permissões de arquivo

Você pode configurar suas permissões de arquivo dentro de suas unidades do Windows usando as opções de montagem em WSL. conf. As opções de montagem permitem que você defina as máscaras de permissões `umask`, `dmask` e `fmask`. A `umask` é aplicada a todos os arquivos, a `dmask` é aplicada apenas aos diretórios e a `fmask` é aplicada apenas aos arquivos. Essas máscaras de permissão são então colocadas por meio de uma operação OR lógica quando são aplicadas a arquivos, por exemplo: se você tiver um valor `umask` de `023` e um valor `fmask` de `022`, a máscara de permissões resultante para os arquivos será `023`. 

Consulte a página do documento [' gerenciar distribuições do Linux '](./wsl-config.md) para obter instruções sobre como fazer isso.
<!-- TODO: Add # to the link-->

