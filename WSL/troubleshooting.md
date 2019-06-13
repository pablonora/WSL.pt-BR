---
title: Solução de problemas de Susbystem do Windows para Linux
description: Fornece informações detalhadas sobre erros comuns e emite as pessoas se deparar durante a execução Linux em Susbystem o Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: feb9e25da73eeb0d7f0cef4014221a42e2ca179b
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040850"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Solução de problemas de subsistema Windows para Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash perde a conectividade de rede quando conectada a uma VPN

Se depois de se conectar a uma VPN em Windows, bash perde a conectividade de rede, tente essa solução alternativa de dentro do bash. Essa solução alternativa permitirá que você substituir manualmente a resolução de DNS por meio de `/etc/resolv.conf`.

1. Anote o servidor DNS da VPN de ação `ipconfig.exe /all`
2. Faça uma cópia do resolv. conf existente `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Desvincular o resolv.con atual `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Abra `/etc/resolv.conf` e <br/>
   a. Exclua a primeira linha do arquivo, que diz "\# este arquivo foi gerado automaticamente pelo WSL. Para interromper a geração automática desse arquivo, remova essa linha. ". <br/>
   b. Adicione a entrada DNS de (1) acima como a primeira entrada na lista de servidores DNS. <br/>
   c. Feche o arquivo. <br/>

Depois de desconectar a VPN, será preciso reverter as alterações para `/etc/resolv.conf`. Para fazer isso, execute:
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Iniciando o WSL ou instalar uma distribuição retorna um código de erro

Siga [estas instruções](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) para coletar logs detalhados e arquivar um problema no nosso GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Atualizando o Bash no Ubuntu no Windows

Há dois componentes do Bash no Ubuntu no Windows que podem exigir a atualização. 

1. O subsistema Windows para Linux
  
   Atualizar esta parte do Bash no Ubuntu no Windows permitirá que qualquer novo contornos de correções na [notas de versão](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes). Certifique-se de que você assinou ao programa Windows Insider e que a compilação está atualizada. Para ter maior controle de detalhamento, incluindo a redefinição de sua Ubuntu check-out da instância de [página de referência do comando](https://msdn.microsoft.com/en-us/commandline/wsl/reference).

2. Os binários de usuário do Ubuntu 

   Atualizar esta parte do Bash no Ubuntu no Windows instalará todas as atualizações para os binários de usuário do Ubuntu incluindo aplicativos que você instalou via apt-get. Para atualizar a executar os seguintes comandos no Bash:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Erros de atualização de APT-get
Alguns pacotes usam recursos que ainda não implementamos ainda. `udev`, por exemplo, ainda não tem suporte e faz com que diversos `apt-get upgrade` erros.

Para corrigir problemas relacionados à `udev`, siga as etapas a seguir:

1. Escreva o seguinte para `/usr/sbin/policy-rc.d` e salve suas alterações.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. Adicionar permissões de execução ao `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Execute os seguintes comandos
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error: 0x80040306 "na instalação
Isso tem a ver com o fato de que não há suporte para console herdado.
Para desativar o console herdado:

1. Abra cmd.exe
1. Clique com botão direito no título da barra -> Propriedades -> desmarque usar console herdado
1. Clique em OK

### <a name="error-0x80040154-after-windows-update"></a>"Error: 0x80040154 "após a atualização do Windows
O subsistema do Windows para o recurso do Linux pode ser desabilitado durante uma atualização do Windows. Se isso acontecer, o recurso do Windows deve ser habilitado novamente. Instruções para habilitar o subsistema Windows para Linux pode ser encontrada na [guia de instalação](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

### <a name="changing-the-display-language"></a>Alterar o idioma de exibição
Instalação do WSL tentará alterar automaticamente a localidade do Ubuntu para coincidir com a localidade de sua instalação do Windows.  Se você não quiser esse comportamento, você pode executar este comando para alterar a localidade do Ubuntu, após a conclusão da instalação.  Você precisará reiniciar bash.exe para que essa alteração tenha efeito.

A seguir o exemplo altera a localidade en-US:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Problemas de instalação após a restauração do sistema do Windows
1.  Excluir o `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` pasta. <br/>
  **Observação: Não faça isso se o recurso opcional está totalmente instalado e funcionando.**
2.  Habilitar o recurso opcional do WSL (se ainda não estiver)
3.  Reinicialização
4.  lxrun / desinstalar/completo
5.  Instalar o bash

### <a name="no-internet-access-in-wsl"></a>Sem acesso à internet no WSL
Alguns usuários relataram problemas com aplicativos específicos de firewall bloqueando o acesso à internet no WSL.  Os firewalls relatados são:

1. Kaspersky
1. AVG
1. Avast

Em alguns casos permite desativar o firewall para acesso.  Em alguns casos a simples presença do firewall instalado procura para bloquear o acesso.

### <a name="permission-denied-error-when-using-ping"></a>Erro de negado permissão ao usar o ping
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14388-to-windows-10-anniversary-update"></a>[Atualização de aniversário](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

São necessários privilégios de administrador no Windows para executar o ping no WSL.  Para executar o ping, execute o Bash no Ubuntu no Windows como administrador ou execute bash.exe em um prompt CMD/PowerShell com privilégios de administrador.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14926"></a>[Compilação 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  Privilégios de administrador não é mais necessários.

### <a name="bash-is-hung"></a>Bash está suspenso
Se enquanto estiver trabalhando com o bash, você achar que bash é suspenso (ou em deadlock) e não está respondendo às entradas, nos ajudar a diagnosticar o problema ao coletar e relatar um despejo de memória. Observe que essas etapas causará uma pane em seu sistema. Não faça isso se você não estiver familiarizado com isso, ou salva seu trabalho antes de fazer isso.  <br/>
Para coletar um despejo de memória:
1. Altere o tipo de despejo de memória para "despejo de memória completo". Ao alterar o tipo de despejo, anote o tipo atual.
2. Use o [etapas](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) configurar falha usando o teclado de controle.
3. Reprodução de travamento ou um deadlock.
4. Falha do sistema usando a sequência de teclas de (2).
5. O sistema irá falhar e coletar o despejo de memória.
6. Depois que o sistema for reiniciado, relatam o DMP para secure@microsoft.com. O local padrão do arquivo de despejo é %SystemRoot%\memory.dmp ou C:\Windows\memory.dmp se c: é a unidade do sistema. No email, observe que o despejo é para o WSL ou Bash na equipe do Windows.
7. Restaure o tipo de despejo de memória para a configuração original.

### <a name="check-your-build-number"></a>Verifique o seu número de build

Para localizar o que número de build de arquitetura de seu PC e Windows, abra  
**As configurações** > **sistema** > **sobre**

Procure os **Build do sistema operacional** e **tipo de sistema** campos.  
    ![Captura de tela de compilação e o tipo de sistema de campos](media/system.png) 


Para localizar o número de build do Windows Server, execute o seguinte no PowerShell:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Confirmar que WSL está habilitado
Você pode confirmar que o subsistema Windows para Linux está habilitado executando o seguinte no PowerShell:  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Problemas de conexão do OpenSSH-Server
Tentando conectar-se o servidor SSH falhou com o seguinte erro: "Conexão fechada pelo 127.0.0.1 porta 22".
1. Verifique se que seu OpenSSH Server está em execução:
   ``` BASH
   sudo service ssh status
   ```
   e você já seguiu o tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. O serviço sshd de parar e iniciar o sshd em modo de depuração:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. Verifique os logs de inicialização e certifique-se de HostKeys estão disponíveis e você não vir as mensagens de log, como:
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

Se você vir esse tipo de mensagem e as chaves estão ausentes em `/etc/ssh/`, você precisará regenerar as chaves ou apenas Limpar & instalar openssh-server:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

