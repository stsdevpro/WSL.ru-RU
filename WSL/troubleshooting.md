---
title: Устранение неполадок подсистемы Windows для Linux
description: Содержит подробные сведения о распространенных ошибках и проблемах, с которыми сталкиваются пользователи при выполнении Linux в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 09/28/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: f4040cbe9faf5d55324b56974dd5677052224dd1
ms.sourcegitcommit: d5d3dd8b91e93d46653f9512bceafd8b5340255f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96443748"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="d4906-104">Устранение неполадок подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="d4906-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="d4906-105">Для получения поддержки по вопросам, связанным с WSL, изучите наш [репозиторий продукта WSL на сайте GitHub](https://github.com/Microsoft/wsl/issues).</span><span class="sxs-lookup"><span data-stu-id="d4906-105">For support with issues related to WSL, please see our [WSL product repo on GitHub](https://github.com/Microsoft/wsl/issues).</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="d4906-106">Поиск описанных проблем, связанных с вашей проблемой</span><span class="sxs-lookup"><span data-stu-id="d4906-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="d4906-107">При возникновении технических проблем используйте [репозиторий продукта](https://github.com/Microsoft/wsl/issues).</span><span class="sxs-lookup"><span data-stu-id="d4906-107">For technical issues, use the [product repo](https://github.com/Microsoft/wsl/issues).</span></span>

<span data-ttu-id="d4906-108">При возникновении проблем, связанных с содержимым этой документации, используйте [репозиторий документов](https://github.com/MicrosoftDocs/wsl/issues).</span><span class="sxs-lookup"><span data-stu-id="d4906-108">For issues related to the contents of this documentation, use the [docs repo](https://github.com/MicrosoftDocs/wsl/issues).</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="d4906-109">Отправка отчета об ошибке</span><span class="sxs-lookup"><span data-stu-id="d4906-109">Submit a bug report</span></span>

<span data-ttu-id="d4906-110">При возникновении ошибок, связанных с функциями или компонентами WSL, отправьте сообщение о проблеме в репозитории продуктов: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="d4906-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="d4906-111">Отправка запроса на добавление возможностей</span><span class="sxs-lookup"><span data-stu-id="d4906-111">Submit a feature request</span></span>

<span data-ttu-id="d4906-112">Чтобы запросить новую возможность, связанную с функциональностью или совместимостью WSL, [создайте запрос в репозитории продуктов](https://github.com/Microsoft/wsl/issues).</span><span class="sxs-lookup"><span data-stu-id="d4906-112">To request a new feature related to WSL functionality or compatibility, [file an issue in the product repo](https://github.com/Microsoft/wsl/issues).</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="d4906-113">Участие в разработке документации</span><span class="sxs-lookup"><span data-stu-id="d4906-113">Contribute to the docs</span></span>

<span data-ttu-id="d4906-114">Чтобы внести изменения в документацию по WSL, отправьте запрос на вытягивание в репозитории документов: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="d4906-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="d4906-115">Терминал или командная строка</span><span class="sxs-lookup"><span data-stu-id="d4906-115">Terminal or Command Line</span></span>

<span data-ttu-id="d4906-116">Наконец, если ваша проблема связана с терминалом Windows, консолью Windows или интерфейсом командной строки, используйте репозиторий терминалов Windows: https://github.com/microsoft/terminal</span><span class="sxs-lookup"><span data-stu-id="d4906-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="d4906-117">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="d4906-117">Common issues</span></span>

### <a name="im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2"></a><span data-ttu-id="d4906-118">Я использую Windows 10 версии 1903, но не вижу параметры для WSL 2.</span><span class="sxs-lookup"><span data-stu-id="d4906-118">I'm on Windows 10 version 1903 and I still do not see options for WSL 2</span></span>

<span data-ttu-id="d4906-119">Скорее всего, это связано с тем, что на компьютере еще не установлены исправления для WSL 2.</span><span class="sxs-lookup"><span data-stu-id="d4906-119">This is likely because your machine has not yet taken the backport for WSL 2.</span></span> <span data-ttu-id="d4906-120">Чтобы решить эту проблему самым простым способом, перейдите в параметры Windows, нажмите кнопку "Проверить наличие обновлений" и установите последние обновления в системе.</span><span class="sxs-lookup"><span data-stu-id="d4906-120">The simplest way to resolve this is by going to Windows Settings and clicking 'Check for Updates' to install the latest updates on your system.</span></span> <span data-ttu-id="d4906-121">Изучите [полные инструкции по получению исправления для старой версии](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span><span class="sxs-lookup"><span data-stu-id="d4906-121">See [the full instructions on taking the backport](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span></span>

<span data-ttu-id="d4906-122">Если после нажатия кнопки "Проверить наличие обновлений" вы не получили обновление, можно [установить исправления KB4566116 вручную](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4566116).</span><span class="sxs-lookup"><span data-stu-id="d4906-122">If you hit 'Check for Updates' and still do not receive the update you can [install KB KB4566116 manually](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4566116).</span></span>  

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a><span data-ttu-id="d4906-123">Ошибка. 0x1bc, когда `wsl --set-default-version 2`</span><span class="sxs-lookup"><span data-stu-id="d4906-123">Error: 0x1bc when `wsl --set-default-version 2`</span></span>

<span data-ttu-id="d4906-124">Это может произойти, если язык интерфейса или язык системы не является английским.</span><span class="sxs-lookup"><span data-stu-id="d4906-124">This may happen when 'Display Language' or 'System Locale' setting is not English.</span></span>

```powershell
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

<span data-ttu-id="d4906-125">Фактическая ошибка для `0x1bc`:</span><span class="sxs-lookup"><span data-stu-id="d4906-125">THe actual error for `0x1bc` is:</span></span>

```powershell
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

<span data-ttu-id="d4906-126">См. сведения о проблеме [5749](https://github.com/microsoft/WSL/issues/5749).</span><span class="sxs-lookup"><span data-stu-id="d4906-126">For more information, please refer to issue [5749](https://github.com/microsoft/WSL/issues/5749)</span></span>

### <a name="cannot-access-wsl-files-from-windows"></a><span data-ttu-id="d4906-127">Не удается получить доступ к файлам WSL из Windows</span><span class="sxs-lookup"><span data-stu-id="d4906-127">Cannot access WSL files from Windows</span></span>

<span data-ttu-id="d4906-128">Файловый сервер протокола 9p предоставляет службу на стороне Linux, которая позволяет Windows получить доступ к файловой системе Linux.</span><span class="sxs-lookup"><span data-stu-id="d4906-128">A 9p protocol file server provides the service on the Linux side to allow Windows to access the Linux file system.</span></span> <span data-ttu-id="d4906-129">Если вы не можете получить доступ к WSL с помощью `\\wsl$` в Windows, возможно, это вызвано неправильным запуском 9P.</span><span class="sxs-lookup"><span data-stu-id="d4906-129">If you cannot access WSL using `\\wsl$` on Windows, it could be because 9P did not start correctly.</span></span>

<span data-ttu-id="d4906-130">Чтобы убедиться в этом, можно проверить журналы запуска с помощью команды `dmesg |grep 9p`. Если ошибки есть, отобразятся сведения о них.</span><span class="sxs-lookup"><span data-stu-id="d4906-130">To check this, you can check the start up logs using: `dmesg |grep 9p`, and this will show you any errors.</span></span> <span data-ttu-id="d4906-131">Вывод выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d4906-131">A successfull output looks like the following:</span></span>

```bash
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

<span data-ttu-id="d4906-132">Дополнительные сведения об этой ошибке см. в [этом потоке GitHub](https://github.com/microsoft/wsl/issues/5307).</span><span class="sxs-lookup"><span data-stu-id="d4906-132">Please see [this Github thread](https://github.com/microsoft/wsl/issues/5307) for further discussion on this issue.</span></span>

### <a name="cant-start-wsl-2-distribution-and-only-see-wsl-2-in-output"></a><span data-ttu-id="d4906-133">Не удается запустить дистрибутив WSL 2, а в выходных данных отображается только WSL 2.</span><span class="sxs-lookup"><span data-stu-id="d4906-133">Can't start WSL 2 distribution and only see 'WSL 2' in output</span></span>

<span data-ttu-id="d4906-134">Если язык интерфейса не английский, возможно, отображается усеченная версия текста ошибки.</span><span class="sxs-lookup"><span data-stu-id="d4906-134">If your display language is not English, then it is possible you are seeing a truncated version of an error text.</span></span>

```powershell
C:\Users\me>wsl
WSL 2
```

<span data-ttu-id="d4906-135">Чтобы устранить эту проблему, перейдите по адресу `https://aka.ms/wsl2kernel` и установите ядро вручную, следуя инструкциям на этой странице документации.</span><span class="sxs-lookup"><span data-stu-id="d4906-135">To resolve this issue, please visit `https://aka.ms/wsl2kernel` and install the kernel manually by following the directions on that doc page.</span></span> 

### <a name="command-not-found-when-executing-windows-exe-in-linux"></a><span data-ttu-id="d4906-136">Ошибка `command not found` при выполнении исполняемых файлов Windows в Linux</span><span class="sxs-lookup"><span data-stu-id="d4906-136">`command not found` when executing windows .exe in linux</span></span>

<span data-ttu-id="d4906-137">Пользователи могут запускать исполняемые файлы Windows, например notepad.exe, прямо в среде Linux.</span><span class="sxs-lookup"><span data-stu-id="d4906-137">Users can run Windows executables like notepad.exe directly from Linux.</span></span> <span data-ttu-id="d4906-138">Но иногда это действие приводит к ошибке "Команда не найдена", как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="d4906-138">Sometimes, you may hit "command not found" like below:</span></span> 

```Bash
$ notepad.exe
-bash: notepad.exe: command not found
```

<span data-ttu-id="d4906-139">Если в переменной $PATH нет обязательных путей Win32, подсистема взаимодействие не сможет найти EXE-файл.</span><span class="sxs-lookup"><span data-stu-id="d4906-139">If there are no win32 paths in your $PATH, interop isn't going to find the .exe.</span></span>
<span data-ttu-id="d4906-140">Чтобы проверить это, выполните `echo $PATH` в среде Linux.</span><span class="sxs-lookup"><span data-stu-id="d4906-140">You can verify it by running `echo $PATH` in Linux.</span></span> <span data-ttu-id="d4906-141">В выходных данных вы должны увидеть путь к win32 (например, /mnt/c/Windows).</span><span class="sxs-lookup"><span data-stu-id="d4906-141">It's expected that you will see a win32 path (for example, /mnt/c/Windows) in the output.</span></span>
<span data-ttu-id="d4906-142">Если вы не видите эти пути Windows, скорее всего переменная PATH перезаписана оболочкой Linux.</span><span class="sxs-lookup"><span data-stu-id="d4906-142">If you can't see any Windows paths then most likely your PATH is being overwritten by your Linux shell.</span></span> 

<span data-ttu-id="d4906-143">Ниже приведен пример файла /etc/profile на ОС Debian, который вызывал такую проблему:</span><span class="sxs-lookup"><span data-stu-id="d4906-143">Here is a an example that /etc/profile on Debian contributed to the problem:</span></span>

```Bash
if [ "`id -u`" -eq 0 ]; then
  PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
else
  PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games"
fi
```

<span data-ttu-id="d4906-144">Чтобы решить эту проблему в среде Debian, нужно удалить приведенные выше строки.</span><span class="sxs-lookup"><span data-stu-id="d4906-144">The correct way on Debian is to remove above lines.</span></span>
<span data-ttu-id="d4906-145">Вы также можете добавить значения в переменную $PATH во время назначения, как показано ниже, но это может вызвать [другие проблемы](https://salsa.debian.org/debian/WSL/-/commit/7611edba482fd0b3f67143aa0fc1e2cc1d4100a6) с WSL и VSCode.</span><span class="sxs-lookup"><span data-stu-id="d4906-145">You may also append $PATH during the assignment like below, but this lead to some [other problems](https://salsa.debian.org/debian/WSL/-/commit/7611edba482fd0b3f67143aa0fc1e2cc1d4100a6) with WSL and VSCode..</span></span>

<span data-ttu-id="d4906-146">Дополнительные сведения см. в описании проблем [5296](https://github.com/microsoft/WSL/issues/5296) и [5779](https://github.com/microsoft/WSL/issues/5779).</span><span class="sxs-lookup"><span data-stu-id="d4906-146">For more information, see issue [5296](https://github.com/microsoft/WSL/issues/5296) and issue [5779](https://github.com/microsoft/WSL/issues/5779).</span></span>

### <a name="error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed"></a><span data-ttu-id="d4906-147">"Ошибка: 0x80370102 The virtual machine could not be started because a required feature is not installed (Не удалось запустить виртуальную машину, так как не установлена необходимая функция).</span><span class="sxs-lookup"><span data-stu-id="d4906-147">"Error: 0x80370102 The virtual machine could not be started because a required feature is not installed."</span></span>

<span data-ttu-id="d4906-148">Включите компонент платформы виртуальных машин Windows и убедитесь, что в BIOS включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="d4906-148">Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.</span></span>

1. <span data-ttu-id="d4906-149">Проверка [требований к системе Hyper-V](/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span><span class="sxs-lookup"><span data-stu-id="d4906-149">Check the [Hyper-V system requirements](/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span></span>

2. <span data-ttu-id="d4906-150">Если компьютер является виртуальной машиной, включите [вложенную виртуализацию](./wsl2-faq.md#can-i-run-wsl-2-in-a-virtual-machine) вручную.</span><span class="sxs-lookup"><span data-stu-id="d4906-150">If your machine is a VM, please enable [nested virtualization](./wsl2-faq.md#can-i-run-wsl-2-in-a-virtual-machine) manually.</span></span> <span data-ttu-id="d4906-151">Запустите PowerShell с правами администратора и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d4906-151">Launch powershell with admin, and run:</span></span>

    ```powershell
    Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
    ```

3. <span data-ttu-id="d4906-152">Следуйте рекомендациям производителя компьютера, чтобы включить виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="d4906-152">Please follow guidelines from your PC's manufacturer on how to enable virtualization.</span></span> <span data-ttu-id="d4906-153">Как правило, для проверки того, что эти функции включены в ЦП, может использоваться BIOS системы.</span><span class="sxs-lookup"><span data-stu-id="d4906-153">In general, this can involve using the system BIOS to ensure that these features are enabled on your CPU.</span></span> <span data-ttu-id="d4906-154">Инструкции для этого процесса могут быть разными для разных компьютеров, один из примеров вы можете изучить в [этой статье](https://www.bleepingcomputer.com/tutorials/how-to-enable-cpu-virtualization-in-your-computer-bios/) от Bleeping Computer.</span><span class="sxs-lookup"><span data-stu-id="d4906-154">Instructions for this process can vary from machine to machine, please see [this article](https://www.bleepingcomputer.com/tutorials/how-to-enable-cpu-virtualization-in-your-computer-bios/) from Bleeping Computer for an example.</span></span>

4. <span data-ttu-id="d4906-155">Перезагрузите компьютер после включения дополнительного компонента `Virtual Machine Platform`.</span><span class="sxs-lookup"><span data-stu-id="d4906-155">Restart your machine after enabling the `Virtual Machine Platform` optional component.</span></span>

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="d4906-156">Bash утрачивает подключение к сети после подключения к сети VPN</span><span class="sxs-lookup"><span data-stu-id="d4906-156">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="d4906-157">Если после подключения к VPN в Windows оболочка Bash утрачивает подключение к сети, попробуйте воспользоваться этим обходным решением в Bash.</span><span class="sxs-lookup"><span data-stu-id="d4906-157">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="d4906-158">Это решение позволит вручную переопределить разрешение DNS с помощью `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="d4906-158">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="d4906-159">Запишите DNS-сервер виртуальной частной сети. Для этого выполните `ipconfig.exe /all`</span><span class="sxs-lookup"><span data-stu-id="d4906-159">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="d4906-160">Создайте копию существующего resolv.conf, выполнив `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span><span class="sxs-lookup"><span data-stu-id="d4906-160">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="d4906-161">Разорвите связь с текущим файлом resolv.conf, выполнив команду `sudo unlink /etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="d4906-161">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="d4906-162">Откройте `/etc/resolv.conf` и сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="d4906-162">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="d4906-163">a.</span><span class="sxs-lookup"><span data-stu-id="d4906-163">a.</span></span> <span data-ttu-id="d4906-164">Удалите из файла первую строку с текстом "\# This file was automatically generated by WSL.</span><span class="sxs-lookup"><span data-stu-id="d4906-164">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="d4906-165">To stop automatic generation of this file, remove this line." (Этот файл был автоматически создан WSL. Чтобы остановить автоматическое создание этого файла, удалите данную строку).</span><span class="sxs-lookup"><span data-stu-id="d4906-165">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="d4906-166">b.</span><span class="sxs-lookup"><span data-stu-id="d4906-166">b.</span></span> <span data-ttu-id="d4906-167">Добавьте запись DNS из пункта 1 выше в качестве первой записи в списке DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="d4906-167">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="d4906-168">c.</span><span class="sxs-lookup"><span data-stu-id="d4906-168">c.</span></span> <span data-ttu-id="d4906-169">Закройте файл.</span><span class="sxs-lookup"><span data-stu-id="d4906-169">Close the file.</span></span> <br/>

<span data-ttu-id="d4906-170">После отключения VPN необходимо будет отменить изменения в `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="d4906-170">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="d4906-171">Для этого сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="d4906-171">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="d4906-172">При запуске WSL или установке дистрибутива возвращается код ошибки</span><span class="sxs-lookup"><span data-stu-id="d4906-172">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="d4906-173">Выполните [эти инструкции](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs), чтобы получить подробные журналы и сообщить о возникшей проблеме на портале GitHub.</span><span class="sxs-lookup"><span data-stu-id="d4906-173">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="d4906-174">Обновление Bash для Ubuntu в Windows</span><span class="sxs-lookup"><span data-stu-id="d4906-174">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="d4906-175">Два компонента Bash для Ubuntu в Windows могут требовать обновления.</span><span class="sxs-lookup"><span data-stu-id="d4906-175">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="d4906-176">Подсистема Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="d4906-176">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="d4906-177">Обновление этой части Bash для Ubuntu в Windows обеспечит применение всех новых исправлений, описанных в [заметках о выпуске](./release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="d4906-177">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="d4906-178">Убедитесь, что вы подписаны на Программу предварительной оценки Windows и что ваша сборка обновлена.</span><span class="sxs-lookup"><span data-stu-id="d4906-178">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="d4906-179">Чтобы обеспечить более точное управление, включая сброс экземпляра Ubuntu, ознакомьтесь со [страницей справочных материалов по командам](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="d4906-179">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="d4906-180">Двоичные файлы пользователя Ubuntu</span><span class="sxs-lookup"><span data-stu-id="d4906-180">The Ubuntu user binaries</span></span>

   <span data-ttu-id="d4906-181">При обновлении этой части Bash для Ubuntu в Windows будут установлены все обновления двоичных файлов пользователя Ubuntu, включая приложения, установленные с помощью apt-get.</span><span class="sxs-lookup"><span data-stu-id="d4906-181">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="d4906-182">Чтобы выполнить обновление, выполните следующие команды в Bash.</span><span class="sxs-lookup"><span data-stu-id="d4906-182">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="d4906-183">Ошибки apt-get upgrade</span><span class="sxs-lookup"><span data-stu-id="d4906-183">Apt-get upgrade errors</span></span>

<span data-ttu-id="d4906-184">Некоторые пакеты используют функции, которые еще не реализованы.</span><span class="sxs-lookup"><span data-stu-id="d4906-184">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="d4906-185">Например, `udev`пока не поддерживается и вызывает несколько ошибок `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="d4906-185">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="d4906-186">Чтобы устранить проблемы, связанные с `udev`, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d4906-186">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="d4906-187">Введите приведенный ниже код в `/usr/sbin/policy-rc.d` и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="d4906-187">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="d4906-188">Добавьте разрешения на выполнение в `/usr/sbin/policy-rc.d`:</span><span class="sxs-lookup"><span data-stu-id="d4906-188">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="d4906-189">Выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="d4906-189">Run the following commands:</span></span>

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="d4906-190">"Ошибка: 0x80040306" при установке</span><span class="sxs-lookup"><span data-stu-id="d4906-190">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="d4906-191">Это связано с тем, что мы не поддерживаем устаревшую консоль.</span><span class="sxs-lookup"><span data-stu-id="d4906-191">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="d4906-192">Чтобы отключить устаревшую консоль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d4906-192">To turn off legacy console:</span></span>

1. <span data-ttu-id="d4906-193">Выполните файл cmd.exe.</span><span class="sxs-lookup"><span data-stu-id="d4906-193">Open cmd.exe</span></span>
1. <span data-ttu-id="d4906-194">Щелкните правой кнопкой мыши строку заголовка и выберите "Свойства", затем снимите флажок "Использовать прежнюю версию консоли".</span><span class="sxs-lookup"><span data-stu-id="d4906-194">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="d4906-195">Нажмите кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="d4906-195">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="d4906-196">"Ошибка: 0x80040154" после обновления Windows</span><span class="sxs-lookup"><span data-stu-id="d4906-196">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="d4906-197">Компонент "Подсистема Windows для Linux" может быть отключен во время обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="d4906-197">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="d4906-198">В этом случае данную функцию Windows необходимо включить заново.</span><span class="sxs-lookup"><span data-stu-id="d4906-198">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="d4906-199">Инструкции по включению подсистемы Windows для Linux можно найти в [руководстве по установке](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="d4906-199">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="d4906-200">Изменение отображаемого языка</span><span class="sxs-lookup"><span data-stu-id="d4906-200">Changing the display language</span></span>

<span data-ttu-id="d4906-201">Установщик WSL попытается автоматически изменить языковой стандарт Ubuntu в соответствии с языковым стандартом установки Windows.</span><span class="sxs-lookup"><span data-stu-id="d4906-201">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="d4906-202">Если это нежелательно, можно выполнить приведенную ниже команду, чтобы изменить языковой стандарт Ubuntu после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="d4906-202">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="d4906-203">Чтобы это изменение вступило в силу, потребуется повторно запустить bash.exe.</span><span class="sxs-lookup"><span data-stu-id="d4906-203">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="d4906-204">В приведенном ниже примере языковой стандарт изменяется на EN-US.</span><span class="sxs-lookup"><span data-stu-id="d4906-204">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="d4906-205">Проблемы установки после восстановления системы Windows</span><span class="sxs-lookup"><span data-stu-id="d4906-205">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="d4906-206">Удалите папку `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="d4906-206">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="d4906-207">**Примечание. Не делайте этого, если дополнительный компонент полностью установлен и работает.**</span><span class="sxs-lookup"><span data-stu-id="d4906-207">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="d4906-208">Включите дополнительный компонент WSL (если он еще не включен).</span><span class="sxs-lookup"><span data-stu-id="d4906-208">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="d4906-209">Выполните перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="d4906-209">Reboot</span></span>
4. <span data-ttu-id="d4906-210">Выполните команду lxrun /uninstall /full</span><span class="sxs-lookup"><span data-stu-id="d4906-210">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="d4906-211">Установите Bash.</span><span class="sxs-lookup"><span data-stu-id="d4906-211">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="d4906-212">Нет доступа к Интернету в WSL</span><span class="sxs-lookup"><span data-stu-id="d4906-212">No internet access in WSL</span></span>

<span data-ttu-id="d4906-213">Некоторые пользователи сообщили о проблемах с определенными приложениями брандмауэра, блокирующими доступ к Интернету в WSL.</span><span class="sxs-lookup"><span data-stu-id="d4906-213">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="d4906-214">Сообщили о следующих брандмауэрах:</span><span class="sxs-lookup"><span data-stu-id="d4906-214">The firewalls reported are:</span></span>

1. <span data-ttu-id="d4906-215">Kaspersky;</span><span class="sxs-lookup"><span data-stu-id="d4906-215">Kaspersky</span></span>
2. <span data-ttu-id="d4906-216">AVG;</span><span class="sxs-lookup"><span data-stu-id="d4906-216">AVG</span></span>
3. <span data-ttu-id="d4906-217">Avast.</span><span class="sxs-lookup"><span data-stu-id="d4906-217">Avast</span></span>

<span data-ttu-id="d4906-218">В некоторых случаях отключение брандмауэра обеспечивает доступ.</span><span class="sxs-lookup"><span data-stu-id="d4906-218">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="d4906-219">В некоторых случаях доступ блокируется просто при наличии установленного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d4906-219">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="d4906-220">Ошибка "Отказ в разрешении" при проверке связи</span><span class="sxs-lookup"><span data-stu-id="d4906-220">Permission Denied error when using ping</span></span>

<span data-ttu-id="d4906-221">В выпуске [Windows Anniversary Update, версия 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update) для проверки связи в WSL требуются **права администратора**.</span><span class="sxs-lookup"><span data-stu-id="d4906-221">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="d4906-222">Чтобы выполнить проверку связи, запустите Bash для Ubuntu в Windows от имени администратора или запустите bash.exe из командной строки или сеанса PowerShell с привилегиями администратора.</span><span class="sxs-lookup"><span data-stu-id="d4906-222">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="d4906-223">В более поздних версиях Windows ([сборка 14926+](./release-notes.md#build-14926)) права администратора не требуются.</span><span class="sxs-lookup"><span data-stu-id="d4906-223">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="d4906-224">Bash перестал отвечать на запросы</span><span class="sxs-lookup"><span data-stu-id="d4906-224">Bash is hung</span></span>

<span data-ttu-id="d4906-225">Если при работе с Bash вы обнаружите, что Bash перестал отвечать на запросы (или взаимозаблокирован), помогите нам диагностировать проблему путем сбора и передачи дампа памяти.</span><span class="sxs-lookup"><span data-stu-id="d4906-225">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="d4906-226">Обратите внимание на то, что выполнение этих действий приведет к сбою системы.</span><span class="sxs-lookup"><span data-stu-id="d4906-226">Note that these steps will crash your system.</span></span> <span data-ttu-id="d4906-227">Не делайте этого, если вас это не устраивает, либо предварительно сохраните результаты своей работы.</span><span class="sxs-lookup"><span data-stu-id="d4906-227">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="d4906-228">Сбор дампа памяти</span><span class="sxs-lookup"><span data-stu-id="d4906-228">To collect a memory dump</span></span>

1. <span data-ttu-id="d4906-229">Измените тип дампа памяти на "Полный дамп памяти".</span><span class="sxs-lookup"><span data-stu-id="d4906-229">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="d4906-230">При изменении типа дампа запишите текущий тип.</span><span class="sxs-lookup"><span data-stu-id="d4906-230">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="d4906-231">Выполните [эти действия](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809), чтобы настроить аварийное завершение с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="d4906-231">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="d4906-232">Воспроизведите взаимоблокировку или прекращение ответа на запросы.</span><span class="sxs-lookup"><span data-stu-id="d4906-232">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="d4906-233">Выполните аварийное завершение системы с помощью последовательности клавиш из пункта 2.</span><span class="sxs-lookup"><span data-stu-id="d4906-233">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="d4906-234">Произойдет аварийное завершение системы и будет собран дамп памяти.</span><span class="sxs-lookup"><span data-stu-id="d4906-234">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="d4906-235">После перезагрузки системы отправьте memory.dmp на адрес электронной почты secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d4906-235">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="d4906-236">По умолчанию файл дампа находится в папке %SystemRoot%\memory.dmp или C:\Windows\memory.dmp, если C: является системным диском.</span><span class="sxs-lookup"><span data-stu-id="d4906-236">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="d4906-237">В письме укажите, что дамп предназначен для команды разработчиков WSL или Bash в Windows.</span><span class="sxs-lookup"><span data-stu-id="d4906-237">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="d4906-238">Восстановите исходное значение типа дампа памяти.</span><span class="sxs-lookup"><span data-stu-id="d4906-238">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="d4906-239">Проверка номера сборки</span><span class="sxs-lookup"><span data-stu-id="d4906-239">Check your build number</span></span>

<span data-ttu-id="d4906-240">Чтобы узнать архитектуру компьютера и номер сборки Windows, выберите</span><span class="sxs-lookup"><span data-stu-id="d4906-240">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="d4906-241">**Параметры** > **Система** > **О программе**</span><span class="sxs-lookup"><span data-stu-id="d4906-241">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="d4906-242">Найдите поля **Сборка ОС** и **Тип системы**.</span><span class="sxs-lookup"><span data-stu-id="d4906-242">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="d4906-243">![Снимок экрана с полями "Сборка ОС" и "Тип системы"](media/system.png)</span><span class="sxs-lookup"><span data-stu-id="d4906-243">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="d4906-244">Чтобы найти номер сборки Windows Server, выполните в PowerShell следующую команду.</span><span class="sxs-lookup"><span data-stu-id="d4906-244">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="d4906-245">Подтверждение включения WSL</span><span class="sxs-lookup"><span data-stu-id="d4906-245">Confirm WSL is enabled</span></span>

<span data-ttu-id="d4906-246">Вы можете убедиться, что подсистема Windows для Linux включена, выполнив в PowerShell следующую команду.</span><span class="sxs-lookup"><span data-stu-id="d4906-246">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="d4906-247">Проблемы с подключением к серверу OpenSSH</span><span class="sxs-lookup"><span data-stu-id="d4906-247">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="d4906-248">Попытка подключения к серверу SSH завершается следующей ошибкой: "Connection closed by 127.0.0.1 port 22" (Подключение закрыто узлом 127.0.0.1 через порт 22).</span><span class="sxs-lookup"><span data-stu-id="d4906-248">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="d4906-249">Убедитесь, что сервер OpenSSH работает</span><span class="sxs-lookup"><span data-stu-id="d4906-249">Make sure your OpenSSH Server is running:</span></span>

   ```bash
   sudo service ssh status
   ```

   <span data-ttu-id="d4906-250">и вы следовали указаниям в этом руководстве: https://ubuntu.com/server/docs/service-openssh.</span><span class="sxs-lookup"><span data-stu-id="d4906-250">and you've followed this tutorial: https://ubuntu.com/server/docs/service-openssh</span></span>

2. <span data-ttu-id="d4906-251">Завершите работу службы sshd и запустите sshd в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="d4906-251">Stop the sshd service and start sshd in debug mode:</span></span>

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="d4906-252">Проверьте журналы запуска и убедитесь, что ключи сервера доступны и в журнале нет сообщений, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d4906-252">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

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

<span data-ttu-id="d4906-253">Если вы видите такие сообщения и в разделе `/etc/ssh/` отсутствуют ключи, потребуется повторно создать ключи или просто очистить и установить сервер OpenSSH.</span><span class="sxs-lookup"><span data-stu-id="d4906-253">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="d4906-254">"Указанная сборка не найдена".</span><span class="sxs-lookup"><span data-stu-id="d4906-254">"The referenced assembly could not be found."</span></span> <span data-ttu-id="d4906-255">Это сообщение может появиться при включении дополнительного компонента WSL.</span><span class="sxs-lookup"><span data-stu-id="d4906-255">when enabling the WSL optional feature</span></span>

<span data-ttu-id="d4906-256">Данная ошибка связана с неправильным состоянием установки.</span><span class="sxs-lookup"><span data-stu-id="d4906-256">This error is related to being in a bad install state.</span></span> <span data-ttu-id="d4906-257">Чтобы устранить эту проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d4906-257">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="d4906-258">Если вы используете команду включения компонента WSL в PowerShell, попробуйте использовать графический пользовательский интерфейс. Для этого откройте меню "Пуск", выполните поиск фразы "Включение или отключение компонентов Windows", а затем из списка выберите "Подсистема Windows для Linux". Этот дополнительный компонент будет установлен.</span><span class="sxs-lookup"><span data-stu-id="d4906-258">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="d4906-259">Обновите версию Windows, выбрав "Параметры" > "Обновления" и щелкнув "Проверить наличие обновлений".</span><span class="sxs-lookup"><span data-stu-id="d4906-259">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="d4906-260">Если оба способа не помогли и вам нужно использовать WSL, рассмотрите возможность обновления на месте, переустановив Windows 10 с установочного носителя и выбрав параметр "Сохранить все", чтобы сохранить свои приложения и файлы.</span><span class="sxs-lookup"><span data-stu-id="d4906-260">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="d4906-261">Инструкции по такой установке можно найти на странице [Переустановка Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="d4906-261">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>

### <a name="correct-ssh-related-permission-errors"></a><span data-ttu-id="d4906-262">Правильные (связанные с SSH) ошибки разрешений</span><span class="sxs-lookup"><span data-stu-id="d4906-262">Correct (SSH related) permission errors</span></span>

<span data-ttu-id="d4906-263">Если вы видите эту ошибку:</span><span class="sxs-lookup"><span data-stu-id="d4906-263">If you're seeing this error:</span></span>

```bash
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

<span data-ttu-id="d4906-264">Чтобы устранить эту проблему, добавьте следующий текст в файл ```/etc/wsl.conf```:</span><span class="sxs-lookup"><span data-stu-id="d4906-264">To fix this, append the following to the the ```/etc/wsl.conf``` file:</span></span>

```bash
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

<span data-ttu-id="d4906-265">Обратите внимание, что добавление этой команды будет включать метаданные и изменять разрешения для файлов Windows, показанных в WSL.</span><span class="sxs-lookup"><span data-stu-id="d4906-265">Please note that adding this command will include metadata and modify the file permissions on the Windows files seen from WSL.</span></span> <span data-ttu-id="d4906-266">См. сведения о [разрешениях файловой системы](./file-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d4906-266">Please see the [File System Permissions](./file-permissions.md) for more information.</span></span>

### <a name="running-windows-commands-fails-inside-a-distribution"></a><span data-ttu-id="d4906-267">Выполнение команд Windows завершается сбоем в дистрибутиве</span><span class="sxs-lookup"><span data-stu-id="d4906-267">Running Windows commands fails inside a distribution</span></span>

<span data-ttu-id="d4906-268">Некоторые дистрибутивы, [доступные в Microsoft Store](install-win10.md#step-6---install-your-linux-distribution-of-choice), еще не полностью поддерживают возможность выполнения команд Windows в [Терминале](https://en.wikipedia.org/wiki/Linux_console).</span><span class="sxs-lookup"><span data-stu-id="d4906-268">Some distributions [available in Microsoft Store](install-win10.md#step-6---install-your-linux-distribution-of-choice) are yet not fully compatible to run Windows commands in [Terminal](https://en.wikipedia.org/wiki/Linux_console) out of the box.</span></span> <span data-ttu-id="d4906-269">Если при выполнении `powershell.exe /c start .` или любой другой команды Windows возникает ошибка `-bash: powershell.exe: command not found`, ее можно устранить, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d4906-269">If you get an error `-bash: powershell.exe: command not found` running `powershell.exe /c start .` or any other Windows command, you can resolve it following these steps:</span></span>

1. <span data-ttu-id="d4906-270">В дистрибутиве WSL выполните `echo $PATH`.</span><span class="sxs-lookup"><span data-stu-id="d4906-270">In your WSL distribution run `echo $PATH`.</span></span>  
   <span data-ttu-id="d4906-271">Если `/mnt/c/Windows/system32` отсутствует, что-то переопределяет стандартную переменную PATH.</span><span class="sxs-lookup"><span data-stu-id="d4906-271">If it does not include: `/mnt/c/Windows/system32` something is redefining the standard PATH variable.</span></span>
2. <span data-ttu-id="d4906-272">Проверьте параметры профиля с помощью `cat /etc/profile`.</span><span class="sxs-lookup"><span data-stu-id="d4906-272">Check profile settings with `cat /etc/profile`.</span></span>  
   <span data-ttu-id="d4906-273">Если присутствует назначение переменной PATH, измените файл, чтобы закомментировать блок назначения PATH, используя символ **#** .</span><span class="sxs-lookup"><span data-stu-id="d4906-273">If it contains assignment of the PATH variable, edit the file to comment out PATH assignment block with a **#** character.</span></span>
3. <span data-ttu-id="d4906-274">Проверьте, существует ли файл wsl.conf (`cat /etc/wsl.conf`), и убедитесь, что он не содержит `appendWindowsPath=false`. В противном случае закомментируйте эту строку.</span><span class="sxs-lookup"><span data-stu-id="d4906-274">Check if wsl.conf is present `cat /etc/wsl.conf` and make sure it does not contain `appendWindowsPath=false`, otherwise comment it out.</span></span>
4. <span data-ttu-id="d4906-275">Перезапустите дистрибутив, введя `wsl -t `, после чего следует имя дистрибутива, либо выполните `wsl --shutdown` в cmd или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d4906-275">Restart distribution by typing `wsl -t ` followed by distribution name or run `wsl --shutdown` either in cmd or PowerShell.</span></span>

### <a name="unable-to-boot-after-installing-wsl-2"></a><span data-ttu-id="d4906-276">Не удается выполнить загрузку после установки WSL 2</span><span class="sxs-lookup"><span data-stu-id="d4906-276">Unable to boot after installing WSL 2</span></span>

<span data-ttu-id="d4906-277">Мы осведомлены о проблемах, из-за которых пользователям не удается выполнить загрузку после установки WSL 2.</span><span class="sxs-lookup"><span data-stu-id="d4906-277">We are aware of an issue affecting users where they are unable to boot after installing WSL 2.</span></span> <span data-ttu-id="d4906-278">Пока мы полностью диагностировали эту проблему, от пользователей поступали сообщения о том, что помочь в ее устранении может [изменение размера буфера](https://github.com/microsoft/WSL/issues/4784#issuecomment-639219363) или [установка правильных драйверов](https://github.com/microsoft/WSL/issues/4784#issuecomment-675702244).</span><span class="sxs-lookup"><span data-stu-id="d4906-278">While we fully diagnose those issue, users have reported that [changing the buffer size](https://github.com/microsoft/WSL/issues/4784#issuecomment-639219363) or [installing the right drivers](https://github.com/microsoft/WSL/issues/4784#issuecomment-675702244) can help address this.</span></span> <span data-ttu-id="d4906-279">Просматривайте новейшие сведения об этой [проблеме на сайте GitHub](https://github.com/microsoft/WSL/issues/4784).</span><span class="sxs-lookup"><span data-stu-id="d4906-279">Please view this [Github issue](https://github.com/microsoft/WSL/issues/4784) to see the latest updates on this issue.</span></span> 
