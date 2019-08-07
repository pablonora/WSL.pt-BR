---
title: Notas de versão do subsistema Windows para Linux
description: Notas de versão do subsistema Windows para Linux.  Atualizado semanalmente.
keywords: BashOnWindows, Bash, WSL, Windows, subsistema Windows para Linux, windowssubsystem, Ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: b03d837e0ab3a371fd676e37b5c65a173824f84c
ms.sourcegitcommit: 9175a28f04573f25338358faf61d73b1a5d1ade6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68832120"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Notas de versão do subsistema Windows para Linux


## <a name="build-18945"></a>Build 18945
Para obter informações gerais do Windows sobre o Build 18945 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).

### <a name="wsl"></a>WSL
* [WSL2] Permitir que Soquetes TCP de escuta em WSL2 sejam acessíveis a partir do host usando localhost: Port
* [WSL2] Correções para falhas de instalação/conversão e diagnóstico adicional para rastrear problemas futuros [GH 4105] 
* [WSL2] Melhorar o diagnóstico de problemas de rede WSL2
* [WSL2] Atualizar a versão do kernel para 4.19.55
* [WSL2] Atualizar o kernel com as opções de configuração necessárias para o Docker [GH 4165]
* [WSL2] Aumente o número de CPUs atribuídas à VM do utilitário leve para ser a mesma do host (anteriormente limitada em 8 por CONFIG_NR_CPUS na configuração do kernel) [GH 4137]
* [WSL2] Criar um arquivo de permuta para a VM leve do WSL2
* [WSL2] Permitir que as montagens de usuário fiquem visíveis \\por meio\\ \\de WSL $ distribuição (por exemplo, sshfs) [GH 4172]
* [WSL2] Melhorar o desempenho do sistema de arquivos 9P
* [WSL2] Garantir que a ACL do VHD não aumente o limite [GH 4126]
* [WSL2] Atualizar a configuração do kernel para dar suporte a squashfs e xt_conntrack [GH 4107, 4123]
* [WSL2] Correção para interoperabilidade. opção/etc/WSL.conf habilitada [GH 4140]
* [WSL2] Retornar ENOTSUP se o sistema de arquivos não der suporte a EAs
* [WSL2] Corrigir a parada CopyFile com \\ \\WSL $
* Mude o umask padrão para 0022 e adicione a configuração FileSystem. umask a/etc/WSL.conf
* Corrigir o wslpath para resolver corretamente o symlinks, isso foi regressivo no 19h1 [GH 4078]
* Introduza o arquivo%\\UserProfile%. wslconfig para ajustar as configurações de WSL2
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a>Build 18917
Para obter informações gerais do Windows sobre o Build 18917 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).

### <a name="wsl"></a>WSL
* WSL 2 já está disponível! Consulte o [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para obter mais detalhes.
* Corrigir uma regressão em que a inicialização de processos do Windows via symlinks não funcionou corretamente [GH 3999]
* Adicione WSL. exe--List--Verbose, WSL. exe--List--Quiet e WSL. exe--Import--opções de versão a WSL. exe
* Adicionar WSL. exe--opção de desligamento
* Plano 9: Permitir que a abertura de um diretório para gravação seja realizada com sucesso

## <a name="build-18890"></a>Build 18890
Para obter informações gerais do Windows sobre o Build 18890 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).

### <a name="wsl"></a>WSL
* Vazamento de soquete sem bloqueio [GH 2913]
* A entrada de EOF para o terminal pode bloquear leituras subsequentes [GH 3421]
* Atualize o cabeçalho de resolução. conf para fazer referência a WSL. conf [discutido no GH 3928]
* Deadlock no código de exclusão de epoll [GH 3922]
* Manipular espaços em argumentos para--Import e – export [GH 3932]
* A extensão de arquivos mmap não funciona corretamente [GH 3939]
* Correção do problema com \\o ARM64 WSL $ Access não funcionar corretamente
* Adicionar melhor ícone padrão para WSL. exe

## <a name="build-18342"></a>Build 18342
Para obter informações gerais do Windows sobre o Build 18342 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Adicionamos a capacidade para os usuários acessarem arquivos do Linux em um WSL distribuição do Windows. Esses arquivos podem ser acessados por meio da linha de comando, e também aplicativos do Windows, como explorador de arquivos, VSCode, etc. podem interagir com esses arquivos. Acesse seus arquivos navegando \\até \\WSL\\$ < distro_name > ou consulte uma lista de distribuições em execução navegando \\até \\WSL $
* Adicionar marcas de informações de CPU adicionais e corrigir os valores de Cpus_allowed [_list] [GH 2234]
* Suporte a exec de thread não líder [GH 3800]
* Tratar falhas de atualização de configuração como não fatal [GH 3785]
* Atualizar binfmt para lidar corretamente com os deslocamentos [GH 3768]
* Habilitar o mapeamento de unidades de rede para o plano 9 [GH 3854]
* Suporte para Windows-> Linux e Linux-> Tradução de caminho do Windows para montagens de associação
* Criar seções somente leitura para mapeamentos em arquivos abertos somente leitura

## <a name="build-18334"></a>Build 18334
Para obter informações gerais do Windows sobre o Build 18334 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Reprojetar a maneira como o fuso horário do Windows é mapeado para um fuso horário do Linux [GH 3747]
* Corrigir vazamentos de memória e adicionar novas funções de conversão de cadeia de caracteres [GH 3746]
* SIGCONT em um thread sem threads é um não operacional [GH 3741] 
* Exibir corretamente os descritores de arquivo de soquete e epoll no/proc/Self/FD

## <a name="build-18305"></a>Build 18305
Para obter informações gerais do Windows sobre o Build 18305 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* pthreads perder o acesso a arquivos quando o thread primário sair [GH 3589]
* TIOCSCTTY deve ignorar o parâmetro "Force", a menos que seja necessário [GH 3652]
* melhorias na linha de comando do WSL. exe e adição de funcionalidade de importação/exportação.
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a>Build 18277
Para obter informações gerais do Windows sobre o Build 18277 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Corrigir o erro "não há suporte para essa interface" introduzido na compilação 18272 [GH 3645]
* Ignorar o sinalizador MNT_FORCE para o syscall umount [GH 3605]
* Alternar a interoperabilidade WSL para usar a API CreatePseudoConsole oficial
* Manter nenhum valor de tempo limite durante a reinicialização de FUTEX_WAIT

## <a name="build-18272"></a>Build 18272
Para obter informações gerais do Windows sobre o Build 18272 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **ALERTA** Há um problema nessa compilação que torna o WSL inoperante. Ao tentar iniciar sua distribuição, você verá um erro "nenhuma interface com suporte". O problema foi corrigido e estará na compilação rápida do insider da próxima semana. Se você tiver instalado essa compilação, poderá reverter para a compilação anterior do Windows usando "voltar para a versão anterior do Windows 10" em Settings-> Update & Security-> Recovery.

## <a name="build-18267"></a>Build 18267
Para obter informações gerais do Windows sobre o Build 18267 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Correção do problema em que o processo zumbi pode não ser aproveitado e permanecer indefinidamente.
* WslRegisterDistribution paralisa se a mensagem de erro exceder o comprimento máximo [GH 3592]
* Permitir que o fsync tenha sucesso para arquivos somente leitura no DrvFs [GH 3556]
* Verifique se os diretórios/bin e/sbin existem antes de criar symlinks dentro de [GH 3584]
* Adicionou um mecanismo de tempo limite de encerramento de instância para instâncias de WSL. O tempo limite é definido atualmente como 15 segundos, o que significa que a instância será encerrada 15 segundos após o último processo de WSL sair. Para encerrar uma distribuição imediatamente, use:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Build 17763 (1809)
Para obter informações gerais do Windows sobre o Build 17763 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* Verificação de permissão syscall setanteriority muito estrita para alterar a mesma prioridade de thread [GH 1838]
* Verifique se o tempo de interrupção não polarizado é usado para o tempo de inicialização para evitar retornar valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]
* Tratar symlinks no intérprete WSL binfmt [GH 3424]
* Melhor manipulação da limpeza do descritor de arquivo de líder do grupo de threads.
* Alterne WSL para usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter para evitar o estouro [GH 3252]
* A anexação ptrace pode causar um valor de retorno insatisfatório de chamadas do sistema [GH 1731]
* Corrigir vários problemas relacionados ao AF_UNIX [GH 3371]
* Correção do problema que poderia causar falha de interoperabilidade WSL se o diretório de trabalho atual tiver menos de 5 caracteres [GH 3379]
* Evite um segundo atraso na falha de conexões de loopback para portas inexistentes [GH 3286]
* Adicionar arquivo stub/proc/sys/FS/File-Max [GH 2893]
* Informações mais precisas sobre o escopo do IPV6.
* Suporte do PR_SET_PTRACER [GH 3053]
* O sistema de arquivos de pipe inadvertidamente limpa o evento epoll disparado por borda [GH 3276]
* O executável do Win32 iniciado via NTFS symlink não respeita o symlink Name [GH 2909]
* Suporte ao zumbi melhorado [GH 1353]
* Adicionar entradas WSL. conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correção para getsockname nem sempre retornando tipo de família de soquetes UNIX [GH 1774]
* Adicionar suporte para TIOCSTI [GH 1863]
* Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]
* Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]
* Corrigir o problema de verificação de permissão na pasta raiz [GH 3304]
* Suporte limitado para os IOCTLs de teclado TTY KDGKBTYPE, KDGKBMODE e KDSKBMODE.
* Os aplicativos da interface do usuário do Windows devem ser executados mesmo quando iniciados em segundo plano.
* Adicionar a opção WSL-u ou--User [GH 1203]
* Corrigir problemas de inicialização do WSL quando a inicialização rápida estiver habilitada [GH 2576]
* Os soquetes UNIX precisam reter as credenciais de pares desconectados [GH 3183]
* Soquetes UNIX sem bloqueio com falha indefinidamente com EAGAIN [GH 3191]
* Case = off é o novo tipo de montagem de drvfs padrão [GH 2937, 3212, 3328]
    * Consulte o [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.
* Adicione wslconfig/Terminate para interromper a execução de distribuições.
* Corrija o problema com as entradas do menu de contexto do Shell WSL que não manipulam corretamente caminhos com espaços.
* Expor a diferenciação de maiúsculas e minúsculas por diretório como um atributo estendido
* ARM64 Emular operações de manutenção de cache. Resolver o [problema dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs: apenas caracteres de escape de saída no intervalo privado que correspondem a um caractere de escape.
* Corrigir erro off-by-One na validação de comprimento do interpretador ELF [GH 3154]
* WSL timers absolutos com um tempo no passado não são disparados [GH 3091]
* Verifique se os pontos de nova análise criados recentemente estão listados como tal no diretório pai.
* Crie de forma atômica diretórios que diferenciam maiúsculas de minúsculas no DrvFs.
* Correção de um problema adicional em que operações multi-threaded podiam retornar ENOENT mesmo que o arquivo exista. [GH 2712]
* Correção da falha de inicialização do WSL quando o UMCI está habilitado. [GH 3020]
* Adicione o menu de contexto do Explorer para iniciar o WSL [GH 437, 603, 1836]. Para usar, mantenha Shift e clique com o botão direito do mouse quando estiver em uma janela do Explorer.
* Corrigir comportamento de não bloqueio de soquete do UNIX [GH 2822, 3100]
* Corrija o comando do NetLink suspenso conforme relatado no GH 2026.
* Adicionar suporte para os sinalizadores de propagação de montagem [GH 2911].
* Correção do problema com truncamento não causando eventos INotifyPropertyChanged [GH 2978].
* Adicione a opção--exec para WSL. exe para invocar um único binário sem um shell.
* Adicionar--opção de distribuição para WSL. exe para selecionar um distribuição específico.
* Suporte limitado para dmesg. Os aplicativos agora podem fazer logon no dmesg. O driver WSL registra informações limitadas no dmesg. No futuro, isso pode ser estendido para transportar outras informações/diagnósticos do driver.
    * Observação: no momento, há suporte para `/dev/kmsg` dmesg por meio da interface do dispositivo. `syslog`Ainda não há suporte para a interface syscall. E, portanto, algumas das opções `dmesg` `-S`de linha de comando, como `-C` , não funcionam.
* Alterar o GID e o modo padrão de dispositivos seriais para corresponder ao nativo [GH 3042]
* O DrvFs agora dá suporte a atributos estendidos.
    * Observação: DrvFs tem algumas limitações sobre o nome dos atributos estendidos. Alguns caracteres (como '/', ': ' e '\*') não são permitidos e os nomes de atributos estendidos não diferenciam maiúsculas de minúsculas em DrvFs

## <a name="build-18252-skip-ahead"></a>Build 18252 (pular para a frente)
Para obter informações gerais do Windows sobre o Build 18252 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Mover os binários init e bsdtar para fora do lxssmanager dll e para uma pasta de ferramentas separada
* Corrigir a corrida ao fechar o descritor de arquivo ao usar o CLONE_FILES
* Manipular campos opcionais no/proc/pid/mountinfo ao traduzir caminhos de DrvFs
* Permitir que DrvFs mknod tenha sucesso sem suporte de metadados para S_IFREG
* Os arquivos ReadOnly criados em DrvFs devem ter o atributo ReadOnly definido [GH 3411]
* Adicionar o auxiliar/sbin/mount.drvfs para lidar com a montagem de DrvFs
* Use renomeação POSIX em DrvFs.
* Permitir tradução de caminho em volumes sem um GUID de volume.

## <a name="build-17738-fast"></a>Build 17738 (rápido)
Para obter informações gerais do Windows sobre o Build 17738 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* Verificação de permissão syscall setanteriority muito estrita para alterar a mesma prioridade de thread [GH 1838]
* Verifique se o tempo de interrupção não polarizado é usado para o tempo de inicialização para evitar retornar valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]
* Tratar symlinks no intérprete WSL binfmt [GH 3424]
* Melhor manipulação da limpeza do descritor de arquivo de líder do grupo de threads.

## <a name="build-17728-fast"></a>Build 17728 (rápido)
Para obter informações gerais do Windows sobre o Build 17728 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Alterne WSL para usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter para evitar o estouro [GH 3252]
* A anexação ptrace pode causar um valor de retorno insatisfatório de chamadas do sistema [GH 1731]
* Corrigir vários problemas relacionados ao AF_UNIX [GH 3371]
* Correção do problema que poderia causar falha de interoperabilidade WSL se o diretório de trabalho atual tiver menos de 5 caracteres [GH 3379]

## <a name="build-18204-skip-ahead"></a>Build 18204 (pular para a frente)
Para obter informações gerais do Windows sobre o Build 18204 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Inadvertenly do sistema de arquivos de pipe limpando o evento epoll disparado por borda [GH 3276]
* O executável do Win32 iniciado via NTFS symlink não respeita o symlink Name [GH 2909]

## <a name="build-17723-fast"></a>Build 17723 (rápido)
Para obter informações gerais do Windows sobre o Build 17723 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Evite um segundo atraso na falha de conexões de loopback para portas inexistentes [GH 3286]
* Adicionar arquivo stub/proc/sys/FS/File-Max [GH 2893]
* Informações mais precisas sobre o escopo do IPV6.
* Suporte do PR_SET_PTRACER [GH 3053]
* Inadvertenly do sistema de arquivos de pipe limpando o evento epoll disparado por borda [GH 3276]
* O executável do Win32 iniciado via NTFS symlink não respeita o symlink Name [GH 2909]

## <a name="build-17713"></a>Build 17713
Para obter informações gerais do Windows sobre o Build 17713 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Suporte ao zumbi melhorado [GH 1353]
* Adicionar entradas WSL. conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correção para getsockname nem sempre retornando tipo de família de soquetes UNIX [GH 1774]
* Adicionar suporte para TIOCSTI [GH 1863]
* Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]
* Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]
* Corrigir o problema de verificação de permissão na pasta raiz [GH 3304]
* Suporte limitado para os IOCTLs de teclado TTY KDGKBTYPE, KDGKBMODE e KDSKBMODE.
* Os aplicativos da interface do usuário do Windows devem ser executados mesmo quando iniciados em segundo plano.

## <a name="build-17704"></a>Build 17704
Para obter informações gerais do Windows sobre o Build 17704 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Adicionar a opção WSL-u ou--User [GH 1203]
* Corrigir problemas de inicialização do WSL quando a inicialização rápida estiver habilitada [GH 2576]
* Os soquetes UNIX precisam reter as credenciais de pares desconectados [GH 3183]
* Soquetes UNIX sem bloqueio com falha indefinidamente com EAGAIN [GH 3191]
* Case = off é o novo tipo de montagem de drvfs padrão [GH 2937, 3212, 3328]
    * Consulte o [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.
* Adicione wslconfig/Terminate para interromper a execução de distribuições.

## <a name="build-17692"></a>Build 17692
Para obter informações gerais do Windows sobre o Build 17692 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Corrija o problema com as entradas do menu de contexto do Shell WSL que não manipulam corretamente caminhos com espaços.
* Expor a diferenciação de maiúsculas e minúsculas por diretório como um atributo estendido
* ARM64 Emular operações de manutenção de cache. Resolver o [problema dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs: apenas caracteres de escape de saída no intervalo privado que correspondem a um caractere de escape.

## <a name="build-17686"></a>Build 17686
Para obter informações gerais do Windows sobre o Build 17686 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Corrigir erro off-by-One na validação de comprimento do interpretador ELF [GH 3154]
* WSL timers absolutos com um tempo no passado não são disparados [GH 3091]
* Verifique se os pontos de nova análise criados recentemente estão listados como tal no diretório pai.
* Crie de forma atômica diretórios que diferenciam maiúsculas de minúsculas no DrvFs.

## <a name="build-17677"></a>Build 17677
Para obter informações gerais do Windows sobre o Build 17677 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Correção de um problema adicional em que operações multi-threaded podiam retornar ENOENT mesmo que o arquivo exista. [GH 2712]
* Correção da falha de inicialização do WSL quando o UMCI está habilitado. [GH 3020]

## <a name="build-17666"></a>Build 17666
Para obter informações gerais do Windows sobre o Build 17666 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>AVISO: Há um problema que impede a execução do WSL em alguns chipsets AMD [GH 3134]. Uma correção está pronta e preparando-se para o Branch do insider Build.
* Adicione o menu de contexto do Explorer para iniciar o WSL [GH 437, 603, 1836]. Para usar manter pressionada e clicar com o botão direito do mouse quando estiver em uma janela do Explorer.
* Corrigir comportamento de não bloqueio de soquete do UNIX [GH 2822, 3100]
* Corrija o comando do NetLink suspenso conforme relatado no GH 2026.
* Adicionar suporte para os sinalizadores de propagação de montagem [GH 2911].
* Correção do problema com truncamento não causando eventos INotifyPropertyChanged [GH 2978].
* Adicione a opção--exec para WSL. exe para invocar um único binário sem um shell.
* Adicionar--opção de distribuição para WSL. exe para selecionar um distribuição específico.

## <a name="build-17655-skip-ahead"></a>Build 17655 (pular para a frente)
Para obter informações gerais do Windows sobre o Build 17655 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Suporte limitado para dmesg. Os aplicativos agora podem fazer logon no dmesg. O driver WSL registra informações limitadas no dmesg. No futuro, isso pode ser estendido para transportar outras informações/diagnósticos do driver.
    * Observação: no momento, há suporte para `/dev/kmsg` dmesg por meio da interface do dispositivo. `syslog`Ainda não há suporte para a interface sycall. E, portanto, algumas das opções `dmesg` `-S`de linha de comando, como `-C` , não funcionam.
* Correção de um problema em que as operações multi-threaded podiam retornar ENOENT, mesmo que o arquivo exista. [GH 2712]

## <a name="build-17639-skip-ahead"></a>Build 17639 (pular para a frente)
Para obter informações gerais do Windows sobre o Build 17639 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Alterar o GID e o modo padrão de dispositivos seriais para corresponder ao nativo [GH 3042]
* O DrvFs agora dá suporte a atributos estendidos.
    * Observação: DrvFs tem algumas limitações sobre o nome dos atributos estendidos. Em particular, alguns caracteres (como '/', ': ' e '\*') não são permitidos, e os nomes de atributos estendidos não diferenciam maiúsculas de minúsculas em DrvFs

## <a name="build-17133-fast"></a>Build 17133 (rápido)
Para obter informações gerais do Windows sobre o Build 17133 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Correção para o travamento no WSL. [GH 3039, 3034]

## <a name="build-17128-fast"></a>Build 17128 (rápido)
Para obter informações gerais do Windows sobre o Build 17128 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* Nenhum

## <a name="build-17627-skip-ahead"></a>Build 17627 (pular para a frente)
Para obter informações gerais do Windows sobre o Build 17627 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Adicione suporte para as operações que reconhecem o Futex PI. [GH 1006]
    * Observe que as prioridades não são atualmente um recurso WSL com suporte para que haja limitações, mas o uso padrão deve ser desbloqueado.
* Suporte do firewall do Windows para processos WSL. [GH 1852]
    * Por exemplo, para permitir que o processo Python WSL escute em qualquer porta, use o cmd do Windows com privilégios elevados:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Para obter detalhes adicionais sobre como adicionar regras de firewall, consulte [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Respeitar o shell padrão do usuário ao usar WSL. exe. [GH 2372]
* Relatar todas as interfaces de rede como Ethernet. [GH 2996]
* Melhor manipulação do arquivo/etc/passwd corrompido. [GH 3001]

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17618-skip-ahead"></a>Build 17618 (pular para a frente)
Para obter informações gerais do Windows sobre o Build 17618 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Introduza a funcionalidade pseudoconsole para NT Interop [GH 988, 1366, 1433, 1542, 2370, 2406].
* O mecanismo de instalação herdado (lxrun. exe) foi preterido. O mecanismo com suporte para a instalação de distribuições é por meio do Microsoft Store.

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17110"></a>Build 17110
Para obter informações gerais do Windows sobre o Build 17110 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Permitir que/init seja encerrado do Windows [GH 2928].
* O DrvFs agora usa a diferenciação de maiúsculas e minúsculas por diretório por padrão (equivalente à opção de montagem "Case = dir").
    * Usar "Case = Force" (o comportamento antigo) requer a definição de uma chave do registro. Execute o seguinte comando para habilitar "Case = Force" se você precisar usá-lo: reg Add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1
    * Se você tiver diretórios existentes criados com WSL na versão anterior do Windows que precisam diferenciar maiúsculas de minúsculas, use fsutil. exe para marcá-los como diferenciação de maiúsculas e minúsculas: fsutil. exe file setcasesensitiveinfo <path> Enable
* Cadeias de caracteres de término nulas retornadas da syscall uname.

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17107"></a>Build 17107
Para obter informações gerais do Windows sobre o Build 17107 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Suporte a TCSETSF e TCSETSW nos pontos de extremidade mestre PTY [GH 2552].
* Iniciar processos de interoperabilidade simultâneas pode resultar em EINVAL [GH 2813].
* Corrija PTRACE_ATTACH para mostrar o status de rastreamento adequado em/proc/pid/status.
* Corrija a corrida em que os processos de curta duração clonados com os sinalizadores CLEARTID e dsvid podem sair sem limpar o endereço de TID.
* Exiba uma mensagem ao atualizar os diretórios do sistema de arquivos do Linux ao mudar de uma compilação anterior à 17093. Para obter mais detalhes sobre as alterações do sistema de arquivos 17093, consulte as notas de versão para [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17101"></a>Build 17101
Para obter informações gerais do Windows sobre o Build 17101 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Suporte para signalfd. [GH 129]
* Suporte a nomes de arquivos que contêm caracteres NTFS ilegais codificando-os como caracteres Unicode privados. [GH 1514]
* A montagem automática fará fallback para somente leitura quando não houver suporte para gravação. [GH 2603]
* Permitir colagem de pares substitutos Unicode (como caracteres de Emoji). [GH 2765]
* Pseudo-arquivos em/proc e/sys devem retornar leitura e gravação prontos de Select, votação, epoll, et al. [GH 2838]
* Correção do problema que pode fazer com que o serviço entre em loop infinito quando o registro foi adulterado ou está corrompido.
* Corrija as mensagens do NetLink para trabalhar com a versão mais recente (upstream 4,14) do iproute2.

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17093"></a>Build 17093
Para obter informações gerais do Windows sobre o Build 17093 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Importante:
Ao iniciar o WSL pela primeira vez após a atualização para essa compilação, ele precisa executar algum trabalho atualizando os diretórios do sistema de arquivos do Linux. Isso pode levar até vários minutos, então WSL pode parecer ser iniciado lentamente. Isso só deve ocorrer uma vez para cada distribuição instalada por meio da loja.
* Suporte de distinção de maiúsculas e minúsculas aprimorado no DrvFs.
    * O DrvFs agora dá suporte à distinção de maiúsculas e minúsculas por diretório. Esse é um novo sinalizador que pode ser definido em diretórios para indicar que todas as operações nesses diretórios devem ser tratadas como diferenciando maiúsculas de minúsculas, o que permite até que os aplicativos do Windows Abram corretamente arquivos que diferem apenas por maiúsculas e minúsculas.
    * DrvFs tem novas opções de montagem que controlam a diferenciação de maiúsculas e minúsculas em uma base por diretório
        * Case = Force: todos os diretórios são tratados como diferenciando maiúsculas de minúsculas (exceto para a raiz da unidade). Os novos diretórios criados com WSL são marcados como diferenciando maiúsculas de minúsculas. Esse é o comportamento herdado, exceto para marcar novos diretórios como diferenciar maiúsculas de minúsculas.
        * Case = dir: somente os diretórios com o sinalizador de sensibilidade de caso por diretório são tratados como diferenciando maiúsculas de minúsculas; outros diretórios não diferenciam maiúsculas de minúsculas. Os novos diretórios criados com WSL são marcados como diferenciando maiúsculas de minúsculas.
        * Case = off: somente os diretórios com o sinalizador de sensibilidade de caso por diretório são tratados como diferenciando maiúsculas de minúsculas; outros diretórios não diferenciam maiúsculas de minúsculas. Os novos diretórios criados com WSL são marcados como não diferencia maiúsculas de minúsculas.
    * Observação: os diretórios criados por WSL em versões anteriores não têm esse sinalizador definido, portanto, não serão tratados como diferenciação de maiúsculas e minúsculas se você usar a opção "Case = dir". Uma maneira de definir esse sinalizador em diretórios existentes estará disponível em breve.
    * Exemplo de montagem com essas opções (para unidades existentes, você deve primeiro desmontar antes de poder montar com opções diferentes): sudo mount-t drvfs C:/mnt/c-o case = dir
    * Por enquanto, Case = Force ainda é a opção padrão. Isso será alterado para Case = dir no futuro.
* Agora você pode usar barras invertidas em caminhos do Windows ao montar DrvFs, por exemplo: sudo mount-t DrvFs//Server/share/mnt/share
* WSL agora processa o arquivo/etc/fstab durante o início da instância [GH 2636].
    * Isso é feito antes da montagem automática de unidades de DrvFs; todas as unidades que já foram montadas pelo fstab não serão remontadas automaticamente, permitindo que você altere o ponto de montagem de unidades específicas.
    * Esse comportamento pode ser desativado usando WSL. conf.
* Os arquivos Mount, mountinfo e mountstats no/proc escapar corretamente caracteres especiais, como barras invertidas e espaços [GH 2799]
* Arquivos especiais criados com DrvFs, como links simbólicos do WSL, ou FIFOs e soquetes quando os metadados estão habilitados, agora podem ser copiados e movidos do Windows.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL é mais configurável com WSL. conf
Adicionamos um método para configurar automaticamente determinadas funcionalidades no WSL que serão aplicadas toda vez que você iniciar o subsistema. Isso inclui opções de montagem automática e configuração de rede. Saiba mais sobre isso em nossa postagem no blog em: https://aka.ms/wslconf

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX permite conexões de soquete entre processos do Linux em processos nativos do WSL e do Windows
Os aplicativos WSL e Windows agora podem se comunicar entre si por meio de soquetes UNIX. Imagine que você deseja executar um serviço no Windows e disponibilizá-lo para aplicativos do Windows e do WSL. Agora, isso é possível com os soquetes do UNIX. Leia mais em nossa postagem no blog em https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Suporte a mmap () com MAP_NORESERVE [GH 121, 2784]
* Suporte a CLONE_PTRACE e CLONE_UNTRACED [GH 121, 2781]
* Manipular o sinal de encerramento não SIGCHLD no clone [GH 121, 2781]
* Stub/proc/sys/FS/inotify/max_user_instances e/proc/sys/FS/inotify/max_user_watches [GH 1705]
* Erro ao carregar binários ELF que contêm cabeçalhos de carga com deslocamentos diferentes de zero [GH 1884]
* Zero os bytes de página à direita ao carregar imagens.
* Reduzir os casos em que o execve encerra o processo silenciosamente

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17083"></a>Build 17083
Para obter informações gerais do Windows sobre o Build 17083 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Correção de verificação relacionada a epoll [GH 2798, 2801, 2857]
* Correção de travamentos ao desativar ASLR [GH 1185, 2870]
* Garantir que as operações mmap apareçam atômicas [GH 2732]

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17074"></a>Build 17074
Para obter informações gerais do Windows sobre o Build 17074 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Formato de armazenamento fixo de metadados DrvFs [GH 2777] </br>
**Importante:** Os metadados DrvFs criados antes dessa compilação serão exibidos incorretamente ou não. Para corrigir os arquivos afetados, use chmod e aldelet para aplicar novamente os metadados.
* Corrigido o problema com vários sinais e syscalls reiniciável.

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17063"></a>Build 17063
Para obter informações gerais do Windows sobre o Build 17063 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* O DrvFs dá suporte a metadados adicionais do Linux. Isso permite definir o proprietário e o modo de arquivos usando chmod/alownerion e também a criação de arquivos especiais, como FIFOs, soquetes UNIX e arquivos de dispositivo. Isso é desabilitado por padrão por enquanto, pois ainda é experimental.
**Observação:**  Corrigimos um bug no formato de metadados usado pelo DrvFs. Embora os metadados funcionem nesse Build para experimentação, as compilações futuras não lêem corretamente os metadados criados por essa compilação.  Talvez seja necessário atualizar manualmente o proprietário para arquivos modificados e os dispositivos com uma ID de dispositivo personalizada precisarão ser recriados.

  Para habilitar, monte DrvFs com a opção de metadados (para habilitá-lo em uma montagem existente, você deve primeiro desmontá-lo):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  As permissões do Linux são adicionadas como metadados adicionais ao arquivo; Eles não afetam as permissões do Windows.  Lembre-se de que a edição de um arquivo usando um editor do Windows pode remover os metadados. Nesse caso, o arquivo será revertido para suas permissões padrão.

* Adição de opções de montagem a DrvFs para controlar arquivos sem metadados.
  * UID: a ID de usuário usada para o proprietário de todos os arquivos.
  * GID: a ID do grupo usada para o proprietário de todos os arquivos.
  * umask: uma máscara octal de permissões a serem excluídas para todos os arquivos e diretórios.
  * fMask: uma máscara octal de permissões a serem excluídas para todos os arquivos regulares.
  * dmask: uma máscara octal de permissões a serem excluídas para todos os diretórios.

  Por exemplo:
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Combine com a opção de metadados para especificar permissões padrão para arquivos sem metadados.

* Introduziu uma nova variável de `WSLENV`ambiente,, para configurar como as variáveis de ambiente fluem entre WSL e Win32.

  Por exemplo:

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV`é uma lista delimitada por dois-pontos de variáveis de ambiente que pode ser incluída ao iniciar processos de WSL de processos Win32 ou Win32 de WSL.  Cada variável pode ser sufixada com uma barra seguida por sinalizadores para especificar como ela é traduzida.
  * DTI O valor é um caminho que deve ser convertido entre caminhos WSL e caminhos Win32.
  * debug O valor é uma lista de caminhos. No WSL, é uma lista delimitada por dois-pontos. No Win32, é uma lista delimitada por ponto-e-vírgula.
  * t O valor só deve ser incluído ao invocar WSL do Win32
  * Mostrar O valor só deve ser incluído ao invocar o Win32 de WSL

  Você pode definir `WSLENV` em. bashrc ou no ambiente personalizado do Windows para seu usuário.

* montagens de drvfs preserva corretamente os carimbos de data/hora do tar, CP-p (GH 1939)
* drvfs symlinks relate o tamanho correto (GH 2641)
* leitura/gravação funciona para tamanhos de e/s muito grandes (GH 2653)
* waitpid trabalha com IDs de grupo de processos (GH 2534)
* desempenho de mmap significativamente melhorado para grandes regiões de reserva; melhora o desempenho do GHC (GH 1671)
* suporte a personalidades para READ_IMPLIES_EXEC; corrige máximo e CLISP (GH 1185)
* MProtect dá suporte a PROT_GROWSDOWN; Corrige CLISP (GH 1128)
* correções de falhas de página no modo de excesso de confirmação; corrige SBCL (GH 1128)
* o clone dá suporte a mais combinações de sinalizadores
* Suporte Select/epoll de arquivos epoll (anteriormente um não op).
* Notificar ptrace de syscalls não implementados.
* Ignorar interfaces que não estão em funcionamento ao gerar nomes de resolução. conf [GH 2694]
* Enumere as interfaces de rede sem endereço físico. [GH 2685]
* Correções e aprimoramentos de bugs adicionais.

### <a name="linux-tools-available-to-developers-on-windows"></a>Ferramentas do Linux disponíveis para desenvolvedores no Windows

* A linha de comando do Windows ferramentas inclui bsdtar (tar) e ondulação.
  Leia [este blog](https://aka.ms/tarcurlwindows) para saber mais sobre a adição dessas duas novas ferramentas e veja como elas estão moldando a experiência do desenvolvedor no Windows.

*   `AF_UNIX`está disponível no SDK do Windows Insider (17061 +).
  Leia [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para saber mais sobre `AF_UNIX` como os desenvolvedores do Windows podem usá-lo.

### <a name="console"></a>Console
* Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.


## <a name="build-17046"></a>Build 17046

Para obter informações gerais do Windows sobre o Build 17046 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Permitir que processos sejam executados sem um terminal ativo. [GH 709, 1007, 1511, 2252, 2391, et al.]
- Melhor suporte a CLONE_VFORK e CLONE_VM. [GH 1878, 2615]
- Ignorar drivers de filtro de TDI para operações de rede WSL. [GH 1554]
- DrvFs cria NT symlinks quando determinadas condições são atendidas. [GH 353, 1475, 2602]
    - O destino do link deve ser relativo, não deve cruzar nenhum ponto de montagem ou symlinks e deve existir.
    - O usuário deve ter SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (isso normalmente requer que você inicie o WSL. exe com privilégios elevados), a menos que o modo de desenvolvedor esteja ativado.
    - Em todas as outras situações, o DrvFs ainda cria WSL symlinks.
- Permitir a execução de instâncias de WSL elevadas e não elevadas simultaneamente.
- Suporte a/proc/sys/kernel/yama/ptrace_scope
- Adicione wslpath ao WSL <-> conversões de caminho do Windows. [GH 522, 1243, 1834, 2327, et al.]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Console
- Sem correções.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.


## <a name="build-17040"></a>Build 17040

Para obter informações gerais do Windows sobre o Build 17040 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Nenhuma correção desde 17035.

#### <a name="console"></a>Console
- Nenhuma correção desde 17035.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17035"></a>Build 17035

Para obter informações gerais do Windows sobre o Build 17035 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- O acesso a arquivos em DrvFs pode ocasionalmente falhar com EINVAL. [GH 2448]

#### <a name="console"></a>Console
- Alguma perda de cor ao inserir/excluir linhas no modo VT.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17025"></a>Build 17025

Para obter informações gerais do Windows sobre o Build 17025 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Inicie os processos iniciais em um novo grupo de processo de primeiro plano [GH 1653, 2510].
- Correções de entrega SIGHUP [GH 2496].
- Gere o nome de ponte virtual padrão se nenhum for fornecido [GH 2497].
- Implemente/proc/sys/kernel/Random/boot_id [GH 2518].
- Mais correções de pipe stdout/stderr de interoperabilidade.
- Chamada do sistema syncfs de stub.

#### <a name="console"></a>Console
- Corrigir a conversão de VT de entrada para consoles de terceiros [GH 111]

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="build-17017"></a>Build 17017

Para obter informações gerais do Windows sobre o Build 17017 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Ignorar cabeçalhos de programa ELF vazios [GH 330].
- Permitir que o LxssManager Crie instâncias WSL para usuários não interativos (SSH e suporte a tarefas agendadas) [GH 777, 1602].
- Suporte ao WSL-> Win32-> os cenários de WSL ("criação") [GH 1228].
- Suporte limitado para encerramento de aplicativos de console invocados via Interop [GH 1614].
- Suporte a opções de montagem para devpts [GH 1948].
- Ptrace bloqueando a inicialização do filho [GH 2333].
- EPOLLET faltam alguns eventos [GH 2462].
- Retornar mais dados para PTRACE_GETSIGINFO.
- Getolgas com lseek fornece resultados incorretos.
- Corrija algumas travas do aplicativo de interoperabilidade Win32, aguardando a entrada em um pipe que não tenha mais dados.
- Suporte a O_ASYNC para arquivos TTY/PTY.
- Melhorias e correções de bugs adicionais

#### <a name="console"></a>Console
- Nenhuma alteração relacionada ao console nesta versão.

### <a name="ltp-results"></a>Resultados do LTP:
Teste em andamento.

## <a name="fall-creators-update"></a>Atualização do Fall Creators

## <a name="build-16288"></a>Build 16288

Para obter informações gerais do Windows sobre o Build 16288 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Inicializar corretamente e reportar UID, GID e modo para descritores de arquivo de soquete [GH 2490]
- Melhorias e correções de bugs adicionais

#### <a name="console"></a>Console
- Nenhuma alteração relacionada ao console nesta versão.

### <a name="ltp-results"></a>Resultados do LTP:
Nenhuma alteração desde 16273

## <a name="build-16278"></a>Build 16278

Para obter informações gerais do Windows sobre o Build 162738 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Desmapear explicitamente exibições mapeadas de seções com backup de arquivo ao dividir o estado LX MM [GH 2415]
- Melhorias e correções de bugs adicionais

#### <a name="console"></a>Console
- Nenhuma alteração relacionada ao console nesta versão.

### <a name="ltp-results"></a>Resultados do LTP:
Nenhuma alteração desde 16273

## <a name="build-16275"></a>Build 16275

Para obter informações gerais do Windows sobre o Build 162735 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Nenhuma alteração relacionada ao WSL nesta versão.

#### <a name="console"></a>Console
- Nenhuma alteração relacionada ao console nesta versão.

### <a name="ltp-results"></a>Resultados do LTP:
Nenhuma alteração desde 16273

## <a name="build-16273"></a>Build 16273

Para obter informações gerais do Windows sobre o Build 16273 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Corrigido um problema em que DrvFs às vezes relatou o tipo de arquivo errado para diretórios [GH 2392]
- Permitir a criação de soquetes NETLINK_KOBJECT_UEVENT para desbloquear programas que usam UEVENT [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- Adicionar suporte para conexão sem bloqueio [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- Implementar o sinalizador de chamada do sistema clone CLONE_FS [GH 2242]
- Corrigir problemas em relação a não lidar com guias ou aspas corretamente no NT Interop [GH 1625, 2164]
- Resolver erro de acesso negado ao tentar iniciar novamente instâncias de WSL [GH 651, 2095]
- Implementar operações Futex FUTEX_REQUEUE e FUTEX_CMP_REQUEUE [GH 2242]
- Corrigir permissões para vários arquivos SysFs [GH 2214]
- Corrigir o travamento da pilha do Haskell durante a instalação [GH 2290]
- Implementar sinalizadores ' C ' ' O ' e ' P ' do binfmt_misc [GH 2103]
- Adicionar/proc/sys/kernel/SHMMAX/shmmni &/threads-Max [GH 1753]
- Adicionar suporte parcial para chamada do sistema ioprio_set [GH 498]
- SO_REUSEPORT de stub & Adicionar suporte para SO_PASSCRED para soquetes NetLink [GH 69]
- Retornar códigos de erro diferentes de RegisterDistribuiton se uma distribuição estiver sendo instalada ou desinstalado no momento.
- Permitir o cancelamento de registro de distribuições de WSL parcialmente instaladas por meio de wslconfig. exe
- Corrigir o travamento do teste de soquete Python do UDP:: MSG_PEEK
- Melhorias e correções de bugs adicionais

#### <a name="console"></a>Console
- Nenhuma alteração relacionada ao console nesta versão.

### <a name="ltp-results"></a>Resultados do LTP:
Total de testes: 1904<br/>
Total de testes ignorados: 209<br/>
Total de falhas: 229<br/>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Build 16257

Para obter informações gerais do Windows sobre o Build 16257 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Implementar chamada do sistema prlimit64
- Adicionar suporte para ulimit-n (setrlimit RLIMIT_NOFILE) [GH 1688]
- MSG_MORE de stub para Soquetes TCP [GH 2351]
- Corrigir comportamento de vetor auxiliar AT_EXECFN inválido [GH 2133]
- Corrigir comportamento de copiar/colar para console/TTY e adicionar melhor manipulação de buffer completo [GH 2204, 2131]
- Definir AT_SECURE em vetor auxiliar para programas Set-User-ID e Set-Group-ID [GH 2031]
- Psuedo-ponto de extremidade do terminal mestre não tratando TIOCPGRP [GH 1063]
- Corrigir o lseek faz para rebobinar diretórios no LxFs [GH 2310]
- /dev/ptmx trava após uso intenso [GH 1882]
- Melhorias e correções de bugs adicionais

#### <a name="console"></a>Console
- Correção para linhas horizontais/sublinhados em todos os lugares [GH 2168]
- Correção para a ordem de processo alterada, tornando o NPM mais difícil de fechar [GH 2170]
- Adicionou nosso novo esquema de cores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>Resultados do LTP:
Nenhuma alteração desde 16251

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`prlimit64`<br/>

### <a name="known-issues"></a>Problemas Conhecidos
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[Problema do GitHub 2392: Pastas do Windows não reconhecidas pelo WSL...](https://github.com/Microsoft/BashOnWindows/issues/2392)
No Build 16257, WSL tem problemas ao enumerar arquivos/pastas do Windows `/mnt/c/...`via.
Esse problema foi corrigido e deve ser liberado na criação de insiders durante a semana, começando em 8/14/2017.

<br/>

## <a name="build-16251"></a>Build 16251

Para obter informações gerais do Windows sobre o Build 16251 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Remova a marca beta do componente opcional WSL, confira postagem no [blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obter detalhes.
- Inicializar corretamente UID e GID salvos para os binários Set-User-ID e Set-Group-ID em exec [GH 962, 1415, 2072]
- Adicionado suporte para ptrace PTRACE_O_TRACEEXIT [GH 555]
- Adicionado suporte para ptrace PTRACE_GETFPREGS e PTRACE_GETREGSET com NT_FPREGSET [GH 555]
- Correção de ptrace para parar em sinais ignorados
- Melhorias e correções de bugs adicionais

#### <a name="console"></a>Console
- Nenhuma alteração relacionada ao console nesta versão.

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes de passagem: 768</br>
Número de testes com falha: 244</br>
Número de testes ignorados: 96</br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Build 16241

Para obter informações gerais do Windows sobre o Build 16241 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Nenhuma alteração relacionada ao WSL nesta versão.

#### <a name="console"></a>Console
- Correção para a saída do caractere errado para as linhas de cruzamento DEC, originalmente relatadas [aqui](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- Correção para nenhum texto de saída exibido na página de código 65001 (UTF8)
- Não transfira as alterações feitas aos valores RGB de uma cor para outras partes da paleta na alteração de seleção. Isso tornará a planilha de propriedades do console muito mais fácil de usar.
- CTRL + S parece não funcionar corretamente
- Sem negrito/Dim totalmente ausente dos códigos de escape ANSI [GH 2174]
- O console não dá suporte corretamente a temas de cor do vim [GH 1706]
- Não é possível colar determinados caracteres [GH 2149]
- O redimensionamento de refluxo interage de acordo com o redimensionamento de uma janela bash quando as coisas estão na linha de comando/edição [GH ConEmu 1123]
- CTRL-L deixa a tela suja [GH 1978]
- Bug de renderização do console ao exibir VT em HDPI [GH 1907]
- Japansese caracteres parecem estranhos com o caractere Unicode U + 30FB [GH 2146]
- Melhorias e correções de bugs adicionais

</br>

## <a name="build-16237"></a>Build 16237

Para obter informações gerais do Windows sobre o Build 16237 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Fixo
- Usar atributos padrão para arquivos sem EAs em lxfs (raiz, raiz, 0000)
- Suporte adicionado para distribuições que usam atributos estendidos
- Corrigir o preenchimento das entradas retornadas por getolgas e getdents64
- Corrigir a verificação de permissões para a chamada do sistema shmctl SHM_STAT [GH 2068]
- Corrigido o estado de epoll inicial incorreto para ttys [GH 2231]
- Corrigir DrvFs readdir não retornando todas as entradas [GH 2077]
- Corrigir LxFs readdir quando os arquivos estiverem desvinculados [GH 2077]
- Permitir que arquivos drvfs não vinculados sejam reabertos por meio do procfs
- Substituição da chave do registro global adicionada para desabilitar os recursos do WSL (Interop/montagem de unidade)
- Corrigir a contagem de blocos incorretos em "stat" para DrvFs (e LxFs) [GH 1894]
- Melhorias e correções de bugs adicionais

</br>

## <a name="build-16232"></a>Build 16232

Para obter informações gerais do Windows sobre o Build 16232 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Nenhuma alteração relacionada ao WSL nesta versão.

</br>

## <a name="build-16226"></a>Build 16226

Para obter informações gerais do Windows sobre o Build 16226 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Fixo
- suporte de syscalls relacionado a xattr (getxattr, setxattr, listxattr, removexattr).
- Security. capablity xattr support.
- Compatibilidade aprimorada com determinados sistemas de arquivos e filtros, incluindo servidores SMB não MS. [GH #1952]
- Suporte aprimorado para espaços reservados do OneDrive, espaços reservados do GVFS e arquivos compactados do sistema operacional compactado.
- Melhorias e correções de bugs adicionais

</br>

## <a name="build-16215"></a>Build 16215

Para obter informações gerais do Windows sobre o Build 16215 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Fixo
- O WSL não exige mais o modo de desenvolvedor.
- Suporte a junções de diretório em drvfs.
- Manipule a desinstalação de pacotes Appx de distribuição de WSL.
- Atualize procfs para mostrar mapeamentos privados e compartilhados.
- Adicione capacidade de wslconfig. exe para limpar distribuições parcialmente instaladas ou desinstaladas.
- Adicionado suporte para IP_MTU_DISCOVER para Soquetes TCP. [GH 1639, 2115, 2205]
- Inferir a família de protocolos para rotas para AF_INADDR.
- Aprimoramentos de dispositivo serial [GH 1929].

</br>

## <a name="build-16199"></a>Build 16199

Para obter informações gerais do Windows sobre o Build 16199 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Nenhuma alteração relacionada ao WSL nessas versões.

</br>

## <a name="build-16193"></a>Build 16193

Para obter informações gerais do Windows sobre o Build 16193 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Condição de corrida entre o envio de SIGCONT e um encerramento de um @ GH 1973]
- alterar dispositivos tty e PTY para relatar FILE_DEVICE_NAMED_PIPE em vez de FILE_DEVICE_CONSOLE [GH 1840]
- Correção de SSH para IP_OPTIONS
- A montagem do DrvFs foi movida para o daemon init [GH 1862, 1968, 1767, 1933]
- Adicionado suporte em DrvFs para os seguintes NT symlinks.

</br>

## <a name="build-16184"></a>Build 16184

Para obter informações gerais do Windows sobre o Build 16184 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Tarefa de manutenção do pacote apt removida (lxrun. exe/update)
- A saída corrigida não aparece nos processos do Windows no node. js [GH 1840]
- Relaxar os requisitos de alinhamento no lxcore [GH 1794]
- Manipulação fixa do sinalizador AT_EMPTY_PATH em um número de chamadas do sistema.
- Correção do problema em que a exclusão de arquivos DrvFs com identificadores abertos fará com que o arquivo apresente comportamento indefinido [GH 544, 966, 1357, 1535, 1615]
- o/etc/hosts agora herdará entradas do arquivo hosts do Windows (%WINDIR%\System32\Drivers\Etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>Build 16179

Para obter informações gerais do Windows sobre o Build 16179 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Nenhuma alteração de WSL desta semana.

</br>

## <a name="build-16176"></a>Build 16176

Para obter informações gerais do Windows sobre o Build 16176 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Fixo

- [Suporte serial habilitado](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- Opção de soquete IP adicionada IP_OPTIONS [GH 1116]
- Função pwritev implementada (ao carregar o arquivo para Nginx/PHP-FPM) [GH 1506]
- Opções de soquete IP adicionadas IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- Suporte para a opção socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]
- Adição de IP (V6) _MTU Socket Option para aplicativos nó, traceroute, busca, Nslookup, host
- Opção de soquete IP adicionada IPV6_UNICAST_HOPS
- [Aprimoramentos do sistema de arquivos](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * Permitir a montagem de caminhos UNC
    * Habilitar o suporte CDFS no drvfs
    * Manipular corretamente as permissões para sistemas de arquivos de rede no drvfs
    * Adicionar suporte para unidades remotas ao drvfs
    * Habilitar o suporte a FAT no drvfs
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP
Nenhuma alteração desde 15042

</br>

## <a name="build-16170"></a>Build 16170

Para obter informações gerais do Windows sobre o Build 16170 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Lançamos uma nova [postagem de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutindo nossos esforços para testar o WSL.

### <a name="fixed"></a>Fixo

- Opção de soquete de suporte IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- Adicione suporte para PTRACE_OLDSETOPTIONS. [GH 1692]
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP
Nenhuma alteração desde 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Compilar o 15046 para a atualização do Windows 10 para criadores
Não há mais correções WSL ou recursos planejados para inclusão na atualização de criadores para o Windows 10. As notas de versão do WSL serão retomadas nas próximas semanas para as adições direcionadas ao próximo Windows Update principal. Para obter informações gerais do Windows sobre o Build 15046 e futuras versões do Insider, visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Build 15042

Para obter informações gerais do Windows sobre o Build 15042 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Fixo

- Correção de um deadlock ao remover um caminho que termina em ".."
- Corrigido um problema em que FIONBIO não retornava 0 no êxito [GH 1683]
- Correção do problema com leituras de comprimento zero de soquetes de datagrama inet
- Corrigir um possível deadlock devido à condição de corrida na pesquisa de inode de drvfs [GH 1675]
- Suporte estendido para dados complementares de soquete UNIX; SCM_CREDENTIALS e SCM_RIGHTS [GH 514, 613, 1326]
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 737</br>
Número de não aprovados (com falha, ignorado, etc...): 255

</br>

## <a name="build-15031"></a>Build 15031

Para obter informações gerais do Windows sobre o Build 15031 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Fixo

- Corrigido um bug em que o tempo (2) se comportaria esporadicamente.
- Corrigido e problema em que * SIGPROCMASK syscalls poderia corromper a máscara de sinal.
- Agora, retorne o comprimento de linha de comando completo na notificação de criação de processo WSL. [GH 1632]
- WSL agora relata a saída do thread por meio do ptrace para travas do GDB. [GH 1196]
- Corrigido o bug em que PTYs seria interrompido depois de tmux de e/s pesada. [GH 1358]
- Correção da validação de tempo limite em muitas chamadas do sistema (Futex, SEMTIMEDOP, ppoll, sigtimedwait, itimer, timer_create)
- Adicionado suporte eventfd EFD_SEMAPHORE [GH 452]
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 737</br>
Número de não aprovados (com falha, ignorado, etc...): 255 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Build 15025

Para obter informações gerais do Windows sobre o Build 15025 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Fixo

- Correção para o bug que quebrou o grep 2,27 [GH 1578]
- Sinalizador EFD_SEMAPHORE implementado para syscall eventfd2 [GH 452]
- Implementado/proc/[pid]/net/ipv6_route [GH 1608]
- Suporte de e/s controlado por sinal para soquetes de fluxo do UNIX [GH 393, 68]
- Suporte a F_GETPIPE_SZ e F_SETPIPE_SZ [GH 1012]
- Implementar syscall recvmmsg () [GH 1531]
- Corrigido o bug em que epoll_wait () não estava aguardando [GH 1609]
- Implementar/proc/version_signature
- O syscall de hoje retorna uma falha se os dois descritores de arquivo se referirem ao mesmo pipe
- Implementação do comportamento correto para SO_PEERCRED para soquetes UNIX
- Manipulação de parâmetro inválida de syscall tkill corrigida
- Alterações para aumentar o preformace de drvfs
- Correção secundária para bloqueio de e/s Ruby
- Corrigido recvmsg () retornando EINVAL para o sinalizador MSG_DONTWAIT para os soquetes inet [GH 1296]
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 732</br>
Número de não aprovados (com falha, ignorado, etc...): 255 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Build 15019

Para obter informações gerais do Windows sobre o Build 15019 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Fixo

- Correção do bug que reportou incorretamente o uso da CPU em procfs para ferramentas como htop (GH 823, 945, 971)
- Ao chamar Open () com O_TRUNC em um arquivo existente, INotifyPropertyChanged agora gera IN_MODIFY antes de IN_OPEN
- Correções para SO_ERROR de soquetes UNIX getsockopt para habilitar postgress [GH 61, 1354]
- Implementar o/proc/sys/net/Core/SOMAXCONN para o idioma GO
- Apt-obter tarefa de histórico de atualização de pacote agora é executada oculta da exibição
- Limpar escopo do localhost IPv6 (falha de Spring-Framework (Java)).
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 714 </br>
Número de não aprovados (com falha, ignorado, etc...): 249 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Build 15014

Para obter informações gerais do Windows sobre o Build 15014 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fixo

- CTRL + C agora funciona conforme o esperado
- htop e PS auxw agora mostram a utilização de recursos correta (GH #516)
- Tradução básica de exceções NT para sinais. (GH #513)
- fallocate agora falha com ENOSPC ao ficar sem espaço em vez de EINVAL (GH #1571)
- /Proc/sys/kernel/sem. adicionados
- Implementadas chamadas do sistema semop e SEMTIMEDOP
- Correção de erros nslookup com IP_RECVTOS & IPV6_RECVTCLASS Socket Option (GH 69)
- Suporte para opções de soquete IP_RECVTTL e IPV6_RECVHOPLIMIT
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 709 </br>
Número de não aprovados (com falha, ignorado, etc...): 255 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Resumo de syscall
Total de syscalls: 384 </br>
Total implementado: 235 </br>
Total de fragmentado: 22 </br>
Total não implementado: 127 </br>
[Detalhamento detalhado](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Build 15007

Para obter informações gerais do Windows sobre o Build 15007 visite o [blog do Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Problema conhecido

- Há um bug conhecido em que o console não reconhece algumas entradas CTRL + <key> .  Isso inclui o comando CTRL-c que atuará como um pressionamento normal de ' C'.

  - Solução alternativa: Mapeie uma chave alternativa para CTRL + C. Por exemplo, para mapear CTRL + K para CTRL + C, `stty intr \^k`faça o:.  Esse mapeamento é por terminal e terá que ser feito *toda* vez que o bash for iniciado. Os usuários podem explorar a opção para incluí-lo em seus`.bashrc`

### <a name="fixed"></a>Fixo

- Correção do problema em que a execução do WSL consumiria 100% de um núcleo de CPU
- A opção de soquete IP_PKTINFO, IPV6_RECVPKTINFO agora tem suporte. (GH #851, 987)
- Truncar o endereço físico da interface de rede para 16 bytes em lxcore (GH #1452, 1414, 1343, 468, 308)
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 709 </br>
Número de não aprovados (com falha, ignorado, etc...): 255 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Build 15002

Para obter informações gerais do Windows sobre o Build 15002 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Problema conhecido

Dois problemas conhecidos:
- Há um bug conhecido em que o console não reconhece algumas entradas CTRL + <key> .  Isso inclui o comando CTRL-c que atuará como um pressionamento normal de ' C'.

  - Solução alternativa: Mapeie uma chave alternativa para CTRL + C. Por exemplo, para mapear CTRL + K para CTRL + C, `stty intr \^k`faça o:.  Esse mapeamento é por terminal e terá que ser feito *toda* vez que o bash for iniciado. Os usuários podem explorar a opção para incluí-lo em seus`.bashrc`

- Enquanto o WSL estiver executando um thread do sistema, consumirá 100% de um núcleo de CPU.  A causa raiz foi resolvida e corrigida internamente.

### <a name="fixed"></a>Fixo

- Todas as sessões de bash agora devem ser criadas no mesmo nível de permissão.  A tentativa de iniciar uma sessão em um nível diferente será bloqueada.  Isso significa que os consoles admin e não admin não podem ser executados ao mesmo tempo. (GH #626)
<br/>
- Implementadas as seguintes mensagens NETLINK_ROUTEs (requer administrador do Windows)
     - RTM_NEWADDR (dá `ip addr add`suporte)
     - RTM_NEWROUTE (dá `ip route add`suporte)
     - RTM_DELADDR (dá `ip addr del`suporte)
     - RTM_DELROUTE (dá `ip route del`suporte)
- A verificação de tarefa agendada dos pacotes a serem atualizados não será mais executada em uma conexão limitada (GH #1371)
- Corrigido o erro em que a tubulação fica presa, ou seja, bash-c "ls-alR/" | bash-c "Cat" (GH #1214)
- Opção TCP_KEEPCNT Socket implementada (GH #843)
- Opção de soquete IP_MTU_DISCOVER INET implementada (GH #720, 717, 170, 69)
- Funcionalidade herdada removida para executar binários NT a partir de init com a pesquisa de NT Path. (GH #1325)
- Corrigir o modo de/dev/kmsg para permitir acesso de leitura/grupo (0644) (GH #1321)
- Implementado/proc/sys/kernel/Random/UUID (GH #1092)
- Erro corrigido em que a hora de início do processo foi mostrada como ano 2432 (GH #974)
- Variável de ambiente de termo padrão alternada para xterm-256color (GH #1446)
- Modificou a maneira como a confirmação de processamento é calculada durante o processo Fork. (GH #1286)
- /Proc/sys/VM/overcommit_memory. implementados (GH #1286)
- Arquivo/proc/net/Route implementado (GH #69)
- Corrigido o erro em que o nome do atalho foi localizado incorretamente (GH #696)
- A lógica de análise Elf fixa que está validando incorretamente os cabeçalhos de programa deve ser menor que (ou igual a) PATH_MAX. (GH #1048)
- Implementado o retorno de chamada statfs para procfs, sysfs, cgroupfs e binfmtfs (GH #1378)
- Correção das janelas AptPackageIndexUpdate que não serão fechadas (GH #1184, também discutidas em GH #1193)
- Adicionado suporte de ADDR_NO_RANDOMIZE de personalidade de ASLR. (GH #1148, 1128)
- Melhoria de PTRACE_GETSIGINFO, SIGSEGV, para rastreamentos de pilha gdb apropriados durante o AV (GH #875)
- A análise de Elf não falha mais para binários patchelf. (GH #471)
- DNS de VPN propagado para/etc/resolv.conf (GH #416, 1350)
- Melhorias no TCP Close para transferência de dados mais confiável. (GH #610, 616, 1025, 1335)
- Agora, retorne o código de erro correto quando muitos arquivos estiverem abertos (EMFILE). (GH #1126, 2090)
- O log de auditoria do Windows agora relata o nome da imagem em processar criar auditoria.
- Agora, falha normalmente ao iniciar bash. exe de dentro de uma janela de bash
- Mensagem de erro adicionada quando a interoperabilidade não consegue acessar um diretório de trabalho em LxFs (ou seja, notepad. exe. bashrc)
- Corrigido o problema em que o caminho do Windows foi truncado em WSL
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 690 </br>
Número de não aprovados (com falha, ignorado, etc...): 274 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Build 14986

Para obter informações gerais do Windows sobre o Build 14986 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Fixo

- Correção de bugchecks com NetLink e PTY IOCTLs
- A versão do kernel agora relata 4.4.0-43 para consistência com Xenial
- O bash. exe agora é iniciado quando a entrada é direcionada para ' nul: ' (GH #1259)
- IDs de thread agora relatadas corretamente em procfs (GH #967)
- IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Sinalizadores IN_ISDIR agora têm suporte em inotify_add_watch () (GH #1280)
- Implemente timer_create e chamadas de sistema relacionadas.  Isso habilita o suporte a GHC (GH #307)
- Corrigido o problema em que o ping retornou um tempo de 0.000 MS (GH #1296)
- Retorne o código de erro correto quando muitos arquivos forem abertos.
- Correção do problema em WSL em que a solicitação do NetLink para dados da interface de rede falharia com EINVAL se o endereço de hardware da interface for 32-bytes (como a interface teredo)
   - Observe que o utilitário "IP" do Linux contém um bug em que ele falhará se WSL relatar um endereço de hardware de 32 bytes. Esse é um bug em "IP", não WSL. O utilitário "IP" codifica o tamanho do buffer de cadeia de caracteres usado para imprimir o endereço de hardware e esse buffer é muito pequeno para imprimir um endereço de hardware de 32 bytes.
- Correções e aprimoramentos adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 669 </br>
Número de não aprovados (com falha, ignorado, etc...): 258 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Build 14971

Para obter informações gerais do Windows sobre o Build 14971 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Fixo

 - Devido a circunstâncias além do nosso controle, não há atualizações nessa compilação para o subsistema do Windows para Linux.  As atualizações agendadas regularmente serão retomadas na próxima versão.

### <a name="ltp-results"></a>Resultados do LTP:
Não alterado de 14965 </br>
Número de testes aprovados: 664 </br>
Número de não aprovados (com falha, ignorado, etc...): 263 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Build 14965

Para obter informações gerais do Windows sobre o Build 14965 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Fixo

- Suporte para RTM_GETLINK e RTM_GETADDR do protocolo NetLink Sockets NETLINK_ROUTE (GH #468)
  - Habilita os comandos ifconfig e IP para enumeração de rede
  - Mais informações podem ser encontradas em nossa [postagem no blog de rede WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- /sbin agora está no caminho do usuário por padrão
- O caminho de usuário do NT agora é acrescentado ao caminho WSL por padrão (ou seja, agora você pode digitar notepad. exe sem adicionar system32 ao caminho do Linux)
- Adicionado suporte para/proc/sys/kernel/cap_last_cap
- Os binários do NT agora podem ser iniciados em WSL quando o diretório de trabalho atual contém caracteres não-ANSI (GH #1254)
- Permitir desligamento no soquete de fluxo UNIX desconectado.
- Adicionado suporte para PR_GET_PDEATHSIG.
- Adicionado suporte para CLONE_PARENT
- Corrigido o erro em que a tubulação fica presa, ou seja, bash-c "ls-alR/" | bash-c "Cat" (GH #1214)
- Manipule solicitações para se conectar ao terminal atual.
- Marque/proc/<pid>/oom_score_adj como gravável.
- Adicione a pasta/sys/FS/CGroup.
- sched_setaffinity deve retornar o número de máscara de bits de afinidade
- Corrigir a lógica de validação ELF que pressupõe incorretamente que os caminhos do intérprete devem ter menos de 64 caracteres. (GH #743)
- Abrir descritores de arquivo podem manter a janela do console aberta (GH #1187)
- Erro de Fixeed em que renomear () falhou com barra à direita no nome de destino (GH #1008)
- Implementar arquivo/proc/net/dev
- Correção de pings 0.000 MS devido à resolução do timer.
- Implementado/proc/Self/Environ (GH #730)
- Bugs e melhorias adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 664 </br>
Número de não aprovados (com falha, ignorado, etc...): 263 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Build 14959

Para obter informações gerais do Windows sobre o Build 14959 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Fixo

- Notificação de processo RsFilter aprimorada para Windows.  Informações adicionais encontradas no [blog do WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).
- Estabilidade aprimorada com a interoperabilidade do Windows
- Corrigido o erro 0x80070057 ao iniciar o bash. exe quando a proteção de dados empresariais (EDP) estiver habilitada
- Bugs e melhorias adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 665 </br>
Número de não aprovados (com falha, ignorado, etc...): 263 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Build 14955

Para obter informações gerais do Windows sobre o Build 14955 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Fixo

 - Devido a circunstâncias além do nosso controle, não há atualizações nessa compilação para o subsistema do Windows para Linux.  As atualizações agendadas regularmente serão retomadas na próxima versão.

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 665 </br>
Número de não aprovados (com falha, ignorado, etc...): 263 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Build 14951

Para obter informações gerais do Windows sobre o Build 14951 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Novo recurso: Interoperabilidade do Windows/Ubuntu
Os binários do Windows agora podem ser chamados diretamente da linha de comando WSL.  Isso dá aos usuários a capacidade de interagir com o ambiente e o sistema do Windows de uma maneira que não foi possível.  Como um exemplo rápido, agora é possível que os usuários executem os seguintes comandos:

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

Mais informações podem ser encontradas em:

- [Blog da equipe do WSL para interoperabilidade](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [Documentação do MSDN Interop](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>Fixo

- O Ubuntu 16, 4 (Xenial) agora está instalado para todas as novas instâncias de WSL.  Os usuários com instâncias 14, 4 (confiáveis) existentes não serão atualizados automaticamente.
- A localidade definida durante a instalação agora é exibida
- Melhorias de terminal, incluindo bugs em que o redirecionamento de um processo WSL para um arquivo nem sempre funciona
- O tempo de vida do console deve estar vinculado ao tempo de vida do bash. exe
- O tamanho da janela do console deve usar tamanho visível, não tamanho do buffer
- Bugs e melhorias adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 665 </br>
Número de não aprovados (com falha, ignorado, etc...): 263 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Build 14946

Para obter informações gerais do Windows sobre o Build 14946 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Fixo

- Correção de um problema que impedia a criação de contas de usuário WSL para usuários com NT Names que contenham espaços ou aspas. 
- Altere VolFs e DrvFs para retornar 0 para a contagem de links do diretório em stat
- Suporte à opção de soquete IPV6_MULTICAST_HOPS.
- Limite para um loop de e/s de console único por TTY. Exemplo: o seguinte comando é possível:
  - bash-c "ecoar dados" | bash-c "ssh user@example.com " Cat > foo. txt ' "

- substituir espaços por tabulações em/proc/cpuinfo (GH #1115)
- DrvFs agora aparece em mountinfo com um nome que corresponde ao volume montado do Windows
- /Home e/root agora aparecem em mountinfo com nomes corretos
- Bugs e melhorias adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 665 </br>
Número de não aprovados (com falha, ignorado, etc...): 263 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Build 14942

Para obter informações gerais do Windows sobre o Build 14942 visite o [blog do Windows](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Fixo

- Vários bugchecks endereçados, incluindo a falha de rede "tentativa de executar a memória noexecute" que estava bloqueando o SSH
- o suporte do inotifiy para notificações geradas de aplicativos do Windows no DrvFs agora está em
- Implemente TCP_KEEPIDLE e TCP_KEEPINTVL para mongod. (GH #695)
- Implementar a chamada do sistema pivot_root
- Implementar opção de soquete para SO_DONTROUTE
- Bugs e melhorias adicionais


### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 665 </br>
Número de não aprovados (com falha, ignorado, etc...): 263 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Build 14936

Para obter informações gerais do Windows sobre o Build 14936 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Observação: O WSL instalará o Ubuntu versão 16, 4 (Xenial) em vez do Ubuntu 14, 4 (trusty) em uma versão futura.  Essa alteração se aplicará a pessoas que instalam novas instâncias (lxrun. exe/install ou a primeira execução de bash. exe).  As instâncias existentes com confiança não serão atualizadas automaticamente. Os usuários podem atualizar sua imagem de confiança para Xenial usando o comando do-Release-upgrade.

### <a name="known-issue"></a>Problema conhecido
WSL está enfrentando um problema com algumas implementações de soquete.  A verificação de bugs se manifesta como uma falha com o erro "tentativa de execução de noexecute MEMORY".  A manifestação mais comum desse problema é uma falha ao usar SSH.  A causa raiz é corrigida em compilações internas e será enviada por push para pessoas da primeira oportunidade.

### <a name="fixed"></a>Fixo

- Implementada a chamada do sistema chroot
- Melhorias no INotifyPropertyChanged, ~~incluindo suporte para notificações geradas de aplicativos do Windows no DrvFs~~
  - Correção O suporte do INotifyPropertyChanged para alterações provenientes de aplicativos do Windows não estão disponíveis no momento.
- Associação de soquete a IPv6:<port n> : agora dá suporte a IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)
- Comportamento de WNOWAIT para waitid systemcall implementado (GH #638)
- Suporte para opções de soquete de IP IP_HDRINCL e IP_TTL
- Leitura de comprimento zero () deve retornar imediatamente (GH #975)
- Manipule corretamente nomes de arquivos e prefixos de nome de arquivo que não incluem um terminador nulo em um arquivo. tar.
- suporte do epoll para/dev/null
- Corrigir a origem do tempo de/dev/Alarm
- Bash-c agora é capaz de redirecionar para um arquivo
- Bugs e melhorias adicionais

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 664 </br>
Número de não aprovados (com falha, ignorado, etc...): 264 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Build 14931

Para obter informações gerais do Windows sobre o Build 14931 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Fixo

 - Devido a circunstâncias além do nosso controle, não há atualizações nessa compilação para o subsistema do Windows para Linux.  As atualizações agendadas regularmente serão retomadas na próxima versão.

<br/>

## <a name="build-14926"></a>Build 14926

Para obter informações gerais do Windows sobre o Build 14926 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Fixo

- O ping agora funciona em consoles que não têm privilégios de administrador
- O Ping6 agora tem suporte, também sem privilégios de administrador
- Suporte a INotifyPropertyChanged para arquivos modificados por meio de WSL. (GH #216)
  - Sinalizadores com suporte:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - ler saída: LX_IN_ISDIR, LX_IN_IGNORED
  - Problema conhecido: Modificar arquivos de aplicativos do Windows não gera eventos
- O soquete UNIX agora dá suporte a SCM_CREDENTIALS

### <a name="ltp-results"></a>Resultados do LTP:
Número de testes aprovados: 651 </br>
Número de não aprovados (com falha, ignorado, etc...): 258 </br>
[Logs de execução de teste do LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Build 14915

Para obter informações gerais do Windows sobre o Build 14915 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fixo
-  Socketpair para soquetes de datagramas UNIX (GH #262)
- Suporte a soquetes UNIX para SO_REUSEADDR
- Suporte a soquetes UNIX para SO_BROADCAST (GH #568)
- Suporte a soquetes UNIX para SOCK_SEQPACKET (GH #758, #546)
- Adição de suporte para envio, recebimento e desligamento de soquete de datagrama UNIX
- Correção de verificação devido à validação de parâmetro mmap inválida para endereços não fixos. (GH #847)
- Suporte para Suspensão/retomada de Estados de terminal
- Suporte para TIOCPKT IOCTL para desbloquear o utilitário de tela (GH #774)
    - Problema conhecido: Teclas de função não operacionais
- Correção de uma corrida em TimerFd que poderia fazer com que um membro livre ' ReaderReady ' fosse acessado pelo LxpTimerFdWorkerRoutine (GH #814)
- Habilitar suporte à chamada do sistema reiniciável para Futex, pesquisa e clock_nanosleep
- Adicionado suporte à montagem de associação
- descompartilhar para suporte de namespace de montagem
    - Problema conhecido: Ao criar um novo namespace de montagem `unshare(CLONE_NEWNS)` com o diretório de trabalho atual, ele continuará a apontar para o namespace antigo
- Melhorias e correções de bugs adicionais

<br/>

## <a name="build-14905"></a>Build 14905

Para obter informações gerais do Windows sobre o Build 14905 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Agora há suporte para chamadas reiniciáveis do sistema (GH #349, GH #520)
- Symlinks para diretórios que terminam em/agora operacional (GH #650)
- RNDGETENTCNT IOCTL implementado para/dev/random
- Implementou os arquivos/proc/[pid]/mounts,/proc/[pid]/mountinfo e/proc/[pid]/mountstats
- Bugs e melhorias adicionais

</br>

## <a name="build-14901"></a>Build 14901
Primeira compilação do insider Build para a versão de atualização de aniversário do Windows 10.

Para obter informações gerais do Windows sobre o Build 14901 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Fixo
- Problema de barra à direita fixa
    - Comandos como `$ mv a/c/ a/b/` agora funcionam
- Instalar agora solicita se a localidade do Ubuntu deve ser definida como localidade do Windows
- Suporte do procfs para a pasta NS
- Adição de montagem e desmontagem para sistemas de arquivos tmpfs, procfs e sysfs
- Corrigir mknod [at] assinatura da ABI de 32 bits
- Soquetes UNIX movidos para o modelo de expedição
- O tamanho do buffer de recebimento de soquete INET usando o setsockopt deve ser respeitado
- Implementar sinalizador de mensagem de recebimento de soquete do UNIX MSG_CMSG_CLOEXEC
- Processo Linux de redirecionamento de pipe STDIN/STDOUT (GH #2)
    - Permite a tubulação de comandos bash-c no CMD.  Exemplo: > dir | bash-c "grep foo"
- O bash agora pode ser instalado em sistemas com vários Pagefiles (GH #538, #358)
- O tamanho do buffer do soquete INET padrão deve corresponder ao da configuração padrão do Ubuntu
- Alinhar xattr syscalls ao listxattr
- Retornar apenas interfaces com um endereço IPv4 válido de SIOCGIFCONF
- Corrigir a ação padrão de sinal quando injetada por ptrace
- implementar/proc/sys/VM/min_free_kbytes
- Use os valores de registro de contexto do computador ao restaurar o contexto em sigreturn
    - Isso resolve o problema em que o Java e o javac estavam suspensos para alguns usuários
- Implementar/proc/sys/kernel/hostname

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Compilar 14388 para atualização de aniversário do Windows 10
Para obter informações gerais do Windows sobre o Build 14388 visite o [blog do Windows](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Fixo
- Correções para se preparar para a atualização de aniversário do Windows 10 em 8/2
  - Mais informações sobre WSL na atualização de aniversário podem ser encontradas em nosso [blog](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>Build 14376
Para obter informações gerais do Windows sobre o Build 14376 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Fixo
- Removidas algumas instâncias em que apt-get paralisa (GH #493)
- Corrigido um problema em que as montagens vazias não foram manipuladas corretamente
- Corrigido um problema em que os ramdisks não foram montados corretamente
- Alterar a aceitação de soquete do UNIX para os sinalizadores de suporte (GH parcial #451)
- Correção de bluescreen relacionado à rede comum
- Bluescreen corrigido ao acessar/proc/[pid]/Task (GH #523)
- Correção da utilização alta da CPU para alguns cenários de PTY (GH #488, #504)
- Bugs e melhorias adicionais

<br/>

## <a name="build-14371"></a>Build 14371
Para obter informações gerais do Windows sobre o Build 14371 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Fixo
- Correção da corrida de tempo com SIGCHLD e Wait () ao usar ptrace
- Corrigido algum comportamento quando os caminhos têm um #432 (GH) à direita
- Corrigido o problema com a falha de renomeação/desvinculação devido a identificadores abertos para filhos
- Bugs e melhorias adicionais

<br/>

## <a name="build-14366"></a>Build 14366
Para obter informações gerais do Windows sobre o Build 14366 visite o [blog do Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Fixo
- Correção na criação de arquivo por meio de symlinks
-   Adicionado listxattr para Python (GH 385)
-   Bugs e melhorias adicionais

### <a name="syscall-support"></a>Suporte a syscall
-   Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>Build 14361
Para obter informações gerais do Windows sobre o Build 14361 visite o [blog do Windows](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Fixo
- O DrvFs agora diferencia maiúsculas de minúsculas quando executado no bash no Ubuntu no Windows.
  - Os usuários podem Case. txt e maiúsculas e minúsculas. TXT em suas unidades/mnt/c
  - A diferenciação de maiúsculas e minúsculas só tem suporte no bash no Ubuntu no Windows. Quando fora do bash, o NTFS relatará os arquivos corretamente, mas o comportamento inesperado poderá ocorrer interagindo com os arquivos do Windows.
  - A raiz de cada volume (ou seja,/mnt/c) não diferencia maiúsculas de minúsculas
  - Mais informações sobre como lidar com esses arquivos no Windows podem ser encontradas [aqui](https://support.microsoft.com/en-us/kb/100625).
- Suporte de PTY/TTY muito aprimorado.  Aplicativos como TMUX agora com suporte (GH #40)
- Problema de instalação corrigido em que as contas de usuário não são sempre criadas
- Estrutura de ARG de linha de comando otimizada que permite a lista de argumentos extremamente longo. (GH #153)
- Agora é possível excluir e alread_onlyr arquivos do DrvFs
- Correção de algumas instâncias em que o terminal trava na desconexão (GH #43)
- o chmod e o proprietário agora funcionam em dispositivos tty
- Permitir conexão a 0.0.0.0 e:: as localhost (GH #388)
- Sendmsg/recvmsg agora lida com um comprimento de vetor de e/s de > 1 (Partial GH #376)
- Os usuários agora podem recusar o arquivo de hosts gerados automaticamente (GH #398)
- Corresponder automaticamente a localidade do Linux à localidade do NT durante a instalação (GH #11)
- Adicionado o arquivo/proc/sys/VM/swappiness (GH #306)
- strace agora é encerrado corretamente
- Permitir que os pipes sejam reabertos por meio de/proc/Self/FD (GH #222)
- Ocultar diretórios em%LOCALAPPDATA%\lxss de DrvFs (GH #270)
- Melhor manipulação do bash. exe ~.  Comandos como "bash ~-c ls" agora têm suporte (GH #467)
- Os soquetes agora notificam epoll leitura disponíveis durante o desligamento (GH #271)
- lxrun/Uninstall realiza um trabalho melhor de exclusão dos arquivos e pastas
- PS-f corrigida (GH #246)
- Suporte aprimorado para aplicativos X11, como xEmacs (GH #481)
- Tamanho da pilha de thread inicial atualizado para corresponder à configuração padrão do Ubuntu e relatando o tamanho corretamente para o syscall get_rlimit (GH #172, #258)
- Relatório aprimorado de nomes de imagem de processo RsFilter (por exemplo, para auditoria)
- Implementado o/proc/mountinfo para o comando df
- O código de erro symlink foi corrigido para o nome filho. e..
- Aprimoramentos bugs e melhorias adicionais

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Build 14352
Para obter informações gerais do Windows sobre o Build 14352 visite o [blog do Windows](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Fixo
- Correção do problema em que arquivos grandes não foram baixados/criados corretamente.  Isso deve desbloquear NPM e outros cenários (GH #3, GH #313)
- Removeu algumas instâncias em que os soquetes travam
- Correção de alguns erros de ptrace
- Correção do problema com o WSL, permitindo que os nomes de um ou mais de 255 caracteres
- Suporte aprimorado para caracteres que não são do inglês
- Adicionar dados atuais de fuso horário do Windows e definir como padrão
- ID de dispositivo exclusivo para cada ponto de montagem (correção do JRE – GH #49)
- Correção do problema com caminhos que contêm "." e ".."
- Suporte a FIFO adicionado (GH #71)
- Formato atualizado de reresolvible. conf para corresponder ao formato nativo do Ubuntu
- Algumas procfs limpeza
- Ping habilitado para consoles do administrador (GH #18)

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Build 14342
Para obter informações gerais do Windows sobre o Build 14342, o [blog do Windows](https://aka.ms/wip14342). <br/>

Informações sobre VolFs e DriveFs podem ser encontradas no [blog do WSL](https://blogs.msdn.microsoft.com/wsl). <br/>

### <a name="fixed"></a>Fixo
- Corrigido o problema de instalação quando o usuário do Windows tinha caracteres Unicode no nome de usuário
- A solução apt-get update udev nas perguntas frequentes agora é fornecida por padrão na primeira execução
- Symlinks habilitados nos diretórios do<drive>DriveFs (/MNT/)
- Symlinks agora funciona entre DriveFs e VolFs
- Problema de análise de caminho de nível superior resolvido: ls.//agora funcionará como esperado
- NPM instalar em DriveFs e as opções-g agora estão funcionando
- Problema corrigido ao impedir que o servidor PHP seja iniciado
- Valores de ambiente padrão atualizados, como $PATH para combinar mais de perto o Ubuntu nativo
- Adicionada uma tarefa de manutenção semanal no Windows para atualizar o cache do pacote apt
- Correção do problema com a validação de cabeçalho ELF, WSL agora dá suporte a todas as opções de Melkor
- O Shell do zsh é funcional
- Binários go pré-compilados agora têm suporte
- A solicitação na primeira execução do bash. exe agora está localizada corretamente
- /proc/meminfo agora retorna informações corretas
- Os soquetes agora têm suporte no VFS
- /dev agora montado como tempfs
- FIFO agora com suporte
- Sistemas de vários núcleos agora mostrados corretamente em/proc/cpuinfo
- Aprimoramentos adicionais e mensagens de erro baixando durante a primeira execução
- Melhorias de syscall e bugs. Lista syscall com suporte abaixo.
- Bugs e melhorias adicionais

### <a name="known-issues"></a>Problemas Conhecidos
- Não resolvendo '.. ' corretamente no DriveFs em alguns casos

### <a name="syscall-support"></a>Suporte a syscall
Veja abaixo uma lista de syscalls novos ou aprimorados que têm alguma implementação no WSL. O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a>Build 14332

Para obter informações gerais do Windows sobre o Build 14332 visite o [blog do Windows](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Fixo
- Melhor resolução. conf, incluindo a priorização de entradas DNS
- Problema com a movimentação de arquivos e diretórios entre unidades/mnt e não/mnt
- Agora, os arquivos tar podem ser criados com symlinks
- Diretório/Run/Lock padrão adicionado na criação da instância
- Atualizar/dev/null para retornar informações de estado adequadas
- Erros adicionais ao baixar durante a primeira execução
- Melhorias de syscall e bugs. Lista syscall com suporte abaixo.
- Aprimoramentos bugs e melhorias adicionais

### <a name="syscall-support"></a>Suporte a syscall
Abaixo está a nova syscall que tem alguma implementação no WSL. O syscall nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Build 14328

Para obter informações gerais do Windows sobre o Build 14332 visite o [blog do Windows](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Novos recursos
* Agora dê suporte a usuários do Linux.  A instalação do bash no Ubuntu no Windows solicitará a criação de um usuário do Linux.  Para obter mais informações, visite https://aka.ms/wslusers
* Hostname agora está definido como o nome do computador Windows, não há mais@localhost
* Para obter mais informações sobre a compilação 14328, visite: https://aka.ms/wip14328

### <a name="fixed"></a>Fixo
* Aprimoramentos do symlink para<drive> arquivos não/mnt/
    * NPM instalar agora funciona
    * Agora, o JDK/JRE é instalável usando as instruções encontradas [aqui](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).
    * problema conhecido: o symlinks não funciona para montagens do Windows.  A funcionalidade estará disponível em uma compilação posterior
* Top e htop agora são exibidos
* Mensagens de erro adicionais para algumas falhas de instalação
* Melhorias de syscall e bugs.  Lista syscall com suporte abaixo.
* Aprimoramentos bugs e melhorias adicionais

### <a name="syscall-support"></a>Suporte a syscall
Abaixo está uma lista de syscalls que têm alguma implementação em WSL.  O syscalls nessa lista tem suporte em pelo menos um cenário, mas talvez não tenha todos os parâmetros com suporte no momento.

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
