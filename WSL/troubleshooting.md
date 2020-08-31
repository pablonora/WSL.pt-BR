---
title: Solução de problemas do Subsistema Windows para Linux
description: Fornece informações detalhadas sobre erros comuns e problemas que as pessoas têm ao executar o Linux no Subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 84aecf4f6111cca47ece3c2421be659fb5a27771
ms.sourcegitcommit: a5534257c236cefeebe86e6b3fc4be0be8fac24e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "88714848"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="8e200-104">Solução de problemas do Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="8e200-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="8e200-105">Para obter suporte com problemas relacionados ao WSL, consulte nosso repositório do GitHub:</span><span class="sxs-lookup"><span data-stu-id="8e200-105">For support with issues related to WSL, please see our GitHub repo:</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="8e200-106">Procure problemas existentes relacionados ao seu problema</span><span class="sxs-lookup"><span data-stu-id="8e200-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="8e200-107">Para problemas técnicos, use o repositório do produto: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="8e200-107">For technical issues, use the product repo: https://github.com/Microsoft/wsl/issues</span></span>

<span data-ttu-id="8e200-108">Para problemas relacionados ao conteúdo desta documentação, use o repositório de documentos: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="8e200-108">For issues related to the contents of this documentation, use the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="8e200-109">Enviar um relatório de bugs</span><span class="sxs-lookup"><span data-stu-id="8e200-109">Submit a bug report</span></span>

<span data-ttu-id="8e200-110">Para bugs relacionados a funções ou recursos do WSL, registre um problema no repositório do produto: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="8e200-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="8e200-111">Enviar uma solicitação de recurso</span><span class="sxs-lookup"><span data-stu-id="8e200-111">Submit a feature request</span></span>

<span data-ttu-id="8e200-112">Para solicitar um novo recurso relacionado à funcionalidade ou à compatibilidade do WSL, registre um problema no repositório do produto: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="8e200-112">To request a new feature related to WSL functionality or compatibility, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="8e200-113">Contribuir com os documentos</span><span class="sxs-lookup"><span data-stu-id="8e200-113">Contribute to the docs</span></span>

<span data-ttu-id="8e200-114">Para contribuir com a documentação do WSL, envie uma solicitação de pull no repositório de documentos: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="8e200-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="8e200-115">Terminal ou Linha de comando</span><span class="sxs-lookup"><span data-stu-id="8e200-115">Terminal or Command Line</span></span>

<span data-ttu-id="8e200-116">Por fim, se o problema estiver relacionado ao Terminal do Windows, ao console do Windows ou à interface do usuário da linha de comando, use o repositório de terminal do Windows: https://github.com/microsoft/terminal</span><span class="sxs-lookup"><span data-stu-id="8e200-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="8e200-117">Problemas comuns</span><span class="sxs-lookup"><span data-stu-id="8e200-117">Common issues</span></span>

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a><span data-ttu-id="8e200-118">Erro: 0x1bc quando `wsl --set-default-version 2`</span><span class="sxs-lookup"><span data-stu-id="8e200-118">Error: 0x1bc when `wsl --set-default-version 2`</span></span>
<span data-ttu-id="8e200-119">Isso pode acontecer quando a configuração de 'Idioma de Exibição' ou 'Localidade do Sistema' não é inglês.</span><span class="sxs-lookup"><span data-stu-id="8e200-119">This may happen when 'Display Language' or 'System Locale' setting is not English.</span></span>
```
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

<span data-ttu-id="8e200-120">O erro real em `0x1bc` é:</span><span class="sxs-lookup"><span data-stu-id="8e200-120">THe actual error for `0x1bc` is:</span></span>
```
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

<span data-ttu-id="8e200-121">Para obter mais informações, veja o problema [5749](https://github.com/microsoft/WSL/issues/5749)</span><span class="sxs-lookup"><span data-stu-id="8e200-121">For more information, please refer to issue [5749](https://github.com/microsoft/WSL/issues/5749)</span></span>


### <a name="cannot-access-wsl-files-from-windows"></a><span data-ttu-id="8e200-122">Não é possível acessar arquivos do WSL por meio do Windows</span><span class="sxs-lookup"><span data-stu-id="8e200-122">Cannot access WSL files from Windows</span></span>
<span data-ttu-id="8e200-123">Um servidor de arquivos do protocolo 9P fornece o serviço no lado do Linux para permitir que o Windows acesse o sistema de arquivos do Linux.</span><span class="sxs-lookup"><span data-stu-id="8e200-123">A 9p protocol file server provides the service on the Linux side to allow Windows to access the Linux file system.</span></span> <span data-ttu-id="8e200-124">Se você não conseguir acessar o WSL usando o `\\wsl$` no Windows, isso poderá ser devido a uma inicialização incorreta do 9P.</span><span class="sxs-lookup"><span data-stu-id="8e200-124">If you cannot access WSL using `\\wsl$` on Windows, it could be because 9P did not start correctly.</span></span>

<span data-ttu-id="8e200-125">Para conferir isso, é possível verificar os logs de inicialização usando `dmesg |grep 9p`, o que mostra os erros existentes.</span><span class="sxs-lookup"><span data-stu-id="8e200-125">To check this, you can check the start up logs using: `dmesg |grep 9p`, and this will show you any errors.</span></span> <span data-ttu-id="8e200-126">Uma saída bem-sucedida tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="8e200-126">A successfull output looks like the following:</span></span> 

```
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

<span data-ttu-id="8e200-127">Confira [este thread do GitHub](https://github.com/microsoft/wsl/issues/5307) para discussões mais aprofundadas sobre esse problema.</span><span class="sxs-lookup"><span data-stu-id="8e200-127">Please see [this Github thread](https://github.com/microsoft/wsl/issues/5307) for further discussion on this issue.</span></span>

### <a name="cant-start-wsl-2-distro-and-only-see-wsl-2-in-output"></a><span data-ttu-id="8e200-128">Não é possível iniciar a distribuição do WSL 2, e apenas o texto 'WSL 2' é exibido na saída</span><span class="sxs-lookup"><span data-stu-id="8e200-128">Can't start WSL 2 distro and only see 'WSL 2' in output</span></span>
<span data-ttu-id="8e200-129">Se seu idioma de exibição não for inglês, talvez você esteja vendo uma versão truncada de um texto de erro.</span><span class="sxs-lookup"><span data-stu-id="8e200-129">If your display language is not English, then it is possible you are seeing a truncated version of an error text.</span></span>

```powershell
C:\Users\me>wsl
WSL 2
```

<span data-ttu-id="8e200-130">Para resolver esse problema, visite `https://aka.ms/wsl2kernel` e instale o kernel manualmente, seguindo as instruções nessa página da documentação.</span><span class="sxs-lookup"><span data-stu-id="8e200-130">To resolve this issue, please visit `https://aka.ms/wsl2kernel` and install the kernel manually by following the directions on that doc page.</span></span> 

### <a name="please-enable-the-virtual-machine-platform-windows-feature-and-ensure-virtualization-is-enabled-in-the-bios"></a><span data-ttu-id="8e200-131">Habilite o recurso Plataforma de Máquina Virtual do Windows e verifique se a virtualização está habilitada na BIOS.</span><span class="sxs-lookup"><span data-stu-id="8e200-131">Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.</span></span>

1. <span data-ttu-id="8e200-132">Verifique os [requisitos do sistema do Hyper-V](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span><span class="sxs-lookup"><span data-stu-id="8e200-132">Check the [Hyper-V system requirements](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span></span>
2. <span data-ttu-id="8e200-133">Se o computador for uma VM, habilite a [virtualização aninhada](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine) manualmente.</span><span class="sxs-lookup"><span data-stu-id="8e200-133">If your machine is a VM, please enable [nested virtualization](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine) manually.</span></span> <span data-ttu-id="8e200-134">Inicie o PowerShell com direitos de administrador e execute:</span><span class="sxs-lookup"><span data-stu-id="8e200-134">Launch powershell with admin, and run:</span></span> 

```powershell
Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
```

3. <span data-ttu-id="8e200-135">Siga as diretrizes do fabricante do seu PC sobre como habilitar a virtualização.</span><span class="sxs-lookup"><span data-stu-id="8e200-135">Please follow guidelines from your PC's manufacturer on how to enable virtualization.</span></span> <span data-ttu-id="8e200-136">Geralmente, isso envolve o uso da BIOS do sistema para garantir que esses recursos estejam habilitados em sua CPU.</span><span class="sxs-lookup"><span data-stu-id="8e200-136">In general, this can involve using the system BIOS to ensure that these features are enabled on your CPU.</span></span> 
4. <span data-ttu-id="8e200-137">Reinicie o computador depois de habilitar o componente opcional `Virtual Machine Platform`.</span><span class="sxs-lookup"><span data-stu-id="8e200-137">Restart your machine after enabling the `Virtual Machine Platform` optional component.</span></span> 

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="8e200-138">O Bash perde conectividade de rede quando conectado a uma VPN</span><span class="sxs-lookup"><span data-stu-id="8e200-138">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="8e200-139">Se, depois de se conectar a uma VPN no Windows, o Bash perder a conectividade de rede, tente essa solução alternativa de dentro do Bash.</span><span class="sxs-lookup"><span data-stu-id="8e200-139">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="8e200-140">Essa solução alternativa permitirá que você substitua manualmente a resolução DNS por meio do `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="8e200-140">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="8e200-141">Anote o servidor DNS da VPN ao fazer `ipconfig.exe /all`</span><span class="sxs-lookup"><span data-stu-id="8e200-141">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="8e200-142">Faça uma cópia do `sudo cp /etc/resolv.conf /etc/resolv.conf.new` do resolv.conf existente</span><span class="sxs-lookup"><span data-stu-id="8e200-142">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="8e200-143">Desvincule o `sudo unlink /etc/resolv.conf` do resolv.conf atual</span><span class="sxs-lookup"><span data-stu-id="8e200-143">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="8e200-144">Abra `/etc/resolv.conf` e</span><span class="sxs-lookup"><span data-stu-id="8e200-144">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="8e200-145">a.</span><span class="sxs-lookup"><span data-stu-id="8e200-145">a.</span></span> <span data-ttu-id="8e200-146">Exclua a primeira linha do arquivo, que diz "\# Este arquivo foi gerado automaticamente pelo WSL.</span><span class="sxs-lookup"><span data-stu-id="8e200-146">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="8e200-147">Para interromper a geração automática deste arquivo, remova esta linha".</span><span class="sxs-lookup"><span data-stu-id="8e200-147">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="8e200-148">b.</span><span class="sxs-lookup"><span data-stu-id="8e200-148">b.</span></span> <span data-ttu-id="8e200-149">Adicione a entrada DNS de (1) acima como a primeira entrada na lista de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="8e200-149">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="8e200-150">c.</span><span class="sxs-lookup"><span data-stu-id="8e200-150">c.</span></span> <span data-ttu-id="8e200-151">Feche o arquivo.</span><span class="sxs-lookup"><span data-stu-id="8e200-151">Close the file.</span></span> <br/>

<span data-ttu-id="8e200-152">Depois de desconectar a VPN, você precisará reverter as alterações para `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="8e200-152">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="8e200-153">Para isso, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e200-153">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="8e200-154">Iniciar o WSL ou instalar uma distribuição retorna um código de erro</span><span class="sxs-lookup"><span data-stu-id="8e200-154">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="8e200-155">Siga [estas instruções](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) para coletar logs detalhados e arquivar um problema em nosso GitHub.</span><span class="sxs-lookup"><span data-stu-id="8e200-155">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="8e200-156">Como atualizar o Bash do Ubuntu no Windows</span><span class="sxs-lookup"><span data-stu-id="8e200-156">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="8e200-157">Há dois componentes do Bash do Ubuntu no Windows que podem exigir atualização.</span><span class="sxs-lookup"><span data-stu-id="8e200-157">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="8e200-158">O Subsistema Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="8e200-158">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="8e200-159">Atualizar essa parte do Bash do Ubuntu no Windows permitirá novas correções destacadas nas [notas sobre a versão](./release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="8e200-159">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="8e200-160">Certifique-se de que você está inscrito no Programa Windows Insider e que seu build está atualizado.</span><span class="sxs-lookup"><span data-stu-id="8e200-160">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="8e200-161">Para obter um controle mais detalhado, incluindo a redefinição da instância do Ubuntu, confira a [página de referência de comando](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="8e200-161">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="8e200-162">Os binários de usuário do Ubuntu</span><span class="sxs-lookup"><span data-stu-id="8e200-162">The Ubuntu user binaries</span></span>

   <span data-ttu-id="8e200-163">A atualização dessa parte do Bash do Ubuntu no Windows instalará todas as atualizações nos binários de usuário do Ubuntu, incluindo os aplicativos que você instalou via apt-get.</span><span class="sxs-lookup"><span data-stu-id="8e200-163">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="8e200-164">Para fazer isso, execute os seguintes comandos no Bash:</span><span class="sxs-lookup"><span data-stu-id="8e200-164">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="8e200-165">Erros de atualização do apt-get</span><span class="sxs-lookup"><span data-stu-id="8e200-165">Apt-get upgrade errors</span></span>

<span data-ttu-id="8e200-166">Alguns pacotes usam recursos que ainda não implementamos.</span><span class="sxs-lookup"><span data-stu-id="8e200-166">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="8e200-167">`udev`, por exemplo, ainda não é compatível e causa vários erros de `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="8e200-167">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="8e200-168">Para corrigir problemas relacionados ao `udev`, siga as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="8e200-168">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="8e200-169">Grave o seguinte no `/usr/sbin/policy-rc.d` e salve suas alterações.</span><span class="sxs-lookup"><span data-stu-id="8e200-169">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="8e200-170">Adicione permissões de execução a `/usr/sbin/policy-rc.d`:</span><span class="sxs-lookup"><span data-stu-id="8e200-170">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="8e200-171">Execute os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="8e200-171">Run the following commands:</span></span>

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="8e200-172">"Error: 0x80040306" na instalação</span><span class="sxs-lookup"><span data-stu-id="8e200-172">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="8e200-173">Isso tem a ver com o fato de não damos suporte ao console herdado.</span><span class="sxs-lookup"><span data-stu-id="8e200-173">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="8e200-174">Para desligar o console herdado:</span><span class="sxs-lookup"><span data-stu-id="8e200-174">To turn off legacy console:</span></span>

1. <span data-ttu-id="8e200-175">Abra cmd.exe</span><span class="sxs-lookup"><span data-stu-id="8e200-175">Open cmd.exe</span></span>
1. <span data-ttu-id="8e200-176">Clique com o botão direito do mouse na barra de título-> Propriedades-> desmarque Usar console herdado</span><span class="sxs-lookup"><span data-stu-id="8e200-176">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="8e200-177">Clique em OK</span><span class="sxs-lookup"><span data-stu-id="8e200-177">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="8e200-178">"Error: 0x80040154" após atualização do Windows</span><span class="sxs-lookup"><span data-stu-id="8e200-178">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="8e200-179">O recurso Subsistema Windows para Linux pode ser desabilitado durante uma atualização do Windows.</span><span class="sxs-lookup"><span data-stu-id="8e200-179">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="8e200-180">Se isso acontecer, o recurso do Windows deverá ser habilitado novamente.</span><span class="sxs-lookup"><span data-stu-id="8e200-180">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="8e200-181">As instruções para habilitar o Subsistema Windows para Linux podem ser encontradas no [Guia de instalação](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="8e200-181">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="8e200-182">Como alterar o idioma de exibição</span><span class="sxs-lookup"><span data-stu-id="8e200-182">Changing the display language</span></span>

<span data-ttu-id="8e200-183">A instalação do WSL tentará alterar automaticamente a localidade do Ubuntu para corresponder à localidade da instalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="8e200-183">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="8e200-184">Se você não quiser esse comportamento, poderá executar esse comando para alterar a localidade do Ubuntu após a conclusão da instalação.</span><span class="sxs-lookup"><span data-stu-id="8e200-184">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="8e200-185">Você precisará reiniciar o bash.exe para que essa alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="8e200-185">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="8e200-186">O exemplo abaixo altera a localidade para en-US:</span><span class="sxs-lookup"><span data-stu-id="8e200-186">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="8e200-187">Problemas de instalação após a restauração do sistema do Windows</span><span class="sxs-lookup"><span data-stu-id="8e200-187">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="8e200-188">Exclua a pasta `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="8e200-188">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="8e200-189">**Observação: Não faça isso se o recurso opcional estiver totalmente instalado e funcionando.**</span><span class="sxs-lookup"><span data-stu-id="8e200-189">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="8e200-190">Habilitar o recurso opcional do WSL (se ainda não estiver habilitado)</span><span class="sxs-lookup"><span data-stu-id="8e200-190">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="8e200-191">Reinicialização</span><span class="sxs-lookup"><span data-stu-id="8e200-191">Reboot</span></span>
4. <span data-ttu-id="8e200-192">lxrun /uninstall /full</span><span class="sxs-lookup"><span data-stu-id="8e200-192">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="8e200-193">Instale o Bash</span><span class="sxs-lookup"><span data-stu-id="8e200-193">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="8e200-194">Sem acesso à Internet no WSL</span><span class="sxs-lookup"><span data-stu-id="8e200-194">No internet access in WSL</span></span>

<span data-ttu-id="8e200-195">Alguns usuários relataram problemas com aplicativos de firewall específicos que bloqueiam o acesso à Internet no WSL.</span><span class="sxs-lookup"><span data-stu-id="8e200-195">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="8e200-196">Os firewalls relatados são:</span><span class="sxs-lookup"><span data-stu-id="8e200-196">The firewalls reported are:</span></span>

1. <span data-ttu-id="8e200-197">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="8e200-197">Kaspersky</span></span>
2. <span data-ttu-id="8e200-198">AVG</span><span class="sxs-lookup"><span data-stu-id="8e200-198">AVG</span></span>
3. <span data-ttu-id="8e200-199">Avast</span><span class="sxs-lookup"><span data-stu-id="8e200-199">Avast</span></span>

<span data-ttu-id="8e200-200">Em alguns casos, desligar o firewall permite o acesso.</span><span class="sxs-lookup"><span data-stu-id="8e200-200">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="8e200-201">Em outros, simplesmente ter o firewall instalado bloqueia o acesso.</span><span class="sxs-lookup"><span data-stu-id="8e200-201">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="8e200-202">Erro de permissão negada ao usar ping</span><span class="sxs-lookup"><span data-stu-id="8e200-202">Permission Denied error when using ping</span></span>

<span data-ttu-id="8e200-203">Para a [Atualização de Aniversário do Windows, versão 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), são necessários **privilégios de administrador** no Windows para executar o ping no WSL.</span><span class="sxs-lookup"><span data-stu-id="8e200-203">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="8e200-204">Para executar o ping, execute o Bash do Ubuntu no Windows como administrador ou execute bash.exe em um prompt do CMD/PowerShell com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="8e200-204">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="8e200-205">Para versões posteriores do Windows, [Build 14926 e posteriores](./release-notes.md#build-14926), os privilégios de administrador não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="8e200-205">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="8e200-206">Bash suspenso</span><span class="sxs-lookup"><span data-stu-id="8e200-206">Bash is hung</span></span>

<span data-ttu-id="8e200-207">Se, ao trabalhar com o Bash, você descobrir que ele está suspenso (ou em deadlock) e não está respondendo às entradas, ajude-nos a diagnosticar o problema coletando e relatando um despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="8e200-207">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="8e200-208">Observe que essas etapas apresentarão falha no sistema.</span><span class="sxs-lookup"><span data-stu-id="8e200-208">Note that these steps will crash your system.</span></span> <span data-ttu-id="8e200-209">Não faça isso se não estiver familiarizado ou salve seu trabalho antes.</span><span class="sxs-lookup"><span data-stu-id="8e200-209">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="8e200-210">Para coletar um despejo de memória</span><span class="sxs-lookup"><span data-stu-id="8e200-210">To collect a memory dump</span></span>

1. <span data-ttu-id="8e200-211">Altere o tipo de despejo de memória para "despejo de memória completo".</span><span class="sxs-lookup"><span data-stu-id="8e200-211">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="8e200-212">Ao alterar o tipo de despejo, anote seu tipo atual.</span><span class="sxs-lookup"><span data-stu-id="8e200-212">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="8e200-213">Use as [etapas](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) para configurar a falha usando o controle de teclado.</span><span class="sxs-lookup"><span data-stu-id="8e200-213">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="8e200-214">Reproduza o travamento ou o deadlock.</span><span class="sxs-lookup"><span data-stu-id="8e200-214">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="8e200-215">Cause uma falha no sistema usando a sequência de teclas de (2).</span><span class="sxs-lookup"><span data-stu-id="8e200-215">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="8e200-216">O sistema falhará e coletará o despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="8e200-216">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="8e200-217">Após a reinicialização do sistema, relate o memory.dmp a secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8e200-217">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="8e200-218">A localização padrão do arquivo de despejo será %SystemRoot%\memory.dmp ou C:\Windows\memory.dmp se a unidade do sistema for C:.</span><span class="sxs-lookup"><span data-stu-id="8e200-218">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="8e200-219">No email, observe que o despejo é para o WSL ou Bash na equipe do Windows.</span><span class="sxs-lookup"><span data-stu-id="8e200-219">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="8e200-220">Restaure o tipo de despejo de memória para a configuração original.</span><span class="sxs-lookup"><span data-stu-id="8e200-220">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="8e200-221">Verifique o número de build</span><span class="sxs-lookup"><span data-stu-id="8e200-221">Check your build number</span></span>

<span data-ttu-id="8e200-222">Para encontrar a arquitetura do seu PC e o número de build do Windows, abra</span><span class="sxs-lookup"><span data-stu-id="8e200-222">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="8e200-223">**Configurações** > **Sistema** > **Sobre**</span><span class="sxs-lookup"><span data-stu-id="8e200-223">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="8e200-224">Procure os campos **Build do SO** e **Tipo de Sistema**.</span><span class="sxs-lookup"><span data-stu-id="8e200-224">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="8e200-225">![Captura de tela dos campos Build e Tipo de Sistema](media/system.png)</span><span class="sxs-lookup"><span data-stu-id="8e200-225">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="8e200-226">Para localizar o número de build do Windows Server, execute o seguinte no PowerShell:</span><span class="sxs-lookup"><span data-stu-id="8e200-226">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="8e200-227">Confirme se o WSL está habilitado</span><span class="sxs-lookup"><span data-stu-id="8e200-227">Confirm WSL is enabled</span></span>

<span data-ttu-id="8e200-228">É possível confirmar se o Subsistema Windows para Linux está habilitado executando o seguinte no PowerShell:</span><span class="sxs-lookup"><span data-stu-id="8e200-228">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="8e200-229">Problemas de conexão do servidor OpenSSH</span><span class="sxs-lookup"><span data-stu-id="8e200-229">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="8e200-230">Falha ao tentar conectar seu servidor SSH com o seguinte erro: "Conexão encerrada pela porta 22, 127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="8e200-230">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="8e200-231">Verifique se o servidor OpenSSH está em execução:</span><span class="sxs-lookup"><span data-stu-id="8e200-231">Make sure your OpenSSH Server is running:</span></span>

   ```bash
   sudo service ssh status
   ```

   <span data-ttu-id="8e200-232">e que você seguiu este tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span><span class="sxs-lookup"><span data-stu-id="8e200-232">and you've followed this tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span></span>

2. <span data-ttu-id="8e200-233">Interrompa o serviço SSHD e inicie o SSHD no modo de depuração:</span><span class="sxs-lookup"><span data-stu-id="8e200-233">Stop the sshd service and start sshd in debug mode:</span></span>

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="8e200-234">Verifique os logs de inicialização e certifique-se de que as HostKeys estejam disponíveis e que você não veja mensagens de log, como:</span><span class="sxs-lookup"><span data-stu-id="8e200-234">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

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

<span data-ttu-id="8e200-235">Se você vir essas mensagens e as chaves estiverem ausentes em `/etc/ssh/`, será necessário regenerar as chaves ou apenas limpar e instalar o servidor OpenSSH:</span><span class="sxs-lookup"><span data-stu-id="8e200-235">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="8e200-236">"Não foi possível encontrar o assembly referenciado."</span><span class="sxs-lookup"><span data-stu-id="8e200-236">"The referenced assembly could not be found."</span></span> <span data-ttu-id="8e200-237">ao habilitar o recurso opcional WSL (Subsistema Windows para Linux)</span><span class="sxs-lookup"><span data-stu-id="8e200-237">when enabling the WSL optional feature</span></span>

<span data-ttu-id="8e200-238">Este erro está relacionado a um estado de instalação inadequado.</span><span class="sxs-lookup"><span data-stu-id="8e200-238">This error is related to being in a bad install state.</span></span> <span data-ttu-id="8e200-239">Conclua as etapas a seguir para tentar corrigir esse problema:</span><span class="sxs-lookup"><span data-stu-id="8e200-239">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="8e200-240">Se você estiver executando o comando Habilitar recurso WSL do PowerShell, tente usar a GUI em vez de abrir o menu Iniciar, pesquisando "Ativar ou desativar recursos do Windows" e, na lista, selecione "Subsistema do Windows para Linux", que instalará o componente opcional.</span><span class="sxs-lookup"><span data-stu-id="8e200-240">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="8e200-241">Atualize sua versão do Windows acessando Configurações, Atualizações e clicando em "Verificar se há atualizações"</span><span class="sxs-lookup"><span data-stu-id="8e200-241">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="8e200-242">Se ambas falharem e você precisar acessar o WSL, considere atualizar no local reinstalando o Windows 10 com uma mídia de instalação e selecionando "Manter Tudo" para que seus aplicativos e arquivos sejam preservados.</span><span class="sxs-lookup"><span data-stu-id="8e200-242">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="8e200-243">É possível encontrar instruções para fazer isso na [página Reinstalar o Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="8e200-243">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>

### <a name="correct-ssh-related-permission-errors"></a><span data-ttu-id="8e200-244">Erros de permissão corretos (relacionados a SSH)</span><span class="sxs-lookup"><span data-stu-id="8e200-244">Correct (SSH related) permission errors</span></span>

<span data-ttu-id="8e200-245">Se você vir este erro:</span><span class="sxs-lookup"><span data-stu-id="8e200-245">If you're seeing this error:</span></span>

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

<span data-ttu-id="8e200-246">Para corrigi-lo, acrescente o seguinte ao arquivo ```/etc/wsl.conf```:</span><span class="sxs-lookup"><span data-stu-id="8e200-246">To fix this, append the following to the the ```/etc/wsl.conf``` file:</span></span>

```
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

<span data-ttu-id="8e200-247">Ao adicionar esse comando, você incluirá metadados e modificará as permissões do arquivo nos arquivos Windows vistos em WSL.</span><span class="sxs-lookup"><span data-stu-id="8e200-247">Please note that adding this command will include metadata and modify the file permissions on the Windows files seen from WSL.</span></span> <span data-ttu-id="8e200-248">Confira as [Permissões do sistema de arquivos](./file-permissions.md) para saber mais.</span><span class="sxs-lookup"><span data-stu-id="8e200-248">Please see the [File System Permissions](./file-permissions.md) for more information.</span></span>
