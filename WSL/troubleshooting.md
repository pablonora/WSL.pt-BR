---
title: Solução de problemas do Subsistema Windows para Linux
description: Fornece informações detalhadas sobre erros comuns e problemas que as pessoas têm ao executar o Linux no Subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: a73de13853c124de38cae1b9c6c51d0ee9978d44
ms.sourcegitcommit: f1780bf174c67c531864497ae78cf3f26ef68503
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71205977"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Solução de problemas do Subsistema Windows para Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>O Bash perde conectividade de rede quando conectado a uma VPN

Se, depois de se conectar a uma VPN no Windows, o Bash perder a conectividade de rede, tente essa solução alternativa de dentro do Bash. Essa solução alternativa permitirá que você substitua manualmente a resolução DNS por meio do `/etc/resolv.conf`.

1. Anote o servidor DNS da VPN ao fazer `ipconfig.exe /all`
2. Faça uma cópia do `sudo cp /etc/resolv.conf /etc/resolv.conf.new` do resolv.conf existente
3. Desvincule o `sudo unlink /etc/resolv.conf` do resolv.con atual
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Abra `/etc/resolv.conf` e <br/>
   a. Exclua a primeira linha do arquivo, que diz "\# Este arquivo foi gerado automaticamente pelo WSL. Para interromper a geração automática deste arquivo, remova esta linha". <br/>
   b. Adicione a entrada DNS de (1) acima como a primeira entrada na lista de servidores DNS. <br/>
   c. Feche o arquivo. <br/>

Depois de desconectar a VPN, você precisará reverter as alterações para `/etc/resolv.conf`. Para isso, faça o seguinte:
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Iniciar o WSL ou instalar uma distribuição retorna um código de erro

Siga [estas instruções](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) para coletar logs detalhados e arquivar um problema em nosso GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Como atualizar o Bash do Ubuntu no Windows

Há dois componentes do Bash do Ubuntu no Windows que podem exigir atualização. 

1. O Subsistema Windows para Linux
  
   Atualizar essa parte do Bash do Ubuntu no Windows permitirá novas correções destacadas nas [notas sobre a versão](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes). Certifique-se de que você está inscrito no Programa Windows Insider e que seu build está atualizado. Para obter um controle mais detalhado, incluindo a redefinição da instância do Ubuntu, confira a [página de referência de comando](https://msdn.microsoft.com/en-us/commandline/wsl/reference).

2. Os binários de usuário do Ubuntu 

   A atualização dessa parte do Bash do Ubuntu no Windows instalará todas as atualizações nos binários de usuário do Ubuntu, incluindo os aplicativos que você instalou via apt-get. Para fazer isso, execute os seguintes comandos no Bash:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Erros de atualização do apt-get
Alguns pacotes usam recursos que ainda não implementamos. `udev`, por exemplo, ainda não é compatível e causa vários erros de `apt-get upgrade`.

Para corrigir problemas relacionados ao `udev`, siga as seguintes etapas:

1. Grave o seguinte no `/usr/sbin/policy-rc.d` e salve suas alterações.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. Adicione permissões de execução a `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Execute os comandos a seguir
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error: 0x80040306" na instalação
Isso tem a ver com o fato de não damos suporte ao console herdado.
Para desligar o console herdado:

1. Abra cmd.exe
1. Clique com o botão direito do mouse na barra de título-> Propriedades-> desmarque Usar console herdado
1. Clique em OK

### <a name="error-0x80040154-after-windows-update"></a>"Error: 0x80040154" após atualização do Windows
O recurso Subsistema Windows para Linux pode ser desabilitado durante uma atualização do Windows. Se isso acontecer, o recurso do Windows deverá ser habilitado novamente. As instruções para habilitar o Subsistema Windows para Linux podem ser encontradas no [Guia de instalação](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

### <a name="changing-the-display-language"></a>Como alterar o idioma de exibição
A instalação do WSL tentará alterar automaticamente a localidade do Ubuntu para corresponder à localidade da instalação do Windows.  Se você não quiser esse comportamento, poderá executar esse comando para alterar a localidade do Ubuntu após a conclusão da instalação.  Você precisará reiniciar o bash.exe para que essa alteração entre em vigor.

O exemplo abaixo altera a localidade para en-US:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Problemas de instalação após a restauração do sistema do Windows
1.  Exclua a pasta `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`. <br/>
  **Observação: Não faça isso se o recurso opcional estiver totalmente instalado e funcionando.**
2.  Habilitar o recurso opcional do WSL (se ainda não estiver habilitado)
3.  Reinicialização
4.  lxrun /uninstall /full
5.  Instale o Bash

### <a name="no-internet-access-in-wsl"></a>Sem acesso à Internet no WSL
Alguns usuários relataram problemas com aplicativos de firewall específicos que bloqueiam o acesso à Internet no WSL.  Os firewalls relatados são:

1. Kaspersky
1. AVG
1. Avast

Em alguns casos, desligar o firewall permite o acesso.  Em alguns casos, simplesmente ter o firewall instalado bloqueia o acesso.

### <a name="permission-denied-error-when-using-ping"></a>Erro de permissão negada ao usar ping
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14388-to-windows-10-anniversary-update"></a>[Atualização de aniversário](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

São necessários privilégios de administrador no Windows para executar o ping no WSL.  Para executar o ping, execute o Bash do Ubuntu no Windows como administrador ou execute bash.exe em um prompt do CMD/PowerShell com privilégios de administrador.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14926"></a>[Build 14926+](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  Os privilégios de administrador não são mais necessários.

### <a name="bash-is-hung"></a>Bash suspenso
Se, ao trabalhar com o Bash, você descobrir que ele está suspenso (ou em deadlock) e não está respondendo às entradas, ajude-nos a diagnosticar o problema coletando e relatando um despejo de memória. Observe que essas etapas apresentarão falha no sistema. Não faça isso se não estiver familiarizado ou salve seu trabalho antes.  <br/>
Para coletar um despejo de memória:
1. Altere o tipo de despejo de memória para "despejo de memória completo". Ao alterar o tipo de despejo, anote seu tipo atual.
2. Use as [etapas](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) para configurar a falha usando o controle de teclado.
3. Reproduza o travamento ou o deadlock.
4. Cause uma falha no sistema usando a sequência de teclas de (2).
5. O sistema falhará e coletará o despejo de memória.
6. Após a reinicialização do sistema, relate o memory.dmp a secure@microsoft.com. A localização padrão do arquivo de despejo será %SystemRoot%\memory.dmp ou C:\Windows\memory.dmp se a unidade do sistema for C:. No email, observe que o despejo é para o WSL ou Bash na equipe do Windows.
7. Restaure o tipo de despejo de memória para a configuração original.

### <a name="check-your-build-number"></a>Verifique o número de build

Para encontrar a arquitetura do seu PC e o número de build do Windows, abra  
**Configurações** > **Sistema** > **Sobre**

Procure os campos **Build do SO** e **Tipo de Sistema**.  
    ![Captura de tela dos campos Build e Tipo de Sistema](media/system.png) 


Para localizar o número de build do Windows Server, execute o seguinte no PowerShell:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Confirme se o WSL está habilitado
É possível confirmar se o Subsistema Windows para Linux está habilitado executando o seguinte no PowerShell:  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Problemas de conexão do servidor OpenSSH
Falha ao tentar conectar seu servidor SSH com o seguinte erro: "Conexão encerrada pela porta 22, 127.0.0.1".
1. Verifique se o servidor OpenSSH está em execução:
   ``` BASH
   sudo service ssh status
   ```
   e que você seguiu este tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Interrompa o serviço SSHD e inicie o SSHD no modo de depuração:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. Verifique os logs de inicialização e certifique-se de que as HostKeys estejam disponíveis e que você não veja mensagens de log, como:
   ```
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

Se você vir essas mensagens e as chaves estiverem ausentes em `/etc/ssh/`, será necessário regenerar as chaves ou apenas limpar e instalar o servidor OpenSSH:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

