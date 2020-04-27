---
title: Solução de problemas do Subsistema Windows para Linux
description: Fornece informações detalhadas sobre erros comuns e problemas que as pessoas têm ao executar o Linux no Subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 9028f1e89e92da94d82b16603b3af60876a4cb86
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "79318140"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="c5e77-104">Solução de problemas do Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="c5e77-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="c5e77-105">Para obter suporte com problemas relacionados ao WSL, consulte nosso repositório do GitHub:</span><span class="sxs-lookup"><span data-stu-id="c5e77-105">For support with issues related to WSL, please see our GitHub repo:</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="c5e77-106">Procure problemas existentes relacionados ao seu problema</span><span class="sxs-lookup"><span data-stu-id="c5e77-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="c5e77-107">Para problemas técnicos, use o repositório do produto: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="c5e77-107">For technical issues, use the product repo: https://github.com/Microsoft/wsl/issues</span></span>

<span data-ttu-id="c5e77-108">Para problemas relacionados ao conteúdo desta documentação, use o repositório de documentos: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="c5e77-108">For issues related to the contents of this documentation, use the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="c5e77-109">Enviar um relatório de bugs</span><span class="sxs-lookup"><span data-stu-id="c5e77-109">Submit a bug report</span></span>

<span data-ttu-id="c5e77-110">Para bugs relacionados a funções ou recursos do WSL, registre um problema no repositório do produto: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="c5e77-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="c5e77-111">Enviar uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="c5e77-111">Submit a feature request</span></span>

<span data-ttu-id="c5e77-112">Para solicitar um novo recurso relacionado à funcionalidade ou à compatibilidade do WSL, registre um problema no repositório do produto: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="c5e77-112">To request a new feature related to WSL functionality or compatibility, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="c5e77-113">Contribuir com os documentos</span><span class="sxs-lookup"><span data-stu-id="c5e77-113">Contribute to the docs</span></span>

<span data-ttu-id="c5e77-114">Para contribuir com a documentação do WSL, envie uma solicitação de pull no repositório de documentos: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="c5e77-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="c5e77-115">Terminal ou Linha de comando</span><span class="sxs-lookup"><span data-stu-id="c5e77-115">Terminal or Command Line</span></span>

<span data-ttu-id="c5e77-116">Por fim, se o problema estiver relacionado ao Terminal do Windows, ao console do Windows ou à interface do usuário da linha de comando, use o repositório de terminal do Windows: https://github.com/microsoft/terminal</span><span class="sxs-lookup"><span data-stu-id="c5e77-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="c5e77-117">Problemas comuns</span><span class="sxs-lookup"><span data-stu-id="c5e77-117">Common issues</span></span>

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="c5e77-118">O Bash perde conectividade de rede quando conectado a uma VPN</span><span class="sxs-lookup"><span data-stu-id="c5e77-118">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="c5e77-119">Se, depois de se conectar a uma VPN no Windows, o Bash perder a conectividade de rede, tente essa solução alternativa de dentro do Bash.</span><span class="sxs-lookup"><span data-stu-id="c5e77-119">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="c5e77-120">Essa solução alternativa permitirá que você substitua manualmente a resolução DNS por meio do `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="c5e77-120">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="c5e77-121">Anote o servidor DNS da VPN ao fazer `ipconfig.exe /all`</span><span class="sxs-lookup"><span data-stu-id="c5e77-121">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="c5e77-122">Faça uma cópia do `sudo cp /etc/resolv.conf /etc/resolv.conf.new` do resolv.conf existente</span><span class="sxs-lookup"><span data-stu-id="c5e77-122">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="c5e77-123">Desvincule o `sudo unlink /etc/resolv.conf` do resolv.conf atual</span><span class="sxs-lookup"><span data-stu-id="c5e77-123">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="c5e77-124">Abra `/etc/resolv.conf` e</span><span class="sxs-lookup"><span data-stu-id="c5e77-124">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="c5e77-125">a.</span><span class="sxs-lookup"><span data-stu-id="c5e77-125">a.</span></span> <span data-ttu-id="c5e77-126">Exclua a primeira linha do arquivo, que diz "\# Este arquivo foi gerado automaticamente pelo WSL.</span><span class="sxs-lookup"><span data-stu-id="c5e77-126">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="c5e77-127">Para interromper a geração automática deste arquivo, remova esta linha".</span><span class="sxs-lookup"><span data-stu-id="c5e77-127">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="c5e77-128">b.</span><span class="sxs-lookup"><span data-stu-id="c5e77-128">b.</span></span> <span data-ttu-id="c5e77-129">Adicione a entrada DNS de (1) acima como a primeira entrada na lista de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="c5e77-129">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="c5e77-130">c.</span><span class="sxs-lookup"><span data-stu-id="c5e77-130">c.</span></span> <span data-ttu-id="c5e77-131">Feche o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c5e77-131">Close the file.</span></span> <br/>

<span data-ttu-id="c5e77-132">Depois de desconectar a VPN, você precisará reverter as alterações para `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="c5e77-132">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="c5e77-133">Para isso, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c5e77-133">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="c5e77-134">Iniciar o WSL ou instalar uma distribuição retorna um código de erro</span><span class="sxs-lookup"><span data-stu-id="c5e77-134">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="c5e77-135">Siga [estas instruções](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) para coletar logs detalhados e arquivar um problema em nosso GitHub.</span><span class="sxs-lookup"><span data-stu-id="c5e77-135">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="c5e77-136">Como atualizar o Bash do Ubuntu no Windows</span><span class="sxs-lookup"><span data-stu-id="c5e77-136">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="c5e77-137">Há dois componentes do Bash do Ubuntu no Windows que podem exigir atualização.</span><span class="sxs-lookup"><span data-stu-id="c5e77-137">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="c5e77-138">O Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="c5e77-138">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="c5e77-139">Atualizar essa parte do Bash do Ubuntu no Windows permitirá novas correções destacadas nas [notas sobre a versão](./release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="c5e77-139">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="c5e77-140">Certifique-se de que você está inscrito no Programa Windows Insider e que seu build está atualizado.</span><span class="sxs-lookup"><span data-stu-id="c5e77-140">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="c5e77-141">Para obter um controle mais detalhado, incluindo a redefinição da instância do Ubuntu, confira a [página de referência de comando](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="c5e77-141">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="c5e77-142">Os binários de usuário do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="c5e77-142">The Ubuntu user binaries</span></span>

   <span data-ttu-id="c5e77-143">A atualização dessa parte do Bash do Ubuntu no Windows instalará todas as atualizações nos binários de usuário do Ubuntu, incluindo os aplicativos que você instalou via apt-get.</span><span class="sxs-lookup"><span data-stu-id="c5e77-143">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="c5e77-144">Para fazer isso, execute os seguintes comandos no Bash:</span><span class="sxs-lookup"><span data-stu-id="c5e77-144">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="c5e77-145">Erros de atualização do apt-get</span><span class="sxs-lookup"><span data-stu-id="c5e77-145">Apt-get upgrade errors</span></span>

<span data-ttu-id="c5e77-146">Alguns pacotes usam recursos que ainda não implementamos.</span><span class="sxs-lookup"><span data-stu-id="c5e77-146">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="c5e77-147">`udev`, por exemplo, ainda não é compatível e causa vários erros de `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="c5e77-147">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="c5e77-148">Para corrigir problemas relacionados ao `udev`, siga as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="c5e77-148">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="c5e77-149">Grave o seguinte no `/usr/sbin/policy-rc.d` e salve suas alterações.</span><span class="sxs-lookup"><span data-stu-id="c5e77-149">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="c5e77-150">Adicione permissões de execução a `/usr/sbin/policy-rc.d`:</span><span class="sxs-lookup"><span data-stu-id="c5e77-150">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="c5e77-151">Execute os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="c5e77-151">Run the following commands:</span></span>

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="c5e77-152">"Error: 0x80040306" na instalação</span><span class="sxs-lookup"><span data-stu-id="c5e77-152">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="c5e77-153">Isso tem a ver com o fato de não damos suporte ao console herdado.</span><span class="sxs-lookup"><span data-stu-id="c5e77-153">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="c5e77-154">Para desligar o console herdado:</span><span class="sxs-lookup"><span data-stu-id="c5e77-154">To turn off legacy console:</span></span>

1. <span data-ttu-id="c5e77-155">Abra cmd.exe</span><span class="sxs-lookup"><span data-stu-id="c5e77-155">Open cmd.exe</span></span>
1. <span data-ttu-id="c5e77-156">Clique com o botão direito do mouse na barra de título-> Propriedades-> desmarque Usar console herdado</span><span class="sxs-lookup"><span data-stu-id="c5e77-156">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="c5e77-157">Clique em OK</span><span class="sxs-lookup"><span data-stu-id="c5e77-157">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="c5e77-158">"Error: 0x80040154" após atualização do Windows</span><span class="sxs-lookup"><span data-stu-id="c5e77-158">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="c5e77-159">O recurso Subsistema Windows para Linux pode ser desabilitado durante uma atualização do Windows.</span><span class="sxs-lookup"><span data-stu-id="c5e77-159">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="c5e77-160">Se isso acontecer, o recurso do Windows deverá ser habilitado novamente.</span><span class="sxs-lookup"><span data-stu-id="c5e77-160">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="c5e77-161">As instruções para habilitar o Subsistema Windows para Linux podem ser encontradas no [Guia de instalação](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="c5e77-161">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="c5e77-162">Como alterar o idioma de exibição</span><span class="sxs-lookup"><span data-stu-id="c5e77-162">Changing the display language</span></span>

<span data-ttu-id="c5e77-163">A instalação do WSL tentará alterar automaticamente a localidade do Ubuntu para corresponder à localidade da instalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="c5e77-163">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="c5e77-164">Se você não quiser esse comportamento, poderá executar esse comando para alterar a localidade do Ubuntu após a conclusão da instalação.</span><span class="sxs-lookup"><span data-stu-id="c5e77-164">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="c5e77-165">Você precisará reiniciar o bash.exe para que essa alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="c5e77-165">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="c5e77-166">O exemplo abaixo altera a localidade para en-US:</span><span class="sxs-lookup"><span data-stu-id="c5e77-166">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="c5e77-167">Problemas de instalação após a restauração do sistema do Windows</span><span class="sxs-lookup"><span data-stu-id="c5e77-167">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="c5e77-168">Exclua a pasta `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="c5e77-168">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="c5e77-169">**Observação: Não faça isso se o recurso opcional estiver totalmente instalado e funcionando.**</span><span class="sxs-lookup"><span data-stu-id="c5e77-169">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="c5e77-170">Habilitar o recurso opcional do WSL (se ainda não estiver habilitado)</span><span class="sxs-lookup"><span data-stu-id="c5e77-170">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="c5e77-171">Reinicialização</span><span class="sxs-lookup"><span data-stu-id="c5e77-171">Reboot</span></span>
4. <span data-ttu-id="c5e77-172">lxrun /uninstall /full</span><span class="sxs-lookup"><span data-stu-id="c5e77-172">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="c5e77-173">Instale o Bash</span><span class="sxs-lookup"><span data-stu-id="c5e77-173">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="c5e77-174">Sem acesso à Internet no WSL</span><span class="sxs-lookup"><span data-stu-id="c5e77-174">No internet access in WSL</span></span>

<span data-ttu-id="c5e77-175">Alguns usuários relataram problemas com aplicativos de firewall específicos que bloqueiam o acesso à Internet no WSL.</span><span class="sxs-lookup"><span data-stu-id="c5e77-175">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="c5e77-176">Os firewalls relatados são:</span><span class="sxs-lookup"><span data-stu-id="c5e77-176">The firewalls reported are:</span></span>

1. <span data-ttu-id="c5e77-177">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="c5e77-177">Kaspersky</span></span>
2. <span data-ttu-id="c5e77-178">AVG</span><span class="sxs-lookup"><span data-stu-id="c5e77-178">AVG</span></span>
3. <span data-ttu-id="c5e77-179">Avast</span><span class="sxs-lookup"><span data-stu-id="c5e77-179">Avast</span></span>

<span data-ttu-id="c5e77-180">Em alguns casos, desligar o firewall permite o acesso.</span><span class="sxs-lookup"><span data-stu-id="c5e77-180">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="c5e77-181">Em outros, simplesmente ter o firewall instalado bloqueia o acesso.</span><span class="sxs-lookup"><span data-stu-id="c5e77-181">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="c5e77-182">Erro de permissão negada ao usar ping</span><span class="sxs-lookup"><span data-stu-id="c5e77-182">Permission Denied error when using ping</span></span>

<span data-ttu-id="c5e77-183">Para a [Atualização de Aniversário do Windows, versão 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), são necessários **privilégios de administrador** no Windows para executar o ping no WSL.</span><span class="sxs-lookup"><span data-stu-id="c5e77-183">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="c5e77-184">Para executar o ping, execute o Bash do Ubuntu no Windows como administrador ou execute bash.exe em um prompt do CMD/PowerShell com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="c5e77-184">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="c5e77-185">Para versões posteriores do Windows, [Build 14926 e posteriores](./release-notes.md#build-14926), os privilégios de administrador não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="c5e77-185">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="c5e77-186">Bash suspenso</span><span class="sxs-lookup"><span data-stu-id="c5e77-186">Bash is hung</span></span>

<span data-ttu-id="c5e77-187">Se, ao trabalhar com o Bash, você descobrir que ele está suspenso (ou em deadlock) e não está respondendo às entradas, ajude-nos a diagnosticar o problema coletando e relatando um despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="c5e77-187">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="c5e77-188">Observe que essas etapas apresentarão falha no sistema.</span><span class="sxs-lookup"><span data-stu-id="c5e77-188">Note that these steps will crash your system.</span></span> <span data-ttu-id="c5e77-189">Não faça isso se não estiver familiarizado ou salve seu trabalho antes.</span><span class="sxs-lookup"><span data-stu-id="c5e77-189">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="c5e77-190">Para coletar um despejo de memória</span><span class="sxs-lookup"><span data-stu-id="c5e77-190">To collect a memory dump</span></span>

1. <span data-ttu-id="c5e77-191">Altere o tipo de despejo de memória para "despejo de memória completo".</span><span class="sxs-lookup"><span data-stu-id="c5e77-191">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="c5e77-192">Ao alterar o tipo de despejo, anote seu tipo atual.</span><span class="sxs-lookup"><span data-stu-id="c5e77-192">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="c5e77-193">Use as [etapas](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) para configurar a falha usando o controle de teclado.</span><span class="sxs-lookup"><span data-stu-id="c5e77-193">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="c5e77-194">Reproduza o travamento ou o deadlock.</span><span class="sxs-lookup"><span data-stu-id="c5e77-194">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="c5e77-195">Cause uma falha no sistema usando a sequência de teclas de (2).</span><span class="sxs-lookup"><span data-stu-id="c5e77-195">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="c5e77-196">O sistema falhará e coletará o despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="c5e77-196">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="c5e77-197">Após a reinicialização do sistema, relate o memory.dmp a secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c5e77-197">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="c5e77-198">A localização padrão do arquivo de despejo será %SystemRoot%\memory.dmp ou C:\Windows\memory.dmp se a unidade do sistema for C:.</span><span class="sxs-lookup"><span data-stu-id="c5e77-198">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="c5e77-199">No email, observe que o despejo é para o WSL ou Bash na equipe do Windows.</span><span class="sxs-lookup"><span data-stu-id="c5e77-199">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="c5e77-200">Restaure o tipo de despejo de memória para a configuração original.</span><span class="sxs-lookup"><span data-stu-id="c5e77-200">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="c5e77-201">Verifique o número de build</span><span class="sxs-lookup"><span data-stu-id="c5e77-201">Check your build number</span></span>

<span data-ttu-id="c5e77-202">Para encontrar a arquitetura do seu PC e o número de build do Windows, abra</span><span class="sxs-lookup"><span data-stu-id="c5e77-202">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="c5e77-203">**Configurações** > **Sistema** > **Sobre**</span><span class="sxs-lookup"><span data-stu-id="c5e77-203">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="c5e77-204">Procure os campos **Build do SO** e **Tipo de Sistema**.</span><span class="sxs-lookup"><span data-stu-id="c5e77-204">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="c5e77-205">![Captura de tela dos campos Build e Tipo de Sistema](media/system.png)</span><span class="sxs-lookup"><span data-stu-id="c5e77-205">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="c5e77-206">Para localizar o número de build do Windows Server, execute o seguinte no PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c5e77-206">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="c5e77-207">Confirme se o WSL está habilitado</span><span class="sxs-lookup"><span data-stu-id="c5e77-207">Confirm WSL is enabled</span></span>

<span data-ttu-id="c5e77-208">É possível confirmar se o Subsistema Windows para Linux está habilitado executando o seguinte no PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c5e77-208">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="c5e77-209">Problemas de conexão do servidor OpenSSH</span><span class="sxs-lookup"><span data-stu-id="c5e77-209">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="c5e77-210">Falha ao tentar conectar seu servidor SSH com o seguinte erro: "Conexão encerrada pela porta 22, 127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="c5e77-210">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="c5e77-211">Verifique se o servidor OpenSSH está em execução:</span><span class="sxs-lookup"><span data-stu-id="c5e77-211">Make sure your OpenSSH Server is running:</span></span>

   ```bash
   sudo service ssh status
   ```

   <span data-ttu-id="c5e77-212">e que você seguiu este tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span><span class="sxs-lookup"><span data-stu-id="c5e77-212">and you've followed this tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span></span>

2. <span data-ttu-id="c5e77-213">Interrompa o serviço SSHD e inicie o SSHD no modo de depuração:</span><span class="sxs-lookup"><span data-stu-id="c5e77-213">Stop the sshd service and start sshd in debug mode:</span></span>

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="c5e77-214">Verifique os logs de inicialização e certifique-se de que as HostKeys estejam disponíveis e que você não veja mensagens de log, como:</span><span class="sxs-lookup"><span data-stu-id="c5e77-214">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

   ```BASH
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

<span data-ttu-id="c5e77-215">Se você vir essas mensagens e as chaves estiverem ausentes em `/etc/ssh/`, será necessário regenerar as chaves ou apenas limpar e instalar o servidor OpenSSH:</span><span class="sxs-lookup"><span data-stu-id="c5e77-215">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="c5e77-216">"Não foi possível encontrar o assembly referenciado."</span><span class="sxs-lookup"><span data-stu-id="c5e77-216">"The referenced assembly could not be found."</span></span> <span data-ttu-id="c5e77-217">ao habilitar o recurso opcional WSL (Subsistema Windows para Linux)</span><span class="sxs-lookup"><span data-stu-id="c5e77-217">when enabling the WSL optional feature</span></span>

<span data-ttu-id="c5e77-218">Este erro está relacionado a um estado de instalação inadequado.</span><span class="sxs-lookup"><span data-stu-id="c5e77-218">This error is related to being in a bad install state.</span></span> <span data-ttu-id="c5e77-219">Conclua as etapas a seguir para tentar corrigir esse problema:</span><span class="sxs-lookup"><span data-stu-id="c5e77-219">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="c5e77-220">Se você estiver executando o comando Habilitar recurso WSL do PowerShell, tente usar a GUI em vez de abrir o menu Iniciar, pesquisando "Ativar ou desativar recursos do Windows" e, na lista, selecione "Subsistema do Windows para Linux", que instalará o componente opcional.</span><span class="sxs-lookup"><span data-stu-id="c5e77-220">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="c5e77-221">Atualize sua versão do Windows acessando Configurações, Atualizações e clicando em "Verificar se há atualizações"</span><span class="sxs-lookup"><span data-stu-id="c5e77-221">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="c5e77-222">Se ambas falharem e você precisar acessar o WSL, considere atualizar no local reinstalando o Windows 10 com uma mídia de instalação e selecionando "Manter Tudo" para que seus aplicativos e arquivos sejam preservados.</span><span class="sxs-lookup"><span data-stu-id="c5e77-222">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="c5e77-223">É possível encontrar instruções para fazer isso na [página Reinstalar o Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="c5e77-223">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>

### <a name="correct-ssh-related-permission-errors"></a><span data-ttu-id="c5e77-224">Erros de permissão corretos (relacionados a SSH)</span><span class="sxs-lookup"><span data-stu-id="c5e77-224">Correct (SSH related) permission errors</span></span>

<span data-ttu-id="c5e77-225">Se você vir este erro:</span><span class="sxs-lookup"><span data-stu-id="c5e77-225">If you're seeing this error:</span></span>

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

<span data-ttu-id="c5e77-226">Para corrigi-lo, acrescente o seguinte ao arquivo ```/etc/wsl.conf```:</span><span class="sxs-lookup"><span data-stu-id="c5e77-226">To fix this, append the following to the the ```/etc/wsl.conf``` file:</span></span>

```
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

<span data-ttu-id="c5e77-227">Ao adicionar esse comando, você incluirá metadados e modificará as permissões do arquivo nos arquivos Windows vistos em WSL.</span><span class="sxs-lookup"><span data-stu-id="c5e77-227">Please note that adding this command will include metadata and modify the file permissions on the Windows files seen from WSL.</span></span> <span data-ttu-id="c5e77-228">Confira as [Permissões do sistema de arquivos](./file-permissions.md) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="c5e77-228">Please see the [File System Permissions](./file-permissions.md) for more information.</span></span>
