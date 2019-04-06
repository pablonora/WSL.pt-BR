---
title: Notas de versão do subsistema do Windows para Linux
description: Notas de versão para o subsistema Windows para Linux.  Atualizada semanalmente.
keywords: BashOnWindows, bash, o wsl, o windows, o subsistema do windows para linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 3eee7ff6d1f8302e98cde84fccabf5d9113c83f2
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063624"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Notas de versão do subsistema do Windows para Linux

## <a name="build-18342"></a>Compilação 18342
Para Windows geral informações sobre compilação 18342, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Adicionamos a capacidade dos usuários acessar os arquivos do Linux em uma distribuição WSL do Windows. Esses arquivos podem ser acessados por meio da linha de comando e também aplicativos do Windows, como o Explorador de arquivos, VSCode, etc. podem interagir com esses arquivos. Acessar seus arquivos, navegando até \\ \\$ wsl\\< distro_name >, ou ver uma lista de execução de distribuições, navegando até \\ \\$ wsl
* Adicionar marcas de informações adicionais de CPU e corrigir os valores de Cpus_allowed [ lista] [GH 2234]
* Suporte a execução de thread não líder [GH 3800]
* Tratar falhas de atualização de configuração como não-fatais [GH 3785]
* Atualizar binfmt para lidar adequadamente com deslocamentos [GH 3768]
* Habilitar o mapeamento unidades de rede para planejar 9 [GH 3854]
* Suporte ao Windows -> Linux e tradução de caminho do Windows para montagens -> do Linux
* Criar seções somente leitura para mapeamentos em arquivos abertos somente leitura

## <a name="build-18334"></a>Compilação 18334
Para Windows geral informações sobre compilação 18334, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Reestruturação da maneira que a zona de tempo do Windows é mapeada para um fuso horário do Linux [GH 3747]
* Corrigir vazamentos de memória e adicionar novas funções de conversão de cadeia de caracteres [GH 3746]
* SIGCONT em um threadgroup sem threads é não operacional [GH 3741] 
* Exibir corretamente os descritores de arquivo de soquete e epoll em /proc/self/fd

## <a name="build-18305"></a>Compilação 18305
Para Windows geral informações sobre compilação 18305, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* pthreads perder o acesso aos arquivos quando o thread primário é encerrado [GH 3589]
* TIOCSCTTY deve ignorar o parâmetro "force", a menos que seja necessário [GH 3652]
* aprimoramentos de linha de comando wsl.exe e adição de importação / exportação de funcionalidade.
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

## <a name="build-18277"></a>Compilação 18277
Para Windows geral informações sobre compilação 18277, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Corrigir o erro "nenhuma interface deste tipo suportada" apresentado na compilação 18272 [GH 3645]
* Ignorar o sinalizador de MNT_FORCE unmount syscall [GH 3605]
* Alternar a interoperabilidade do WSL para usar a API oficial do CreatePseudoConsole
* Não manter nenhum valor de tempo limite quando FUTEX_WAIT é reiniciado

## <a name="build-18272"></a>Compilação 18272
Para Windows geral informações sobre compilação 18272, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **AVISO:** Há um problema nesta compilação que faz o WSL inoperável. Ao tentar iniciar sua distribuição, você verá um erro "Nenhuma interface deste tipo suportada". O problema foi corrigido e estará no build Insider rápido da próxima semana. Se você tiver instalado essa compilação, você pode reverter para a compilação anterior do Windows usando "Ir para a versão anterior do Windows 10" nas configurações -> atualização de & segurança -> Recovery.

## <a name="build-18267"></a>Compilação 18267
Para Windows geral informações sobre compilação 18267, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Corrija o problema em que o processo zumbi não pode ser reaped e permanecerão enfileirados indefinidamente.
* WslRegisterDistribution trava se a mensagem de erro excede o tamanho máximo [GH 3592]
* Permitir fsync bem-sucedido para arquivos somente leitura em DrvFs [GH 3556]
* Certifique-se de que pastas /bin e /sbin existem antes de criar links simbólicos dentro de [GH 3584]
* Adicionado um mecanismo de tempo limite de encerramento de instância para instâncias WSL. Atualmente, o limite é definido como 15 segundos, que significa que a instância será encerrada 15 segundos após o último processo WSL é encerrado. Para encerrar uma distribuição imediatamente, use:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Compilar 17763 (1809)
Para Windows geral informações sobre compilação 17763, visite o [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* Verificação de permissão de syscall SetPriority muito restrita para alterar a prioridade do thread mesmo [GH 1838]
* Certifique-se de que o tempo de interrupção não polarizada é usado para o tempo de inicialização para evitar o retorno de valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* Tratar links simbólicos no interpretador WSL binfmt [GH 3424]
* Melhor tratamento de limpeza de descritor de arquivo threadgroup líder.
* Alternar WSL usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter de kernel para evitar estouro [GH 3252]
* Ptrace conexão pode fazer com que o valor de retorno incorreto de chamadas do sistema [GH 1731]
* Correção relacionada AF_UNIX vários problemas [GH 3371]
* Correção do problema que poderia causar a interoperabilidade do WSL falhar se o diretório de trabalho atual é menor que 5 caracteres [GH 3379]
* Evitar um atraso de segundo, as conexões de loopback às portas não existente [GH 3286] com falha
* Adicionar arquivo de stub /proc/sys/fs/file-max [GH 2893]
* Informações mais precisas do escopo de IPV6.
* Suporte PR_SET_PTRACER [GH 3053]
* Sistema de arquivos do pipe limpando inadvertidamente o evento de borda disparada epoll [GH 3276]
* Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]
* Melhor suporte de zumbi [GH 1353]
* Adicionar entradas de wsl.conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correção para getsockname nem sempre retornar o tipo de família do soquete UNIX [GH 1774]
* Adicionar suporte para TIOCSTI [GH 1863]
* Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]
* Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]
* Corrigir o problema na pasta raiz [GH 3304] de verificação de permissão
* Suporte limitado para TTY teclado ioctls KDGKBTYPE, KDGKBMODE e KDSKBMODE.
* Aplicativos de interface do usuário do Windows devem ser executado mesmo quando iniciado em segundo plano.
* Adicione a opção wsl -u ou --usuário [GH 1203]
* Corrigir problemas de inicialização WSL inicialização rápida está habilitada [GH 2576]
* Soquetes do UNIX precisam manter credenciais de par desconectada [GH 3183]
* Soquetes do Unix sem-bloqueio apresentando indefinidamente EAGAIN [GH 3191]
* Caso = off, é os novo drvfs padrão [2937 de GH, 3212, 3328] do tipo de montagem
    * Ver [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.
* Adicionar wslconfig / encerrar para interromper a execução de distribuições.
* Corrigi o problema com o contexto de shell WSL entradas de menu que não tratar corretamente os caminhos com espaços.
* Expor diferenciação por diretório como um atributo estendido
* ARM64: Emule as operações de manutenção do cache. Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).
* DrvFs: unescape apenas caracteres no intervalo particular que correspondem ao caractere de escape.
* Corrigir o erro off-by-one na validação de comprimento ELF analisador interpretador [GH 3154]
* Temporizadores WSL absolutos com um tempo no passado não disparam [GH 3091]
* Certifique-se recentemente de arquivos esparsos criados estão listados como tal no diretório pai.
* Atomicamente Crie diretórios diferencia maiusculas de minúsculas no DrvFs.
* Foi corrigido um problema adicional em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe. [GH 2712]
* WSL fixa inicie falha quando UMCI está habilitado. [GH 3020]
* Adicione menu de contexto do explorer para iniciar o WSL [GH 437, 603, 1836]. Para usar, mantenha a tecla shift e clique com botão direito quando estiver em uma janela do explorer.
* Corrigir o comportamento de não bloqueio de soquete Unix [GH 2822, 3100]
* Correção de travamento comando NETLINK conforme relatado na 2026 GH.
* Adicione suporte para sinalizadores de propagação de montagem [GH 2911].
* Corrigi o problema com eventos de inotify não causam truncamento [GH 2978].
* Adicione--opção de exec para wsl.exe invocar um binário único sem um shell.
* Adicione--opção de distribuição para wsl.exe selecionar uma distribuição específica.
* Suporte limitado para dmesg. Aplicativos agora podem fazer dmesg. Driver WSL registra informações limitadas dmesg. No futuro, isso pode ser estendido para executar outro informações/diagnóstico do driver.
    * Observação: dmesg é suportado atualmente por meio de `/dev/kmsg` interface de dispositivo. `syslog` ainda não há suporte para a interface de syscall. E, portanto, algumas da `dmesg` opções de linha de comando como `-S`, `-C` não funcionam.
* Alterar gid padrão e o modo de dispositivos seriais para corresponder nativo [GH 3042]
* DrvFs agora dá suporte a atributos estendidos.
    * Observação: DrvFs tem algumas limitações no nome dos atributos estendidos. Alguns caracteres (como '/', ':' e '\*') não são permitido e estendidos nomes de atributo não diferenciam maiusculas de minúsculas em DrvFs

## <a name="build-18252-skip-ahead"></a>Compilação 18252 (Ignorar em frente)
Para Windows geral informações sobre compilação 18252, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Mova os binários de init e bsdtar fora lxssmanager dll e em uma pasta de ferramentas separadas
* Corrigir a corrida em torno de fechar o descritor de arquivo ao usar CLONE_FILES
* Lidar com campos opcionais no /proc/pid/mountinfo ao traduzir DrvFs caminhos
* Permitir mknod DrvFs seja bem-sucedida sem suporte de metadados para S_IFREG
* Arquivos somente leitura criados em DrvFs devem ter o atributo somente leitura definido [GH 3411]
* Adicionar /sbin/mount.drvfs auxiliar para lidar com a montagem de DrvFs
* Use DrvFs renomeação POSIX.
* Permita a tradução de caminho em volumes sem um GUID de volume.

## <a name="build-17738-fast"></a>Compilar 17738 (rápida)
Para Windows geral informações sobre compilação 17738, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* Verificação de permissão de syscall SetPriority muito restrita para alterar a prioridade do thread mesmo [GH 1838]
* Certifique-se de que o tempo de interrupção não polarizada é usado para o tempo de inicialização para evitar o retorno de valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* Tratar links simbólicos no interpretador WSL binfmt [GH 3424]
* Melhor tratamento de limpeza de descritor de arquivo threadgroup líder.

## <a name="build-17728-fast"></a>Compilar 17728 (rápida)
Para Windows geral informações sobre compilação 17728, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Alternar WSL usar KeQueryInterruptTimePrecise em vez de KeQueryPerformanceCounter de kernel para evitar estouro [GH 3252]
* Ptrace conexão pode fazer com que o valor de retorno incorreto de chamadas do sistema [GH 1731]
* Correção de a que um número de AF_UNIX relacionadas problemas [GH 3371]
* Correção do problema que poderia causar a interoperabilidade do WSL falhar se o diretório de trabalho atual é menor que 5 caracteres [GH 3379]

## <a name="build-18204-skip-ahead"></a>Compilação 18204 (Ignorar em frente)
Para Windows geral informações sobre compilação 18204, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Redirecionar inadvertenly de sistema de arquivos, limpando o evento de borda disparada epoll [GH 3276]
* Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]

## <a name="build-17723-fast"></a>Compilar 17723 (rápida)
Para Windows geral informações sobre compilação 17723, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Evitar um atraso de segundo, as conexões de loopback às portas não existente [GH 3286] com falha
* Adicionar arquivo de stub /proc/sys/fs/file-max [GH 2893]
* Informações mais precisas do escopo de IPV6.
* Suporte PR_SET_PTRACER [GH 3053]
* Redirecionar inadvertenly de sistema de arquivos, limpando o evento de borda disparada epoll [GH 3276]
* Iniciada por meio de NTFS symlink executável do Win32 não respeita symlink nome [GH 2909]

## <a name="build-17713"></a>Compilação 17713
Para Windows geral informações sobre compilação 17713, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Melhor suporte de zumbi [GH 1353]
* Adicionar entradas de wsl.conf para controlar o comportamento de interoperabilidade do Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correção para getsockname nem sempre retornar o tipo de família do soquete UNIX [GH 1774]
* Adicionar suporte para TIOCSTI [GH 1863]
* Soquetes sem bloqueio no processo de conexão devem retornar EAGAIN para tentativas de gravação [GH 2846]
* Suporte a interoperabilidade em VHDs montados [GH 3246, 3291]
* Corrigir o problema na pasta raiz [GH 3304] de verificação de permissão
* Suporte limitado para TTY teclado ioctls KDGKBTYPE, KDGKBMODE e KDSKBMODE.
* Aplicativos de interface do usuário do Windows devem ser executado mesmo quando iniciado em segundo plano.

## <a name="build-17704"></a>Compilação 17704
Para Windows geral informações sobre compilação 17704, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Adicione a opção wsl -u ou --usuário [GH 1203]
* Corrigir problemas de inicialização WSL inicialização rápida está habilitada [GH 2576]
* Soquetes do UNIX precisam manter credenciais de par desconectada [GH 3183]
* Soquetes do Unix sem-bloqueio apresentando indefinidamente EAGAIN [GH 3191]
* Caso = off, é os novo drvfs padrão [2937 de GH, 3212, 3328] do tipo de montagem
    * Ver [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obter mais informações.
* Adicionar wslconfig / encerrar para interromper a execução de distribuições.

## <a name="build-17692"></a>Compilação 17692
Para Windows geral informações sobre compilação 17692, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Corrigi o problema com o contexto de shell WSL entradas de menu que não tratar corretamente os caminhos com espaços.
* Expor diferenciação por diretório como um atributo estendido
* ARM64: Emule as operações de manutenção do cache. Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).
* DrvFs: unescape apenas caracteres no intervalo particular que correspondem ao caractere de escape.

## <a name="build-17686"></a>Compilação 17686
Para Windows geral informações sobre compilação 17686, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Corrigir o erro off-by-one na validação de comprimento ELF analisador interpretador [GH 3154]
* Temporizadores WSL absolutos com um tempo no passado não disparam [GH 3091]
* Certifique-se recentemente de arquivos esparsos criados estão listados como tal no diretório pai.
* Atomicamente Crie diretórios diferencia maiusculas de minúsculas no DrvFs.

## <a name="build-17677"></a>Compilação 17677
Para Windows geral informações sobre compilação 17677, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Foi corrigido um problema adicional em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe. [GH 2712]
* WSL fixa inicie falha quando UMCI está habilitado. [GH 3020]

## <a name="build-17666"></a>Compilação 17666
Para Windows geral informações sobre compilação 17666, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>AVISO: Há um problema, impedindo que o WSL seja executado em alguns chipsets AMD [GH 3134]. Uma correção está pronto e fazendo seu caminho para o branch de Build do Insider.
* Adicione menu de contexto do explorer para iniciar o WSL [GH 437, 603, 1836]. Para usar shift espera e o botão direito do mouse quando estiver em uma janela do explorer.
* Corrigir o comportamento de não bloqueio de soquete unix [GH 2822, 3100]
* Correção de travamento comando NETLINK conforme relatado na 2026 GH.
* Adicione suporte para sinalizadores de propagação de montagem [GH 2911].
* Corrigi o problema com eventos de inotify não causam truncamento [GH 2978].
* Adicione--opção de exec para wsl.exe invocar um binário único sem um shell.
* Adicione--opção de distribuição para wsl.exe selecionar uma distribuição específica.

## <a name="build-17655-skip-ahead"></a>Compilação 17655 (Ignorar em frente)
Para Windows geral informações sobre compilação 17655, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Suporte limitado para dmesg. Aplicativos agora podem fazer dmesg. Driver WSL registra informações limitadas dmesg. No futuro, isso pode ser estendido para executar outro informações/diagnóstico do driver.
    * Observação: dmesg é suportado atualmente por meio de `/dev/kmsg` interface de dispositivo. `syslog` ainda não há suporte para a interface sycall. E, portanto, algumas da `dmesg` opções de linha de comando como `-S`, `-C` não funcionam.
* Corrigido um problema em que operações multithreaded poderia retornar ENOENT, mesmo que o arquivo existe. [GH 2712]

## <a name="build-17639-skip-ahead"></a>Compilação 17639 (Ignorar em frente)
Para Windows geral informações sobre compilação 17639, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Alterar gid padrão e o modo de dispositivos seriais para corresponder nativo [GH 3042]
* DrvFs agora dá suporte a atributos estendidos.
    * Observação: DrvFs tem algumas limitações no nome dos atributos estendidos. Em particular, alguns caracteres (como '/', ':' e '\*') não são permitido e estendidos nomes de atributo não diferenciam maiusculas de minúsculas em DrvFs

## <a name="build-17133-fast"></a>Compilar 17133 (rápida)
Para Windows geral informações sobre compilação 17133, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Correção de suspensão no WSL. [GH 3039, 3034]

## <a name="build-17128-fast"></a>Compilar 17128 (rápida)
Para Windows geral informações sobre compilação 17128, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* Nenhuma

## <a name="build-17627-skip-ahead"></a>Compilação 17627 (Ignorar em frente)
Para Windows geral informações sobre compilação 17627, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Adicione suporte para as operações de reconhecimento de pi futex. [GH 1006]
    * Observe que as prioridades não são atualmente suporte para o recurso WSL portanto, há limitações, mas o uso padrão deve ser desbloqueado.
* Suporte ao firewall do Windows para processos WSL. [GH 1852]
    * Por exemplo, para permitir que o WSL python processar para escutar em qualquer porta, use o cmd do Windows com privilégios elevados:
```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Para obter detalhes adicionais sobre como adicionar regras de firewall, consulte [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Respeite o shell padrão do usuário ao usar wsl.exe. [GH 2372]
* Relatar todas as interfaces de rede ethernet. [GH 2996]
* Uma melhor manipulação do arquivo /etc/passwd corrompido. [GH 3001]

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17618-skip-ahead"></a>Compilação 17618 (Ignorar em frente)
Para Windows geral informações sobre compilação 17618, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Introduzir pseudoconsole funcionalidades para interoperabilidade do NT [GH 988, 1366, 1433, 1542, 2370, 2406].
* O mecanismo de instalação herdada (lxrun.exe) foi preterido. O mecanismo com suporte para a instalação de distribuições é por meio do Microsoft Store.

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17110"></a>Compilação 17110
Para Windows geral informações sobre compilação 17110, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Permitir /init ser encerrado de Windows [GH 2928].
* DrvFs agora usa por diretório diferenciar maiusculas de minúsculas por padrão (equivalente a "caso = dir" opção de montagem).
    * Usando "caso = force" (o comportamento antigo) requer a definição de uma chave do registro. Execute o seguinte comando para habilitar "caso = force" Se você precisar usá-lo: reg adicionar HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1
    * Se você tiver criados com o WSL na versão mais antiga do Windows que precisam ser diferencia maiusculas de minúsculas de diretórios existentes, use fsutil.exe para marcá-los em maiusculas e minúsculas: fsutil.exe arquivo setcasesensitiveinfo <path> habilitar
* Cadeias de caracteres retornadas de syscall o uname terminadas com NULL.

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17107"></a>Compilação 17107
Para Windows geral informações sobre compilação 17107, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Suporte a TCSETSF e TCSETSW em pontos de extremidade mestre pty [GH 2552].
* Iniciar os processos simultâneos de interoperabilidade pode resultar em EINVAL [GH 2813].
* Corrigi PTRACE_ATTACH para mostrar o status de rastreamento apropriado no /proc/pid/status.
* Corrida de correção em que os processos de curta duração clonados com os CLEARTID SETTID sinalizadores e pode ser fechado sem limpar o endereço TID.
* Exiba uma mensagem ao atualizar os diretórios de sistema de arquivos do Linux, ao mover de uma compilação de pré-17093. Para obter mais detalhes sobre as alterações do sistema de 17093 arquivo, consulte as notas de versão para [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17101"></a>Compilação 17101
Para Windows geral informações sobre compilação 17101, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Suporte para signalfd. [GH 129]
* Suporte a nomes de arquivo que contém caracteres inválidos de NTFS, codificá-los como caracteres de Unicode particulares. [GH 1514]
* Montagem automática usarão somente leitura quando não há suporte para gravação. [GH 2603]
* Permitir a colagem dos pares substitutos de Unicode (como caracteres emoji). [GH 2765]
* Arquivos pseudo /proc e /sys devem retornar leitura e gravação pronto para de select, sondagem, epoll, et al. [GH 2838]
* Corrija o problema que poderia fazer com que o serviço entrar em loop infinito quando o registro foi violado ou corrompido.
* Corrija as mensagens netlink para trabalhar com a versão mais recente (upstream 4.14) iproute2.

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17093"></a>Compilação 17093
Para Windows geral informações sobre compilação 17093, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Importante:
Ao iniciar o WSL pela primeira vez após a atualização para esta compilação, ele precisará executar algum trabalho atualizando os diretórios de sistema de arquivos do Linux. Isso pode levar vários minutos, portanto, pode parecer WSL iniciam lentamente. Isso deve ocorrer apenas uma vez para cada distribuição têm instalado da loja.
* Suporte aprimorado de maiusculas e minúsculas no DrvFs.
    * DrvFs agora dá suporte a diferenciação de maiusculas por diretório. Isso é um novo sinalizador que pode ser definido em diretórios para indicar que todas as operações nesses diretórios devem ser tratadas como diferencia maiusculas de minúsculas, que permite que até mesmo aplicativos Windows corretamente abrir arquivos que diferem somente maiusculas.
    * DrvFs possui novas opções de montagem, controlando a diferenciação de maiusculas em uma base por diretório
        * Caso = força: todos os diretórios são tratados como diferencia maiusculas de minúsculas (exceto para a raiz da unidade). Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas. Esse é o comportamento herdado, exceto para marcar os novos diretórios diferencia maiusculas de minúsculas.
        * Caso = dir: somente diretórios com o sinalizador de diferenciação de maiusculas por diretório diferenciam maiusculas e minúsculas; outros diretórios diferenciam maiusculas de minúsculas. Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas.
        * Caso = desativado: somente diretórios com o sinalizador de diferenciação de maiusculas por diretório diferenciam maiusculas e minúsculas; outros diretórios diferenciam maiusculas de minúsculas. Novos diretórios criados com WSL são marcados como diferencia maiusculas de minúsculas.
    * Observação: diretórios criados pelo WSL em versões anteriores não têm esse sinalizador definido, portanto, não será tratada como diferencia maiusculas de minúsculas se você usar o "caso = dir" opção. Uma maneira de definir esse sinalizador nos diretórios existentes em breve.
    * Exemplo de montagem com as seguintes opções (para as unidades existentes, você deve primeiro desmontar antes de montar com opções diferentes): sudo mount -t drvfs c: mnt/c -o caso = dir
    * Por enquanto, caso = força ainda é a opção padrão. Isso será alterado para caso = dir no futuro.
* Agora você pode usar barras "/" em caminhos do Windows ao montar DrvFs, por exemplo: -t drvfs //server/share /mnt/share de montagem sudo
* Agora, o WSL processa o arquivo /etc/fstab durante a inicialização de instância [GH 2636].
    * Isso é feito antes de montar automaticamente DrvFs unidades; todas as unidades que já foram montadas por fstab serão não remontadas automaticamente, permitindo que você altere o ponto de montagem para unidades específicas.
    * Esse comportamento pode ser desativado usando wsl.conf.
* Os arquivos de montagem, mountinfo e mountstats no /proc corretamente escapar caracteres especiais como barras invertidas e de espaços [GH 2799]
* Arquivos especiais criados com DrvFs como links simbólicos do WSL, ou fifos e soquetes quando os metadados estiverem habilitados, agora podem ser copiados e movidos do Windows.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL é mais configurável com wsl.conf
Adicionamos um método para que você configure automaticamente algumas funcionalidades em WSL que será aplicada sempre que iniciar o subsistema. Isso inclui opções de montagem automática e a configuração de rede. Saiba mais sobre isso em nossa postagem de blog em: https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX permite conexões de soquete entre processos do Linux no WSL e processos nativos do Windows
Aplicativos WSL e o Windows agora podem se comunicar entre si em soquetes do Unix. Imagine que você deseja executar um serviço no Windows e torná-lo disponível para aplicativos do Windows e WSL. Agora, que é possível com soquetes do Unix. Leia mais em nosso blog postagem em https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Suporte mmap() com MAP_NORESERVE [GH 121, 2784]
* Suporte CLONE_PTRACE e CLONE_UNTRACED [GH 121, 2781]
* Lidar com sinal de encerramento não SIGCHLD em clone [GH 121, 2781]
* /Proc/sys/fs/inotify/max_user_instances de stub e /proc/sys/fs/inotify/max_user_watches [GH 1705]
* Erro ao carregar os binários do ELF que contêm cabeçalhos de carga com deslocamentos diferente de zero [GH 1884]
* Zerar à direita de bytes de página ao carregar imagens.
* Reduzir casos em que execve silenciosamente encerra o processo

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17083"></a>Build 17083
Para Windows geral informações sobre compilação 17083, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Fixa de verificação de bugs relacionada a epoll [2798 de GH, 2801, 2857]
* Fixos travamentos quando desativar ASLR [GH 1185, 2870]
* Certifique-se de operações mmap aparecem atômica [GH 2732]

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17074"></a>Build 17074
Para Windows geral informações sobre compilação 17074, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Formato de armazenamento fixa de metadados DrvFs [GH 2777] </br>
**Importante:** Metadados de DrvFs criado antes desta compilação serão exibidos incorretamente ou não. Para corrigir arquivos afetados, use chmod e alterar o proprietário para reaplicar os metadados.
* Correção do problema com vários sinais e syscalls reinicializável.

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17063"></a>Build 17063
Para Windows geral informações sobre compilação 17063, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* DrvFs dá suporte a metadados adicionais de Linux. Isso permite definir o proprietário e o modo de arquivos usando chmod/alterar o proprietário e também a criação de arquivos especiais, como fifos, soquetes do unix e arquivos do dispositivo. Isso está desabilitado por padrão por enquanto, pois é ainda experimental.
**Observação:**  Corrigimos um bug no formato de metadados usado pelo DrvFs. Enquanto trabalha metadados nessa compilação para experimentação, os builds futuros não corretamente lerá metadados criados por essa compilação.  Talvez você precise atualizar manualmente o proprietário de arquivos modificados e dispositivos com uma ID de dispositivo personalizada precisa ser recriada.

  Para habilitar a montagem DrvFs com a opção de metadados (para habilitá-lo em uma montagem existente, você deve primeiro desmontá-la):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Permissões de Linux são adicionadas como metadados adicionais no arquivo; elas não afetam as permissões do Windows.  Lembre-se de que a edição de um arquivo usando um editor do Windows pode remover os metadados. Nesse caso, o arquivo será revertido para suas permissões padrão.

* Opções de montagem adicionado para DrvFs para controlar arquivos sem metadados.
  * UID: a ID de usuário usada para o proprietário de todos os arquivos.
  * GID: a ID do grupo usada para o proprietário de todos os arquivos.
  * umask: uma máscara de permissões para excluir todos os arquivos e diretórios de octal.
  * fmask: uma máscara de permissões para excluir todos os arquivos regulares de octal.
  * dmask: uma máscara de permissões para excluir para todos os diretórios de octal.

  Por exemplo: 
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Combine com a opção de metadados para especificar as permissões padrão de arquivos sem metadados.

* Introduzida uma nova variável de ambiente, `WSLENV`, para configurar como as variáveis de ambiente fluam entre WSL e Win32.

  Por exemplo: 

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` é uma lista delimitada por dois-pontos das variáveis de ambiente que pode ser incluído ao iniciar processos WSL do Win32 ou Win32 do WSL.  Cada variável pode ser sufixado com uma barra invertida seguida por sinalizadores para especificar como ele é convertido.
  * p: O valor é um caminho que deve ser traduzido entre os caminhos de Win32 e WSL.
  * l: O valor é uma lista de caminhos. Em WSL, é uma lista delimitada por dois-pontos. No Win32, é uma lista delimitada por ponto e vírgula.
  * u: O valor só deve ser incluído ao invocar o WSL do Win32
  * gravação: O valor só deve ser incluído ao invocar Win32 de WSL

  Você pode definir `WSLENV` em. bashrc ou no ambiente do Windows personalizado para o usuário.

* drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)
* links simbólicos de drvfs relatam o tamanho correto (GH 2641)
* leitura/gravação funciona para tamanhos de e/s muito grandes (GH 2653)
* waitpid funciona com IDs (GH 2534) do grupo de processo
* desempenho significativamente aprimorado mmap para regiões de reserva grande; melhora o desempenho de ghc (GH 1671)
* dá suporte a personalidade para READ_IMPLIES_EXEC; corrige maxima e clisp (GH 1185)
* mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)
* correções de falhas de página no modo; de excesso de alocação correções sbcl (GH 1128)
* Clone dá suporte a mais combinações de sinalizadores
* Suporte a select/epoll de arquivos epoll (anteriormente não operacional).
* Notificar ptrace de syscalls não implementada.
* Ignorar as interfaces que não estão ao gerar nameservers resolv. conf [GH 2694]
* Enumere as interfaces de rede com nenhum endereço físico. [GH 2685]
* Correções de bugs adicionais e aprimoramentos.

### <a name="linux-tools-available-to-developers-on-windows"></a>Ferramentas do Linux disponíveis para desenvolvedores no Windows

* Cadeia de ferramentas de linha de comando do Windows inclui bsdtar (tar) e o curl.
  Leia [este blog](https://aka.ms/tarcurlwindows) para saber mais sobre a adição dessas duas novas ferramentas e ver como eles moldando a experiência do desenvolvedor no Windows.

*   `AF_UNIX` está disponível no SDK Windows Insider (17061 +).
  Leia [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para saber mais sobre `AF_UNIX` e como os desenvolvedores no Windows podem usá-lo.

### <a name="console"></a>Console
* Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.


## <a name="build-17046"></a>Compilação 17046

Para Windows geral informações sobre compilação 17046, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Permitir que os processos sejam executados sem um terminal de Active Directory. [GH 709, 1007, 1511, 2252, 2391, et al.]
- Melhor suporte a CLONE_VFORK e CLONE_VM. [GH 1878, 2615]
- Ignore drivers de filtro TDI WSL operações de rede. [GH 1554]
- DrvFs cria links simbólicos do NT quando determinadas condições forem atendidas. [GH 353, 1475, 2602]
    - O destino do link deve ser relativo, não deve ultrapassar o quaisquer pontos de montagem ou links simbólicos e deve existir.
    - O usuário deve ter SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (Isso normalmente exige que você inicie wsl.exe com privilégios elevados), a menos que o modo de desenvolvedor está ativado.
    - Em outras situações, DrvFs ainda cria links simbólicos WSL.
- Permitir executando com privilégios elevados e sem privilégios elevados instâncias WSL simultaneamente.
- Suporte /proc/sys/kernel/yama/ptrace_scope
- Adicione wslpath para fazer WSL <> – conversões de caminho do Windows. [GH 522, 1243, 1834, 2327, et al.]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Console
- Não há correções.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.


## <a name="build-17040"></a>Build 17040

Para Windows geral informações sobre compilação 17040, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Não há correções desde 17035.

#### <a name="console"></a>Console
- Não há correções desde 17035.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17035"></a>Compilação 17035

Para Windows geral informações sobre compilação 17035, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Acessando arquivos em DrvFs pode falhar ocasionalmente EINVAL. [GH 2448]

#### <a name="console"></a>Console
- Alguma perda de cor ao inserir/excluir linhas no modo de VT.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17025"></a>Build 17025

Para Windows geral informações no build 17025, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Inicie processos inicias em um novo grupo de processo de primeiro plano [GH 1653, 2510].
- Entrega SIGHUP corrige [GH 2496].
- Gere nome da ponte virtual padrão se não houver nenhuma [GH 2497].
- Implemente /proc/sys/kernel/random/boot_id [GH 2518].
- Correções de pipe de stdout/stderr mais interoperabilidade.
- Stub syncfs chamada do sistema.

#### <a name="console"></a>Console
- Corrija a entrada tradução VT para consoles de terceiros [GH 111]

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="build-17017"></a>Compilação 17017

Para Windows geral informações sobre compilação 17017, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Ignore cabeçalhos de programa ELF vazios [GH 330].
- Permitir LxssManager criar instâncias WSL para os usuários não interativo (ssh e agendada suporte de tarefa) [777 GH 1602].
- Suporte WSL -> Win32 -> [GH 1228] de cenários WSL ("início").
- Suporte limitado para a terminação de aplicativos de console, invocado por meio de interoperabilidade [GH 1614].
- Suporte a opções de montagem para devpts [GH 1948].
- Ptrace bloqueando a inicialização de filho [GH 2333].
- EPOLLET faltando alguns eventos [GH 2462].
- Retorne mais dados para PTRACE_GETSIGINFO.
- Getdents com lseek fornece resultados incorretos.
- Corrigi alguns travamentos de interoperabilidade do aplicativo do Win32, aguardando a entrada em um pipe que não tem mais nenhum dado.
- Suporte O_ASYNC para arquivos de tty/pty.
- Outros aperfeiçoamentos e correções de bugs

#### <a name="console"></a>Console
- Nenhum Console relacionados a alterações nesta versão.

### <a name="ltp-results"></a>LTP resultados:
Teste em andamento.

## <a name="fall-creators-update"></a>Atualização do Fall Creators

## <a name="build-16288"></a>Build 16288

Para Windows geral informações sobre compilação 16288, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Inicializar corretamente e relatar uid e gid modo de soquete para descritores de arquivo [GH 2490]
- Outros aperfeiçoamentos e correções de bugs

#### <a name="console"></a>Console
- Nenhum Console relacionados a alterações nesta versão.

### <a name="ltp-results"></a>LTP resultados:
Nenhuma alteração desde 16273

## <a name="build-16278"></a>Compilação 16278

Para Windows geral informações sobre compilação 162738, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Cancelar explicitamente o mapeamento de exibições mapeadas de seções de backup em arquivo quando subdividir o estado de MM LX [GH 2415]
- Outros aperfeiçoamentos e correções de bugs

#### <a name="console"></a>Console
- Nenhum Console relacionados a alterações nesta versão.

### <a name="ltp-results"></a>LTP resultados:
Nenhuma alteração desde 16273

## <a name="build-16275"></a>Compilação 16275

Para Windows geral informações sobre compilação 162735, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Nenhum WSL relacionados a alterações nesta versão.

#### <a name="console"></a>Console
- Nenhum Console relacionados a alterações nesta versão.

### <a name="ltp-results"></a>LTP resultados:
Nenhuma alteração desde 16273

## <a name="build-16273"></a>Compilação 16273

Para Windows geral informações sobre compilação 16273, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Corrigido um problema em que o DrvFs relatado, às vezes, o tipo de arquivo incorreto para diretórios [GH 2392]
- Permitir a criação de soquetes NETLINK_KOBJECT_UEVENT desbloquear programas uevent que use [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- Adicionar suporte para conexão sem bloqueio [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- Implemente CLONE_FS clonar o sinalizador de chamada do sistema [GH 2242]
- Corrigir problemas em torno de não lidar com guias ou aspas corretamente na interoperabilidade de NT [GH 1625, 2164]
- Resolver o erro ao tentar iniciar novamente WSL instâncias [GH 651, 2095] o acesso negado
- Implementar operações futex FUTEX_REQUEUE e FUTEX_CMP_REQUEUE [GH 2242]
- Corrija as permissões para vários arquivos SysFs [GH 2214]
- Corrigir Haskell travamento de pilha durante a instalação do [GH 2290]
- Implementar binfmt_misc "C" ' l'e 'P' sinalizadores [GH 2103]
- Adicionar /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]
- Adicionar suporte parcial para a chamada do sistema ioprio_set [GH 498]
- Criar um stub SO_REUSEPORT & adicionando suporte para SO_PASSCRED para soquetes netlink [GH 69]
- Retornar códigos de erro diferentes de RegisterDistribuiton se uma distribuição está instalado ou desinstalado.
- Permitir cancelamento de registro de distribuições de WSL parcialmente instaladas por meio de wslconfig.exe
- Corrigir a suspensão de teste de soquete python de udp::msg_peek
- Outros aperfeiçoamentos e correções de bugs

#### <a name="console"></a>Console
- Nenhum Console relacionados a alterações nesta versão.

### <a name="ltp-results"></a>LTP resultados:
Total de testes: 1904<br/>
Testes ignorados do total: 209<br/>
Total de falhas: 229<br/>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Compilação 16257

Para Windows geral informações sobre compilação 16257, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Implementar a chamada do sistema prlimit64
- Adicionar suporte para ulimit – n (setrlimit RLIMIT_NOFILE) [GH 1688]
- Stub MSG_MORE para soquetes TCP [GH 2351]
- Corrigir o comportamento de vetor auxiliar AT_EXECFN inválido [GH 2133]
- Corrigir o comportamento de copiar/colar para console/tty e adicionar melhor buffer cheio tratamento [GH 2204, 2131]
- Defina AT_SECURE na auxiliar vetor para programas em set-user-ID e set-group-ID [GH 2031]
- Ponto de extremidade mestre pseudo-terminal não manipulando TIOCPGRP [GH 1063]
- Correção de lseek faz para retroceder diretórios em LxFs [GH 2310]
- /dev/ptmx trava depois de uso intenso [GH 1882]
- Outros aperfeiçoamentos e correções de bugs

#### <a name="console"></a>Console
- Correção para horizontal linhas/sublinhados em todos os lugares [GH 2168]
- Corrigir para processar pedido alterado NPM tornando mais difícil fechar [GH 2170]
- Adicionado o novo esquema de cores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP resultados:
Nenhuma alteração desde 16251

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`prlimit64`<br/>

### <a name="known-issues"></a>Problemas conhecidos
#### [<a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>Problema do GitHub 2392: Pastas do Windows não reconhecido pelo WSL...](https://github.com/Microsoft/BashOnWindows/issues/2392)
No build 16257, o WSL tem problemas ao enumerar arquivos/pastas do Windows por meio de `/mnt/c/...`.
Esse problema foi corrigido e devem ser liberado no build Insiders durante a semana começar 14/8/2017.

<br/>

## <a name="build-16251"></a>Compilação 16251

Para Windows geral informações sobre compilação 16251, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Remover marca de versão beta do componente opcional do WSL, consulte [postagem de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obter detalhes.
- Inicializar corretamente o conjunto salvo uid e gid para set-user-ID e a ID do grupo de conjunto de binários em exec [GH 962 do MSExchangeTransport, 1415, 2072]
- Suporte adicionado para ptrace PTRACE_O_TRACEEXIT [GH 555]
- Suporte adicionado para ptrace PTRACE_GETFPREGS e PTRACE_GETREGSET com NT_FPREGSET [GH 555]
- Corrigido ptrace parar em sinais ignorado
- Outros aperfeiçoamentos e correções de bugs

#### <a name="console"></a>Console
- Nenhum Console relacionados a alterações nesta versão.

### <a name="ltp-results"></a>LTP resultados:
Número de testes aprovados: 768</br>
Número de testes com falha: 244</br>
Número de testes ignorados: 96</br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Compilação 16241

Para Windows geral informações sobre compilação 16241, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Fixo
#### <a name="wsl"></a>WSL
- Nenhum WSL relacionados a alterações nesta versão.

#### <a name="console"></a>Console
- Correção para gerar o caractere incorreto para dez linhas de cruzamento, relatado originalmente [aqui](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- Correção para nenhum texto de saída que está sendo exibido na página de código 65001 (utf8)
- Não transfira as alterações feitas em valores RGB da cor de um para outras partes da paleta, alterar a seleção. Isso fará a folha de propriedades de console muito mais fácil de usar.
- CTRL + S parece não funcionar corretamente
- Não negrito /-Dim completamente ausentes de códigos de escape ANSI [GH 2174]
- Console corretamente não dá suporte a temas de cores Vim [GH 1706]
- Não é possível colar determinados caracteres [GH 2149]
- Redimensionamento refluxo de forma estranha interage com o redimensionamento de uma janela de bash quando coisas está na linha de comando/Editar [GH ConEmu 1123]
- CTRL + L sair da tela suja [GH 1978]
- Bug de renderização do console ao exibir VT em HDPI [GH 1907]
- Caracteres Japansese pareçam estranhos com o caractere Unicode U + 30FB [GH 2146]
- Outros aperfeiçoamentos e correções de bugs

</br>

## <a name="build-16237"></a>Build 16237

Para Windows geral informações sobre compilação 16237, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Fixo
- Use os atributos padrão para arquivos sem EAs no lxfs (raiz, raiz, 0000)
- Adicionado suporte para as distribuições que usam atributos estendidos
- Correção de enchimento de entradas retornadas pela getdents e getdents64
- Corrigir a verificação de permissões para a chamada do sistema shmctl SHM_STAT [GH 2068]
- Estado fixo epoll inicial incorreto para ttys [GH 2231]
- Corrigir a leitura do DrvFs diret não retornando todas as entradas [GH 2077]
- Corrigir LxFs leitura diret quando os arquivos estão desvinculado [GH 2077]
- Permitir que arquivos drvfs desvinculado ser reaberto por meio de procfs
- Adicionada a substituição da chave de registro global para desabilitar os recursos WSL (interoperabilidade / montagem da unidade)
- Correção de contagem incorreta de bloco em "estatística" para DrvFs (e LxFs) [GH 1894]
- Outros aperfeiçoamentos e correções de bugs

</br>

## <a name="build-16232"></a>Compilação 16232

Para Windows geral informações sobre compilação 16232, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Nenhum WSL relacionados a alterações nesta versão.

</br>

## <a name="build-16226"></a>Compilação 16226

Para Windows geral informações sobre compilação 16226, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Fixo
- xattr relacionadas ao suporte de syscalls (getxattr, setxattr, listxattr, removexattr).
- suporte de xattr Security.capablity.
- Compatibilidade aprimorada com certos sistemas de arquivos e filtros, incluindo servidores SMB não MS. [GH #1952]
- Suporte aprimorado para espaços reservados do OneDrive, espaços reservados do GVFS e compacta OS arquivos compactados.
- Outros aperfeiçoamentos e correções de bugs

</br>

## <a name="build-16215"></a>Compilação 16215

Para Windows geral informações sobre compilação 16215, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Fixo
- WSL não exige o modo de desenvolvedor.
- Suporte a junções de diretório no drvfs.
- Lidar com a desinstalação dos pacotes de appx de distribuição de WSL.
- Atualização procfs Mostrar privado e compartilhado mapeamentos.
- Adicione capacidade para wslconfig.exe limpar as distribuições que são parcialmente instaladas ou desinstaladas.
- Adicionado suporte para IP_MTU_DISCOVER para soquetes TCP. [GH 1639, 2115, 2205]
- Inferir a família de protocolo para as rotas para AF_INADDR.
- Melhorias do dispositivo serial [GH 1929].

</br>

## <a name="build-16199"></a>Compilação 16199

Para Windows geral informações sobre compilação 16199, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Nenhum WSL relacionados a alterações nessas versões.

</br>

## <a name="build-16193"></a>Compilação 16193

Para Windows geral informações sobre compilação 16193, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Condição de corrida entre o envio SIGCONT e um threadgroup encerrando [GH 1973]
- alterar dispositivos tty e pty para relatório FILE_DEVICE_NAMED_PIPE em vez de FILE_DEVICE_CONSOLE [GH 1840]
- Correção SSH para IP_OPTIONS
- Movido DrvFs montagem para init daemon [GH 1862, 1968, 1767, 1933]
- Adicionado suporte em DrvFs para seguir links simbólicos do NT.

</br>

## <a name="build-16184"></a>Compilação 16184

Para Windows geral informações sobre compilação 16184, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Removida a tarefa de manutenção de pacotes apt (lxrun.exe /update)
- Correção da saída não aparecendo de processos do Windows no Node. js [GH 1840]
- Reduza os requisitos de alinhamento no lxcore [GH 1794]
- Corrigido o tratamento do sinalizador AT_EMPTY_PATH em um número de chamadas do sistema.
- Corrigido um problema em que a exclusão DrvFs arquivos com identificadores abertos fará com que o arquivo a apresentar um comportamento indefinido [GH 544,966,1357,1535,1615]
- / etc/hosts agora herdarão as entradas do arquivo de hosts do Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>Compilação 16179

Para Windows geral informações sobre compilação 16179, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Nenhuma alteração WSL desta semana.

</br>

## <a name="build-16176"></a>Compilação 16176

Para Windows geral informações sobre compilação 16176, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Fixo

- [Suporte serial habilitado](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- Opção de soquete adicionada IP IP_OPTIONS [GH 1116]
- Implementado função pwritev (ao carregar o arquivo para PHP/nginx-FPM) [GH 1506]
- Adição de opções de soquete IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- Suporte para a opção de soquete IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]
- Opção de soquete _MTU IP (V6) adicionada para o nó de aplicativos, traceroute, dig, nslookup e host
- Opção de soquete adicionada IP IPV6_UNICAST_HOPS
- [Aprimoramentos do sistema de arquivos](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * Permitir que a montagem de caminhos UNC
    * Habilitar o suporte CDFS em drvfs
    * Lidar corretamente com permissões de rede para sistemas de arquivos em drvfs
    * Adicionar suporte para unidades remotas a drvfs
    * Habilitar FAT dar suporte a drvfs
- Aprimoramentos e correções adicionais

### <a name="ltp-results"></a>Resultados LTP
Nenhuma alteração desde 15042

</br>

## <a name="build-16170"></a>Compilação 16170

Para Windows geral informações sobre compilação 16170, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Lançamos um novo [postagem de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutindo nossos esforços para testar o WSL.

### <a name="fixed"></a>Fixo

- Soquete de suporte à opção IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- Adicione suporte para PTRACE_OLDSETOPTIONS. [GH 1692]
- Melhorias e correções adicionais

### <a name="ltp-results"></a>Resultados LTP
Nenhuma alteração desde 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Compilar 15046 para o Windows 10 Creators Update
Há não mais WSL correções ou recursos planejados para inclusão na atualização para o Windows 10 para criadores. Notas de versão do WSL serão retomada nas próximas semanas para adições de direcionamento a próxima atualização importante do Windows. Para Windows geral informações sobre compilação 15046 e Insider futuras versões visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Compilação 15042

Para Windows geral informações sobre compilação 15042, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Fixo

- Correção de um deadlock durante a remoção de um caminho que termina em ".."
- Corrigido um problema em que FIONBIO não retornando 0 em caso de sucesso [GH 1683]
- Corrigido o problema com comprimento zero leituras de soquetes de datagrama inet
- Corrigir um possível deadlock devido a condição de corrida na pesquisa de inode drvfs [GH 1675]
- O suporte estendido para dados de auxiliares de soquete unix; SCM_CREDENTIALS e SCM_RIGHTS [GH 514, 613, 1326]
- Melhorias e correções adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 737</br>
Número de falha (com falha, ignorada, etc...): 255

</br>

## <a name="build-15031"></a>Compilação 15031

Para Windows geral informações sobre compilação 15031, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Fixo

- Corrigido um bug onde time(2) esporadicamente seria inadequados.
- Corrigido e emitir onde * SIGPROCMASK syscalls pode corromper a máscara de sinal.
- Agora retorne comprimento de linha de comando completa na notificação de criação de processo WSL. [GH 1632]
- WSL agora relata a saída de thread por meio de ptrace suspensões GDB. [GH 1196]
- Corrigido o bug onde ptys poderia ser interrompido após a pesado tmux e/s. [GH 1358]
- Validação de tempo limite fixo em várias chamadas do sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)
- Suporte EFD_SEMAPHORE eventfd adicionado [GH 452]
- Melhorias e correções adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 737</br>
Número de falha (com falha, ignorada, etc...): 255 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Compilação 15025

Para Windows geral informações sobre compilação 15025, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Fixo

- Correção de bug que grep quebrado 2.27 [GH 1578]
- Sinalizador EFD_SEMAPHORE implementado para eventfd2 syscall [GH 452]
- Implemented /proc/[pid]/net/ipv6_route [GH 1608]
- Sinal controlado por suporte de e/s para soquetes de fluxo de unix [GH 393, 68]
- Suporte F_GETPIPE_SZ e F_SETPIPE_SZ [GH 1012]
- Implementar recvmmsg() syscall [GH 1531]
- Corrigido o bug onde epoll_wait() não estava esperando [GH 1609]
- Implement /proc/version_signature
- Syscall Tee agora retorna falha se ambos os descritores de arquivo se referirem ao mesmo pipe
- Implementado comportamento correto em SO_PEERCRED para soquetes do Unix
- Manipulação de parâmetro inválido de syscall tkill fixa
- Alterações para aumentar a preformace de drvfs
- Correção secundária para o bloqueio de e/s do Ruby
- Fixo recvmsg() retornando EINVAL para o sinalizador MSG_DONTWAIT para soquetes inet [GH 1296]
- Melhorias e correções adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 732</br>
Número de falha (com falha, ignorada, etc...): 255 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Compilação 15019

Para Windows geral informações sobre compilação 15019, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Fixo

- Corrigido um bug que relatou incorretamente o uso da CPU em procfs para ferramentas como htop (GH 823, 945, 971)
- Ao chamar Open () com O_TRUNC em uma existente arquivo inotify agora gera IN_MODIFY antes IN_OPEN
- Correções para getsockopt de soquete do unix SO_ERROR habilitar postgress [GH 61, 1354]
- Implementar /proc/sys/net/core/somaxconn para a linguagem GO
- Tarefa de segundo plano de atualização de pacote de APT-get agora é executado oculta da exibição
- Escopo claro para o localhost do ipv6 (Spring-Framework(Java) falha).
- Melhorias e correções adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 714 </br>
Número de falha (com falha, ignorada, etc...): 249 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Compilação 15014

Para Windows geral informações sobre compilação 15014, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fixo

- CTRL + C agora funciona conforme o esperado
- htop e ps auxw agora mostram correto utilização de recursos (GH #516)
- Tradução básica de exceções de NT para sinais. (#513 GH)
- Agora fallocate falha com ENOSPC quando ficando sem espaço, em vez de EINVAL (GH #1571)
- /Proc/sys/kernel/sem adicionado.
- Chamadas do sistema semop e semtimedop implementadas
- Erros de nslookup fixo com a opção de soquete IP_RECVTOS & IPV6_RECVTCLASS (GH 69)
- Suporte para opções de soquete IP_RECVTTL e IPV6_RECVHOPLIMIT
- Melhorias e correções adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 709 </br>
Número de falha (com falha, ignorada, etc...): 255 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Resumo de syscall
Syscalls total: 384 </br>
Total implementado: 235 </br>
Total de fazer o stub: 22 </br>
Total de não implementado: 127 </br>
[Análise detalhada](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Build 15007

Para Windows geral informações sobre compilação 15007, visite o [Blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Problema conhecido

- Há um bug conhecido no qual o console não reconhece algumas Ctrl + <key> entrada.  Isso inclui o comando ctrl-c, que agirá como um pressionamento de tecla "c" normal.

  - Solução alternativa: Mapear uma chave alternativa para Ctrl + C. Por exemplo, para mapear Ctrl + K, Ctrl + c fazer: `stty intr \^k`.  Esse mapeamento é por terminal e precisará ser feito *cada* bash do tempo é iniciado. Os usuários podem explorar a opção de incluir isso no seu `.bashrc`

### <a name="fixed"></a>Fixo

- Corrigido o problema onde executando WSL consuma 100% de um núcleo de CPU
- Opção IP_PKTINFO, IPV6_RECVPKTINFO agora tem suportada de soquete. (GH #851 987)
- Truncar o endereço físico de interface de rede para 16 bytes no lxcore (GH #1452, 1414, 1343, 468, 308)
- Melhorias e correções adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 709 </br>
Número de falha (com falha, ignorada, etc...): 255 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Build 15002

Para Windows geral informações no build 15002, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Problema conhecido

Dois problemas conhecidos:
- Há um bug conhecido no qual o console não reconhece algumas Ctrl + <key> entrada.  Isso inclui o comando ctrl-c, que agirá como um pressionamento de tecla "c" normal.

  - Solução alternativa: Mapear uma chave alternativa para Ctrl + C. Por exemplo, para mapear Ctrl + K, Ctrl + c fazer: `stty intr \^k`.  Esse mapeamento é por terminal e precisará ser feito *cada* bash do tempo é iniciado. Os usuários podem explorar a opção de incluir isso no seu `.bashrc`

- Enquanto WSL está em execução, um thread de sistema consumirá 100% de um núcleo de CPU.  A causa raiz foi resolvida e corrigida internamente.

### <a name="fixed"></a>Fixo

- Agora, todas as sessões de bash devem ser criadas no mesmo nível de permissão.  Tentativa de iniciar uma sessão em um nível diferente será bloqueada.  Isso significa que os consoles de administrador e não-administrador não pode ser executado ao mesmo tempo. (#626 GH)
<br/>
- Implementado as seguintes mensagens NETLINK_ROUTE (requer o administrador do Windows)
     - RTM_NEWADDR (dá suporte a `ip addr add`)
     - RTM_NEWROUTE (dá suporte a `ip route add`)
     - RTM_DELADDR (dá suporte a `ip addr del`)
     - RTM_DELROUTE (supports `ip route del`)
- Tarefa agendada, verificação de pacotes atualizar não serão mais executados em uma conexão limitada (GH #1371)
- Corrigido o erro em que canalizar obtém isto é, paralisada bash - c "ls - alR /" | bash -c "gato" (GH #1214)
- Opção de soquete TCP_KEEPCNT implementada (GH #843)
- Opção de soquete IP_MTU_DISCOVER INET implementada (GH #720, 717, 170, 69)
- Removida a funcionalidade herdada para executar binários de NT de init com pesquisa de caminho do NT. (GH #1325)
- Corrigir o modo de desenvolvimento/kmsg para permitir o acesso de leitura do grupo / (0644) (GH #1321)
- /Proc/sys/kernel/random/uuid implementado (GH #1092)
- Corrigido o erro em que a hora de início do processo estava mostrando como ano 2432 (GH #974)
- Variável de ambiente de termo padrão comutada para xterm-256color (GH #1446)
- Modificado da maneira que o processo de confirmação é calculada durante a bifurcação do processo. (#1286 GH)
- /Proc/sys/vm/overcommit_memory implementado. (#1286 GH)
- Arquivo /proc/net/route implementado (GH #69)
- Correção de erro em que o nome do atalho foi incorretamente localizado (GH #696)
- Elf fixa analisando a lógica que valida incorretamente os cabeçalhos do programa deve ser menor que (ou igual a) PATH_MAX. (GH #1048)
- Retorno de chamada statfs implementado para procfs, sysfs, cgroupfs e binfmtfs (GH #1378)
- Windows AptPackageIndexUpdate fixo que não será fechado (1184 de # GH, também são discutidas em GH #1193)
- Personalidade ASLR adicionada suporte ADDR_NO_RANDOMIZE. (GH #1148, 1128)
- PTRACE_GETSIGINFO aprimorada, SIGSEGV para rastreamentos de pilha do gdb adequado durante AV (GH #875)
- ELF, não há mais de análise falha por patchelf binários. (#471 GH)
- VPN DNS propagadas para /etc/resolv.conf (GH #416 1350)
- Feche o melhorias para TCP mais confiável para transferência de dados. (GH #610, 616, 1025, 1335)
- Código de erro correto agora retornam quando há muitos arquivos abertos (EMFILE). (GH #1126, 2090)
- Auditoria do Windows agora relatórios de log de nome de imagem no processo de criar uma auditoria.
- Normalmente falham ao iniciar bash.exe de dentro de uma janela de bash
- Mensagem de erro adicionado ao interoperabilidade não consegue acessar um diretório de trabalho em LxFs (ou seja, notepad.exe. bashrc)
- Corrigido um problema em que o caminho do Windows foi truncado no WSL
- Melhorias e correções adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 690 </br>
Número de falha (com falha, ignorada, etc...): 274 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Compilação 14986

Para Windows geral informações sobre compilação 14986, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Fixo

- Verificações de bugs fixas com Netlink e Pty IOCTLs
- Versão do kernel agora relata 4.4.0-43 para manter a consistência com Xenial
- Bash.exe agora inicia quando a entrada direcionada para ' nul:' (GH #1259)
- IDs de thread agora é relatada corretamente no procfs (GH 967 de #)
- IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Sinalizadores IN_ISDIR agora têm suportados no inotify_add_watch() (GH 1280 de #)
- Implemente timer_create e chamadas do sistema relacionados.  Isso habilita o suporte GHC (GH #307)
- Corrigido um problema em que o ping retornado um tempo de 0.000ms (GH #1296)
- Retorne o código de erro correta quando muitos arquivos são abertos.
- Problema corrigido no WSL em que a solicitação Netlink para dados de interface de rede falharia com EINVAL se o endereço da interface hardware for 32-bytes (como a interface Teredo)
   - Observe que o utilitário Linux "ip" contém um bug em que ele falhará se WSL relata um endereço de hardware de 32 bytes. Este é um bug no "ip", não WSL. O "ip" utilitário embute o comprimento do buffer de cadeia de caracteres usado para imprimir o endereço de hardware, e esse buffer for muito pequeno para imprimir um endereço de hardware de 32 bytes.
- Melhorias e correções adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 669 </br>
Número de falha (com falha, ignorada, etc...): 258 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Compilação 14971

Para Windows geral informações sobre compilação 14971, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Fixo

 - Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.  As atualizações agendadas regularmente serão retomada na próxima versão.

### <a name="ltp-results"></a>LTP resultados:
Inalterado desde 14965 </br>
Número de aprovação no teste: 664 </br>
Número de falha (com falha, ignorada, etc...): 263 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Compilação 14965

Para Windows geral informações sobre compilação 14965, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Fixo

- Suporte para Netlink soquetes do protocolo NETLINK_ROUTE RTM_GETLINK e RTM_GETADDR (GH #468)
  - Habilita comandos de ifconfig e ip para enumeração de rede
  - Mais informações podem ser encontradas no nosso [postagem de blog de rede WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- /sbin agora está no caminho do usuário por padrão
- Caminho de usuário NT agora anexado ao caminho WSL por padrão (ou seja, você pode agora digitar notepad.exe sem adicionar System32 para o caminho do Linux)
- Suporte adicionado para /proc/sys/kernel/cap_last_cap
- Binários do NT agora pode ser iniciados no WSL quando o diretório de trabalho atual contém caracteres não-ansi (GH #1254)
- Permitir desligamento em soquete de fluxo de unix desconectado.
- Adicionado suporte para PR_GET_PDEATHSIG.
- Suporte adicionado para CLONE_PARENT
- Corrigido o erro em que canalizar obtém isto é, paralisada bash - c "ls - alR /" | bash -c "gato" (GH #1214)
- Tratar solicitações para se conectar ao terminal atual.
- Marcar /proc/.<pid>/oom_score_adj como gravável.
- Adicione pasta /sys/fs/cgroup.
- sched_setaffinity deverá retornar o número de máscara de bits de afinidade
- Corrija a lógica de validação ELF que assume incorretamente os caminhos de interpretador devem ter menos de 64 caracteres. (#743 GH)
- Descritores de arquivo aberto podem manter a janela do console aberta (GH #1187)
- Erro de Fixeed onde Rename () falhou com barra no nome de destino (GH #1008) à direita
- Implementar /proc/net/dev arquivo
- Fixo 0.000ms executa ping devido à resolução do timer.
- /Proc/self/environ implementado (GH #730)
- Melhorias e correções de bugs adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 664 </br>
Número de falha (com falha, ignorada, etc...): 263 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Compilação 14959

Para Windows geral informações sobre compilação 14959, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Fixo

- Notificação aprimorada do processo de Pico para Windows.  Informações adicionais de [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).
- Maior estabilidade com a interoperabilidade do Windows
- Correção de erro 0x80070057 ao iniciar bash.exe quando o Enterprise Data Protection (EDP) está habilitado
- Melhorias e correções de bugs adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 665 </br>
Número de falha (com falha, ignorada, etc...): 263 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Compilação 14955

Para Windows geral informações sobre compilação 14955, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Fixo

 - Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.  As atualizações agendadas regularmente serão retomada na próxima versão.

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 665 </br>
Número de falha (com falha, ignorada, etc...): 263 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Compilação 14951

Para Windows geral informações sobre compilação 14951, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Novo recurso: Windows / interoperabilidade do Ubuntu
Binários do Windows agora podem ser chamados diretamente da linha de comando WSL.  Isso fornece aos usuários a capacidade de interagir com seu ambiente do Windows e o sistema de forma que não foi possível.  Como um exemplo rápido, é possível que os usuários executem os seguintes comandos:

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

Mais informações podem ser encontradas em:

- [Blog da equipe do WSL para interoperabilidade](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [Documentação de interoperabilidade do MSDN](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>Fixo

- Ubuntu 16.04 (Xenial) agora está instalado para todas as novas instâncias WSL.  Os usuários com as instâncias (confiáveis) 14.04 existentes não serão atualizados automaticamente.
- Localidade definida durante a instalação agora é exibida.
- Melhorias de terminal, incluindo o bug em que o redirecionamento de um processo WSL para um arquivo faz nem sempre funcionam
- Tempo de vida do console deve ser vinculado ao tempo de vida de bash.exe
- Tamanho da janela de console deve usar tamanho visível, o tamanho do buffer não
- Melhorias e correções de bugs adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 665 </br>
Número de falha (com falha, ignorada, etc...): 263 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Compilação 14946

Para Windows geral informações sobre compilação 14946, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Fixo

- Corrigido um problema que impediu a criação de contas de usuário do WSL para usuários com nomes de usuário do NT que contêm espaços ou aspas. 
- Alterar VolFs e DrvFs para retornar 0 para a contagem de links do diretório em stat
- Suporte à opção de soquete IPV6_MULTICAST_HOPS.
- Limite a um único console loop de e/s por tty. Exemplo: o comando a seguir é possível:
  - bash -c "dados echo" | bash - c "ssh user@example.com ' cat > foo '"

- Substitua os espaços por guias no /proc/cpuinfo (GH #1115)
- DrvFs agora aparece no mountinfo com um nome que corresponde ao volume montado do Windows
- /Home e raiz agora aparecem no mountinfo com nomes corretos
- Melhorias e correções de bugs adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 665 </br>
Número de falha (com falha, ignorada, etc...): 263 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Compilação 14942

Para Windows geral informações sobre compilação 14942, visite o [Blog Windows](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Fixo

- Um número de verificações de bugs resolvidos, incluindo o "TENTATIVA de executar de /NOEXECUTE memória" rede falha que foi bloqueando SSH
- o suporte para notificações geradas de aplicativos do Windows em DrvFs inotifiy está agora
- Implemente TCP_KEEPIDLE e TCP_KEEPINTVL para mongod. (#695 GH)
- Implementar a chamada do sistema pivot_root
- Implementar a opção de soquete para SO_DONTROUTE
- Melhorias e correções de bugs adicionais


### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 665 </br>
Número de falha (com falha, ignorada, etc...): 263 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Compilação 14936

Para Windows geral informações sobre compilação 14936, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Observação: WSL instalará Ubuntu versão 16.04 (Xenial) em vez do Ubuntu 14.04 (confiável) em uma versão futura.  Essa alteração será aplicada para Insiders instalar novas instâncias (lxrun.exe /install ou primeira execução do bash.exe).  As instâncias existentes com e confiável não serão atualizadas automaticamente. Os usuários podem atualizar suas imagens confiáveis para Xenial usando o comando de atualização de versão.

### <a name="known-issue"></a>Problema conhecido
WSL está enfrentando um problema com algumas implementações de soquete.  A verificação de erro se manifesta como uma falha com o erro "TENTATIVA de executar /NOEXECUTE memória INSUFICIENTE".  A manifestação mais comum desse problema é uma falha ao usar o ssh.  A causa raiz é fixo em compilações internas e será enviada para Insiders assim que possível.

### <a name="fixed"></a>Fixo

- Implementado a chamada do sistema chroot
- Melhorias no inotify ~~incluindo suporte para notificações geradas de aplicativos do Windows em DrvFs~~
  - Correção: Inotify dá suporte para alterações originadas a partir de aplicativos do Windows não está disponíveis no momento.
- Associação de IPv6 de soquete::<port n> agora dá suporte a IPV6_V6ONLY (GH #68, 157 #, #393, 460 #, #674, 740 #, #982, 996 #)
- Comportamento WNOWAIT para waitid systemcall implementado (GH #638)
- Suporte para opções de soquete IP IP_HDRINCL e IP_TTL
- Read () de comprimento zero deve retornar imediatamente (GH #975)
- Tratar corretamente os prefixos de nomes de arquivo e o nome do arquivo que não incluem um terminador nulo em um arquivo. tar.
- suporte a epoll o /dev/null
- Corrigir a fonte de tempo /dev/alarm
- Bash -c agora capaz de redirecionar para um arquivo
- Melhorias e correções de bugs adicionais

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 664 </br>
Número de falha (com falha, ignorada, etc...): 264 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Compilação 14931

Para Windows geral informações sobre compilação 14931, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Fixo

 - Devido a circunstâncias além do nosso controle não existem atualizações nesta compilação para o subsistema Windows para Linux.  As atualizações agendadas regularmente serão retomada na próxima versão.

<br/>

## <a name="build-14926"></a>Compilação 14926

Para Windows geral informações sobre compilação 14926, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Fixo

- Ping agora funciona em consoles que não têm privilégios de administrador
- Ping6 agora tem suportada, também sem privilégios de administrador
- Suporte de Inotify para arquivos modificados por meio de WSL. (GH #216)
  - Sinalizadores com suporte:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - ler a saída: LX_IN_ISDIR, LX_IN_IGNORED
  - Problema conhecido: Modificar arquivos de aplicativos do Windows não gera nenhum evento
- Soquete do UNIX agora dá suporte a SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP resultados:
Número de aprovação no teste: 651 </br>
Número de falha (com falha, ignorada, etc...): 258 </br>
[Logs de execução de teste LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Compilação 14915

Para Windows geral informações sobre compilação 14915, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fixo
-  Socketpair para soquetes de datagrama (GH #262) do unix
- Suporte de soquete do UNIX para SO_REUSEADDR
- Suporte de soquete do UNIX para SO_BROADCAST (GH #568)
- Suporte de soquete do UNIX para SOCK_SEQPACKET (GH #758 546 #)
- Adicionando suporte para envio de soquete de datagrama de unix, recebimento e desligamento
- Corrija a verificação de erro devido à validação de parâmetro inválido mmap para endereços não fixos. (#847 GH)
- Suporte para suspender / retomar de estados de terminal
- Suporte para TIOCPKT ioctl desbloquear o utilitário de tela (GH #774)
    - Problema conhecido: Teclas de função não operacionais
- Corrigida uma corrida no TimerFd que poderia causar um membro liberado ReaderReady seja acessada por LxpTimerFdWorkerRoutine (GH #814)
- Habilitar o suporte de chamada do sistema reinicializável para futex, sondagem e clock_nanosleep
- Suporte de montagem de associação adicionado
- remover o compartilhamento para oferecer suporte ao namespace de montagem
    - Problema conhecido: Ao criar um novo namespace de montagem com `unshare(CLONE_NEWNS)` diretório de trabalho atual continuará apontar para o namespace antigo
- Outros aperfeiçoamentos e correções de bugs

<br/>

## <a name="build-14905"></a>Compilação 14905

Para Windows geral informações sobre compilação 14905, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Fixo
- Sistema reinicializável chamadas agora são suportado (GH #349 GH #520)
- Links simbólicos para diretórios terminando em / agora operacionais (GH #650)
- Implementado ioctl RNDGETENTCNT para /dev/random
- Implementado o /proc/. [pid] / monta /proc/. [pid] / mountinfo e /proc/. [pid] / mountstats arquivos
- Melhorias e correções de bugs adicionais

</br>

## <a name="build-14901"></a>Compilação 14901
Primeiro Insider build para a versão de atualização de aniversário do Windows 10 de postagem.

Para Windows geral informações sobre compilação 14901, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Fixo
- Corrigido o problema de barra "/" à direita
    - Comandos como `$ mv a/c/ a/b/` agora funciona
- Instalando agora solicita se Ubuntu localidade deve ser definida como localidade do Windows
- Procfs suporte para a pasta de ns
- Adicionado a montagem e desmontagem para tmpfs, procfs e sistemas de arquivos sysfs
- Corrigir mknod [arroba], assinatura ABI de 32 bits
- Movido para o modelo de expedição de soquetes do UNIX
- Tamanho do buffer de recebimento INET soquete definido usando o setsockopt deveria ser respeitado.
- Sinalizador de mensagem de recebimento de soquete do unix MSG_CMSG_CLOEXEC implementar
- Redirecionamento de pipe de stdin/stdout de processo do Linux (GH n º 2)
    - Permite que o pipe de comandos de bash - c no CMD.  Exemplo: > dir | bash -c "grep foo"
- Bash agora pode ser instalado em sistemas com vários arquivos de paginação (GH #538 358 #)
- Tamanho do buffer de soquete INET padrão deve corresponder da configuração padrão do Ubuntu
- Alinhar syscalls xattr para listxattr
- Retornar apenas as interfaces com um endereço IPv4 válido de SIOCGIFCONF
- Corrigir a ação padrão de sinal quando injetado por ptrace
- implement /proc/sys/vm/min_free_kbytes
- Use os valores do registro de contexto de máquina ao restaurar o contexto no sigreturn
    - Isso resolve o problema em que o java e javac foram deslocado para alguns usuários
- Implementar /proc/sys/kernel/hostname

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Compilar 14388 para atualização de aniversário do Windows 10
Para Windows geral informações sobre compilação 14388, visite o [Blog Windows](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Fixo
- Correções para se preparar para a atualização de aniversário do Windows 10 em 8/2
  - Para obter mais informações sobre como o WSL na atualização de aniversário podem ser encontradas em nossa [blog](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>Compilação 14376
Para Windows geral informações sobre compilação 14376, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Fixo
- Removido algumas instâncias em que o apt-get trava (GH #493)
- Corrigido um problema em que as montagens vazias não foram tratadas corretamente
- Corrigido um problema em que ramdisks não foram montados corretamente
- Aceitação de soquete do unix de alteração para dar suporte a sinalizadores (parcial GH #451)
- Fixo de rede comuns relacionadas a tela azul
- Corrigido o bluescreen ao acessar /proc/. [pid] / tarefa (GH #523)
- Fixo alta utilização da CPU para alguns cenários pty (GH 488 #, #504)
- Melhorias e correções de bugs adicionais

<br/>

## <a name="build-14371"></a>Compilação 14371
Para Windows geral informações sobre compilação 14371, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Fixo
- Corrigida a corrida de medição de tempo com SIGCHLD e wait() ao usar ptrace
- Corrigidos alguns comportamentos quando os caminhos têm à direita / (GH #432)
- Corrigido o problema com a renomeação/desvincular falhando devido a identificadores abertos para crianças
- Melhorias e correções de bugs adicionais

<br/>

## <a name="build-14366"></a>Compilação 14366
Para Windows geral informações sobre compilação 14366, visite o [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Fixo
- Corrigir na criação do arquivo por meio de links simbólicos
-   Adicionado listxattr para Python (GH 385)
-   Melhorias e correções de bugs adicionais

### <a name="syscall-support"></a>Suporte de syscall
-   Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>O build 14361
Para Windows geral informações no build 14361, visite o [Blog Windows](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Fixo
- DrvFs agora diferencia maiusculas de minúsculas quando em execução no Bash no Ubuntu no Windows.
  - Os usuários case.txt de maio e caso. Unidades de TXT no seu c/dev/emcpowera1
  - Somente há suporte para a diferenciação de maiusculas dentro do Bash no Ubuntu no Windows. Quando fora do NTFS Bash relatará corretamente os arquivos, mas um comportamento inesperado pode ocorrer a interação com os arquivos do Windows.
  - A raiz de cada volume (ou seja, /mnt/c) não diferencia maiusculas de minúsculas
  - Para obter mais informações sobre como tratar esses arquivos no Windows podem ser encontradas [aqui](https://support.microsoft.com/en-us/kb/100625).
- Aperfeiçoou pty / tty suporte.  Aplicativos como TMUX agora tem suporte (GH n º 40)
- Problema de instalação fixa em que contas de usuário criadas nem sempre
- Estrutura de arg de linha de comando, permitindo a lista de argumentos muitíssimo otimizada. (#153 GH)
- Arquivos de read_only agora capaz de excluir e chmod de DrvFs
- Corrigidos alguns casos onde a terminal trava na desconexão (GH n º 43)
- chmod e alterar o proprietário agora funcionam em dispositivos de tty
- Permitir a conexão para 0.0.0.0 e:: como localhost (GH 388)
- Sendmsg/recvmsg agora lidar com um comprimento do vetor de e/s de > 1 (parcial GH #376)
- Os usuários podem agora recusá-la do arquivo de hosts gerada automaticamente (GH #398)
- A correspondência automática de localidade do Linux para a localidade do NT durante a instalação (GH #11)
- Adicionado o arquivo /proc/sys/vm/swappiness (GH #306)
- strace agora é encerrado corretamente
- Permitir que os pipes para ser reaberto por meio de /proc/self/fd (GH #222)
- Ocultar diretórios sob %LOCALAPPDATA%\lxss de DrvFs (GH #270)
- Melhor tratamento de bash.exe ~.  Comandos como "bash ~ ls - c" agora tem suporte (GH #467)
- Soquetes agora notificar epoll leitura disponível durante o desligamento (GH #271)
- lxrun / desinstalação faz um trabalho melhor de excluir os arquivos e pastas
- Corrigido ps -f (GH #246)
- Suporte aprimorado para x11 aplicativos como xEmacs (GH #481)
- Atualizado o tamanho de pilha do thread inicial para corresponder à configuração do Ubuntu padrão e informar o tamanho corretamente para o syscall get_rlimit (GH 172 #, #258)
- Relatórios de nomes de imagem de processo de pico (por exemplo, para fazer auditoria) aprimorados
- /Proc/mountinfo implementado para o comando df
- Correção de código de erro de symlink para o nome do filho. e...
- Melhorias e correções de bug de aprimoramentos adicionais

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Build 14352
Para Windows geral informações no build 14352, visite o [Blog Windows](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Fixo
- Correção do problema em que grandes arquivos não foram baixados / criados corretamente.  Isso deve desbloquear npm e outros cenários (GH n º 3, GH #313)
- Removido algumas instâncias onde soquetes de suspensão
- Corrigidos alguns erros ptrace
- Corrigido o problema com o WSL, permitindo que mais de 255 caracteres de nomes de arquivo
- Suporte aprimorado para caracteres estendidos
- Adicionar dados de fuso horário atual do Windows e definir como padrão
- Do id exclusiva do dispositivo para cada ponto de montagem (fix jre – GH n º 49)
- Corrigir problema com caminhos que contenham "." e ".."
- Adicionado suporte Fifo (GH #71)
- Formato atualizado do resolv. conf para corresponder ao formato nativo do Ubuntu
- Uma limpeza procfs
- Ping habilitado para consoles do administrador (GH n º 18)

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Compilação 14342
Para Windows geral informações sobre compilação 14342 a [Blog Windows](https://aka.ms/wip14342). <br/>

Informações sobre VolFs e DriveFs podem ser encontradas na [WSL Blog](https://blogs.msdn.microsoft.com/wsl). <br/>

### <a name="fixed"></a>Fixo
- Corrigido o problema de instalação quando o usuário do Windows tinha caracteres Unicode no nome de usuário
- A solução alternativa udev de atualização de apt-get nas perguntas Frequentes agora é fornecida por padrão na primeira execução
- Habilitada a links simbólicos no DriveFs (/mnt/<drive>) diretórios
- Links simbólicos agora funcionam entre DriveFs e VolFs
- Caminho de nível superior endereçado ao problema de análise: ls. / / agora funcionará conforme o esperado
- instalar o NPM em DriveFs e as opções -g agora estão trabalhando
- Problema corrigido, impedindo que o servidor PHP iniciando
- Valores de ambiente padrão atualizado, como $PATH para corresponder mais próximos Ubuntu nativo
- Adicionada uma tarefa de manutenção semanal no Windows para atualizar o cache de pacotes apt
- Corrigido um problema com a validação de cabeçalho ELF, WSL agora dá suporte a todas as opções de Melkor
- Shell zsh é funcional
- Agora há suporte para os binários pré-compilados do Go
- Avisar sobre Bash.exe executado pela primeira vez agora está localizado corretamente
- /proc/meminfo agora retorna informações corretas
- Soquetes agora têm suportados no VFS
- /dev agora montado como tempfs
- PEPS agora tem suportada
- Sistemas de vários núcleos agora mostrando corretamente em/proc/cpuinfo
- Melhorias adicionais e mensagens de erro de download durante a primeira execução
- Syscall melhorias e correções de bugs. Syscall com suporte a lista abaixo.
- Melhorias e correções de bugs adicionais

### <a name="known-issues"></a>Problemas conhecidos
- Não Resolvendo '.. ' corretamente em DriveFs em alguns casos

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls novos ou aprimorados que têm uma implementação em WSL. Os syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

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

## <a name="build-14332"></a>Compilação 14332

Para Windows geral informações sobre compilação 14332, visite o [Blog Windows](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Fixo
- Melhor geração de resolv. conf, incluindo a priorizar as entradas DNS
- Problema com a movimentação de arquivos e diretórios entre /mnt e não- / mnt unidades
- Os arquivos tar agora podem ser criados com links simbólicos
- Diretório de /run/lock padrão adicionados na criação da instância
- Atualizar o /dev/null para retornar informações de stat adequada
- Erros adicionais durante o download durante a primeira execução
- Syscall melhorias e correções de bugs. Syscall com suporte a lista abaixo.
- Melhorias e correções de bug de aprimoramentos adicionais

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está a nova syscall que tem alguma implementação em WSL. O syscall nesta lista tem suporte pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Build 14328

Para Windows geral informações sobre compilação 14332, visite o [Blog Windows](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Novos recursos
* Agora dão suporte a usuários do Linux.  Instalação do Bash no Ubuntu no Windows solicitará que para a criação de um usuário do Linux.  Para obter mais informações, visite https://aka.ms/wslusers
* Nome do host agora está definido para o nome do computador Windows, não há mais @localhost
* Para obter mais informações sobre build 14328, visite: https://aka.ms/wip14328

### <a name="fixed"></a>Fixo
* Melhorias de symlink para /mnt/ não<drive> arquivos
    * instalação de NPM agora funciona
    * JDK / jre agora pode ser instalado usando as instruções encontradas [aqui](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).
    * problema conhecido: links simbólicos não funcionam para o Windows monta.  Funcionalidade estará disponível em uma compilação posterior
* parte superior e htop agora exibem
* Mensagens de erro adicionais para algumas falhas de instalação
* Syscall melhorias e correções de bugs.  Syscall com suporte a lista abaixo.
* Melhorias e correções de bug de aprimoramentos adicionais

### <a name="syscall-support"></a>Suporte de syscall
Abaixo está uma lista de syscalls com alguma implementação em WSL.  Syscalls nessa lista são suportados pelo menos um cenário, mas podem não ter todos os parâmetros de suporte no momento.

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
