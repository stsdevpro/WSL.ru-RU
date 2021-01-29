---
title: Заметки о выпуске подсистемы Windows для Linux
description: См. заметки о выпуске подсистемы Windows для Linux. Эти заметки о выпуске содержат исправленные проблемы и обновляются еженедельно.
keywords: заметки о выпуске, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ab6f26a4f9393c78cfa98367016efcf94afb1084
ms.sourcegitcommit: c0478193f16efd4f8221016301ef7a1fd67713e0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98671973"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="60e12-105">Заметки о выпуске подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="60e12-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-21286"></a><span data-ttu-id="60e12-106">Сборка 21286</span><span class="sxs-lookup"><span data-stu-id="60e12-106">Build 21286</span></span>
<span data-ttu-id="60e12-107">Общие сведения о сборке Windows 21286 доступны в [блоге о Windows](https://blogs.windows.com/windows-insider/2021/01/06/announcing-windows-10-insider-preview-build-21286/).</span><span class="sxs-lookup"><span data-stu-id="60e12-107">For general Windows information on build 21286 visit the [Windows blog](https://blogs.windows.com/windows-insider/2021/01/06/announcing-windows-10-insider-preview-build-21286/).</span></span>

* <span data-ttu-id="60e12-108">Введена команда wsl.exe --cd для указания текущего рабочего каталога команды.</span><span class="sxs-lookup"><span data-stu-id="60e12-108">Introduce wsl.exe --cd command to set current working directory of a command.</span></span>
* <span data-ttu-id="60e12-109">Улучшено сопоставление кодов ошибок NTSTATUS и Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-109">Improve mapping of NTSTATUS to Linux error codes.</span></span> <span data-ttu-id="60e12-110">[GH 6063]</span><span class="sxs-lookup"><span data-stu-id="60e12-110">[GH 6063]</span></span>
* <span data-ttu-id="60e12-111">Улучшены отчеты об ошибках при выполнении команды wsl.exe --mount.</span><span class="sxs-lookup"><span data-stu-id="60e12-111">Improve wsl.exe --mount error reporting.</span></span>
* <span data-ttu-id="60e12-112">В etc/wsl.conf добавлен параметр для включения команд запуска:</span><span class="sxs-lookup"><span data-stu-id="60e12-112">Added an option to /etc/wsl.conf to enable start up commands:</span></span>
```
[boot]
command=<string>
```

## <a name="build-20226"></a><span data-ttu-id="60e12-113">Сборка 20226.</span><span class="sxs-lookup"><span data-stu-id="60e12-113">Build 20226</span></span>
<span data-ttu-id="60e12-114">Общие сведения о сборке Windows 20226 доступны в [блоге о Windows](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20226/).</span><span class="sxs-lookup"><span data-stu-id="60e12-114">For general Windows information on build 20226 visit the [Windows blog](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20226/).</span></span>

* <span data-ttu-id="60e12-115">Устранен сбой в службе LxssManager.</span><span class="sxs-lookup"><span data-stu-id="60e12-115">Fix crash in LxssManager service.</span></span> <span data-ttu-id="60e12-116">[GH 5902]</span><span class="sxs-lookup"><span data-stu-id="60e12-116">[GH 5902]</span></span>

## <a name="build-20211"></a><span data-ttu-id="60e12-117">Сборка 20211</span><span class="sxs-lookup"><span data-stu-id="60e12-117">Build 20211</span></span>
<span data-ttu-id="60e12-118">Общие сведения о сборке Windows 20211 доступны в [блоге о Windows](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20211/).</span><span class="sxs-lookup"><span data-stu-id="60e12-118">For general Windows information on build 20211 visit the [Windows blog](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20211/).</span></span>

* <span data-ttu-id="60e12-119">Представлена новая команда `wsl.exe --mount` для подключения физических или виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="60e12-119">Introduce `wsl.exe --mount` for mounting physical or virtual disks.</span></span> <span data-ttu-id="60e12-120">Дополнительные сведения см. в статье [Доступ к файловым системам Linux в Windows и WSL 2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/).</span><span class="sxs-lookup"><span data-stu-id="60e12-120">For more information see [Access Linux filesystems in Windows and WSL 2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/).</span></span>
* <span data-ttu-id="60e12-121">Устранен сбой в службе LxssManager при проверке активности виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="60e12-121">Fix crash in LxssManager service when checking if the VM is idle.</span></span> <span data-ttu-id="60e12-122">[GH 5768]</span><span class="sxs-lookup"><span data-stu-id="60e12-122">[GH 5768]</span></span>
* <span data-ttu-id="60e12-123">Включена поддержка сжатых VHD-файлов.</span><span class="sxs-lookup"><span data-stu-id="60e12-123">Support for compressed VHD files.</span></span> <span data-ttu-id="60e12-124">[GH 4103]</span><span class="sxs-lookup"><span data-stu-id="60e12-124">[GH 4103]</span></span>
* <span data-ttu-id="60e12-125">Убедитесь, что библиотеки пользовательского режима Linux, установленные в c:\windows\system32\lxss\lib, сохраняются при обновлении ОС.</span><span class="sxs-lookup"><span data-stu-id="60e12-125">Ensure that Linux user mode libs installed to c:\windows\system32\lxss\lib are preserved across OS upgrade.</span></span> <span data-ttu-id="60e12-126">[GH 5848]</span><span class="sxs-lookup"><span data-stu-id="60e12-126">[GH 5848]</span></span>
* <span data-ttu-id="60e12-127">Включена возможность получить список дистрибутивов, доступных для установки, с помощью команды `wsl --install --list-distributions`.</span><span class="sxs-lookup"><span data-stu-id="60e12-127">Added the ability to list available distributions that can be installed with `wsl --install --list-distributions`.</span></span>
* <span data-ttu-id="60e12-128">Теперь, когда пользователь выходит из системы, работа экземпляров WSL завершается.</span><span class="sxs-lookup"><span data-stu-id="60e12-128">WSL instances are now terminated when the user logs off.</span></span>

## <a name="build-20190"></a><span data-ttu-id="60e12-129">Сборка 20190</span><span class="sxs-lookup"><span data-stu-id="60e12-129">Build 20190</span></span>
<span data-ttu-id="60e12-130">Общие сведения о сборке Windows 20190 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/08/12/announcing-windows-10-insider-preview-build-20190/).</span><span class="sxs-lookup"><span data-stu-id="60e12-130">For general Windows information on build 20190 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/08/12/announcing-windows-10-insider-preview-build-20190/).</span></span>

* <span data-ttu-id="60e12-131">Исправлена ошибка, препятствующая запуску экземпляров WSL 1.</span><span class="sxs-lookup"><span data-stu-id="60e12-131">Fix bug preventing WSL1 instances from launching.</span></span> <span data-ttu-id="60e12-132">[GH 5633]</span><span class="sxs-lookup"><span data-stu-id="60e12-132">[GH 5633]</span></span>
* <span data-ttu-id="60e12-133">Исправлена ошибка, приводившая к зависанию при перенаправлении выходных данных процесса Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-133">Fix hang when redirecting Windows process output.</span></span> <span data-ttu-id="60e12-134">[GH 5648]</span><span class="sxs-lookup"><span data-stu-id="60e12-134">[GH 5648]</span></span>
* <span data-ttu-id="60e12-135">Добавлен параметр %userprofile%\\.wslconfig для управления временем ожидания при простое виртуальной машины (wsl2.vmIdleTimeout=<время_в_миллисекундах>).</span><span class="sxs-lookup"><span data-stu-id="60e12-135">Add %userprofile%\\.wslconfig option to control the VM idle timeout (wsl2.vmIdleTimeout=<time_in_ms>).</span></span>
* <span data-ttu-id="60e12-136">Включена поддержка запуска псевдонимов выполнения приложений из WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-136">Support launching app execution aliases from WSL.</span></span>
* <span data-ttu-id="60e12-137">Включена поддержка установки ядра WSL2 и дистрибутивов с помощью команды wsl.exe --install.</span><span class="sxs-lookup"><span data-stu-id="60e12-137">Added support for installing the WSL2 kernel and distributions to wsl.exe --install.</span></span>

## <a name="build-20175"></a><span data-ttu-id="60e12-138">Сборка 20175</span><span class="sxs-lookup"><span data-stu-id="60e12-138">Build 20175</span></span>
<span data-ttu-id="60e12-139">Общие сведения о сборке Windows 20175 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/07/22/announcing-windows-10-insider-preview-build-20175/).</span><span class="sxs-lookup"><span data-stu-id="60e12-139">For general Windows information on build 20175 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/07/22/announcing-windows-10-insider-preview-build-20175/).</span></span>

* <span data-ttu-id="60e12-140">В качестве выделяемого по умолчанию объема памяти виртуальной машины WSL2 теперь используется 50 % от памяти узла или 8 ГБ в зависимости от того, что меньше [GH 4166].</span><span class="sxs-lookup"><span data-stu-id="60e12-140">Adjust default memory assignment of WSL2 VM to be 50% of host memory or 8GB, whichever is less [GH 4166].</span></span>
* <span data-ttu-id="60e12-141">Префикс \\\\wsl$ изменен на \\\\wsl для поддержки синтаксического анализа URI.</span><span class="sxs-lookup"><span data-stu-id="60e12-141">Change \\\\wsl$ prefix to \\\\wsl to support URI parsing.</span></span> <span data-ttu-id="60e12-142">Старый путь \\\\wsl$ по-прежнему поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60e12-142">The old \\\\wsl$ path is still supported.</span></span>
* <span data-ttu-id="60e12-143">В архитектуре AMD64 вложенная виртуализация для WSL2 включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60e12-143">Enable nested virtualization for WSL2 by default on amd64.</span></span> <span data-ttu-id="60e12-144">Вы можете отключить ее с помощью команды %userprofile%\\.wslconfig ([wsl2] nestedVirtualization=false).</span><span class="sxs-lookup"><span data-stu-id="60e12-144">You can disable this via %userprofile%\\.wslconfig ([wsl2] nestedVirtualization=false).</span></span>
* <span data-ttu-id="60e12-145">По запросу wsl.exe --update запускается Центр обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="60e12-145">Make wsl.exe --update demand start Microsoft Update.</span></span>
* <span data-ttu-id="60e12-146">В DrvFs поддерживается переименование файлов, доступных только для чтения.</span><span class="sxs-lookup"><span data-stu-id="60e12-146">Support renaming over a read-only file in DrvFs.</span></span>
* <span data-ttu-id="60e12-147">Сообщения об ошибках всегда выводятся на правильной странице кода.</span><span class="sxs-lookup"><span data-stu-id="60e12-147">Ensure error messages are always printed in the correct codepage.</span></span>

## <a name="build-20150"></a><span data-ttu-id="60e12-148">Сборка 20150</span><span class="sxs-lookup"><span data-stu-id="60e12-148">Build 20150</span></span>
<span data-ttu-id="60e12-149">Общие сведения о сборке Windows 20150 см. в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span><span class="sxs-lookup"><span data-stu-id="60e12-149">For general Windows information on build 20150 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span></span>

* <span data-ttu-id="60e12-150">Сведения о вычислениях GPU WSL2 см. в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span><span class="sxs-lookup"><span data-stu-id="60e12-150">WSL2 GPU compute see [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/) for more information.</span></span>
* <span data-ttu-id="60e12-151">Добавлен параметр wsl.exe --install командной строки для быстрой настройки WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-151">Introduce wsl.exe --install command line option to easily set up WSL.</span></span>
* <span data-ttu-id="60e12-152">Добавлен параметр командной строки wsl.exe --update для управления обновлениями ядра WSL2.</span><span class="sxs-lookup"><span data-stu-id="60e12-152">Introduce wsl.exe --update command line option to manage updates to the WSL2 kernel.</span></span> 
* <span data-ttu-id="60e12-153">Используйте WSL2 в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60e12-153">Set WSL2 as the default.</span></span>
* <span data-ttu-id="60e12-154">Увеличено время ожидания корректного завершения работы виртуальной машины WSL2.</span><span class="sxs-lookup"><span data-stu-id="60e12-154">Increase WSL2 vm graceful shutdown timeout.</span></span>
* <span data-ttu-id="60e12-155">Исправлено состояние гонки virtio-9p при сопоставлении памяти устройства.</span><span class="sxs-lookup"><span data-stu-id="60e12-155">Fix virtio-9p race condition when mapping device memory.</span></span>
* <span data-ttu-id="60e12-156">Не запускайте сервер 9p с повышенными привилегиями, если контроль учетных записей отключен.</span><span class="sxs-lookup"><span data-stu-id="60e12-156">Don't run an elevated 9p server if UAC is disabled.</span></span>

## <a name="build-19640"></a><span data-ttu-id="60e12-157">Сборка 19640</span><span class="sxs-lookup"><span data-stu-id="60e12-157">Build 19640</span></span>
<span data-ttu-id="60e12-158">Общие сведения о сборке Windows 19640 см. в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span><span class="sxs-lookup"><span data-stu-id="60e12-158">For general Windows information on build 19640 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span></span>

* <span data-ttu-id="60e12-159">[WSL2] Улучшения стабильности для virtio-9p (drvfs).</span><span class="sxs-lookup"><span data-stu-id="60e12-159">[WSL2] Stability improvements for virtio-9p (drvfs).</span></span>

## <a name="build-19555"></a><span data-ttu-id="60e12-160">Сборка 19555</span><span class="sxs-lookup"><span data-stu-id="60e12-160">Build 19555</span></span>
<span data-ttu-id="60e12-161">Общие сведения о сборке Windows 19555 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span><span class="sxs-lookup"><span data-stu-id="60e12-161">For general Windows information on build 19555 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span></span>

* <span data-ttu-id="60e12-162">[WSL2] Применение memory cgroup для ограничения объема памяти, используемой операциями установки и преобразования [GH 4669].</span><span class="sxs-lookup"><span data-stu-id="60e12-162">[WSL2] Use a memory cgroup to limit the amount of memory used by install and conversion operations [GH 4669]</span></span>
* <span data-ttu-id="60e12-163">Предоставление команды wsl.exe для улучшения обнаружения компонентов, если дополнительный компонент подсистемы Windows для Linux не включен.</span><span class="sxs-lookup"><span data-stu-id="60e12-163">Make wsl.exe present when the Windows Subsystem for Linux optional component is not enabled to improve feature discoverability.</span></span>
* <span data-ttu-id="60e12-164">Изменение wsl.exe для вывода текста справки, если дополнительный компонент WSL не установлен.</span><span class="sxs-lookup"><span data-stu-id="60e12-164">Change wsl.exe to print help text if the WSL optional component is not installed</span></span>
* <span data-ttu-id="60e12-165">Устранение состояния гонки при создании экземпляров.</span><span class="sxs-lookup"><span data-stu-id="60e12-165">Fix race condition when creating instances</span></span>
* <span data-ttu-id="60e12-166">Создание файла wslclient.dll, который содержит все функции командной строки.</span><span class="sxs-lookup"><span data-stu-id="60e12-166">Create wslclient.dll that contains all command line functionality</span></span>
* <span data-ttu-id="60e12-167">Предотвращение аварийного завершения при остановке службы LxssManagerUser.</span><span class="sxs-lookup"><span data-stu-id="60e12-167">Prevent crash during LxssManagerUser service stop</span></span>
* <span data-ttu-id="60e12-168">Исправление завершения работы wslapi.dll при первой ошибке, если значение параметра distroName равно NULL.</span><span class="sxs-lookup"><span data-stu-id="60e12-168">Fix wslapi.dll fast fail when distroName parameter is NULL</span></span>

## <a name="build-19041"></a><span data-ttu-id="60e12-169">Сборка 19041</span><span class="sxs-lookup"><span data-stu-id="60e12-169">Build 19041</span></span>
<span data-ttu-id="60e12-170">Общие сведения о сборке Windows 19041 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span><span class="sxs-lookup"><span data-stu-id="60e12-170">For general Windows information on build 19041 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span></span>

* <span data-ttu-id="60e12-171">[WSL2] Очищение маски сигналов перед запуском процессов.</span><span class="sxs-lookup"><span data-stu-id="60e12-171">[WSL2] Clear the signal mask before launching the processes</span></span>
* <span data-ttu-id="60e12-172">[WSL2] Обновление ядра Linux до версии 4.19.84.</span><span class="sxs-lookup"><span data-stu-id="60e12-172">[WSL2] Update Linux kernel to 4.19.84</span></span>
* <span data-ttu-id="60e12-173">Обработка созданной символической ссылки /etc/resolv.conf, если символическая ссылка не является относительной.</span><span class="sxs-lookup"><span data-stu-id="60e12-173">Handle creation of /etc/resolv.conf symlink when the symlink is non-relative</span></span>

## <a name="build-19028"></a><span data-ttu-id="60e12-174">Сборка 19028</span><span class="sxs-lookup"><span data-stu-id="60e12-174">Build 19028</span></span>
<span data-ttu-id="60e12-175">Общие сведения о сборке Windows 19028 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span><span class="sxs-lookup"><span data-stu-id="60e12-175">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="60e12-176">[WSL2] Ядро Linux обновлено до версии 4.19.81</span><span class="sxs-lookup"><span data-stu-id="60e12-176">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="60e12-177">[WSL2] Разрешение по умолчанию /dev/net/tun изменено на 0666 [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="60e12-177">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="60e12-178">[WSL2] Объем памяти, назначенный виртуальной машине Linux по умолчанию, оптимизирован до 80 % памяти узла</span><span class="sxs-lookup"><span data-stu-id="60e12-178">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="60e12-179">[WSL2] Внесены исправления в работу сервера взаимодействия для обработки запросов со временем ожидания, чтобы сервер не перестал отвечать на запросы из-за неправильных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-179">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="60e12-180">Сборка 19018</span><span class="sxs-lookup"><span data-stu-id="60e12-180">Build 19018</span></span>
<span data-ttu-id="60e12-181">Общие сведения о сборке Windows 19018 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span><span class="sxs-lookup"><span data-stu-id="60e12-181">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="60e12-182">[WSL2] Для исправления неполадок с приложениями .NET по умолчанию используется параметр cache=mmap для подключения ресурсов 9p.</span><span class="sxs-lookup"><span data-stu-id="60e12-182">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="60e12-183">[WSL2] Исправления для ретранслятора localhost [GH 4340].</span><span class="sxs-lookup"><span data-stu-id="60e12-183">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="60e12-184">[WSL2] Добавлен подключаемый общедоступный ресурс tmpfs для передачи состояний между дистрибутивами.</span><span class="sxs-lookup"><span data-stu-id="60e12-184">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="60e12-185">Исправлено восстановление постоянного сетевого диска для \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="60e12-185">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="60e12-186">Сборка 19013</span><span class="sxs-lookup"><span data-stu-id="60e12-186">Build 19013</span></span>
<span data-ttu-id="60e12-187">Общие сведения о сборке Windows 19013 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span><span class="sxs-lookup"><span data-stu-id="60e12-187">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="60e12-188">[WSL2] Повышение производительности памяти служебной виртуальной машины WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-188">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="60e12-189">Память, которая больше не используется, будет освобождена для узла.</span><span class="sxs-lookup"><span data-stu-id="60e12-189">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="60e12-190">[WSL2] Ядро обновлено до версии 4.19.79.</span><span class="sxs-lookup"><span data-stu-id="60e12-190">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="60e12-191">(Добавлены модули CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK и CONFIG_BRIDGE_VLAN_FILTERING.)</span><span class="sxs-lookup"><span data-stu-id="60e12-191">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="60e12-192">[WSL2] Исправлен ретранслятор ввода для обработки ситуаций, когда STDIN является незакрытым обработчиком канала [GH 4424].</span><span class="sxs-lookup"><span data-stu-id="60e12-192">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="60e12-193">При проверке наличия \\\\wsl$ не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="60e12-193">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="60e12-194">Сборка 19002</span><span class="sxs-lookup"><span data-stu-id="60e12-194">Build 19002</span></span>
<span data-ttu-id="60e12-195">Общие сведения о сборке Windows 19002 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="60e12-195">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="60e12-196">[WSL] Устранена проблема с обработкой некоторых знаков Юникода: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="60e12-196">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="60e12-197">[WSL] Исправлена редко возникавшая проблема, приводившая к отмене регистрации дистрибутива, если он запускался сразу после обновления сборки новой сборкой.</span><span class="sxs-lookup"><span data-stu-id="60e12-197">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="60e12-198">[WSL] Устранена незначительная проблема с wsl.exe --shutdown, из-за которой таймеры бездействия экземпляра не отменялись.</span><span class="sxs-lookup"><span data-stu-id="60e12-198">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="60e12-199">Сборка 18995</span><span class="sxs-lookup"><span data-stu-id="60e12-199">Build 18995</span></span>
<span data-ttu-id="60e12-200">Общие сведения о сборке Windows 18995 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="60e12-200">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="60e12-201">[WSL2] Устранена проблема, из-за которой подключения DrvFs прекращали работать после прерывания операции (например, нажатия клавиш CTRL+C) [GH 4377].</span><span class="sxs-lookup"><span data-stu-id="60e12-201">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="60e12-202">[WSL2] Исправлена обработка очень больших сообщений hvsocket [GH 4105].</span><span class="sxs-lookup"><span data-stu-id="60e12-202">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="60e12-203">[WSL2] Устранена проблема с взаимодействием, возникавшая, если в качестве stdin использовался файл [GH 4475].</span><span class="sxs-lookup"><span data-stu-id="60e12-203">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="60e12-204">[WSL2] Устранено аварийное завершение службы при обнаружении непредвиденного состояния сети [GH 4474].</span><span class="sxs-lookup"><span data-stu-id="60e12-204">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="60e12-205">[WSL2] Запрос имени дистрибутива с сервера взаимодействия, если текущий процесс не имеет переменной среды.</span><span class="sxs-lookup"><span data-stu-id="60e12-205">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="60e12-206">[WSL2] Устранена проблема с взаимодействием, возникавшая, если в качестве stdin использовался файл.</span><span class="sxs-lookup"><span data-stu-id="60e12-206">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="60e12-207">[WSL2] Ядро Linux обновлено до версии 4.19.72.</span><span class="sxs-lookup"><span data-stu-id="60e12-207">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="60e12-208">[WSL2] Добавлена возможность указать дополнительные параметры командной строки ядра с помощью wslconfig.</span><span class="sxs-lookup"><span data-stu-id="60e12-208">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="60e12-209">Сборка 18990</span><span class="sxs-lookup"><span data-stu-id="60e12-209">Build 18990</span></span>
<span data-ttu-id="60e12-210">Общие сведения о сборке Windows 18990 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="60e12-210">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="60e12-211">Ускорен вывод списка каталогов в \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="60e12-211">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="60e12-212">[WSL2] Внедрена дополнительная энтропия загрузки [GH 4416].</span><span class="sxs-lookup"><span data-stu-id="60e12-212">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="60e12-213">[WSL2] Исправлено взаимодействие с Windows при использовании su или sudo [GH 4465].</span><span class="sxs-lookup"><span data-stu-id="60e12-213">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="60e12-214">Сборка 18980</span><span class="sxs-lookup"><span data-stu-id="60e12-214">Build 18980</span></span>
<span data-ttu-id="60e12-215">Общие сведения о сборке Windows 18980 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="60e12-215">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="60e12-216">Исправлено чтение символических ссылок, которые запрещают FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="60e12-216">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="60e12-217">Сюда входят все символические ссылки Windows, создаваемые для обеспечения обратной совместимости, такие как "C:\Document and Settings", а также множество символических ссылок в каталоге профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="60e12-217">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="60e12-218">Непредвиденное состояние файловой системы перестало быть неустранимым [GH 4334, 4305].</span><span class="sxs-lookup"><span data-stu-id="60e12-218">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="60e12-219">[WSL2] Добавлена поддержка arm64, если ЦП или встроенное ПО поддерживает виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="60e12-219">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="60e12-220">[WSL2] Непривилегированным пользователям разрешено просматривать журнал ядра.</span><span class="sxs-lookup"><span data-stu-id="60e12-220">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="60e12-221">[WSL2] Исправлена ретрансляция вывода при закрытии сокетов stdout и stderr [GH 4375].</span><span class="sxs-lookup"><span data-stu-id="60e12-221">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="60e12-222">[WSL2] Поддержка сквозного режима батареи и адаптера питания.</span><span class="sxs-lookup"><span data-stu-id="60e12-222">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="60e12-223">[WSL2] Ядро Linux обновлено до версии 4.19.67.</span><span class="sxs-lookup"><span data-stu-id="60e12-223">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="60e12-224">Добавлена возможность задать имя пользователя по умолчанию в /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="60e12-224">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="60e12-225">Сборка 18975</span><span class="sxs-lookup"><span data-stu-id="60e12-225">Build 18975</span></span>
<span data-ttu-id="60e12-226">Общие сведения о сборке Windows 18975 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="60e12-226">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="60e12-227">[WSL2] Исправлен ряд проблем с надежностью localhost [GH 4340].</span><span class="sxs-lookup"><span data-stu-id="60e12-227">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="60e12-228">Сборка 18970</span><span class="sxs-lookup"><span data-stu-id="60e12-228">Build 18970</span></span>
<span data-ttu-id="60e12-229">Общие сведения о сборке Windows 18970 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="60e12-229">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="60e12-230">[WSL2] Синхронизация времени с временем узла при выходе системы из спящего режима [GH 4245].</span><span class="sxs-lookup"><span data-stu-id="60e12-230">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="60e12-231">[WSL2] Создание символических ссылок NT на тома Windows, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="60e12-231">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="60e12-232">[WSL2] Создание дистрибутивов в пространствах имен UTS, IPC, PID и Mount.</span><span class="sxs-lookup"><span data-stu-id="60e12-232">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="60e12-233">[WSL2] Исправлена ретрансляция портов localhost при привязке сервера к localhost напрямую [GH 4353].</span><span class="sxs-lookup"><span data-stu-id="60e12-233">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="60e12-234">[WSL2] Исправлено взаимодействие при перенаправлении вывода [GH 4337].</span><span class="sxs-lookup"><span data-stu-id="60e12-234">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="60e12-235">[WSL2] Поддержка преобразования абсолютных символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="60e12-235">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="60e12-236">[WSL2] Ядро обновлено до версии 4.19.59.</span><span class="sxs-lookup"><span data-stu-id="60e12-236">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="60e12-237">[WSL2] Правильное задание маски подсети для eth0.</span><span class="sxs-lookup"><span data-stu-id="60e12-237">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="60e12-238">[WSL2] Изменение логики для выхода из циклов консольного рабочего процесса при получении сигнала о событии выхода.</span><span class="sxs-lookup"><span data-stu-id="60e12-238">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="60e12-239">[WSL2] Если дистрибутив не работает, то его VHD-файл можно извлечь.</span><span class="sxs-lookup"><span data-stu-id="60e12-239">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="60e12-240">[WSL2] Исправлена библиотека анализа конфигурации, чтобы правильно обрабатывать пустые значения.</span><span class="sxs-lookup"><span data-stu-id="60e12-240">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="60e12-241">[WSL2] Поддержка рабочего стола Docker путем создания подключений между дистрибутивами.</span><span class="sxs-lookup"><span data-stu-id="60e12-241">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="60e12-242">Дистрибутив можно настроить для такого режима, добавив следующую строку в файл /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="60e12-242">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="60e12-243">Сборка 18945</span><span class="sxs-lookup"><span data-stu-id="60e12-243">Build 18945</span></span>
<span data-ttu-id="60e12-244">Общие сведения о сборке Windows 18945 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="60e12-244">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-245">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-245">WSL</span></span>
* <span data-ttu-id="60e12-246">[WSL2] Разрешен доступ к ожидающим передачи данных TCP-сокетам в WSL2 с узла по адресу localhost:<порт>.</span><span class="sxs-lookup"><span data-stu-id="60e12-246">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="60e12-247">[WSL2] Устранены сбои при установке и преобразовании. Добавлена дополнительная диагностика для отслеживания будущих проблем [GH 4105].</span><span class="sxs-lookup"><span data-stu-id="60e12-247">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="60e12-248">[WSL2] Улучшена диагностируемость проблем с сетью WSL2.</span><span class="sxs-lookup"><span data-stu-id="60e12-248">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="60e12-249">[WSL2] Ядро обновлено до версии 4.19.55.</span><span class="sxs-lookup"><span data-stu-id="60e12-249">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="60e12-250">[WSL2] Ядро обновлено с помощью параметров конфигурации, необходимых для Docker [GH 4165].</span><span class="sxs-lookup"><span data-stu-id="60e12-250">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="60e12-251">[WSL2] Увеличено число ЦП, назначаемых упрощенной служебной виртуальной машине, чтобы оно совпадало с числом ЦП узла (ранее это значение было ограничено 8 ЦП с помощью параметра CONFIG_NR_CPUS в конфигурации ядра) [GH 4137].</span><span class="sxs-lookup"><span data-stu-id="60e12-251">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="60e12-252">[WSL2] Создание файла подкачки для упрощенной виртуальной машины WSL2.</span><span class="sxs-lookup"><span data-stu-id="60e12-252">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="60e12-253">[WSL2] Разрешено отображение подключений пользователей в \\\\wsl$\\<имя_дистрибутива> (например, sshfs) [GH 4172].</span><span class="sxs-lookup"><span data-stu-id="60e12-253">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="60e12-254">[WSL2] Повышена производительность файловой системы 9p.</span><span class="sxs-lookup"><span data-stu-id="60e12-254">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="60e12-255">[WSL2] Предотвращение неограниченного роста списка ACL виртуального жесткого диска [GH 4126].</span><span class="sxs-lookup"><span data-stu-id="60e12-255">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="60e12-256">[WSL2] Обновлена конфигурации ядра для поддержки squashfs и xt_conntrack [GH 4107, 4123].</span><span class="sxs-lookup"><span data-stu-id="60e12-256">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="60e12-257">[WSL2] Исправлен параметр interop.enabled в /etc/wsl.conf [GH 4140].</span><span class="sxs-lookup"><span data-stu-id="60e12-257">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="60e12-258">[WSL2] Если файловая система не поддерживает EA, возвращается ENOTSUP.</span><span class="sxs-lookup"><span data-stu-id="60e12-258">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="60e12-259">[WSL2] CopyFile больше не прекращает отвечать на запросы при работе с \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="60e12-259">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="60e12-260">Параметр umask по умолчанию переключен на значение 0022, и добавлен параметр filesystem.umask в /etc/wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="60e12-260">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="60e12-261">Исправлен wslpath, чтобы правильно разрешать символические ссылки, что повторно происходило в 19h1 [GH 4078].</span><span class="sxs-lookup"><span data-stu-id="60e12-261">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="60e12-262">Введен файл %UserProfile%\\.wslconfig для настройки параметров WSL2.</span><span class="sxs-lookup"><span data-stu-id="60e12-262">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="60e12-263">Сборка 18917</span><span class="sxs-lookup"><span data-stu-id="60e12-263">Build 18917</span></span>
<span data-ttu-id="60e12-264">Общие сведения о сборке Windows 18917 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="60e12-264">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-265">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-265">WSL</span></span>
* <span data-ttu-id="60e12-266">Уже доступна версия WSL 2!</span><span class="sxs-lookup"><span data-stu-id="60e12-266">WSL 2 is now available!</span></span> <span data-ttu-id="60e12-267">Дополнительные сведения см. в [блоге](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).</span><span class="sxs-lookup"><span data-stu-id="60e12-267">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="60e12-268">Устранена регрессия, из-за которой запуск процессов Windows через символические ссылки выполнялся некорректно [GH 3999].</span><span class="sxs-lookup"><span data-stu-id="60e12-268">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="60e12-269">Добавлены следующие параметры wsl.exe: wsl.exe --list --verbose, wsl.exe --list --quiet и wsl.exe --import --version.</span><span class="sxs-lookup"><span data-stu-id="60e12-269">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="60e12-270">Добавлен параметр wsl.exe --shutdown.</span><span class="sxs-lookup"><span data-stu-id="60e12-270">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="60e12-271">Plan 9: для успешной работы разрешено открытие каталога для записи.</span><span class="sxs-lookup"><span data-stu-id="60e12-271">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="60e12-272">Сборка 18890</span><span class="sxs-lookup"><span data-stu-id="60e12-272">Build 18890</span></span>
<span data-ttu-id="60e12-273">Общие сведения о сборке Windows 18890 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="60e12-273">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-274">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-274">WSL</span></span>
* <span data-ttu-id="60e12-275">Утечка сокетов не блокирует работу [GH 2913].</span><span class="sxs-lookup"><span data-stu-id="60e12-275">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="60e12-276">Ввод EOF в терминал может заблокировать последующие операции чтения [GH 3421].</span><span class="sxs-lookup"><span data-stu-id="60e12-276">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="60e12-277">В заголовок resolv.conf добавлена ссылка на wsl.conf [рассмотрено в GH 3928].</span><span class="sxs-lookup"><span data-stu-id="60e12-277">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="60e12-278">Взаимоблокировка в коде epoll delete [GH 3922].</span><span class="sxs-lookup"><span data-stu-id="60e12-278">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="60e12-279">Обработка пробелов в аргументах параметров --import и --export [GH 3932].</span><span class="sxs-lookup"><span data-stu-id="60e12-279">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="60e12-280">Расширение файлов, обработанных с помощью mmap, не работает должным образом [GH 3939].</span><span class="sxs-lookup"><span data-stu-id="60e12-280">Extending mmap'd files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="60e12-281">Устранена проблема с доступом ARM64 к \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="60e12-281">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="60e12-282">Улучшен значок по умолчанию для wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="60e12-282">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="60e12-283">Сборка 18342</span><span class="sxs-lookup"><span data-stu-id="60e12-283">Build 18342</span></span>
<span data-ttu-id="60e12-284">Общие сведения о сборке Windows 18342 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="60e12-284">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-285">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-285">WSL</span></span>
* <span data-ttu-id="60e12-286">Мы добавили возможность доступа пользователей к файлам Linux в дистрибутиве WSL из Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-286">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="60e12-287">Доступ к этим файлам можно получить с помощью командной строки. Кроме того, такие приложения для Windows, как проводник, VSCode и т. д., могут взаимодействовать с этими файлами.</span><span class="sxs-lookup"><span data-stu-id="60e12-287">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="60e12-288">Чтобы получить доступ к файлам, перейдите в папку \\\\wsl$\\<имя_дистрибутива>, или просмотрите список выполняющихся дистрибутивов, перейдя в \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="60e12-288">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="60e12-289">Добавлены дополнительные теги сведений о ЦП и исправлены значения Cpus_allowed[_list] [GH 2234].</span><span class="sxs-lookup"><span data-stu-id="60e12-289">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="60e12-290">Поддержка выполнения из ведомого потока [GH 3800].</span><span class="sxs-lookup"><span data-stu-id="60e12-290">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="60e12-291">Ошибки обновления конфигурации не считаются критическими [GH 3785].</span><span class="sxs-lookup"><span data-stu-id="60e12-291">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="60e12-292">Подсистема binfmt обновлена для правильной обработки смещений [GH 3768].</span><span class="sxs-lookup"><span data-stu-id="60e12-292">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="60e12-293">Включено сопоставление сетевых дисков для Plan 9 [GH 3854].</span><span class="sxs-lookup"><span data-stu-id="60e12-293">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="60e12-294">Поддержка преобразования путей Windows в Linux и наоборот для подключения привязок.</span><span class="sxs-lookup"><span data-stu-id="60e12-294">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="60e12-295">Создание разделов только для чтения для сопоставлений файлов, открытых только для чтения.</span><span class="sxs-lookup"><span data-stu-id="60e12-295">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="60e12-296">Сборка 18334</span><span class="sxs-lookup"><span data-stu-id="60e12-296">Build 18334</span></span>
<span data-ttu-id="60e12-297">Общие сведения о сборке Windows 18334 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="60e12-297">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-298">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-298">WSL</span></span>
* <span data-ttu-id="60e12-299">Перепроектирован способ сопоставления часового пояса Windows с часовым поясом Linux [GH 3747].</span><span class="sxs-lookup"><span data-stu-id="60e12-299">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="60e12-300">Устранены утечки памяти и добавлены новые функции преобразования строк [GH 3746].</span><span class="sxs-lookup"><span data-stu-id="60e12-300">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="60e12-301">Выполнение SIGCONT для группы потоков без потоков является холостой командой [GH 3741].</span><span class="sxs-lookup"><span data-stu-id="60e12-301">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="60e12-302">Правильное отображение дескрипторов файлов socket и epoll в /proc/self/fd.</span><span class="sxs-lookup"><span data-stu-id="60e12-302">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="60e12-303">Сборка 18305</span><span class="sxs-lookup"><span data-stu-id="60e12-303">Build 18305</span></span>
<span data-ttu-id="60e12-304">Общие сведения о сборке Windows 18305 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="60e12-304">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-305">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-305">WSL</span></span>
* <span data-ttu-id="60e12-306">Когда основной поток завершает работу, pthreads утрачивает доступ к файлам [GH 3589].</span><span class="sxs-lookup"><span data-stu-id="60e12-306">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="60e12-307">Команда TIOCSCTTY должна игнорировать параметр force, если он не является обязательным [GH 3652].</span><span class="sxs-lookup"><span data-stu-id="60e12-307">TIOCSCTTY should ignore the "force" parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="60e12-308">Усовершенствована командная строка wsl.exe и добавлены функции импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="60e12-308">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="60e12-309">Сборка 18277</span><span class="sxs-lookup"><span data-stu-id="60e12-309">Build 18277</span></span>
<span data-ttu-id="60e12-310">Общие сведения о сборке Windows 18277 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="60e12-310">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-311">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-311">WSL</span></span>
* <span data-ttu-id="60e12-312">Устранена ошибка "Интерфейс не поддерживается" в сборке 18272 [GH 3645].</span><span class="sxs-lookup"><span data-stu-id="60e12-312">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="60e12-313">Игнорируется флаг MNT_FORCE для umount syscall [GH 3605].</span><span class="sxs-lookup"><span data-stu-id="60e12-313">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="60e12-314">Переключено взаимодействие WSL для использования официального API CreatePseudoConsole.</span><span class="sxs-lookup"><span data-stu-id="60e12-314">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="60e12-315">При перезапуске FUTEX_WAIT значение времени ожидания не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="60e12-315">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="60e12-316">Сборка 18272</span><span class="sxs-lookup"><span data-stu-id="60e12-316">Build 18272</span></span>
<span data-ttu-id="60e12-317">Общие сведения о сборке Windows 18272 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="60e12-317">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-318">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-318">WSL</span></span>
* <span data-ttu-id="60e12-319">**Предупреждение**. В этой сборке есть проблема, делающая компонент WSL неработоспособным.</span><span class="sxs-lookup"><span data-stu-id="60e12-319">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="60e12-320">При попытке запустить дистрибутив появится сообщение об ошибке "Интерфейс не поддерживается".</span><span class="sxs-lookup"><span data-stu-id="60e12-320">When trying to launch your distribution you will see a "No such interface supported" error.</span></span> <span data-ttu-id="60e12-321">Эта проблема устранена, и соответствующее исправление будет добавлено в сборку для предварительной оценки с ранним доступом, выпускаемую на следующей неделе.</span><span class="sxs-lookup"><span data-stu-id="60e12-321">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="60e12-322">Если вы установили эту сборку, можно вернуться к предыдущей сборке Windows, выбрав "Параметры" > "Обновление и безопасность" > "Восстановление" и щелкнув "Вернуться к предыдущей версии Windows 10".</span><span class="sxs-lookup"><span data-stu-id="60e12-322">If you've installed this build you can roll back to the previous Windows build using "Go back to the previous version of Windows 10" in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="60e12-323">Сборка 18267</span><span class="sxs-lookup"><span data-stu-id="60e12-323">Build 18267</span></span>
<span data-ttu-id="60e12-324">Общие сведения о сборке Windows 18267 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="60e12-324">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-325">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-325">WSL</span></span>
* <span data-ttu-id="60e12-326">Устранена проблема, из-за которой зомби-процесс мог быть не удален и существовал неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="60e12-326">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="60e12-327">WslRegisterDistribution переставал отвечать на запросы, если сообщение об ошибке превышало максимальную длину [GH 3592].</span><span class="sxs-lookup"><span data-stu-id="60e12-327">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="60e12-328">Разрешено использование fsync с файлами только для чтения в DrvFs [GH 3556].</span><span class="sxs-lookup"><span data-stu-id="60e12-328">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="60e12-329">Перед созданием символических ссылок в каталогах /bin и /sbin убедитесь, что эти каталоги существуют [GH 3584].</span><span class="sxs-lookup"><span data-stu-id="60e12-329">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="60e12-330">Добавлен механизм времени ожидания завершения экземпляра для экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-330">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="60e12-331">Сейчас время ожидания равно 15 секундам, то есть работа экземпляра завершается через 15 секунд после завершения последнего процесса WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-331">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="60e12-332">Чтобы немедленно завершить дистрибутив, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="60e12-332">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="60e12-333">Сборка 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="60e12-333">Build 17763 (1809)</span></span>
<span data-ttu-id="60e12-334">Общие сведения о сборке Windows 17763 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="60e12-334">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-335">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-335">WSL</span></span>
* <span data-ttu-id="60e12-336">Проверка разрешения SetPriority для syscall была слишком строгая для изменения приоритета того же потока [GH 1838].</span><span class="sxs-lookup"><span data-stu-id="60e12-336">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="60e12-337">Убедитесь, что для времени загрузки используется несмещенное время прерывания, чтобы избежать возврата отрицательных значений clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="60e12-337">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="60e12-338">Обработка символических ссылок в интерпретаторе binfmt для WSL [GH 3424].</span><span class="sxs-lookup"><span data-stu-id="60e12-338">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="60e12-339">Улучшена обработка очистки дескриптора файла ведущего потока группы потоков.</span><span class="sxs-lookup"><span data-stu-id="60e12-339">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="60e12-340">Чтобы избежать переполнения, переключите WSL на использование KeQueryInterruptTimePrecise вместо KeQueryPerformanceCounter [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="60e12-340">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="60e12-341">Подключение Ptrace могло вызывать неправильное возвращаемое значение из системных вызовов [GH 1731].</span><span class="sxs-lookup"><span data-stu-id="60e12-341">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="60e12-342">Устранено несколько проблем, связанных с AF_UNIX [GH 3371].</span><span class="sxs-lookup"><span data-stu-id="60e12-342">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="60e12-343">Устранена проблема, которая могла привести к сбою взаимодействия WSL, если длина текущего рабочего каталога была меньше 5 знаков [GH 3379].</span><span class="sxs-lookup"><span data-stu-id="60e12-343">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="60e12-344">Предотвращена задержка в 1 секунду при сбое замыкания на себя подключений к несуществующим портам (GH 3286).</span><span class="sxs-lookup"><span data-stu-id="60e12-344">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="60e12-345">Добавлен файл заглушки /proc/sys/fs/file-max [GH 2893].</span><span class="sxs-lookup"><span data-stu-id="60e12-345">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="60e12-346">Уточнены сведения об области действия IPv6.</span><span class="sxs-lookup"><span data-stu-id="60e12-346">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="60e12-347">Поддержка PR_SET_PTRACER [GH 3053].</span><span class="sxs-lookup"><span data-stu-id="60e12-347">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="60e12-348">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="60e12-348">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="60e12-349">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="60e12-349">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="60e12-350">Улучшена поддержка зомби [GH 1353].</span><span class="sxs-lookup"><span data-stu-id="60e12-350">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="60e12-351">Добавлены записи wsl.conf для управления поведением взаимодействия с Windows [GH 1493].</span><span class="sxs-lookup"><span data-stu-id="60e12-351">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="60e12-352">Устранена проблема, из-за которой команда getsockname не всегда возвращала тип семейства сокетов UNIX [GH 1774].</span><span class="sxs-lookup"><span data-stu-id="60e12-352">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="60e12-353">Добавлена поддержка TIOCSTI [GH 1863].</span><span class="sxs-lookup"><span data-stu-id="60e12-353">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="60e12-354">Неблокирующие сокеты в процессе подключения должны возвращать EAGAIN для попыток записи [GH 2846].</span><span class="sxs-lookup"><span data-stu-id="60e12-354">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="60e12-355">Поддержка взаимодействия с подключенными виртуальными жесткими дисками [GH 3246, 3291].</span><span class="sxs-lookup"><span data-stu-id="60e12-355">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="60e12-356">Устранена проблема с проверкой разрешений для корневой папки [GH 3304].</span><span class="sxs-lookup"><span data-stu-id="60e12-356">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="60e12-357">Ограниченная поддержка вызовов ioctl с аргументами KDGKBTYPE, KDGKBMODE и KDSKBMODE для клавиатуры tty.</span><span class="sxs-lookup"><span data-stu-id="60e12-357">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="60e12-358">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="60e12-358">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="60e12-359">Добавлен параметр wsl --u или --user [GH 1203].</span><span class="sxs-lookup"><span data-stu-id="60e12-359">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="60e12-360">Устранены проблемы с запуском WSL, когда включен быстрый запуск [GH 2576].</span><span class="sxs-lookup"><span data-stu-id="60e12-360">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="60e12-361">Сокеты UNIX должны хранить учетные данные отключенных одноранговых узлов [GH 3183].</span><span class="sxs-lookup"><span data-stu-id="60e12-361">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="60e12-362">Работа неблокирующих сокетов UNIX неограниченное время завершалась сбоем и возвращалось значение EAGAIN [GH 3191].</span><span class="sxs-lookup"><span data-stu-id="60e12-362">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="60e12-363">Новый тип подключения drvfs по умолчанию case=off [GH 2937, 3212, 3328].</span><span class="sxs-lookup"><span data-stu-id="60e12-363">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="60e12-364">Дополнительные сведения см. в [этом блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="60e12-364">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="60e12-365">Добавлен параметр wslconfig /terminate для остановки выполнения дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="60e12-365">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="60e12-366">Устранена проблема с пунктами в контекстном меню оболочки WSL, из-за которой неправильно обрабатывались пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="60e12-366">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="60e12-367">Учет регистра в именах каталогов реализован в качестве расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="60e12-367">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="60e12-368">ARM64: имитация операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="60e12-368">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="60e12-369">Устранена [проблема с dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="60e12-369">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="60e12-370">DrvFs: в частном диапазоне допускаются только неэкранированные знаки, которые соответствуют экранированному знаку.</span><span class="sxs-lookup"><span data-stu-id="60e12-370">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="60e12-371">Устранена ошибка завышения или занижения на единицу при проверке длины интерпретатором анализатора ELF [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="60e12-371">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="60e12-372">Абсолютные таймеры WSL со временем в прошлом не срабатывали [GH 3091].</span><span class="sxs-lookup"><span data-stu-id="60e12-372">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="60e12-373">Убедитесь, что вновь созданные точки повторного анализа указаны как таковые в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="60e12-373">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="60e12-374">Атомарное создание каталогов с учетом регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-374">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="60e12-375">Устранена дополнительная проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="60e12-375">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="60e12-376">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="60e12-376">[GH 2712]</span></span>
* <span data-ttu-id="60e12-377">Устранена ошибка запуска WSL при включенном режиме UMCI.</span><span class="sxs-lookup"><span data-stu-id="60e12-377">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="60e12-378">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="60e12-378">[GH 3020]</span></span>
* <span data-ttu-id="60e12-379">Добавлено контекстное меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="60e12-379">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="60e12-380">Чтобы открыть его, нажмите и удерживайте клавишу SHIFT и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="60e12-380">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="60e12-381">Устранено неблокирующее поведение сокетов UNIX [GH 2822, 3100].</span><span class="sxs-lookup"><span data-stu-id="60e12-381">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="60e12-382">Устранена проблема, из-за которой команда NETLINK переставала отвечать на запросы, как было сообщено в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="60e12-382">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="60e12-383">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="60e12-383">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="60e12-384">Устранена проблема, из-за которой усечение не вызывало события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="60e12-384">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="60e12-385">Добавлен параметр --exec для wsl.exe, позволяющий вызвать отдельный двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="60e12-385">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="60e12-386">Добавлен параметр --distribution для wsl.exe, позволяющий выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="60e12-386">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="60e12-387">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="60e12-387">Limited support for dmesg.</span></span> <span data-ttu-id="60e12-388">Теперь приложения могут входить в dmesg.</span><span class="sxs-lookup"><span data-stu-id="60e12-388">Applications can now log to dmesg.</span></span> <span data-ttu-id="60e12-389">Драйвер WSL записывает ограниченные сведения в dmesg.</span><span class="sxs-lookup"><span data-stu-id="60e12-389">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="60e12-390">В будущем эти возможности можно будет расширить, чтобы записывать другие сведения и данные диагностики из драйвера.</span><span class="sxs-lookup"><span data-stu-id="60e12-390">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="60e12-391">Примечание. Сейчас dmesg поддерживается через интерфейс устройства `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="60e12-391">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="60e12-392">Интерфейс syscall `syslog` пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60e12-392">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="60e12-393">Поэтому некоторые параметры командной строки `dmesg`, такие как `-S` и `-C`, не работают.</span><span class="sxs-lookup"><span data-stu-id="60e12-393">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="60e12-394">Изменены GID и режим по умолчанию для последовательных устройств, чтобы обеспечить соответствие собственному режиму [GH 3042].</span><span class="sxs-lookup"><span data-stu-id="60e12-394">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="60e12-395">Теперь DrvFs поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="60e12-395">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="60e12-396">Примечание. В DrvFs были некоторые ограничения для имен расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="60e12-396">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="60e12-397">Некоторые знаки (например, "/", ":" и "\*") не допускаются, а в именах расширенных атрибутов в DrvFs не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="60e12-397">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="60e12-398">Сборка 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="60e12-398">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="60e12-399">Общие сведения о сборке Windows 18252 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="60e12-399">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-400">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-400">WSL</span></span>
* <span data-ttu-id="60e12-401">Двоичные файлы init и bsdtar перемещены из библиотеки DLL lxssmanager в отдельную папку tools.</span><span class="sxs-lookup"><span data-stu-id="60e12-401">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="60e12-402">Устранено состязание при закрытии дескриптора файла в случае использования CLONE_FILES.</span><span class="sxs-lookup"><span data-stu-id="60e12-402">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="60e12-403">Обработка необязательных полей в /proc/pid/mountinfo при преобразовании путей DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-403">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="60e12-404">Допускается успешное выполнение mknod DrvFs без поддержки метаданных для S_IFREG.</span><span class="sxs-lookup"><span data-stu-id="60e12-404">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="60e12-405">Файлы только для чтения, созданные в DrvFs, должны иметь атрибут readonly [GH 3411].</span><span class="sxs-lookup"><span data-stu-id="60e12-405">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="60e12-406">Добавлено вспомогательное приложение /sbin/mount.drvfs для управления подключением DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-406">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="60e12-407">Использование переименования POSIX в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-407">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="60e12-408">Разрешено преобразование путей в томах без GUID тома.</span><span class="sxs-lookup"><span data-stu-id="60e12-408">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="60e12-409">Сборка 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="60e12-409">Build 17738 (Fast)</span></span>
<span data-ttu-id="60e12-410">Общие сведения о сборке Windows 17738 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="60e12-410">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-411">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-411">WSL</span></span>
* <span data-ttu-id="60e12-412">Проверка разрешения SetPriority для syscall была слишком строгая для изменения приоритета того же потока [GH 1838].</span><span class="sxs-lookup"><span data-stu-id="60e12-412">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="60e12-413">Убедитесь, что для времени загрузки используется несмещенное время прерывания, чтобы избежать возврата отрицательных значений clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="60e12-413">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="60e12-414">Обработка символических ссылок в интерпретаторе binfmt для WSL [GH 3424].</span><span class="sxs-lookup"><span data-stu-id="60e12-414">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="60e12-415">Улучшена обработка очистки дескриптора файла ведущего потока группы потоков.</span><span class="sxs-lookup"><span data-stu-id="60e12-415">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="60e12-416">Сборка 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="60e12-416">Build 17728 (Fast)</span></span>
<span data-ttu-id="60e12-417">Общие сведения о сборке Windows 17728 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="60e12-417">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-418">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-418">WSL</span></span>
* <span data-ttu-id="60e12-419">Чтобы избежать переполнения, переключите WSL на использование KeQueryInterruptTimePrecise вместо KeQueryPerformanceCounter [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="60e12-419">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="60e12-420">Подключение Ptrace могло вызывать неправильное возвращаемое значение из системных вызовов [GH 1731].</span><span class="sxs-lookup"><span data-stu-id="60e12-420">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="60e12-421">Устранен ряд проблем, связанных с AF_UNIX [GH 3371].</span><span class="sxs-lookup"><span data-stu-id="60e12-421">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="60e12-422">Устранена проблема, которая могла привести к сбою взаимодействия WSL, если длина текущего рабочего каталога была меньше 5 знаков [GH 3379].</span><span class="sxs-lookup"><span data-stu-id="60e12-422">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="60e12-423">Сборка 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="60e12-423">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="60e12-424">Общие сведения о сборке Windows 18204 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="60e12-424">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-425">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-425">WSL</span></span>
* <span data-ttu-id="60e12-426">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="60e12-426">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="60e12-427">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="60e12-427">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="60e12-428">Сборка 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="60e12-428">Build 17723 (Fast)</span></span>
<span data-ttu-id="60e12-429">Общие сведения о сборке Windows 17723 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="60e12-429">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-430">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-430">WSL</span></span>
* <span data-ttu-id="60e12-431">Предотвращена задержка в 1 секунду при сбое замыкания на себя подключений к несуществующим портам (GH 3286).</span><span class="sxs-lookup"><span data-stu-id="60e12-431">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="60e12-432">Добавлен файл заглушки /proc/sys/fs/file-max [GH 2893].</span><span class="sxs-lookup"><span data-stu-id="60e12-432">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="60e12-433">Уточнены сведения об области действия IPv6.</span><span class="sxs-lookup"><span data-stu-id="60e12-433">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="60e12-434">Поддержка PR_SET_PTRACER [GH 3053].</span><span class="sxs-lookup"><span data-stu-id="60e12-434">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="60e12-435">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="60e12-435">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="60e12-436">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="60e12-436">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="60e12-437">Сборка 17713</span><span class="sxs-lookup"><span data-stu-id="60e12-437">Build 17713</span></span>
<span data-ttu-id="60e12-438">Общие сведения о сборке Windows 17713 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="60e12-438">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-439">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-439">WSL</span></span>
* <span data-ttu-id="60e12-440">Улучшена поддержка зомби [GH 1353].</span><span class="sxs-lookup"><span data-stu-id="60e12-440">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="60e12-441">Добавлены записи wsl.conf для управления поведением взаимодействия с Windows [GH 1493].</span><span class="sxs-lookup"><span data-stu-id="60e12-441">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="60e12-442">Устранена проблема, из-за которой команда getsockname не всегда возвращала тип семейства сокетов UNIX [GH 1774].</span><span class="sxs-lookup"><span data-stu-id="60e12-442">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="60e12-443">Добавлена поддержка TIOCSTI [GH 1863].</span><span class="sxs-lookup"><span data-stu-id="60e12-443">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="60e12-444">Неблокирующие сокеты в процессе подключения должны возвращать EAGAIN для попыток записи [GH 2846].</span><span class="sxs-lookup"><span data-stu-id="60e12-444">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="60e12-445">Поддержка взаимодействия с подключенными виртуальными жесткими дисками [GH 3246, 3291].</span><span class="sxs-lookup"><span data-stu-id="60e12-445">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="60e12-446">Устранена проблема с проверкой разрешений для корневой папки [GH 3304].</span><span class="sxs-lookup"><span data-stu-id="60e12-446">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="60e12-447">Ограниченная поддержка вызовов ioctl с аргументами KDGKBTYPE, KDGKBMODE и KDSKBMODE для клавиатуры tty.</span><span class="sxs-lookup"><span data-stu-id="60e12-447">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="60e12-448">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="60e12-448">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="60e12-449">Сборка 17704</span><span class="sxs-lookup"><span data-stu-id="60e12-449">Build 17704</span></span>
<span data-ttu-id="60e12-450">Общие сведения о сборке Windows 17704 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="60e12-450">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-451">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-451">WSL</span></span>
* <span data-ttu-id="60e12-452">Добавлен параметр wsl --u или --user [GH 1203].</span><span class="sxs-lookup"><span data-stu-id="60e12-452">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="60e12-453">Устранены проблемы с запуском WSL, когда включен быстрый запуск [GH 2576].</span><span class="sxs-lookup"><span data-stu-id="60e12-453">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="60e12-454">Сокеты UNIX должны хранить учетные данные отключенных одноранговых узлов [GH 3183].</span><span class="sxs-lookup"><span data-stu-id="60e12-454">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="60e12-455">Работа неблокирующих сокетов UNIX неограниченное время завершалась сбоем и возвращалось значение EAGAIN [GH 3191].</span><span class="sxs-lookup"><span data-stu-id="60e12-455">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="60e12-456">Новый тип подключения drvfs по умолчанию case=off [GH 2937, 3212, 3328].</span><span class="sxs-lookup"><span data-stu-id="60e12-456">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="60e12-457">Дополнительные сведения см. в [этом блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="60e12-457">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="60e12-458">Добавлен параметр wslconfig /terminate для остановки выполнения дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="60e12-458">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="60e12-459">Сборка 17692</span><span class="sxs-lookup"><span data-stu-id="60e12-459">Build 17692</span></span>
<span data-ttu-id="60e12-460">Общие сведения о сборке Windows 17692 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="60e12-460">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-461">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-461">WSL</span></span>
* <span data-ttu-id="60e12-462">Устранена проблема с пунктами в контекстном меню оболочки WSL, из-за которой неправильно обрабатывались пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="60e12-462">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="60e12-463">Учет регистра в именах каталогов реализован в качестве расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="60e12-463">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="60e12-464">ARM64: имитация операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="60e12-464">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="60e12-465">Устранена [проблема с dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="60e12-465">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="60e12-466">DrvFs: в частном диапазоне допускаются только неэкранированные знаки, которые соответствуют экранированному знаку.</span><span class="sxs-lookup"><span data-stu-id="60e12-466">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="60e12-467">Сборка 17686</span><span class="sxs-lookup"><span data-stu-id="60e12-467">Build 17686</span></span>
<span data-ttu-id="60e12-468">Общие сведения о сборке Windows 17686 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="60e12-468">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-469">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-469">WSL</span></span>
* <span data-ttu-id="60e12-470">Устранена ошибка завышения или занижения на единицу при проверке длины интерпретатором анализатора ELF [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="60e12-470">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="60e12-471">Абсолютные таймеры WSL со временем в прошлом не срабатывали [GH 3091].</span><span class="sxs-lookup"><span data-stu-id="60e12-471">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="60e12-472">Убедитесь, что вновь созданные точки повторного анализа указаны как таковые в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="60e12-472">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="60e12-473">Атомарное создание каталогов с учетом регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-473">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="60e12-474">Сборка 17677</span><span class="sxs-lookup"><span data-stu-id="60e12-474">Build 17677</span></span>
<span data-ttu-id="60e12-475">Общие сведения о сборке Windows 17677 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="60e12-475">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-476">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-476">WSL</span></span>
* <span data-ttu-id="60e12-477">Устранена дополнительная проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="60e12-477">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="60e12-478">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="60e12-478">[GH 2712]</span></span>
* <span data-ttu-id="60e12-479">Устранена ошибка запуска WSL при включенном режиме UMCI.</span><span class="sxs-lookup"><span data-stu-id="60e12-479">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="60e12-480">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="60e12-480">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="60e12-481">Сборка 17666</span><span class="sxs-lookup"><span data-stu-id="60e12-481">Build 17666</span></span>
<span data-ttu-id="60e12-482">Общие сведения о сборке Windows 17666 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="60e12-482">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-483">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-483">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="60e12-484">ПРЕДУПРЕЖДЕНИЕ! Существует проблема, препятствующая запуску WSL на некоторых наборах микросхем AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="60e12-484">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="60e12-485">Исправление готово и находится в процессе добавления в ветвь сборок для программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-485">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="60e12-486">Добавлено контекстное меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="60e12-486">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="60e12-487">Чтобы открыть его, нажмите и удерживайте клавишу SHIFT и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="60e12-487">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="60e12-488">Устранено неблокирующее поведение сокетов UNIX [GH 2822, 3100].</span><span class="sxs-lookup"><span data-stu-id="60e12-488">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="60e12-489">Устранена проблема, из-за которой команда NETLINK переставала отвечать на запросы, как было сообщено в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="60e12-489">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="60e12-490">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="60e12-490">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="60e12-491">Устранена проблема, из-за которой усечение не вызывало события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="60e12-491">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="60e12-492">Добавлен параметр --exec для wsl.exe, позволяющий вызвать отдельный двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="60e12-492">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="60e12-493">Добавлен параметр --distribution для wsl.exe, позволяющий выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="60e12-493">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="60e12-494">Сборка 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="60e12-494">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="60e12-495">Общие сведения о сборке Windows 17655 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="60e12-495">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-496">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-496">WSL</span></span>
* <span data-ttu-id="60e12-497">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="60e12-497">Limited support for dmesg.</span></span> <span data-ttu-id="60e12-498">Теперь приложения могут входить в dmesg.</span><span class="sxs-lookup"><span data-stu-id="60e12-498">Applications can now log to dmesg.</span></span> <span data-ttu-id="60e12-499">Драйвер WSL записывает ограниченные сведения в dmesg.</span><span class="sxs-lookup"><span data-stu-id="60e12-499">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="60e12-500">В будущем эти возможности можно будет расширить, чтобы записывать другие сведения и данные диагностики из драйвера.</span><span class="sxs-lookup"><span data-stu-id="60e12-500">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="60e12-501">Примечание. Сейчас dmesg поддерживается через интерфейс устройства `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="60e12-501">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="60e12-502">Интерфейс sycall `syslog` еще не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60e12-502">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="60e12-503">Поэтому некоторые параметры командной строки `dmesg`, такие как `-S` и `-C`, не работают.</span><span class="sxs-lookup"><span data-stu-id="60e12-503">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="60e12-504">Устранена проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="60e12-504">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="60e12-505">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="60e12-505">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="60e12-506">Сборка 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="60e12-506">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="60e12-507">Общие сведения о сборке Windows 17639 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="60e12-507">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-508">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-508">WSL</span></span>
* <span data-ttu-id="60e12-509">Изменены GID и режим по умолчанию для последовательных устройств, чтобы обеспечить соответствие собственному режиму [GH 3042].</span><span class="sxs-lookup"><span data-stu-id="60e12-509">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="60e12-510">Теперь DrvFs поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="60e12-510">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="60e12-511">Примечание. В DrvFs были некоторые ограничения для имен расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="60e12-511">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="60e12-512">В частности, некоторые знаки (например, "/", ":" и "\*") не допускаются, а в именах расширенных атрибутов в DrvFs не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="60e12-512">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="60e12-513">Сборка 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="60e12-513">Build 17133 (Fast)</span></span>
<span data-ttu-id="60e12-514">Общие сведения о сборке Windows 17133 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="60e12-514">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-515">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-515">WSL</span></span>
* <span data-ttu-id="60e12-516">Устранено прекращение ответа на запросы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-516">Fix for hang in WSL.</span></span> <span data-ttu-id="60e12-517">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="60e12-517">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="60e12-518">Сборка 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="60e12-518">Build 17128 (Fast)</span></span>
<span data-ttu-id="60e12-519">Общие сведения о сборке Windows 17128 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="60e12-519">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-520">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-520">WSL</span></span>
* <span data-ttu-id="60e12-521">Нет</span><span class="sxs-lookup"><span data-stu-id="60e12-521">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="60e12-522">Сборка 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="60e12-522">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="60e12-523">Общие сведения о сборке Windows 17627 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="60e12-523">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-524">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-524">WSL</span></span>
* <span data-ttu-id="60e12-525">Добавлена поддержка фьютексных операций с поддержкой числа пи.</span><span class="sxs-lookup"><span data-stu-id="60e12-525">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="60e12-526">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="60e12-526">[GH 1006]</span></span>
    * <span data-ttu-id="60e12-527">Обратите внимание на то, что приоритеты в настоящее время не поддерживаются компонентом WSL, так что существуют ограничения, но стандартное использование должно быть доступно.</span><span class="sxs-lookup"><span data-stu-id="60e12-527">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="60e12-528">Поддержка брандмауэра Windows для процессов WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-528">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="60e12-529">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="60e12-529">[GH 1852]</span></span>
    * <span data-ttu-id="60e12-530">Например, чтобы разрешить процессу Python в WSL ожидать передачи данных через какой-либо порт, используйте командную строку Windows с повышенными привилегиями: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="60e12-530">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="60e12-531">Дополнительные сведения о добавлении правил брандмауэра доступны по [этой ссылке](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh).</span><span class="sxs-lookup"><span data-stu-id="60e12-531">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="60e12-532">При использовании wsl.exe учитывается оболочка по умолчанию пользователя.</span><span class="sxs-lookup"><span data-stu-id="60e12-532">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="60e12-533">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="60e12-533">[GH 2372]</span></span>
* <span data-ttu-id="60e12-534">Все сетевые интерфейсы отображаются как Ethernet.</span><span class="sxs-lookup"><span data-stu-id="60e12-534">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="60e12-535">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="60e12-535">[GH 2996]</span></span>
* <span data-ttu-id="60e12-536">Улучшена обработка поврежденного файла /etc/passwd.</span><span class="sxs-lookup"><span data-stu-id="60e12-536">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="60e12-537">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="60e12-537">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="60e12-538">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-538">Console</span></span>
* <span data-ttu-id="60e12-539">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-539">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-540">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-540">LTP Results:</span></span>
<span data-ttu-id="60e12-541">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-541">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="60e12-542">Сборка 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="60e12-542">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="60e12-543">Общие сведения о сборке Windows 17618 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="60e12-543">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-544">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-544">WSL</span></span>
* <span data-ttu-id="60e12-545">Введена функция псевдоконсоли для взаимодействия с NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="60e12-545">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="60e12-546">Устаревший механизм установки (lxrun.exe) является нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="60e12-546">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="60e12-547">Для установки дистрибутивов используется Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="60e12-547">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="60e12-548">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-548">Console</span></span>
* <span data-ttu-id="60e12-549">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-549">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-550">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-550">LTP Results:</span></span>
<span data-ttu-id="60e12-551">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-551">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="60e12-552">Сборка 17110</span><span class="sxs-lookup"><span data-stu-id="60e12-552">Build 17110</span></span>
<span data-ttu-id="60e12-553">Общие сведения о сборке Windows 17110 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="60e12-553">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-554">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-554">WSL</span></span>
* <span data-ttu-id="60e12-555">Разрешено завершение /init из Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="60e12-555">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="60e12-556">Теперь DrvFs по умолчанию учитывает регистр в имени отдельно для каждого каталога (аналогично параметру подключения case=dir).</span><span class="sxs-lookup"><span data-stu-id="60e12-556">DrvFs now uses per-directory case sensitivity by default (equivalent to the "case=dir" mount option).</span></span>
    * <span data-ttu-id="60e12-557">Для использования параметра case=force (прежнее поведение) требуется задать раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="60e12-557">Using "case=force" (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="60e12-558">Выполните следующую команду, чтобы включить режим case=force, если его необходимо использовать: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="60e12-558">Run the following command to enable "case=force" if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="60e12-559">Если у вас есть каталоги, созданные с помощью WSL в более ранней версии Windows, в которых должен учитываться регистр, используйте fsutil.exe, чтобы пометить их как каталоги с учетом регистра: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="60e12-559">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="60e12-560">Строки, возвращаемые из uname syscall, завершаются значением NULL.</span><span class="sxs-lookup"><span data-stu-id="60e12-560">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="60e12-561">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-561">Console</span></span>
* <span data-ttu-id="60e12-562">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-562">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-563">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-563">LTP Results:</span></span>
<span data-ttu-id="60e12-564">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-564">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="60e12-565">Сборка 17107</span><span class="sxs-lookup"><span data-stu-id="60e12-565">Build 17107</span></span>
<span data-ttu-id="60e12-566">Общие сведения о сборке Windows 17107 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="60e12-566">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-567">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-567">WSL</span></span>
* <span data-ttu-id="60e12-568">Поддержка TCSETSF и TCSETSW на главных конечных точках PTY [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="60e12-568">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="60e12-569">Запуск одновременных процессов взаимодействия мог привести к возвращению EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="60e12-569">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="60e12-570">Устранена проблема с PTRACE_ATTACH для отображения правильного состояния трассировки в /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="60e12-570">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="60e12-571">Устранено состязание, когда кратковременные процессы, клонированные с флагами CLEARTID и SETTID, могли завершиться без очистки адреса TID.</span><span class="sxs-lookup"><span data-stu-id="60e12-571">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="60e12-572">Отображается сообщение, если при переходе со сборки, предшествующей сборке 17093, выполняется обновление каталогов файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-572">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="60e12-573">Дополнительные сведения об изменениях в файловой системе в сборке 17093 доступны в заметках о выпуске [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="60e12-573">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="60e12-574">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-574">Console</span></span>
* <span data-ttu-id="60e12-575">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-575">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-576">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-576">LTP Results:</span></span>
<span data-ttu-id="60e12-577">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-577">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="60e12-578">Сборка 17101</span><span class="sxs-lookup"><span data-stu-id="60e12-578">Build 17101</span></span>
<span data-ttu-id="60e12-579">Общие сведения о сборке Windows 17101 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="60e12-579">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-580">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-580">WSL</span></span>
* <span data-ttu-id="60e12-581">Поддержка signalfd.</span><span class="sxs-lookup"><span data-stu-id="60e12-581">Support for signalfd.</span></span> <span data-ttu-id="60e12-582">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="60e12-582">[GH 129]</span></span>
* <span data-ttu-id="60e12-583">Поддержка имен файлов, содержащих недопустимые знаки NTFS, благодаря их кодированию в виде частных знаков Юникода.</span><span class="sxs-lookup"><span data-stu-id="60e12-583">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="60e12-584">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="60e12-584">[GH 1514]</span></span>
* <span data-ttu-id="60e12-585">Функция автоматического подключения будет переключаться в режим только для чтения, если запись не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60e12-585">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="60e12-586">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="60e12-586">[GH 2603]</span></span>
* <span data-ttu-id="60e12-587">Допускается вставка суррогатных пар Юникода (например, знаков эмодзи).</span><span class="sxs-lookup"><span data-stu-id="60e12-587">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="60e12-588">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="60e12-588">[GH 2765]</span></span>
* <span data-ttu-id="60e12-589">Псевдофайлы в /proc и /sys должны возвращаться готовыми для чтения и записи после выполнения команд select, poll, epoll и т. д. [GH 2838].</span><span class="sxs-lookup"><span data-stu-id="60e12-589">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="60e12-590">Устранена проблема, из-за которой служба могла уйти в бесконечный цикл, если реестр был незаконно изменен или поврежден.</span><span class="sxs-lookup"><span data-stu-id="60e12-590">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="60e12-591">Сообщения NETLINK исправлены для работы с более новой версией iproute2 (начиная с версии 4.14).</span><span class="sxs-lookup"><span data-stu-id="60e12-591">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="60e12-592">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-592">Console</span></span>
* <span data-ttu-id="60e12-593">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-593">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-594">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-594">LTP Results:</span></span>
<span data-ttu-id="60e12-595">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-595">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="60e12-596">Сборка 17093</span><span class="sxs-lookup"><span data-stu-id="60e12-596">Build 17093</span></span>
<span data-ttu-id="60e12-597">Общие сведения о сборке Windows 17093 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-597">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="60e12-598">Важно!</span><span class="sxs-lookup"><span data-stu-id="60e12-598">Important:</span></span>
<span data-ttu-id="60e12-599">При запуске WSL в первый раз после обновления до этой сборки необходимо выполнить некоторые действия, чтобы обновить каталоги файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-599">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="60e12-600">Это может занять несколько минут, поэтому может показаться, что WSL медленно запускается.</span><span class="sxs-lookup"><span data-stu-id="60e12-600">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="60e12-601">Это должно произойти только один раз для каждого дистрибутива, установленного из Store.</span><span class="sxs-lookup"><span data-stu-id="60e12-601">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="60e12-602">Улучшена поддержка учета регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-602">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="60e12-603">Теперь DrvFs поддерживает учет регистра отдельно для каждого каталога.</span><span class="sxs-lookup"><span data-stu-id="60e12-603">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="60e12-604">Это новый флаг, который можно задать для каталогов, чтобы указать, что все операции в этих каталогах должны выполняться с учетом регистра, что позволит даже приложениям для Windows правильно открывать файлы, отличающиеся только регистром в именах.</span><span class="sxs-lookup"><span data-stu-id="60e12-604">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="60e12-605">В DrvFs есть новые параметры подключения, управляющие учетом регистра для каждого каталога:</span><span class="sxs-lookup"><span data-stu-id="60e12-605">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="60e12-606">case=force: для всех каталогов учитывается регистр (за исключением корневого диска).</span><span class="sxs-lookup"><span data-stu-id="60e12-606">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="60e12-607">Новые каталоги, созданные с помощью WSL, помечаются как каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="60e12-607">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="60e12-608">Это устаревшее поведение, за исключением пометки новых каталогов как каталогов с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="60e12-608">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="60e12-609">case=dir: регистр учитывается только для каталогов с флагом учета регистра; для других каталогов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="60e12-609">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="60e12-610">Новые каталоги, созданные с помощью WSL, помечаются как каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="60e12-610">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="60e12-611">case=off: регистр учитывается только для каталогов с флагом учета регистра; для других каталогов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="60e12-611">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="60e12-612">Новые каталоги, созданные с помощью WSL, помечаются как каталоги без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="60e12-612">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="60e12-613">Примечание. Каталоги, созданные WSL в предыдущих выпусках, не имеют этого флага, поэтому для них регистр не будет учитываться, если задан параметр case=dir.</span><span class="sxs-lookup"><span data-stu-id="60e12-613">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the "case=dir" option.</span></span> <span data-ttu-id="60e12-614">Способ задания этого флага для существующих каталогов будет реализован в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="60e12-614">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="60e12-615">Пример подключения с этими параметрами (существующие диски необходимо сначала отключить, чтобы подключить их с другими параметрами): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="60e12-615">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="60e12-616">Пока что параметр "case=force" все еще используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60e12-616">For now, case=force is still the default option.</span></span> <span data-ttu-id="60e12-617">В будущем по умолчанию будет использоваться параметр case=dir.</span><span class="sxs-lookup"><span data-stu-id="60e12-617">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="60e12-618">Теперь вы можете использовать косую черту в путях Windows при подключении DrvFs, например: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="60e12-618">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="60e12-619">WSL теперь обрабатывает файл /etc/fstab во время запуска экземпляра [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="60e12-619">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="60e12-620">Это делается до автоматического подключения дисков DrvFs. Все диски, которые уже были подключены fstab, не будут автоматически подключаться. Это позволит вам изменить точку подключения для конкретных дисков.</span><span class="sxs-lookup"><span data-stu-id="60e12-620">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="60e12-621">Это поведение можно отключить с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="60e12-621">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="60e12-622">Файлы mount, mountinfo и mountstats в /proc правильно экранируют специальные знаки, такие как символы обратной косой черты и пробелы [GH 2799].</span><span class="sxs-lookup"><span data-stu-id="60e12-622">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="60e12-623">Теперь можно копировать и перемещать из Windows специальные файлы, созданные с помощью DrvFs, такие как символьные ссылки WSL, или файлы FIFO и сокеты, если метаданные включены.</span><span class="sxs-lookup"><span data-stu-id="60e12-623">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="60e12-624">Можно настроить больше параметров WSL с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="60e12-624">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="60e12-625">Мы добавили метод для автоматической настройки определенных функций в WSL, которые будут применяться при каждом запуске подсистемы.</span><span class="sxs-lookup"><span data-stu-id="60e12-625">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="60e12-626">Сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="60e12-626">This includes automount options and network configuration.</span></span> <span data-ttu-id="60e12-627">Дополнительные сведения об этом можно получить из нашей записи блога: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="60e12-627">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="60e12-628">AF_UNIX позволяет устанавливать подключения через сокет между процессами Linux в собственных процессах WSL и Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-628">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="60e12-629">Теперь приложения WSL и приложения для Windows могут взаимодействовать друг с другом через сокеты UNIX.</span><span class="sxs-lookup"><span data-stu-id="60e12-629">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="60e12-630">Представьте, что вы хотите запустить службу в Windows и сделать ее доступной для приложений для Windows и приложений WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-630">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="60e12-631">Теперь это возможно благодаря сокетам UNIX.</span><span class="sxs-lookup"><span data-stu-id="60e12-631">Now, that's possible with Unix sockets.</span></span> <span data-ttu-id="60e12-632">Узнайте больше в записи блога https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="60e12-632">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-633">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-633">WSL</span></span>
* <span data-ttu-id="60e12-634">Поддержка mmap() с MAP_NORESERVE [GH 121, 2784].</span><span class="sxs-lookup"><span data-stu-id="60e12-634">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="60e12-635">Поддержка CLONE_PTRACE и CLONE_UNTRACED [GH 121, 2781].</span><span class="sxs-lookup"><span data-stu-id="60e12-635">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="60e12-636">Обработка сигнала завершения без SIGCHLD в клоне [GH 121, 2781].</span><span class="sxs-lookup"><span data-stu-id="60e12-636">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="60e12-637">Добавлены заглушки /proc/sys/fs/inotify/max_user_instances и /proc/sys/fs/inotify/max_user_watches [GH 1705].</span><span class="sxs-lookup"><span data-stu-id="60e12-637">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="60e12-638">Устранена ошибка при загрузке двоичных файлов ELF, содержащих заголовки загрузки с ненулевыми смещениями [GH 1884].</span><span class="sxs-lookup"><span data-stu-id="60e12-638">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="60e12-639">Заполнение нулями конечных байтов страниц при загрузке образов.</span><span class="sxs-lookup"><span data-stu-id="60e12-639">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="60e12-640">Сокращены случаи, когда execve автоматически завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="60e12-640">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="60e12-641">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-641">Console</span></span>
* <span data-ttu-id="60e12-642">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-642">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-643">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-643">LTP Results:</span></span>
<span data-ttu-id="60e12-644">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-644">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="60e12-645">Сборка 17083</span><span class="sxs-lookup"><span data-stu-id="60e12-645">Build 17083</span></span>
<span data-ttu-id="60e12-646">Общие сведения о сборке Windows 17083 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-646">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-647">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-647">WSL</span></span>
* <span data-ttu-id="60e12-648">Исправлена критическая ошибка, связанная с epoll [GH 2798, 2801, 2857].</span><span class="sxs-lookup"><span data-stu-id="60e12-648">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="60e12-649">Исправлено прекращение реагирования на запросы при отключении ASLR [GH 1185, 2870].</span><span class="sxs-lookup"><span data-stu-id="60e12-649">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="60e12-650">Обеспечена атомарность операций mmap [GH 2732].</span><span class="sxs-lookup"><span data-stu-id="60e12-650">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="60e12-651">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-651">Console</span></span>
* <span data-ttu-id="60e12-652">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-652">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-653">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-653">LTP Results:</span></span>
<span data-ttu-id="60e12-654">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-654">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="60e12-655">Сборка 17074</span><span class="sxs-lookup"><span data-stu-id="60e12-655">Build 17074</span></span>
<span data-ttu-id="60e12-656">Общие сведения о сборке Windows 17074 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-656">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-657">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-657">WSL</span></span>
* <span data-ttu-id="60e12-658">Исправлен формат хранения метаданных DrvFs [GH 2777].</span><span class="sxs-lookup"><span data-stu-id="60e12-658">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="60e12-659">**Важно!** Метаданные DrvFs, созданные до выпуска этой сборки, будут отображаться неправильно или вообще не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="60e12-659">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="60e12-660">Чтобы исправить затронутые файлы, используйте chmod и chown для повторного применения метаданных.</span><span class="sxs-lookup"><span data-stu-id="60e12-660">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="60e12-661">Устранена проблема с несколькими сигналами и перезапускаемыми вызовами syscall.</span><span class="sxs-lookup"><span data-stu-id="60e12-661">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="60e12-662">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-662">Console</span></span>
* <span data-ttu-id="60e12-663">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-663">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-664">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-664">LTP Results:</span></span>
<span data-ttu-id="60e12-665">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-665">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="60e12-666">Сборка 17063</span><span class="sxs-lookup"><span data-stu-id="60e12-666">Build 17063</span></span>
<span data-ttu-id="60e12-667">Общие сведения о сборке Windows 17063 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-667">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="60e12-668">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-668">WSL</span></span>
* <span data-ttu-id="60e12-669">DrvFs поддерживает дополнительные метаданные Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-669">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="60e12-670">Это позволяет задать владельца и режим файлов с помощью chmod или chown, а также создать специальные файлы, такие как FIFO, сокеты UNIX и файлы устройств.</span><span class="sxs-lookup"><span data-stu-id="60e12-670">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="60e12-671">Сейчас эта функция отключена по умолчанию, так как еще является экспериментальной.</span><span class="sxs-lookup"><span data-stu-id="60e12-671">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="60e12-672">**Примечание**.  Исправлена ошибка в формате метаданных, используемом DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-672">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="60e12-673">Хотя метаданные используются в этой сборке в качестве эксперимента, будущие сборки не будут правильно считывать метаданные, созданные этой сборкой.</span><span class="sxs-lookup"><span data-stu-id="60e12-673">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="60e12-674">Возможно, потребуется вручную обновить владельца измененных файлов, а устройства с пользовательским идентификатором устройства потребуется создать заново.</span><span class="sxs-lookup"><span data-stu-id="60e12-674">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="60e12-675">Чтобы включить эту функцию, подключите DrvFs с параметром metadata (чтобы включить эту функцию для существующего подключения, его необходимо сначала отключить):</span><span class="sxs-lookup"><span data-stu-id="60e12-675">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="60e12-676">Разрешения Linux добавляются в файл в качестве дополнительных метаданных; они не влияют на разрешения Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-676">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="60e12-677">Помните, что изменение файла с помощью редактора Windows может привести к удалению метаданных.</span><span class="sxs-lookup"><span data-stu-id="60e12-677">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="60e12-678">В этом случае будут восстановлены разрешения этого файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60e12-678">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="60e12-679">Добавлены параметры подключения к DrvFs для управления файлами без метаданных.</span><span class="sxs-lookup"><span data-stu-id="60e12-679">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="60e12-680">uid: идентификатор пользователя, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="60e12-680">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="60e12-681">gid: идентификатор группы, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="60e12-681">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="60e12-682">umask: восьмеричная маска разрешений, исключаемых для всех файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="60e12-682">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="60e12-683">fmask: восьмеричная маска разрешений, исключаемых для всех обычных файлов.</span><span class="sxs-lookup"><span data-stu-id="60e12-683">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="60e12-684">dmask: восьмеричная маска разрешений, исключаемых для всех каталогов.</span><span class="sxs-lookup"><span data-stu-id="60e12-684">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="60e12-685">Например:</span><span class="sxs-lookup"><span data-stu-id="60e12-685">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="60e12-686">Используйте вместе с параметром metadata, чтобы указать разрешения по умолчанию для файлов без метаданных.</span><span class="sxs-lookup"><span data-stu-id="60e12-686">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="60e12-687">Появилась новая переменная среды, `WSLENV`, позволяющая настроить поток переменных среды между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="60e12-687">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="60e12-688">Например:</span><span class="sxs-lookup"><span data-stu-id="60e12-688">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="60e12-689">`WSLENV` — разделенный двоеточиями список переменных среды, которые могут быть добавлены при запуске процессов WSL из Win32 или при запуске процессов Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-689">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="60e12-690">Каждая переменная может иметь суффикс с косой чертой, за которой следуют флаги для указания способа преобразования.</span><span class="sxs-lookup"><span data-stu-id="60e12-690">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="60e12-691">p: значение — это путь, который должен быть преобразован между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="60e12-691">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="60e12-692">l: значение — это список путей.</span><span class="sxs-lookup"><span data-stu-id="60e12-692">l: The value is a list of paths.</span></span> <span data-ttu-id="60e12-693">В WSL это список, разделенный двоеточиями.</span><span class="sxs-lookup"><span data-stu-id="60e12-693">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="60e12-694">В Win32 это список, разделенный точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="60e12-694">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="60e12-695">u: это значение должно добавляться только при вызове WSL из Win32.</span><span class="sxs-lookup"><span data-stu-id="60e12-695">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="60e12-696">w: это значение должно добавляться только при вызове Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-696">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="60e12-697">Вы можете задать `WSLENV` в bashrc или в пользовательской среде Windows для пользователя.</span><span class="sxs-lookup"><span data-stu-id="60e12-697">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="60e12-698">Подключения DrvFs правильно сохраняют метки времени из tar, cp -p (GH 1939).</span><span class="sxs-lookup"><span data-stu-id="60e12-698">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="60e12-699">Символические ссылки DrvFs сообщают правильный размер (GH 2641).</span><span class="sxs-lookup"><span data-stu-id="60e12-699">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="60e12-700">Операции чтения и записи могут обрабатывать очень большие объемы ввода-вывода (GH 2653).</span><span class="sxs-lookup"><span data-stu-id="60e12-700">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="60e12-701">Функция waitpid работает с идентификаторами групп процессов (GH 2534).</span><span class="sxs-lookup"><span data-stu-id="60e12-701">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="60e12-702">Значительно улучшена производительность mmap для больших резервных регионов. Повышена производительность ghc (GH 1671).</span><span class="sxs-lookup"><span data-stu-id="60e12-702">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="60e12-703">Personality поддерживает READ_IMPLIES_EXEC; реализованы исправления для maxima и clisp (GH 1185).</span><span class="sxs-lookup"><span data-stu-id="60e12-703">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="60e12-704">Mprotect поддерживает PROT_GROWSDOWN; реализованы исправления для clisp (GH 1128).</span><span class="sxs-lookup"><span data-stu-id="60e12-704">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="60e12-705">Устранены сбои страниц в режиме перегрузки; реализованы исправления для sbcl (GH 1128).</span><span class="sxs-lookup"><span data-stu-id="60e12-705">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="60e12-706">Функция clone поддерживает больше сочетаний флагов.</span><span class="sxs-lookup"><span data-stu-id="60e12-706">clone supports more flags combinations</span></span>
* <span data-ttu-id="60e12-707">Поддержка select/epoll для файлов epoll (ранее это считалось холостой командой).</span><span class="sxs-lookup"><span data-stu-id="60e12-707">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="60e12-708">Уведомление ptrace о нереализованных вызовах syscall.</span><span class="sxs-lookup"><span data-stu-id="60e12-708">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="60e12-709">Игнорирование интерфейсов, которые не выполняются, при создании серверов имен resolv.conf [GH 2694].</span><span class="sxs-lookup"><span data-stu-id="60e12-709">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="60e12-710">Перечисление сетевых интерфейсов без физического адреса.</span><span class="sxs-lookup"><span data-stu-id="60e12-710">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="60e12-711">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="60e12-711">[GH 2685]</span></span>
* <span data-ttu-id="60e12-712">Дополнительные исправления ошибок и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-712">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="60e12-713">Инструменты Linux, доступные для разработчиков в Windows</span><span class="sxs-lookup"><span data-stu-id="60e12-713">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="60e12-714">Цепочка инструментов командной строки Windows включает в себя bsdtar (tar) и curl.</span><span class="sxs-lookup"><span data-stu-id="60e12-714">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="60e12-715">Ознакомьтесь с [этим блогом](https://aka.ms/tarcurlwindows), чтобы узнать больше о добавлении этих двух новых инструментов и о том, как они меняют возможности разработки в Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-715">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they're shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="60e12-716">`AF_UNIX` доступен в пакете SDK для программы предварительной оценки Windows (начиная со сборки 17061).</span><span class="sxs-lookup"><span data-stu-id="60e12-716">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="60e12-717">Ознакомьтесь с [этим блогом](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), чтобы узнать больше о `AF_UNIX` и способах его использования разработчиками в Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-717">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="60e12-718">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-718">Console</span></span>
* <span data-ttu-id="60e12-719">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-719">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-720">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-720">LTP Results:</span></span>
<span data-ttu-id="60e12-721">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-721">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="60e12-722">Сборка 17046</span><span class="sxs-lookup"><span data-stu-id="60e12-722">Build 17046</span></span>

<span data-ttu-id="60e12-723">Общие сведения о сборке Windows 17046 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="60e12-723">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="60e12-724">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-724">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-725">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-725">WSL</span></span>
- <span data-ttu-id="60e12-726">Разрешено выполнение процессов без активного терминала.</span><span class="sxs-lookup"><span data-stu-id="60e12-726">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="60e12-727">[GH 709, 1007, 1511, 2252, 2391 и т. д.]</span><span class="sxs-lookup"><span data-stu-id="60e12-727">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="60e12-728">Улучшена поддержка CLONE_VFORK и CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="60e12-728">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="60e12-729">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="60e12-729">[GH 1878, 2615]</span></span>
- <span data-ttu-id="60e12-730">Пропуск драйверов фильтра TDI для сетевых операций WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-730">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="60e12-731">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="60e12-731">[GH 1554]</span></span>
- <span data-ttu-id="60e12-732">DrvFs создает символические ссылки NT при выполнении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="60e12-732">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="60e12-733">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="60e12-733">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="60e12-734">Цель ссылки должна быть относительной, не должна пересекать точки подключения или символические ссылки и должна существовать.</span><span class="sxs-lookup"><span data-stu-id="60e12-734">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="60e12-735">Пользователь должен иметь разрешение SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (обычно для этого требуется запустить wsl.exe с повышенными привилегиями), если режим разработчика не включен.</span><span class="sxs-lookup"><span data-stu-id="60e12-735">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="60e12-736">Во всех остальных случаях DrvFs по-прежнему создает символические ссылки WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-736">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="60e12-737">Разрешено одновременное выполнение экземпляров WSL с повышенными привилегиями и без повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="60e12-737">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="60e12-738">Поддержка /proc/sys/kernel/yama/ptrace_scope.</span><span class="sxs-lookup"><span data-stu-id="60e12-738">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="60e12-739">Добавлена функция wslpath для преобразования путей WSL в пути Windows и наоборот.</span><span class="sxs-lookup"><span data-stu-id="60e12-739">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="60e12-740">[GH 522, 1243, 1834, 2327 и т. д.]</span><span class="sxs-lookup"><span data-stu-id="60e12-740">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with '/' instead of '\\'

      EX: wslpath 'c:\users'
  ```
  #### <a name="console"></a><span data-ttu-id="60e12-741">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-741">Console</span></span>
- <span data-ttu-id="60e12-742">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-742">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-743">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-743">LTP Results:</span></span>
<span data-ttu-id="60e12-744">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-744">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="60e12-745">Сборка 17040</span><span class="sxs-lookup"><span data-stu-id="60e12-745">Build 17040</span></span>

<span data-ttu-id="60e12-746">Общие сведения о сборке Windows 17040 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="60e12-746">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-747">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-747">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-748">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-748">WSL</span></span>
- <span data-ttu-id="60e12-749">Исправления с момента выпуска сборки 17035 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-749">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-750">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-750">Console</span></span>
- <span data-ttu-id="60e12-751">Исправления с момента выпуска сборки 17035 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-751">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-752">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-752">LTP Results:</span></span>
<span data-ttu-id="60e12-753">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-753">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="60e12-754">Сборка 17035</span><span class="sxs-lookup"><span data-stu-id="60e12-754">Build 17035</span></span>

<span data-ttu-id="60e12-755">Общие сведения о сборке Windows 17035 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="60e12-755">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-756">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-756">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-757">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-757">WSL</span></span>
- <span data-ttu-id="60e12-758">Иногда не удавалось получить доступ к файлам в DrvFs с ошибкой EINVAL.</span><span class="sxs-lookup"><span data-stu-id="60e12-758">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="60e12-759">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="60e12-759">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-760">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-760">Console</span></span>
- <span data-ttu-id="60e12-761">Устранена небольшая потеря цветов при вставке или удалении строк в режиме VT.</span><span class="sxs-lookup"><span data-stu-id="60e12-761">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-762">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-762">LTP Results:</span></span>
<span data-ttu-id="60e12-763">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-763">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="60e12-764">Сборка 17025</span><span class="sxs-lookup"><span data-stu-id="60e12-764">Build 17025</span></span>

<span data-ttu-id="60e12-765">Общие сведения о сборке Windows 17025 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="60e12-765">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-766">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-766">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-767">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-767">WSL</span></span>
- <span data-ttu-id="60e12-768">Запуск начальных процессов в новой группе процессов переднего плана [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="60e12-768">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="60e12-769">Исправления доставки SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="60e12-769">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="60e12-770">Создание имени виртуального моста по умолчанию, если оно не указано [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="60e12-770">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="60e12-771">Реализовано /proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="60e12-771">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="60e12-772">Дополнительные исправления взаимодействия с каналом stdout/stderr.</span><span class="sxs-lookup"><span data-stu-id="60e12-772">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="60e12-773">Заглушка системного вызова syncfs.</span><span class="sxs-lookup"><span data-stu-id="60e12-773">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-774">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-774">Console</span></span>
- <span data-ttu-id="60e12-775">Исправление входного преобразования VT для консолей сторонних разработчиков [GH 111].</span><span class="sxs-lookup"><span data-stu-id="60e12-775">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-776">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-776">LTP Results:</span></span>
<span data-ttu-id="60e12-777">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-777">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="60e12-778">Сборка 17017</span><span class="sxs-lookup"><span data-stu-id="60e12-778">Build 17017</span></span>

<span data-ttu-id="60e12-779">Общие сведения о сборке Windows 17017 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="60e12-779">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-780">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-780">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-781">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-781">WSL</span></span>
- <span data-ttu-id="60e12-782">Пропуск пустых заголовков программы ELF [GH 330].</span><span class="sxs-lookup"><span data-stu-id="60e12-782">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="60e12-783">LxssManager разрешено создавать экземпляры WSL для неинтерактивных пользователей (поддержка SSH и запланированных задач) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="60e12-783">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="60e12-784">Поддержка сценариев WSL > Win32 > WSL ("порождение") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="60e12-784">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="60e12-785">Ограниченная поддержка завершения работы консольных приложений, вызванных посредством взаимодействия [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="60e12-785">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="60e12-786">Поддержка параметров подключения для devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="60e12-786">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="60e12-787">Устранена блокировка Ptrace запуска дочерних процессов [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="60e12-787">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="60e12-788">В EPOLLET отсутствовали некоторые события [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="60e12-788">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="60e12-789">PTRACE_GETSIGINFO возвращает больше данных.</span><span class="sxs-lookup"><span data-stu-id="60e12-789">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="60e12-790">Функция getdents с lseek выдавала неправильные результаты.</span><span class="sxs-lookup"><span data-stu-id="60e12-790">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="60e12-791">Устранены некоторые сценарии, в которых взаимодействующее приложение Win32 переставало отвечать на запросы, ожидая входных данных в канале, который больше не содержал данные.</span><span class="sxs-lookup"><span data-stu-id="60e12-791">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="60e12-792">Поддержка O_ASYNC для файлов tty и pty.</span><span class="sxs-lookup"><span data-stu-id="60e12-792">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="60e12-793">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-793">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-794">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-794">Console</span></span>
- <span data-ttu-id="60e12-795">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="60e12-795">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-796">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-796">LTP Results:</span></span>
<span data-ttu-id="60e12-797">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="60e12-797">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="60e12-798">Обновление Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="60e12-798">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="60e12-799">Сборка 16288</span><span class="sxs-lookup"><span data-stu-id="60e12-799">Build 16288</span></span>

<span data-ttu-id="60e12-800">Общие сведения о сборке Windows 16288 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="60e12-800">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-801">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-801">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-802">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-802">WSL</span></span>
- <span data-ttu-id="60e12-803">Правильная инициализация и отображение UID, GID и режима для дескрипторов файлов сокетов [GH 2490].</span><span class="sxs-lookup"><span data-stu-id="60e12-803">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="60e12-804">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-804">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-805">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-805">Console</span></span>
- <span data-ttu-id="60e12-806">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="60e12-806">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-807">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-807">LTP Results:</span></span>
<span data-ttu-id="60e12-808">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-808">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="60e12-809">Сборка 16278</span><span class="sxs-lookup"><span data-stu-id="60e12-809">Build 16278</span></span>

<span data-ttu-id="60e12-810">Общие сведения о сборке Windows 162738 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="60e12-810">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-811">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-811">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-812">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-812">WSL</span></span>
- <span data-ttu-id="60e12-813">Явная отмена сопоставления сопоставленных представлений разделов с файлами при завершении состояния LX MM [GH 2415].</span><span class="sxs-lookup"><span data-stu-id="60e12-813">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="60e12-814">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-814">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-815">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-815">Console</span></span>
- <span data-ttu-id="60e12-816">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="60e12-816">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-817">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-817">LTP Results:</span></span>
<span data-ttu-id="60e12-818">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-818">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="60e12-819">Сборка 16275</span><span class="sxs-lookup"><span data-stu-id="60e12-819">Build 16275</span></span>

<span data-ttu-id="60e12-820">Общие сведения о сборке Windows 162735 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="60e12-820">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-821">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-821">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-822">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-822">WSL</span></span>
- <span data-ttu-id="60e12-823">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-823">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-824">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-824">Console</span></span>
- <span data-ttu-id="60e12-825">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="60e12-825">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-826">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-826">LTP Results:</span></span>
<span data-ttu-id="60e12-827">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-827">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="60e12-828">Сборка 16273</span><span class="sxs-lookup"><span data-stu-id="60e12-828">Build 16273</span></span>

<span data-ttu-id="60e12-829">Общие сведения о сборке Windows 16273 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-829">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-830">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-830">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-831">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-831">WSL</span></span>
- <span data-ttu-id="60e12-832">Исправлена проблема, из-за которой DrvFs иногда сообщал о неправильном типе файла для каталогов [GH 2392].</span><span class="sxs-lookup"><span data-stu-id="60e12-832">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="60e12-833">Разрешено создание сокетов NETLINK_KOBJECT_UEVENT для разблокирования программ, использующих uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637].</span><span class="sxs-lookup"><span data-stu-id="60e12-833">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="60e12-834">Добавлена поддержка неблокирующего подключения [GH 903, 1391, 1584, 1585, 1829, 2290, 2314].</span><span class="sxs-lookup"><span data-stu-id="60e12-834">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="60e12-835">Реализован флаг системного вызова клонирования CLONE_FS [GH 2242].</span><span class="sxs-lookup"><span data-stu-id="60e12-835">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="60e12-836">Устранены проблемы, связанные с неправильной обработкой знаков табуляции или кавычек при взаимодействии с NT [GH 1625, 2164].</span><span class="sxs-lookup"><span data-stu-id="60e12-836">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="60e12-837">Устранена ошибка отказа в доступе при попытке повторного запуска экземпляров WSL [GH 651, 2095].</span><span class="sxs-lookup"><span data-stu-id="60e12-837">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="60e12-838">Реализованы фьютексные операции FUTEX_REQUEUE и FUTEX_CMP_REQUEUE [GH 2242].</span><span class="sxs-lookup"><span data-stu-id="60e12-838">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="60e12-839">Исправлены разрешения для различных файлов SysFs [GH 2214].</span><span class="sxs-lookup"><span data-stu-id="60e12-839">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="60e12-840">Устранена проблема, из-за которой стек Haskell переставал отвечать на запросы во время установки [GH 2290].</span><span class="sxs-lookup"><span data-stu-id="60e12-840">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="60e12-841">Реализованы флаги binfmt_misc "C", "O" и "P" [GH 2103].</span><span class="sxs-lookup"><span data-stu-id="60e12-841">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="60e12-842">Добавлены /proc/sys/kernel, /shmmax, /shmmni и /threads-max [GH 1753].</span><span class="sxs-lookup"><span data-stu-id="60e12-842">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="60e12-843">Добавлена частичная поддержка системного вызова ioprio_set [GH 498].</span><span class="sxs-lookup"><span data-stu-id="60e12-843">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="60e12-844">Реализована заглушка SO_REUSEPORT и добавлена поддержка SO_PASSCRED для сокетов NETLINK [GH 69].</span><span class="sxs-lookup"><span data-stu-id="60e12-844">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="60e12-845">Возвращение разных кодов ошибок из RegisterDistribuiton, если дистрибутив в данный момент устанавливается или удаляется.</span><span class="sxs-lookup"><span data-stu-id="60e12-845">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="60e12-846">Обеспечена отмена регистрации частично установленных дистрибутивов WSL с помощью wslconfig.exe.</span><span class="sxs-lookup"><span data-stu-id="60e12-846">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="60e12-847">Устранена ошибка, из-за которой сокет Python переставал отвечать на запросы при выполнении udp::msg_peek.</span><span class="sxs-lookup"><span data-stu-id="60e12-847">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="60e12-848">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-848">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-849">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-849">Console</span></span>
- <span data-ttu-id="60e12-850">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="60e12-850">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-851">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-851">LTP Results:</span></span>
<span data-ttu-id="60e12-852">Всего тестов: 1904.</span><span class="sxs-lookup"><span data-stu-id="60e12-852">Total Tests: 1904</span></span><br/>
<span data-ttu-id="60e12-853">Всего пропущенных тестов: 209.</span><span class="sxs-lookup"><span data-stu-id="60e12-853">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="60e12-854">Всего сбоев: 229.</span><span class="sxs-lookup"><span data-stu-id="60e12-854">Total Failures: 229</span></span><br/>
[<span data-ttu-id="60e12-855">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-855">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="60e12-856">Сборка 16257</span><span class="sxs-lookup"><span data-stu-id="60e12-856">Build 16257</span></span>

<span data-ttu-id="60e12-857">Общие сведения о сборке Windows 16257 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-857">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-858">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-858">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-859">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-859">WSL</span></span>
- <span data-ttu-id="60e12-860">Реализован системный вызов prlimit64.</span><span class="sxs-lookup"><span data-stu-id="60e12-860">Implement prlimit64 system call</span></span>
- <span data-ttu-id="60e12-861">Добавлена поддержка ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688].</span><span class="sxs-lookup"><span data-stu-id="60e12-861">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="60e12-862">Заглушка MSG_MORE для TCP-сокетов [GH 2351].</span><span class="sxs-lookup"><span data-stu-id="60e12-862">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="60e12-863">Исправлено недопустимое поведение вспомогательного вектора AT_EXECFN [GH 2133].</span><span class="sxs-lookup"><span data-stu-id="60e12-863">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="60e12-864">Исправлено поведение копирования и вставки для консоли и tty и добавлена улучшенная обработка полного буфера [GH 2204, 2131].</span><span class="sxs-lookup"><span data-stu-id="60e12-864">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="60e12-865">Установка AT_SECURE в дополнительном векторе для программ set-user-ID и set-group-ID [GH 2031].</span><span class="sxs-lookup"><span data-stu-id="60e12-865">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="60e12-866">Главная конечная точка псевдотерминала не обрабатывала TIOCPGRP [GH 1063].</span><span class="sxs-lookup"><span data-stu-id="60e12-866">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="60e12-867">Исправлена проблема lseek с перемоткой каталогов в LxFs [GH 2310].</span><span class="sxs-lookup"><span data-stu-id="60e12-867">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="60e12-868">Исправлена блокировка /dev/ptmx после интенсивного использования [GH 1882].</span><span class="sxs-lookup"><span data-stu-id="60e12-868">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="60e12-869">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-869">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-870">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-870">Console</span></span>
- <span data-ttu-id="60e12-871">Исправлено отображение горизонтальных линий и знаков подчеркивания везде [GH 2168].</span><span class="sxs-lookup"><span data-stu-id="60e12-871">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="60e12-872">Исправлено изменение порядка процессов, усложнявшее закрытие NPM [GH 2170].</span><span class="sxs-lookup"><span data-stu-id="60e12-872">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="60e12-873">Добавлена новая цветовая схема: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/.</span><span class="sxs-lookup"><span data-stu-id="60e12-873">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-874">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-874">LTP Results:</span></span>
<span data-ttu-id="60e12-875">Изменения с момента выпуска сборки 16251 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-875">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="60e12-876">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-876">Syscall Support</span></span>
<span data-ttu-id="60e12-877">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-877">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-878">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-878">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="60e12-879">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="60e12-879">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>[<span data-ttu-id="60e12-880">Проблема GitHub 2392: WSL не распознает папки Windows…</span><span class="sxs-lookup"><span data-stu-id="60e12-880">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="60e12-881">В сборке 16257 в WSL возникли проблемы при перечислении файлов и папок Windows с помощью `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="60e12-881">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="60e12-882">Эта проблема устранена, и исправление будет выпущено в сборке для программы предварительной оценки в течение недели после 14 августа 2017 года.</span><span class="sxs-lookup"><span data-stu-id="60e12-882">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="60e12-883">Сборка 16251</span><span class="sxs-lookup"><span data-stu-id="60e12-883">Build 16251</span></span>

<span data-ttu-id="60e12-884">Общие сведения о сборке Windows 16251 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-884">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-885">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-885">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-886">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-886">WSL</span></span>
- <span data-ttu-id="60e12-887">Удален тег бета-версии из дополнительного компонента WSL. Дополнительные сведения см. в этой [записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).</span><span class="sxs-lookup"><span data-stu-id="60e12-887">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="60e12-888">Правильная инициализация сохраненных заданных UID и GID для двоичных файлов set-user-ID и set-group-ID при выполнении [GH 962, 1415, 2072].</span><span class="sxs-lookup"><span data-stu-id="60e12-888">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="60e12-889">Добавлена поддержка PTRACE_O_TRACEEXIT в ptrace [GH 555].</span><span class="sxs-lookup"><span data-stu-id="60e12-889">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="60e12-890">В ptrace добавлена поддержка PTRACE_GETFPREGS и PTRACE_GETREGSET с NT_FPREGSET [GH 555].</span><span class="sxs-lookup"><span data-stu-id="60e12-890">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="60e12-891">Исправлена проблема, из-за которой выполнение ptrace останавливалось на пропущенных сигналах.</span><span class="sxs-lookup"><span data-stu-id="60e12-891">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="60e12-892">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-892">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-893">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-893">Console</span></span>
- <span data-ttu-id="60e12-894">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="60e12-894">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-895">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-895">LTP Results:</span></span>
<span data-ttu-id="60e12-896">Число пройденных тестов: 768</span><span class="sxs-lookup"><span data-stu-id="60e12-896">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="60e12-897">Число непройденных тестов: 244.</span><span class="sxs-lookup"><span data-stu-id="60e12-897">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="60e12-898">Число пропущенных тестов: 96</span><span class="sxs-lookup"><span data-stu-id="60e12-898">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="60e12-899">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-899">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="60e12-900">Сборка 16241</span><span class="sxs-lookup"><span data-stu-id="60e12-900">Build 16241</span></span>

<span data-ttu-id="60e12-901">Общие сведения о сборке Windows 16241 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-901">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-902">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-902">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="60e12-903">WSL</span><span class="sxs-lookup"><span data-stu-id="60e12-903">WSL</span></span>
- <span data-ttu-id="60e12-904">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-904">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="60e12-905">Консоль</span><span class="sxs-lookup"><span data-stu-id="60e12-905">Console</span></span>
- <span data-ttu-id="60e12-906">Исправлено вывода неправильного знака для пересечения линий DEC, о котором первоначально было сообщено [здесь](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/).</span><span class="sxs-lookup"><span data-stu-id="60e12-906">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="60e12-907">Исправлено отсутствие вывода текста в кодовой странице 65001 (UTF8).</span><span class="sxs-lookup"><span data-stu-id="60e12-907">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="60e12-908">Изменения, внесенные в значения RGB одного цвета, не переносятся в другие части палитры при изменении выбора.</span><span class="sxs-lookup"><span data-stu-id="60e12-908">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="60e12-909">Это заметно облегчит использование страницы свойств консоли.</span><span class="sxs-lookup"><span data-stu-id="60e12-909">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="60e12-910">Нажатие клавиш Ctrl+S не работало правильно.</span><span class="sxs-lookup"><span data-stu-id="60e12-910">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="60e12-911">Un-Bold и -Dim полностью отсутствуют в escape-кодах ANSI [GH 2174].</span><span class="sxs-lookup"><span data-stu-id="60e12-911">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="60e12-912">Консоль неправильно поддерживала цветовые темы Vim [GH 1706].</span><span class="sxs-lookup"><span data-stu-id="60e12-912">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="60e12-913">Не удавалось вставить определенные знаки [GH 2149].</span><span class="sxs-lookup"><span data-stu-id="60e12-913">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="60e12-914">Изменение размера расплавления приводило к необычному изменению размера окна Bash, когда что-то было введено в строке редактирования или командной строке [GH ConEmu 1123].</span><span class="sxs-lookup"><span data-stu-id="60e12-914">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="60e12-915">Нажатие клавиш CTRL+L не очищало экран [GH 1978].</span><span class="sxs-lookup"><span data-stu-id="60e12-915">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="60e12-916">Устранена ошибка отрисовки консоли при отображении VT в HDPI [GH 1907].</span><span class="sxs-lookup"><span data-stu-id="60e12-916">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="60e12-917">Японские знаки выглядели необычно со знаком Юникода U+30FB [GH 2146].</span><span class="sxs-lookup"><span data-stu-id="60e12-917">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="60e12-918">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-918">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="60e12-919">Сборка 16237</span><span class="sxs-lookup"><span data-stu-id="60e12-919">Build 16237</span></span>

<span data-ttu-id="60e12-920">Общие сведения о сборке Windows 16237 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-920">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-921">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-921">Fixed</span></span>
- <span data-ttu-id="60e12-922">Использование атрибутов по умолчанию для файлов без EA в lxfs (root, root, 0000).</span><span class="sxs-lookup"><span data-stu-id="60e12-922">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="60e12-923">Добавлена поддержка дистрибутивов, использующих расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="60e12-923">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="60e12-924">Исправлено заполнение записей, возвращаемых getdents и getdents64.</span><span class="sxs-lookup"><span data-stu-id="60e12-924">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="60e12-925">Исправлена проверка разрешений для системного вызова shmctl SHM_STAT [GH 2068].</span><span class="sxs-lookup"><span data-stu-id="60e12-925">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="60e12-926">Исправлено неправильное начальное состояние epoll для tty [GH 2231].</span><span class="sxs-lookup"><span data-stu-id="60e12-926">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="60e12-927">Устранена проблема в DrvFs, из-за которой команда readdir не возвращала все записи [GH 2077].</span><span class="sxs-lookup"><span data-stu-id="60e12-927">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="60e12-928">Исправлена операция LxFs readdir с несвязанными файлами [GH 2077].</span><span class="sxs-lookup"><span data-stu-id="60e12-928">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="60e12-929">Допускается повторное открытие несвязанных файлов DrvFs с помощью procfs.</span><span class="sxs-lookup"><span data-stu-id="60e12-929">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="60e12-930">Добавлено переопределение глобального раздела реестра для отключения функций WSL (взаимодействие и монтирование дисков).</span><span class="sxs-lookup"><span data-stu-id="60e12-930">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="60e12-931">Исправлено неправильное число блокировок в "stat" для DrvFs (и LxFs) [GH 1894].</span><span class="sxs-lookup"><span data-stu-id="60e12-931">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="60e12-932">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-932">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="60e12-933">Сборка 16232</span><span class="sxs-lookup"><span data-stu-id="60e12-933">Build 16232</span></span>

<span data-ttu-id="60e12-934">Общие сведения о сборке Windows 16232 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-934">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-935">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-935">Fixed</span></span>
- <span data-ttu-id="60e12-936">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-936">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="60e12-937">Сборка 16226</span><span class="sxs-lookup"><span data-stu-id="60e12-937">Build 16226</span></span>

<span data-ttu-id="60e12-938">Общие сведения о сборке Windows 16226 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-938">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-939">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-939">Fixed</span></span>
- <span data-ttu-id="60e12-940">Поддержка системных вызовов, связанных с xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="60e12-940">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="60e12-941">Поддержка security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="60e12-941">security.capablity xattr support.</span></span>
- <span data-ttu-id="60e12-942">Улучшена совместимость с некоторыми файловыми системами и фильтрами, включая серверы SMB сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="60e12-942">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="60e12-943">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="60e12-943">[GH #1952]</span></span>
- <span data-ttu-id="60e12-944">Улучшена поддержка заполнителей OneDrive, заполнителей GVFS и сжатых файлов Compact OS.</span><span class="sxs-lookup"><span data-stu-id="60e12-944">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="60e12-945">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-945">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="60e12-946">Сборка 16215</span><span class="sxs-lookup"><span data-stu-id="60e12-946">Build 16215</span></span>

<span data-ttu-id="60e12-947">Общие сведения о сборке Windows 16215 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-947">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-948">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-948">Fixed</span></span>
- <span data-ttu-id="60e12-949">Для WSL больше не требуется режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="60e12-949">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="60e12-950">Поддержка соединений каталогов в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-950">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="60e12-951">Обработка удаления пакетов appx дистрибутивов WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-951">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="60e12-952">Обновление procfs для отображения частных и общих сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="60e12-952">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="60e12-953">В wslconfig.exe добавлена возможность очистки частично установленных или частично удаленных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="60e12-953">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="60e12-954">Добавлена поддержка IP_MTU_DISCOVER для TCP-сокетов.</span><span class="sxs-lookup"><span data-stu-id="60e12-954">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="60e12-955">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="60e12-955">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="60e12-956">Вывод семейства протоколов для маршрутов к AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="60e12-956">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="60e12-957">Улучшения для последовательных устройств [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="60e12-957">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="60e12-958">Сборка 16199</span><span class="sxs-lookup"><span data-stu-id="60e12-958">Build 16199</span></span>

<span data-ttu-id="60e12-959">Общие сведения о сборке Windows 16199 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-959">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-960">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-960">Fixed</span></span>
- <span data-ttu-id="60e12-961">В этих выпусках нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-961">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="60e12-962">Сборка 16193</span><span class="sxs-lookup"><span data-stu-id="60e12-962">Build 16193</span></span>

<span data-ttu-id="60e12-963">Общие сведения о сборке Windows 16193 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-963">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-964">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-964">Fixed</span></span>
- <span data-ttu-id="60e12-965">Исправлено состояние состязания между отправкой SIGCONT и завершением группы потоков [GH 1973].</span><span class="sxs-lookup"><span data-stu-id="60e12-965">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="60e12-966">Устройства tty и pty изменены для передачи FILE_DEVICE_NAMED_PIPE вместо FILE_DEVICE_CONSOLE [GH 1840].</span><span class="sxs-lookup"><span data-stu-id="60e12-966">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="60e12-967">Исправление SSH для IP_OPTIONS.</span><span class="sxs-lookup"><span data-stu-id="60e12-967">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="60e12-968">Подключение DrvFs перемещено в управляющую программу инициализации [GH 1862, 1968, 1767, 1933].</span><span class="sxs-lookup"><span data-stu-id="60e12-968">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="60e12-969">Добавлена поддержка в DrvFs приведенных ниже символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="60e12-969">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="60e12-970">Сборка 16184</span><span class="sxs-lookup"><span data-stu-id="60e12-970">Build 16184</span></span>

<span data-ttu-id="60e12-971">Общие сведения о сборке Windows 16184 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-971">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-972">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-972">Fixed</span></span>
- <span data-ttu-id="60e12-973">Удалена задача обслуживания пакета apt (lxrun.exe /update).</span><span class="sxs-lookup"><span data-stu-id="60e12-973">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="60e12-974">Исправлено отсутствие выходных данных из процессов Windows в Node.js [GH 1840].</span><span class="sxs-lookup"><span data-stu-id="60e12-974">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="60e12-975">Смягчены требования к соответствию в lxcore [GH 1794].</span><span class="sxs-lookup"><span data-stu-id="60e12-975">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="60e12-976">Исправлена обработка флага AT_EMPTY_PATH в ряде системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="60e12-976">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="60e12-977">Исправлена проблема, из-за которой удаление файлов DrvFs с открытыми дескрипторами приводило к неопределенному поведению файла [GH 544, 966, 1357, 1535, 1615].</span><span class="sxs-lookup"><span data-stu-id="60e12-977">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="60e12-978">Теперь /etc/hosts будет наследовать записи из файла hosts Windows (%windir%\System32\Drivers\Etc\hosts) [GH 1495].</span><span class="sxs-lookup"><span data-stu-id="60e12-978">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="60e12-979">Сборка 16179</span><span class="sxs-lookup"><span data-stu-id="60e12-979">Build 16179</span></span>

<span data-ttu-id="60e12-980">Общие сведения о сборке Windows 16179 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-980">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-981">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-981">Fixed</span></span>
- <span data-ttu-id="60e12-982">На этой неделе изменения в WSL отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-982">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="60e12-983">Сборка 16176</span><span class="sxs-lookup"><span data-stu-id="60e12-983">Build 16176</span></span>

<span data-ttu-id="60e12-984">Общие сведения о сборке Windows 16176 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-984">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-985">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-985">Fixed</span></span>

- <span data-ttu-id="60e12-986">[Включена поддержка последовательных устройств](/archive/blogs/wsl/serial-support-on-the-windows-subsystem-for-linux).</span><span class="sxs-lookup"><span data-stu-id="60e12-986">[Enabled serial support](/archive/blogs/wsl/serial-support-on-the-windows-subsystem-for-linux)</span></span>
- <span data-ttu-id="60e12-987">Добавлен параметр IP-сокета IP_OPTIONS [GH 1116].</span><span class="sxs-lookup"><span data-stu-id="60e12-987">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="60e12-988">Реализована функция pwritev (при передаче файла в nginx/PHP-FPM) [GH 1506].</span><span class="sxs-lookup"><span data-stu-id="60e12-988">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="60e12-989">Добавлены параметры IP-сокета IP_MULTICAST_IF и IPV6_MULTICAST_IF [GH 990].</span><span class="sxs-lookup"><span data-stu-id="60e12-989">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="60e12-990">Поддержка параметров сокета IP_MULTICAST_LOOP и IPV6_MULTICAST_LOOP [GH 1678].</span><span class="sxs-lookup"><span data-stu-id="60e12-990">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="60e12-991">Добавлен параметр сокета IP(V6)_MTU для приложений node, traceroute, dig, nslookup, host.</span><span class="sxs-lookup"><span data-stu-id="60e12-991">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="60e12-992">Добавлен параметр IP-сокета IPV6_UNICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="60e12-992">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- <span data-ttu-id="60e12-993">[Улучшения файловой системы](/archive/blogs/wsl/file-system-improvements-to-the-windows-subsystem-for-linux).</span><span class="sxs-lookup"><span data-stu-id="60e12-993">[Filesystem Improvements](/archive/blogs/wsl/file-system-improvements-to-the-windows-subsystem-for-linux)</span></span>
    * <span data-ttu-id="60e12-994">Разрешено подключение путей UNC.</span><span class="sxs-lookup"><span data-stu-id="60e12-994">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="60e12-995">Включена поддержка CDFS в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-995">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="60e12-996">Правильная обработка разрешений для сетевых файловых систем в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-996">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="60e12-997">Добавлена поддержка удаленных дисков в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-997">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="60e12-998">Включена поддержка файловой системы FAT в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-998">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="60e12-999">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-999">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1000">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1000">LTP Results</span></span>
<span data-ttu-id="60e12-1001">Изменения с момента выпуска сборки 15042 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-1001">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="60e12-1002">Сборка 16170</span><span class="sxs-lookup"><span data-stu-id="60e12-1002">Build 16170</span></span>

<span data-ttu-id="60e12-1003">Общие сведения о сборке Windows 16170 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1003">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="60e12-1004">Мы опубликовали новую[запись блога](/archive/blogs/wsl/testing-the-windows-subsystem-for-linux), в которой обсуждаем наши усилия по тестированию WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1004">We released a new [blog post](/archive/blogs/wsl/testing-the-windows-subsystem-for-linux) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="60e12-1005">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1005">Fixed</span></span>

- <span data-ttu-id="60e12-1006">Поддержка параметров сокета IP_ADD_MEMBERSHIP и IPV6_ADD_MEMBERSHIP [GH 1678].</span><span class="sxs-lookup"><span data-stu-id="60e12-1006">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="60e12-1007">Добавлена поддержка PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="60e12-1007">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="60e12-1008">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="60e12-1008">[GH 1692]</span></span>
- <span data-ttu-id="60e12-1009">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1009">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1010">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1010">LTP Results</span></span>
<span data-ttu-id="60e12-1011">Изменения с момента выпуска сборки 15042 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60e12-1011">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="60e12-1012">Сборка 15046 для Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="60e12-1012">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="60e12-1013">В обновление Creators Update для Windows 10 больше не планируется добавлять какие-либо исправления или функции WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1013">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="60e12-1014">Публикация заметок о выпуске WSL будет возобновлена в ближайшие недели, чтобы охватить дополнения, запланированные в следующих основных версиях в Центре обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1014">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="60e12-1015">Общие сведения о сборке Windows 15046 и будущих выпусках для программы предварительной оценки доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1015">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="60e12-1016">Сборка 15042</span><span class="sxs-lookup"><span data-stu-id="60e12-1016">Build 15042</span></span>

<span data-ttu-id="60e12-1017">Общие сведения о сборке Windows 15042 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1017">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1018">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1018">Fixed</span></span>

- <span data-ttu-id="60e12-1019">Устранена взаимоблокировка при удалении пути, завершающегося "..".</span><span class="sxs-lookup"><span data-stu-id="60e12-1019">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="60e12-1020">Устранена проблема, из-за которой функция FIONBIO не возвращала 0 при успешном выполнении [GH 1683].</span><span class="sxs-lookup"><span data-stu-id="60e12-1020">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="60e12-1021">Устранена проблема с чтением сокетов датаграмм INET нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="60e12-1021">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="60e12-1022">Устранена возможная взаимоблокировка из-за состояния состязания при поиске DrvFs в DrvFs [GH 1675].</span><span class="sxs-lookup"><span data-stu-id="60e12-1022">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="60e12-1023">Расширена поддержка вспомогательных данных сокетов UNIX, SCM_CREDENTIALS и SCM_RIGHTS [GH 514, 613, 1326].</span><span class="sxs-lookup"><span data-stu-id="60e12-1023">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="60e12-1024">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1024">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1025">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1025">LTP Results:</span></span>
<span data-ttu-id="60e12-1026">Число пройденных тестов: 737.</span><span class="sxs-lookup"><span data-stu-id="60e12-1026">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="60e12-1027">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="60e12-1027">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="60e12-1028">Сборка 15031</span><span class="sxs-lookup"><span data-stu-id="60e12-1028">Build 15031</span></span>

<span data-ttu-id="60e12-1029">Общие сведения о сборке Windows 15031 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1029">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1030">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1030">Fixed</span></span>

- <span data-ttu-id="60e12-1031">Исправлена ошибка, из-за которой поведение time(2) иногда было неправильным.</span><span class="sxs-lookup"><span data-stu-id="60e12-1031">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="60e12-1032">Исправлена проблема, из-за которой системный вызов \*SIGPROCMASK мог повредить маску сигнала.</span><span class="sxs-lookup"><span data-stu-id="60e12-1032">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="60e12-1033">Теперь в уведомлении о создании процесса WSL возвращается полная длина командной строки.</span><span class="sxs-lookup"><span data-stu-id="60e12-1033">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="60e12-1034">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="60e12-1034">[GH 1632]</span></span>
- <span data-ttu-id="60e12-1035">Теперь WSL сообщает о выходе из потока посредством ptrace, если GDB перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="60e12-1035">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="60e12-1036">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="60e12-1036">[GH 1196]</span></span>
- <span data-ttu-id="60e12-1037">Исправлена ошибка, из-за которой устройства pty переставали отвечать на запросы после интенсивного ввода-вывода tmux.</span><span class="sxs-lookup"><span data-stu-id="60e12-1037">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="60e12-1038">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="60e12-1038">[GH 1358]</span></span>
- <span data-ttu-id="60e12-1039">Исправлена проверка времени ожидания во многих системных вызовах (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create).</span><span class="sxs-lookup"><span data-stu-id="60e12-1039">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="60e12-1040">Добавлена поддержка eventfd EFD_SEMAPHORE [GH 452].</span><span class="sxs-lookup"><span data-stu-id="60e12-1040">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="60e12-1041">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1041">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1042">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1042">LTP Results:</span></span>
<span data-ttu-id="60e12-1043">Число пройденных тестов: 737.</span><span class="sxs-lookup"><span data-stu-id="60e12-1043">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="60e12-1044">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="60e12-1044">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="60e12-1045">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1045">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="60e12-1046">Сборка 15025</span><span class="sxs-lookup"><span data-stu-id="60e12-1046">Build 15025</span></span>

<span data-ttu-id="60e12-1047">Общие сведения о сборке Windows 15025 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1047">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1048">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1048">Fixed</span></span>

- <span data-ttu-id="60e12-1049">Исправлена ошибка, которая нарушала работу grep 2.27 [GH 1578].</span><span class="sxs-lookup"><span data-stu-id="60e12-1049">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="60e12-1050">Реализован флаг EFD_SEMAPHORE для системного вызова eventfd2 [GH 452].</span><span class="sxs-lookup"><span data-stu-id="60e12-1050">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="60e12-1051">Реализован файл /proc/[pid]/net/ipv6_route [GH 1608].</span><span class="sxs-lookup"><span data-stu-id="60e12-1051">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="60e12-1052">Поддержка управляемого сигналами ввода-вывода для сокетов потоков UNIX [GH 393, 68].</span><span class="sxs-lookup"><span data-stu-id="60e12-1052">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="60e12-1053">Поддержка F_GETPIPE_SZ и F_SETPIPE_SZ [GH 1012].</span><span class="sxs-lookup"><span data-stu-id="60e12-1053">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="60e12-1054">Реализация системного вызова recvmmsg() [GH 1531].</span><span class="sxs-lookup"><span data-stu-id="60e12-1054">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="60e12-1055">Исправлена ошибка, из-за которой функция epoll_wait() не ожидала выполнения [GH 1609].</span><span class="sxs-lookup"><span data-stu-id="60e12-1055">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="60e12-1056">Реализация /proc/version_signature.</span><span class="sxs-lookup"><span data-stu-id="60e12-1056">Implement /proc/version_signature</span></span>
- <span data-ttu-id="60e12-1057">Теперь системный вызов Tee возвращает ошибку, если оба дескриптора файла ссылаются на один и тот же канал.</span><span class="sxs-lookup"><span data-stu-id="60e12-1057">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="60e12-1058">Реализовано правильное поведение SO_PEERCRED для сокетов UNIX.</span><span class="sxs-lookup"><span data-stu-id="60e12-1058">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="60e12-1059">Исправлена недопустимая обработка параметров системного вызова tkill.</span><span class="sxs-lookup"><span data-stu-id="60e12-1059">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="60e12-1060">Внесены изменения для увеличения производительности DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-1060">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="60e12-1061">Незначительное исправление блокировки ввода-вывода Ruby.</span><span class="sxs-lookup"><span data-stu-id="60e12-1061">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="60e12-1062">Исправлена проблема, из-за которой функция recvmsg() возвращала EINVAL для флага MSG_DONTWAIT для сокетов INET [GH 1296].</span><span class="sxs-lookup"><span data-stu-id="60e12-1062">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="60e12-1063">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1063">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1064">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1064">LTP Results:</span></span>
<span data-ttu-id="60e12-1065">Число пройденных тестов: 732.</span><span class="sxs-lookup"><span data-stu-id="60e12-1065">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="60e12-1066">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="60e12-1066">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="60e12-1067">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1067">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="60e12-1068">Сборка 15019</span><span class="sxs-lookup"><span data-stu-id="60e12-1068">Build 15019</span></span>

<span data-ttu-id="60e12-1069">Общие сведения о сборке Windows 15019 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1069">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1070">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1070">Fixed</span></span>

- <span data-ttu-id="60e12-1071">Исправлена ошибка, из-за которой отображались неправильные данные об использовании ЦП в procfs для таких инструментов, как htop [GH 823, 945, 971].</span><span class="sxs-lookup"><span data-stu-id="60e12-1071">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="60e12-1072">Теперь при вызове Open() с O_TRUNC для существующего файла inotify теперь создает IN_MODIFY до IN_OPEN.</span><span class="sxs-lookup"><span data-stu-id="60e12-1072">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="60e12-1073">Исправление getsockopt SO_ERROR в сокетах UNIX для включения возможностей postgress [GH 61, 1354].</span><span class="sxs-lookup"><span data-stu-id="60e12-1073">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="60e12-1074">Реализация /proc/sys/net/core/somaxconn для языка GO.</span><span class="sxs-lookup"><span data-stu-id="60e12-1074">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="60e12-1075">Теперь фоновая задача обновления пакета apt-get запускается из представления в скрытом режиме.</span><span class="sxs-lookup"><span data-stu-id="60e12-1075">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="60e12-1076">Очищена область для IPv6-адреса localhost (сбой (Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="60e12-1076">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="60e12-1077">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1077">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1078">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1078">LTP Results:</span></span>
<span data-ttu-id="60e12-1079">Число пройденных тестов: 714.</span><span class="sxs-lookup"><span data-stu-id="60e12-1079">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="60e12-1080">Число непройденных тестов (неудачных, пропущенных и т. д.): 249.</span><span class="sxs-lookup"><span data-stu-id="60e12-1080">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="60e12-1081">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1081">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="60e12-1082">Сборка 15014</span><span class="sxs-lookup"><span data-stu-id="60e12-1082">Build 15014</span></span>

<span data-ttu-id="60e12-1083">Общие сведения о сборке Windows 15014 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="60e12-1083">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1084">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1084">Fixed</span></span>

- <span data-ttu-id="60e12-1085">Нажатие клавиш CTRL+C теперь работает ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="60e12-1085">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="60e12-1086">Теперь htop и ps auxw показывают правильные данные об использовании ресурсов (GH 516).</span><span class="sxs-lookup"><span data-stu-id="60e12-1086">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="60e12-1087">Простое преобразование исключений NT в сигналы.</span><span class="sxs-lookup"><span data-stu-id="60e12-1087">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="60e12-1088">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="60e12-1088">(GH #513)</span></span>
- <span data-ttu-id="60e12-1089">Теперь при нехватке пространства fallocate завершается ошибкой ENOSPC вместо EINVAL (GH 1571).</span><span class="sxs-lookup"><span data-stu-id="60e12-1089">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="60e12-1090">Добавлен /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="60e12-1090">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="60e12-1091">Реализованы системные вызовы semop и semtimedop.</span><span class="sxs-lookup"><span data-stu-id="60e12-1091">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="60e12-1092">Устранены ошибки nslookup, связанные с параметрами сокета IP_RECVTOS и IPV6_RECVTCLASS (GH 69).</span><span class="sxs-lookup"><span data-stu-id="60e12-1092">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="60e12-1093">Поддержка параметров сокета IP_RECVTTL и IPV6_RECVHOPLIMIT.</span><span class="sxs-lookup"><span data-stu-id="60e12-1093">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="60e12-1094">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1094">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1095">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1095">LTP Results:</span></span>
<span data-ttu-id="60e12-1096">Число пройденных тестов: 709.</span><span class="sxs-lookup"><span data-stu-id="60e12-1096">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="60e12-1097">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="60e12-1097">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="60e12-1098">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1098">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="60e12-1099">Сводка по системным вызовам</span><span class="sxs-lookup"><span data-stu-id="60e12-1099">Syscall Summary</span></span>
<span data-ttu-id="60e12-1100">Всего системных вызовов: 384</span><span class="sxs-lookup"><span data-stu-id="60e12-1100">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="60e12-1101">Всего реализовано: 235.</span><span class="sxs-lookup"><span data-stu-id="60e12-1101">Total Implemented: 235</span></span> </br>
<span data-ttu-id="60e12-1102">Всего заглушено: 22</span><span class="sxs-lookup"><span data-stu-id="60e12-1102">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="60e12-1103">Всего не реализовано: 127</span><span class="sxs-lookup"><span data-stu-id="60e12-1103">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="60e12-1104">Подробная разбивка</span><span class="sxs-lookup"><span data-stu-id="60e12-1104">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="60e12-1105">Сборка 15007</span><span class="sxs-lookup"><span data-stu-id="60e12-1105">Build 15007</span></span>

<span data-ttu-id="60e12-1106">Общие сведения о сборке Windows 15007 доступны в [блоге о Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="60e12-1106">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="60e12-1107">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="60e12-1107">Known Issue</span></span>

- <span data-ttu-id="60e12-1108">Существует известная ошибка, из-за которой консоль не распознает некоторые клавиши CTRL+<key>.</span><span class="sxs-lookup"><span data-stu-id="60e12-1108">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="60e12-1109">Например, это может быть сочетание CTRL+C, которое будет функционировать как обычное нажатие клавиши C.</span><span class="sxs-lookup"><span data-stu-id="60e12-1109">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="60e12-1110">Возможное решение. Сопоставьте альтернативную клавишу с клавишами CTRL+C.</span><span class="sxs-lookup"><span data-stu-id="60e12-1110">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="60e12-1111">Например, чтобы сопоставить клавиши CTRL+K с CTRL+C, выполните следующее: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="60e12-1111">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="60e12-1112">Это сопоставление действует в пределах терминала и должно выполняться *при каждом* запуске Bash.</span><span class="sxs-lookup"><span data-stu-id="60e12-1112">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="60e12-1113">Пользователи могут изучить этот параметр, чтобы включить его в `.bashrc`.</span><span class="sxs-lookup"><span data-stu-id="60e12-1113">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="60e12-1114">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1114">Fixed</span></span>

- <span data-ttu-id="60e12-1115">Исправлена ошибка, из-за которой подсистема WSL потребляла 100 % ресурсов ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="60e12-1115">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="60e12-1116">Теперь поддерживаются параметры сокета IP_PKTINFO и IPV6_RECVPKTINFO.</span><span class="sxs-lookup"><span data-stu-id="60e12-1116">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="60e12-1117">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="60e12-1117">(GH #851, 987)</span></span>
- <span data-ttu-id="60e12-1118">Усечение физического адреса сетевого интерфейса до 16 байтов в lxcore (GH #1452, 1414, 1343, 468, 308).</span><span class="sxs-lookup"><span data-stu-id="60e12-1118">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="60e12-1119">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1119">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1120">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1120">LTP Results:</span></span>
<span data-ttu-id="60e12-1121">Число пройденных тестов: 709.</span><span class="sxs-lookup"><span data-stu-id="60e12-1121">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="60e12-1122">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="60e12-1122">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="60e12-1123">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1123">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="60e12-1124">Сборка 15002</span><span class="sxs-lookup"><span data-stu-id="60e12-1124">Build 15002</span></span>

<span data-ttu-id="60e12-1125">Общие сведения о сборке Windows 15002 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1125">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="60e12-1126">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="60e12-1126">Known Issue</span></span>

<span data-ttu-id="60e12-1127">Две известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="60e12-1127">Two known issues:</span></span>
- <span data-ttu-id="60e12-1128">Существует известная ошибка, из-за которой консоль не распознает некоторые клавиши CTRL+<key>.</span><span class="sxs-lookup"><span data-stu-id="60e12-1128">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="60e12-1129">Например, это может быть сочетание CTRL+C, которое будет функционировать как обычное нажатие клавиши C.</span><span class="sxs-lookup"><span data-stu-id="60e12-1129">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="60e12-1130">Возможное решение. Сопоставьте альтернативную клавишу с клавишами CTRL+C.</span><span class="sxs-lookup"><span data-stu-id="60e12-1130">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="60e12-1131">Например, чтобы сопоставить клавиши CTRL+K с CTRL+C, выполните следующее: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="60e12-1131">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="60e12-1132">Это сопоставление действует в пределах терминала и должно выполняться *при каждом* запуске Bash.</span><span class="sxs-lookup"><span data-stu-id="60e12-1132">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="60e12-1133">Пользователи могут изучить этот параметр, чтобы включить его в `.bashrc`.</span><span class="sxs-lookup"><span data-stu-id="60e12-1133">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="60e12-1134">Во время выполнения WSL системный поток потребляет 100 % ресурсов ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="60e12-1134">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="60e12-1135">Первопричина устранена и исправлена внутри компонента.</span><span class="sxs-lookup"><span data-stu-id="60e12-1135">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="60e12-1136">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1136">Fixed</span></span>

- <span data-ttu-id="60e12-1137">Все сеансы Bash теперь должны создаваться на одном уровне разрешений.</span><span class="sxs-lookup"><span data-stu-id="60e12-1137">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="60e12-1138">Попытка запустить сеанс на другом уровне будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="60e12-1138">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="60e12-1139">Это означает, что консоль администратора и консоль пользователя, не являющегося администратором, не могут работать одновременно.</span><span class="sxs-lookup"><span data-stu-id="60e12-1139">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="60e12-1140">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="60e12-1140">(GH #626)</span></span>
<br/>
- <span data-ttu-id="60e12-1141">Реализованы следующие сообщения NETLINK_ROUTE (требуются права администратора Windows):</span><span class="sxs-lookup"><span data-stu-id="60e12-1141">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="60e12-1142">RTM_NEWADDR (поддерживает `ip addr add`);</span><span class="sxs-lookup"><span data-stu-id="60e12-1142">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="60e12-1143">RTM_NEWROUTE (поддерживает `ip route add`);</span><span class="sxs-lookup"><span data-stu-id="60e12-1143">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="60e12-1144">RTM_DELADDR (поддерживает `ip addr del`);</span><span class="sxs-lookup"><span data-stu-id="60e12-1144">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="60e12-1145">RTM_DELROUTE (поддерживает `ip route del`).</span><span class="sxs-lookup"><span data-stu-id="60e12-1145">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="60e12-1146">Проверка запланированных задач для пакетов, которые необходимо обновить, больше не будет выполняться при лимитном подключении (GH 1371).</span><span class="sxs-lookup"><span data-stu-id="60e12-1146">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="60e12-1147">Исправлена ошибка, из-за которой канал переставал отвечать на запросы, например bash -c "ls -alR /" | bash -c "cat" (GH 1214).</span><span class="sxs-lookup"><span data-stu-id="60e12-1147">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="60e12-1148">Реализован параметр сокета TCP_KEEPCNT (GH 843).</span><span class="sxs-lookup"><span data-stu-id="60e12-1148">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="60e12-1149">Реализован параметр сокета INET IP_MTU_DISCOVER (GH 720, 717, 170, 69).</span><span class="sxs-lookup"><span data-stu-id="60e12-1149">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="60e12-1150">Удалены устаревшие функции для запуска двоичных файлов NT из init с помощью поиска по пути NT.</span><span class="sxs-lookup"><span data-stu-id="60e12-1150">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="60e12-1151">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="60e12-1151">(GH #1325)</span></span>
- <span data-ttu-id="60e12-1152">Исправлен режим /dev/kmsg для разрешения группового и другого доступа на чтение (0644) (GH 1321).</span><span class="sxs-lookup"><span data-stu-id="60e12-1152">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="60e12-1153">Реализован файл /proc/sys/kernel/random/uuid [GH 1092].</span><span class="sxs-lookup"><span data-stu-id="60e12-1153">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="60e12-1154">Исправлена ошибка, из-за которой время начала процесса отображалось как 2432 год (GH 974).</span><span class="sxs-lookup"><span data-stu-id="60e12-1154">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="60e12-1155">Переменная среды TERM по умолчанию заменена xterm-256color (GH 1446).</span><span class="sxs-lookup"><span data-stu-id="60e12-1155">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="60e12-1156">Изменен способ вычисления фиксации процесса во время ветвления процесса.</span><span class="sxs-lookup"><span data-stu-id="60e12-1156">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="60e12-1157">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="60e12-1157">(GH #1286)</span></span>
- <span data-ttu-id="60e12-1158">Реализован файл /proc/sys/VM/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="60e12-1158">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="60e12-1159">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="60e12-1159">(GH #1286)</span></span>
- <span data-ttu-id="60e12-1160">Реализован файл /proc/net/route (GH 69).</span><span class="sxs-lookup"><span data-stu-id="60e12-1160">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="60e12-1161">Исправлена ошибка, из-за которой имя ярлыка было неправильно локализовано (GH 696).</span><span class="sxs-lookup"><span data-stu-id="60e12-1161">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="60e12-1162">Исправлена логика анализа ELF, которая неправильно проверяла заголовки программ, которые должны быть меньше или равны PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="60e12-1162">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="60e12-1163">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="60e12-1163">(GH #1048)</span></span>
- <span data-ttu-id="60e12-1164">Реализован обратный вызов statfs для procfs, sysfs, cgroupfs и binfmtf (GH 1378).</span><span class="sxs-lookup"><span data-stu-id="60e12-1164">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="60e12-1165">Исправлена проблема, из-за которой окна AptPackageIndexUpdate не закрывались (GH 1184, также обсуждается в GH 1193).</span><span class="sxs-lookup"><span data-stu-id="60e12-1165">Fixed AptPackageIndexUpdate windows that won't close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="60e12-1166">Добавлена поддержка ADDR_NO_RANDOMIZE в ASLR personality.</span><span class="sxs-lookup"><span data-stu-id="60e12-1166">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="60e12-1167">[GH 1148, 1128]</span><span class="sxs-lookup"><span data-stu-id="60e12-1167">(GH #1148, 1128)</span></span>
- <span data-ttu-id="60e12-1168">Улучшена функция PTRACE_GETSIGINFO для SIGSEGV для обеспечения правильных трассировок стека GDB во время операций AV (GH 875).</span><span class="sxs-lookup"><span data-stu-id="60e12-1168">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="60e12-1169">Анализ ELF больше не завершается ошибкой для двоичных файлов patchelf.</span><span class="sxs-lookup"><span data-stu-id="60e12-1169">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="60e12-1170">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="60e12-1170">(GH #471)</span></span>
- <span data-ttu-id="60e12-1171">DNS-сервер VPN добавлен в /etc/resolv.conf (GH 416, 1350).</span><span class="sxs-lookup"><span data-stu-id="60e12-1171">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="60e12-1172">Улучшено закрытие TCP-подключений для более надежной передачи данных.</span><span class="sxs-lookup"><span data-stu-id="60e12-1172">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="60e12-1173">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="60e12-1173">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="60e12-1174">Теперь возвращается правильный код ошибки при открытии слишком большого числа файлов (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="60e12-1174">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="60e12-1175">[GH 1126, 2090]</span><span class="sxs-lookup"><span data-stu-id="60e12-1175">(GH #1126, 2090)</span></span>
- <span data-ttu-id="60e12-1176">Журнал аудита Windows теперь отображает имя образа при аудите процесса создания.</span><span class="sxs-lookup"><span data-stu-id="60e12-1176">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="60e12-1177">Теперь запуск bash.exe из окна Bash корректно завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60e12-1177">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="60e12-1178">Добавлено сообщение об ошибке, когда служба взаимодействия не может получить доступ к рабочему каталогу в LxFs (например, notepad.exe. bashrc).</span><span class="sxs-lookup"><span data-stu-id="60e12-1178">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="60e12-1179">Исправлена проблема, из-за которой путь Windows в WSL был усеченным.</span><span class="sxs-lookup"><span data-stu-id="60e12-1179">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="60e12-1180">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1180">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1181">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1181">LTP Results:</span></span>
<span data-ttu-id="60e12-1182">Число пройденных тестов: 690.</span><span class="sxs-lookup"><span data-stu-id="60e12-1182">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="60e12-1183">Число непройденных тестов (неудачных, пропущенных и т. д.): 274.</span><span class="sxs-lookup"><span data-stu-id="60e12-1183">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="60e12-1184">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1184">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1185">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1185">Syscall Support</span></span>
<span data-ttu-id="60e12-1186">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1186">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1187">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1187">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="60e12-1188">Сборка 14986</span><span class="sxs-lookup"><span data-stu-id="60e12-1188">Build 14986</span></span>

<span data-ttu-id="60e12-1189">Общие сведения о сборке Windows 14986 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1189">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1190">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1190">Fixed</span></span>

- <span data-ttu-id="60e12-1191">Исправлены ошибки NETLINK и PTY IOCTL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1191">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="60e12-1192">Теперь отображается версия ядра 4.4.0-43 для обеспечения согласованности с Xenial.</span><span class="sxs-lookup"><span data-stu-id="60e12-1192">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="60e12-1193">Теперь Bash.exe запускается, когда ввод направляется в "nul:" (GH 1259).</span><span class="sxs-lookup"><span data-stu-id="60e12-1193">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="60e12-1194">Теперь идентификаторы потоков отображаются правильно в procfs (GH 967).</span><span class="sxs-lookup"><span data-stu-id="60e12-1194">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="60e12-1195">Теперь в inotify_add_watch() поддерживаются флаги IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR (GH 1280).</span><span class="sxs-lookup"><span data-stu-id="60e12-1195">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="60e12-1196">Реализован timer_create и связанные системные вызовы.</span><span class="sxs-lookup"><span data-stu-id="60e12-1196">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="60e12-1197">Это обеспечивает поддержку GHC (GH 307).</span><span class="sxs-lookup"><span data-stu-id="60e12-1197">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="60e12-1198">Исправлена проблема, из-за которой проверка связи возвращала время 0,000 мс (GH 1296).</span><span class="sxs-lookup"><span data-stu-id="60e12-1198">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="60e12-1199">Возвращается правильный код ошибки при открытии слишком большого числа файлов.</span><span class="sxs-lookup"><span data-stu-id="60e12-1199">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="60e12-1200">Исправлена проблема в WSL, из-за которой запрос NETLINK на данные сетевого интерфейса завершался ошибкой EINVAL, если аппаратный адрес интерфейса был 32-байтовым (например, интерфейс Teredo).</span><span class="sxs-lookup"><span data-stu-id="60e12-1200">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="60e12-1201">Обратите внимание на то, что служебная программа Linux "ip" содержит ошибку, из-за которой произойдет сбой, если WSL сообщит 32-байтовый адрес оборудования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1201">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="60e12-1202">Это ошибка в "ip", а не в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1202">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="60e12-1203">В служебной программе ip прописана в коде длина строкового буфера, используемого для вывода аппаратного адреса, и этот буфер слишком мал для вывода 32-байтового аппаратного адреса.</span><span class="sxs-lookup"><span data-stu-id="60e12-1203">The "ip" utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="60e12-1204">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1204">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1205">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1205">LTP Results:</span></span>
<span data-ttu-id="60e12-1206">Число пройденных тестов: 669.</span><span class="sxs-lookup"><span data-stu-id="60e12-1206">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="60e12-1207">Число непройденных тестов (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="60e12-1207">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="60e12-1208">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1208">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1209">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1209">Syscall Support</span></span>
<span data-ttu-id="60e12-1210">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1210">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1211">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1211">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="60e12-1212">Сборка 14971</span><span class="sxs-lookup"><span data-stu-id="60e12-1212">Build 14971</span></span>

<span data-ttu-id="60e12-1213">Общие сведения о сборке Windows 14971 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1213">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1214">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1214">Fixed</span></span>

 - <span data-ttu-id="60e12-1215">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-1215">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="60e12-1216">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="60e12-1216">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1217">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1217">LTP Results:</span></span>
<span data-ttu-id="60e12-1218">без изменений с момента выпуска сборки 14965.</span><span class="sxs-lookup"><span data-stu-id="60e12-1218">Unchanged from 14965</span></span> </br>
<span data-ttu-id="60e12-1219">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="60e12-1219">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="60e12-1220">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="60e12-1220">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="60e12-1221">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1221">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="60e12-1222">Сборка 14965</span><span class="sxs-lookup"><span data-stu-id="60e12-1222">Build 14965</span></span>

<span data-ttu-id="60e12-1223">Общие сведения о сборке Windows 14965 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1223">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1224">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1224">Fixed</span></span>

- <span data-ttu-id="60e12-1225">Поддержка RTM_GETLINK и RTM_GETADDR для NETLINK_ROUTE в сокетах NETLINK (GH 468).</span><span class="sxs-lookup"><span data-stu-id="60e12-1225">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="60e12-1226">Применение команд ifconfig и ip для перечисления сетей.</span><span class="sxs-lookup"><span data-stu-id="60e12-1226">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="60e12-1227">Дополнительные сведения см. в нашей [записи блога о сетях WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1227">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="60e12-1228">Теперь /sbin добавляется в путь пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60e12-1228">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="60e12-1229">Теперь путь пользователя NT по умолчанию добавляется к пути WSL (т. е. теперь можно ввести notepad.exe, не добавляя System32 в путь Linux).</span><span class="sxs-lookup"><span data-stu-id="60e12-1229">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="60e12-1230">Добавлена поддержка /proc/sys/kernel/cap_last_cap.</span><span class="sxs-lookup"><span data-stu-id="60e12-1230">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="60e12-1231">Теперь двоичные файлы NT можно запускать из WSL, если текущий рабочий каталог содержит знаки, отличные от ANSI (GH 1254).</span><span class="sxs-lookup"><span data-stu-id="60e12-1231">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="60e12-1232">Разрешено завершение работы при отключении сокета потока UNIX.</span><span class="sxs-lookup"><span data-stu-id="60e12-1232">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="60e12-1233">Добавлена поддержка PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="60e12-1233">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="60e12-1234">Добавлена поддержка CLONE_PARENT.</span><span class="sxs-lookup"><span data-stu-id="60e12-1234">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="60e12-1235">Исправлена ошибка, из-за которой канал переставал отвечать на запросы, например bash -c "ls -alR /" | bash -c "cat" (GH 1214).</span><span class="sxs-lookup"><span data-stu-id="60e12-1235">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="60e12-1236">Обработка запросов на подключение к текущему терминалу.</span><span class="sxs-lookup"><span data-stu-id="60e12-1236">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="60e12-1237">Файл /proc/<pid>/oom_score_adj помечен как записываемый.</span><span class="sxs-lookup"><span data-stu-id="60e12-1237">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="60e12-1238">Добавлена папку /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="60e12-1238">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="60e12-1239">Функция sched_setaffinity должна возвращать значение маски битов сходства.</span><span class="sxs-lookup"><span data-stu-id="60e12-1239">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="60e12-1240">Исправлена логика проверки ELF, которая неправильно предполагала, что пути интерпретатора должны содержать менее 64 знаков.</span><span class="sxs-lookup"><span data-stu-id="60e12-1240">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="60e12-1241">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="60e12-1241">(GH #743)</span></span>
- <span data-ttu-id="60e12-1242">Открытые дескрипторы файлов могут оставаться открытыми в окне консоли (GH 1187).</span><span class="sxs-lookup"><span data-stu-id="60e12-1242">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="60e12-1243">Устранена ошибка, из-за которой происходил сбой rename(), если имя цели содержало конечную косую черту (GH 1008).</span><span class="sxs-lookup"><span data-stu-id="60e12-1243">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="60e12-1244">Реализован файл /proc/net/dev.</span><span class="sxs-lookup"><span data-stu-id="60e12-1244">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="60e12-1245">Исправлена ошибка, из-за которой при проверке связи возвращалось значение 0,000 мс из-за разрешения таймера.</span><span class="sxs-lookup"><span data-stu-id="60e12-1245">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="60e12-1246">Реализован файл /proc/self/environ (GH 730).</span><span class="sxs-lookup"><span data-stu-id="60e12-1246">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="60e12-1247">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1247">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1248">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1248">LTP Results:</span></span>
<span data-ttu-id="60e12-1249">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="60e12-1249">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="60e12-1250">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="60e12-1250">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="60e12-1251">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1251">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="60e12-1252">Сборка 14959</span><span class="sxs-lookup"><span data-stu-id="60e12-1252">Build 14959</span></span>

<span data-ttu-id="60e12-1253">Общие сведения о сборке Windows 14959 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="60e12-1253">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1254">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1254">Fixed</span></span>

- <span data-ttu-id="60e12-1255">Улучшены уведомления о процессе Pico для Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1255">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="60e12-1256">Дополнительные сведения см. в [блоге о WSL](/archive/blogs/wsl/wsl-antivirus-and-firewall-compatibility).</span><span class="sxs-lookup"><span data-stu-id="60e12-1256">Additional information found on the [WSL Blog](/archive/blogs/wsl/wsl-antivirus-and-firewall-compatibility).</span></span>
- <span data-ttu-id="60e12-1257">Повышена стабильность взаимодействия с Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1257">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="60e12-1258">Устранена ошибка 0x80070057, возникавшая при запуске bash.exe при включенной защите корпоративных данных (EDP).</span><span class="sxs-lookup"><span data-stu-id="60e12-1258">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="60e12-1259">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1259">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1260">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1260">LTP Results:</span></span>
<span data-ttu-id="60e12-1261">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="60e12-1261">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="60e12-1262">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="60e12-1262">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="60e12-1263">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1263">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="60e12-1264">Сборка 14955</span><span class="sxs-lookup"><span data-stu-id="60e12-1264">Build 14955</span></span>

<span data-ttu-id="60e12-1265">Общие сведения о сборке Windows 14955 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="60e12-1265">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1266">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1266">Fixed</span></span>

 - <span data-ttu-id="60e12-1267">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-1267">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="60e12-1268">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="60e12-1268">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1269">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1269">LTP Results:</span></span>
<span data-ttu-id="60e12-1270">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="60e12-1270">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="60e12-1271">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="60e12-1271">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="60e12-1272">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1272">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="60e12-1273">Сборка 14951</span><span class="sxs-lookup"><span data-stu-id="60e12-1273">Build 14951</span></span>

<span data-ttu-id="60e12-1274">Общие сведения о сборке Windows 14951 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1274">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="60e12-1275">Новая функция: взаимодействие Ubuntu и Windows</span><span class="sxs-lookup"><span data-stu-id="60e12-1275">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="60e12-1276">Теперь двоичные файлы Windows можно вызывать непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1276">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="60e12-1277">Это дает пользователям возможность взаимодействовать со средой и системой Windows способом, который ранее был невозможен.</span><span class="sxs-lookup"><span data-stu-id="60e12-1277">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="60e12-1278">Например, теперь пользователи могут выполнять следующие команды.</span><span class="sxs-lookup"><span data-stu-id="60e12-1278">As a quick example, it is now possible for users to run the following commands:</span></span>

```bash
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="60e12-1279">Дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="60e12-1279">More information can be found at:</span></span>

- [<span data-ttu-id="60e12-1280">Блог команды WSL по взаимодействию</span><span class="sxs-lookup"><span data-stu-id="60e12-1280">WSL Team Blog for Interop</span></span>](/archive/blogs/wsl/windows-and-ubuntu-interoperability)<br/>
- [<span data-ttu-id="60e12-1281">Документация по взаимодействию на сайте MSDN</span><span class="sxs-lookup"><span data-stu-id="60e12-1281">MSDN Interop Documentation</span></span>](./interop.md)<br/>

### <a name="fixed"></a><span data-ttu-id="60e12-1282">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1282">Fixed</span></span>

- <span data-ttu-id="60e12-1283">Ubuntu 16.04 (Xenial) теперь устанавливается для всех новых экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1283">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="60e12-1284">Существующие у пользователей экземпляры Ubuntu 14.04 (Trusty) не будут обновляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="60e12-1284">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="60e12-1285">Теперь отображается языковой стандарт, установленный во время установки.</span><span class="sxs-lookup"><span data-stu-id="60e12-1285">Locale set during install is now displayed</span></span>
- <span data-ttu-id="60e12-1286">Улучшения в терминале, включая устранение ошибки, из-за которой перенаправление процесса WSL в файл не всегда работало.</span><span class="sxs-lookup"><span data-stu-id="60e12-1286">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="60e12-1287">Время существования консоли должно быть связано со временем существования bash.exe.</span><span class="sxs-lookup"><span data-stu-id="60e12-1287">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="60e12-1288">Размер окна консоли должен быть основан на видимом размере, а не размере буфера.</span><span class="sxs-lookup"><span data-stu-id="60e12-1288">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="60e12-1289">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1289">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1290">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1290">LTP Results:</span></span>
<span data-ttu-id="60e12-1291">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="60e12-1291">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="60e12-1292">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="60e12-1292">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="60e12-1293">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1293">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="60e12-1294">Сборка 14946</span><span class="sxs-lookup"><span data-stu-id="60e12-1294">Build 14946</span></span>

<span data-ttu-id="60e12-1295">Общие сведения о сборке Windows 14946 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="60e12-1295">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1296">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1296">Fixed</span></span>

- <span data-ttu-id="60e12-1297">Устранена проблема, которая не позволила создавать учетные записи WSL для пользователей с именами пользователей NT, содержащими пробелы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="60e12-1297">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="60e12-1298">Внесены изменения в VolFs и DrvFs, чтобы возвращалось значение 0 для количества ссылок каталога в stat.</span><span class="sxs-lookup"><span data-stu-id="60e12-1298">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="60e12-1299">Поддержка параметра сокета IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="60e12-1299">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="60e12-1300">Ограничение в один цикл ввода-вывода консоли на tty.</span><span class="sxs-lookup"><span data-stu-id="60e12-1300">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="60e12-1301">Например, можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="60e12-1301">Example: the following command is possible:</span></span>
  - <span data-ttu-id="60e12-1302">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="60e12-1302">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="60e12-1303">Пробелы в /proc/cpuinfo заменены символами табуляции (GH 1115).</span><span class="sxs-lookup"><span data-stu-id="60e12-1303">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="60e12-1304">DrvFs теперь отображается в mountinfo с именем, совпадающим с подключенным томом Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1304">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="60e12-1305">Теперь /home и /root отображаются в mountinfo с правильными именами.</span><span class="sxs-lookup"><span data-stu-id="60e12-1305">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="60e12-1306">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1306">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1307">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1307">LTP Results:</span></span>
<span data-ttu-id="60e12-1308">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="60e12-1308">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="60e12-1309">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="60e12-1309">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="60e12-1310">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1310">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="60e12-1311">Сборка 14942</span><span class="sxs-lookup"><span data-stu-id="60e12-1311">Build 14942</span></span>

<span data-ttu-id="60e12-1312">Общие сведения о сборке Windows 14942 доступны в [блоге о Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="60e12-1312">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1313">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1313">Fixed</span></span>

- <span data-ttu-id="60e12-1314">Исправлен ряд ошибок, в том числе сбой сети ATTEMPTED EXECUTE OF NOEXECUTE MEMORY (Попытка выполнения в недоступной памяти), который блокировал SSH.</span><span class="sxs-lookup"><span data-stu-id="60e12-1314">A number of bugchecks addressed, including the "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" networking crash which was blocking SSH</span></span>
- <span data-ttu-id="60e12-1315">Добавлена поддержка inotifiy для уведомлений, созданных в приложениях для Windows в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-1315">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="60e12-1316">Реализованы параметры TCP_KEEPIDLE и TCP_KEEPINTVL для mongod.</span><span class="sxs-lookup"><span data-stu-id="60e12-1316">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="60e12-1317">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="60e12-1317">(GH #695)</span></span>
- <span data-ttu-id="60e12-1318">Реализован системный вызов pivot_root.</span><span class="sxs-lookup"><span data-stu-id="60e12-1318">Implement the pivot_root system call</span></span>
- <span data-ttu-id="60e12-1319">Реализован параметр сокета для SO_DONTROUTE.</span><span class="sxs-lookup"><span data-stu-id="60e12-1319">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="60e12-1320">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1320">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="60e12-1321">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1321">LTP Results:</span></span>
<span data-ttu-id="60e12-1322">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="60e12-1322">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="60e12-1323">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="60e12-1323">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="60e12-1324">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1324">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1325">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1325">Syscall Support</span></span>
<span data-ttu-id="60e12-1326">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1326">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1327">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1327">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="60e12-1328">Сборка 14936</span><span class="sxs-lookup"><span data-stu-id="60e12-1328">Build 14936</span></span>

<span data-ttu-id="60e12-1329">Общие сведения о сборке Windows 14936 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1329">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="60e12-1330">Примечание. В предстоящем выпуске WSL будет устанавливать версию Ubuntu 16.04 (Xenial) вместо Ubuntu 14.04 (Trusty).</span><span class="sxs-lookup"><span data-stu-id="60e12-1330">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="60e12-1331">Это изменение будет применено к участникам программы предварительной оценки, которые устанавливают новые экземпляры (lxrun.exe /install или первый запуск bash.exe).</span><span class="sxs-lookup"><span data-stu-id="60e12-1331">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="60e12-1332">Существующие экземпляры с версией Trusty не будут обновлены автоматически.</span><span class="sxs-lookup"><span data-stu-id="60e12-1332">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="60e12-1333">Пользователи могут обновить свой образ Trusty до версии Xenial с помощью команды do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="60e12-1333">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="60e12-1334">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="60e12-1334">Known Issue</span></span>
<span data-ttu-id="60e12-1335">В WSL существует проблема с реализацией некоторых сокетов.</span><span class="sxs-lookup"><span data-stu-id="60e12-1335">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="60e12-1336">Ошибка проявляется как сбой с сообщением ATTEMPTED EXECUTE OF NOEXECUTE MEMORY (Попытка выполнения в недоступной памяти).</span><span class="sxs-lookup"><span data-stu-id="60e12-1336">The bugcheck manifests itself as a crash with the error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span></span>  <span data-ttu-id="60e12-1337">Чаще всего этот сбой происходит при использовании SSH.</span><span class="sxs-lookup"><span data-stu-id="60e12-1337">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="60e12-1338">Первопричина исправлена во внутренних сборках, и исправление будет добавлено в сборки для программы предварительной оценки при первой возможности.</span><span class="sxs-lookup"><span data-stu-id="60e12-1338">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="60e12-1339">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1339">Fixed</span></span>

- <span data-ttu-id="60e12-1340">Реализован системный вызов chroot.</span><span class="sxs-lookup"><span data-stu-id="60e12-1340">Implemented the chroot system call</span></span>
- <span data-ttu-id="60e12-1341">Улучшения в inotify, ~~включая поддержку уведомлений, созданных в приложениях для Windows в DrvFs~~.</span><span class="sxs-lookup"><span data-stu-id="60e12-1341">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="60e12-1342">Исправление: В настоящее время недоступна поддержка в inotify изменений, исходящих из приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1342">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="60e12-1343">Привязка сокета к IPV6::<port n> теперь поддерживает IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996).</span><span class="sxs-lookup"><span data-stu-id="60e12-1343">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="60e12-1344">Реализовано поведение WNOWAIT для системного вызова waitid (GH 638).</span><span class="sxs-lookup"><span data-stu-id="60e12-1344">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="60e12-1345">Поддержка параметров IP-сокета IP_HDRINCL и IP_TTL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1345">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="60e12-1346">Результат read() нулевой длины должен возвращаться немедленно (GH 975).</span><span class="sxs-lookup"><span data-stu-id="60e12-1346">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="60e12-1347">Правильная обработка имен файлов и префиксов имен файлов, которые не содержат терминатор NULL в TAR-файле.</span><span class="sxs-lookup"><span data-stu-id="60e12-1347">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="60e12-1348">Поддержка epoll для /dev/null.</span><span class="sxs-lookup"><span data-stu-id="60e12-1348">epoll support for /dev/null</span></span>
- <span data-ttu-id="60e12-1349">Исправлен источник времени /dev/alarm.</span><span class="sxs-lookup"><span data-stu-id="60e12-1349">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="60e12-1350">Теперь команда bash -c может выполнять перенаправление в файл.</span><span class="sxs-lookup"><span data-stu-id="60e12-1350">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="60e12-1351">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1351">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1352">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1352">LTP Results:</span></span>
<span data-ttu-id="60e12-1353">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="60e12-1353">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="60e12-1354">Число непройденных тестов (неудачных, пропущенных и т. д.): 264.</span><span class="sxs-lookup"><span data-stu-id="60e12-1354">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="60e12-1355">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1355">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1356">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1356">Syscall Support</span></span>
<span data-ttu-id="60e12-1357">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1357">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1358">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1358">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="60e12-1359">Сборка 14931</span><span class="sxs-lookup"><span data-stu-id="60e12-1359">Build 14931</span></span>

<span data-ttu-id="60e12-1360">Общие сведения о сборке Windows 14931 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1360">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1361">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1361">Fixed</span></span>

 - <span data-ttu-id="60e12-1362">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-1362">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="60e12-1363">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="60e12-1363">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="60e12-1364">Сборка 14926</span><span class="sxs-lookup"><span data-stu-id="60e12-1364">Build 14926</span></span>

<span data-ttu-id="60e12-1365">Общие сведения о сборке Windows 14926 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1365">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1366">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1366">Fixed</span></span>

- <span data-ttu-id="60e12-1367">Проверка связи теперь работает в консолях без привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="60e12-1367">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="60e12-1368">Теперь поддерживается ping6, также без привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="60e12-1368">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="60e12-1369">Поддержка в inotify файлов, измененных посредством WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1369">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="60e12-1370">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="60e12-1370">(GH #216)</span></span>
  - <span data-ttu-id="60e12-1371">Поддерживаемые флаги:</span><span class="sxs-lookup"><span data-stu-id="60e12-1371">Flags supported:</span></span>
    - <span data-ttu-id="60e12-1372">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="60e12-1372">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="60e12-1373">События inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="60e12-1373">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="60e12-1374">Атрибуты inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="60e12-1374">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="60e12-1375">Выходные данные чтения: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="60e12-1375">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="60e12-1376">Известная проблема: Изменение файлов из приложений Windows не приводит к созданию событий.</span><span class="sxs-lookup"><span data-stu-id="60e12-1376">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="60e12-1377">Сокет UNIX теперь поддерживает SCM_CREDENTIALS.</span><span class="sxs-lookup"><span data-stu-id="60e12-1377">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="60e12-1378">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="60e12-1378">LTP Results:</span></span>
<span data-ttu-id="60e12-1379">Число пройденных тестов: 651</span><span class="sxs-lookup"><span data-stu-id="60e12-1379">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="60e12-1380">Число непройденных тестов (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="60e12-1380">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="60e12-1381">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="60e12-1381">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="60e12-1382">Сборка 14915</span><span class="sxs-lookup"><span data-stu-id="60e12-1382">Build 14915</span></span>

<span data-ttu-id="60e12-1383">Общие сведения о сборке Windows 14915 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="60e12-1383">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1384">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1384">Fixed</span></span>
-  <span data-ttu-id="60e12-1385">Socketpair для сокетов датаграмм UNIX (GH 262).</span><span class="sxs-lookup"><span data-stu-id="60e12-1385">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="60e12-1386">Поддержка сокетов UNIX для SO_REUSEADDR.</span><span class="sxs-lookup"><span data-stu-id="60e12-1386">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="60e12-1387">Поддержка сокетов UNIX для SO_BROADCAST (GH 568).</span><span class="sxs-lookup"><span data-stu-id="60e12-1387">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="60e12-1388">Поддержка сокетов UNIX для SOCK_SEQPACKET (GH 758, 546).</span><span class="sxs-lookup"><span data-stu-id="60e12-1388">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="60e12-1389">Добавлена поддержка send, recv и shutdown для сокетов датаграмм UNIX.</span><span class="sxs-lookup"><span data-stu-id="60e12-1389">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="60e12-1390">Устранена ошибка из-за неправильной проверки параметров mmap для нефиксированных адресов.</span><span class="sxs-lookup"><span data-stu-id="60e12-1390">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="60e12-1391">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="60e12-1391">(GH #847)</span></span>
- <span data-ttu-id="60e12-1392">Поддержка приостановки и возобновления состояний терминала.</span><span class="sxs-lookup"><span data-stu-id="60e12-1392">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="60e12-1393">Поддержка TIOCPKT ioctl для разблокировки служебной программы Screen (GH 774).</span><span class="sxs-lookup"><span data-stu-id="60e12-1393">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="60e12-1394">Известная проблема: Не работают функциональные клавиши.</span><span class="sxs-lookup"><span data-stu-id="60e12-1394">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="60e12-1395">Исправлено состязание в TimerFd, которое могло привести к обращению LxpTimerFdWorkerRoutine к освобожденному элементу ReaderReady (GH 814).</span><span class="sxs-lookup"><span data-stu-id="60e12-1395">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="60e12-1396">Включена поддержка перезапускаемых системных вызовов для futex, poll и clock_nanosleep.</span><span class="sxs-lookup"><span data-stu-id="60e12-1396">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="60e12-1397">Добавлена поддержка подключения привязки.</span><span class="sxs-lookup"><span data-stu-id="60e12-1397">Added bind mount support</span></span>
- <span data-ttu-id="60e12-1398">Поддержка отмены общего доступа для пространства имен подключения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1398">unshare for mount namespace support</span></span>
    - <span data-ttu-id="60e12-1399">Известная проблема: При создании пространства имен подключения посредством `unshare(CLONE_NEWNS)` текущий рабочий каталог будет по-прежнему указывать на старое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="60e12-1399">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="60e12-1400">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="60e12-1400">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="60e12-1401">Сборка 14905</span><span class="sxs-lookup"><span data-stu-id="60e12-1401">Build 14905</span></span>

<span data-ttu-id="60e12-1402">Общие сведения о сборке Windows 14905 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1402">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1403">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1403">Fixed</span></span>
- <span data-ttu-id="60e12-1404">Теперь поддерживаются перезапускаемые системные вызовы (GH 349, GH 520).</span><span class="sxs-lookup"><span data-stu-id="60e12-1404">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="60e12-1405">Теперь функционируют символические ссылки на каталоги, которые заканчиваются косой чертой "/" (GH 650).</span><span class="sxs-lookup"><span data-stu-id="60e12-1405">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="60e12-1406">Реализован параметр RNDGETENTCNT ioctl для /dev/random.</span><span class="sxs-lookup"><span data-stu-id="60e12-1406">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="60e12-1407">Реализованы файлы /proc/[pid]/mounts, /proc/[pid]/mountinfo и /proc/[pid]/mountstats.</span><span class="sxs-lookup"><span data-stu-id="60e12-1407">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="60e12-1408">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1408">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="60e12-1409">Сборка 14901</span><span class="sxs-lookup"><span data-stu-id="60e12-1409">Build 14901</span></span>
<span data-ttu-id="60e12-1410">Первая сборка для программы предварительной оценки для выпуска после юбилейного обновления Windows 10.</span><span class="sxs-lookup"><span data-stu-id="60e12-1410">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="60e12-1411">Общие сведения о сборке Windows 14901 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1411">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1412">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1412">Fixed</span></span>
- <span data-ttu-id="60e12-1413">Исправлена проблема конечной косой черты.</span><span class="sxs-lookup"><span data-stu-id="60e12-1413">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="60e12-1414">Теперь работают такие команды, как `$ mv a/c/ a/b/`.</span><span class="sxs-lookup"><span data-stu-id="60e12-1414">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="60e12-1415">Теперь при установке отображается запрос, позволяющий установить языковый стандарт Ubuntu, совпадающий с языковым стандартом Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1415">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="60e12-1416">Поддержка procfs для папки ns.</span><span class="sxs-lookup"><span data-stu-id="60e12-1416">Procfs support for ns folder</span></span>
- <span data-ttu-id="60e12-1417">Добавлены функции подключения и отключения для файловых систем tmpfs, procfs и sysfs.</span><span class="sxs-lookup"><span data-stu-id="60e12-1417">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="60e12-1418">Исправлена 32-разрядная подпись ABI для mknod[at].</span><span class="sxs-lookup"><span data-stu-id="60e12-1418">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="60e12-1419">Сокеты UNIX переведены на модель диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="60e12-1419">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="60e12-1420">Размер буфера recv сокета INET, заданный с помощью setsockopt, должен учитываться.</span><span class="sxs-lookup"><span data-stu-id="60e12-1420">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="60e12-1421">Реализован флаг получения сообщения MSG_CMSG_CLOEXEC для сокетов UNIX.</span><span class="sxs-lookup"><span data-stu-id="60e12-1421">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="60e12-1422">Перенаправление канала stdin/stdout процесса Linux (GH 2).</span><span class="sxs-lookup"><span data-stu-id="60e12-1422">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="60e12-1423">Разрешена конвейерная передача команд bash -c в командную строку.</span><span class="sxs-lookup"><span data-stu-id="60e12-1423">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="60e12-1424">Пример:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="60e12-1424">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="60e12-1425">Теперь Bash можно установить в системах с несколькими файлами подкачки (GH 538, 358).</span><span class="sxs-lookup"><span data-stu-id="60e12-1425">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="60e12-1426">Размер буфера сокета INET по умолчанию должен соответствовать установке Ubuntu по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60e12-1426">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="60e12-1427">Системные вызовы xattr согласованы с listxattr.</span><span class="sxs-lookup"><span data-stu-id="60e12-1427">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="60e12-1428">SIOCGIFCONF возвращает только интерфейсы с допустимым IPv4-адресом.</span><span class="sxs-lookup"><span data-stu-id="60e12-1428">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="60e12-1429">Исправлено действие по умолчанию для сигнала при внедрении с помощью ptrace.</span><span class="sxs-lookup"><span data-stu-id="60e12-1429">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="60e12-1430">Реализован файл /proc/sys/vm/min_free_kbytes.</span><span class="sxs-lookup"><span data-stu-id="60e12-1430">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="60e12-1431">Использование значений реестра для контекста компьютера при восстановлении контекста в sigreturn.</span><span class="sxs-lookup"><span data-stu-id="60e12-1431">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="60e12-1432">Это устраняет проблему, из-за которой у некоторых пользователей java и javac переставали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="60e12-1432">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="60e12-1433">Реализован файл /proc/sys/kernel/hostname.</span><span class="sxs-lookup"><span data-stu-id="60e12-1433">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1434">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1434">Syscall Support</span></span>
<span data-ttu-id="60e12-1435">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1435">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1436">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1436">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="60e12-1437">Сборка 14388 для юбилейного обновления Windows 10</span><span class="sxs-lookup"><span data-stu-id="60e12-1437">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="60e12-1438">Общие сведения о сборке Windows 14388 доступны в [блоге о Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="60e12-1438">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="60e12-1439">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1439">Fixed</span></span>
- <span data-ttu-id="60e12-1440">Исправления для подготовки к выпуску юбилейного обновления Windows 10 2-го августа.</span><span class="sxs-lookup"><span data-stu-id="60e12-1440">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="60e12-1441">Дополнительные сведения о компоненте WSL в юбилейном обновлении можно найти на нашем [блоге](/archive/blogs/wsl/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1441">More information about WSL in the Anniversary Update can be found on our [blog](/archive/blogs/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="60e12-1442">Сборка 14376</span><span class="sxs-lookup"><span data-stu-id="60e12-1442">Build 14376</span></span>
<span data-ttu-id="60e12-1443">Общие сведения о сборке Windows 14376 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1443">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="60e12-1444">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1444">Fixed</span></span>
- <span data-ttu-id="60e12-1445">Удалены некоторые экземпляры, в которых функция apt-get переставала отвечать на запросы (GH 493).</span><span class="sxs-lookup"><span data-stu-id="60e12-1445">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="60e12-1446">Исправлена проблема, из-за которой неправильно обрабатывались пустые подключения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1446">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="60e12-1447">Исправлена проблема, из-за которой неправильно подключались диски ramdisk.</span><span class="sxs-lookup"><span data-stu-id="60e12-1447">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="60e12-1448">Изменена процедура принятия сокетов UNIX для поддержки флагов (частично GH 451).</span><span class="sxs-lookup"><span data-stu-id="60e12-1448">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="60e12-1449">Исправлена распространенная проблема с сетью, вызывавшая ошибку "синий экран".</span><span class="sxs-lookup"><span data-stu-id="60e12-1449">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="60e12-1450">Устранена ошибка "синий экран" при доступе к /proc/[pid]/task (GH 523).</span><span class="sxs-lookup"><span data-stu-id="60e12-1450">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="60e12-1451">Исправлена высокая загрузка ЦП для некоторых сценариев использования pty (GH 488, 504).</span><span class="sxs-lookup"><span data-stu-id="60e12-1451">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="60e12-1452">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1452">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="60e12-1453">Сборка 14371</span><span class="sxs-lookup"><span data-stu-id="60e12-1453">Build 14371</span></span>
<span data-ttu-id="60e12-1454">Общие сведения о сборке Windows 14371 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1454">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="60e12-1455">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1455">Fixed</span></span>
- <span data-ttu-id="60e12-1456">Исправлено состязание за синхронизацию SIGCHLD и wait() при использовании ptrace.</span><span class="sxs-lookup"><span data-stu-id="60e12-1456">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="60e12-1457">Исправлена обработка путей, которые завершаются косой чертой "/" (GH 432).</span><span class="sxs-lookup"><span data-stu-id="60e12-1457">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="60e12-1458">Устранен сбой при переименовании или отмене связи из-за открытых дескрипторов дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="60e12-1458">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="60e12-1459">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1459">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="60e12-1460">Сборка 14366</span><span class="sxs-lookup"><span data-stu-id="60e12-1460">Build 14366</span></span>
<span data-ttu-id="60e12-1461">Общие сведения о сборке Windows 14366 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1461">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="60e12-1462">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1462">Fixed</span></span>
- <span data-ttu-id="60e12-1463">Исправлено создание файла с помощью символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="60e12-1463">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="60e12-1464">Добавлена функция listxattr для Python (GH 385).</span><span class="sxs-lookup"><span data-stu-id="60e12-1464">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="60e12-1465">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1465">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1466">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1466">Syscall Support</span></span>
-   <span data-ttu-id="60e12-1467">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1467">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1468">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1468">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="60e12-1469">Сборка 14361</span><span class="sxs-lookup"><span data-stu-id="60e12-1469">Build 14361</span></span>
<span data-ttu-id="60e12-1470">Общие сведения о сборке Windows 14361 доступны в [блоге о Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="60e12-1470">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="60e12-1471">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1471">Fixed</span></span>
- <span data-ttu-id="60e12-1472">Теперь в DrvFs учитывается регистр при выполнении в Bash для Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1472">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="60e12-1473">Пользователи могут хранить на дисках в /mnt/c и файл case.txt, и файл CASE.TXT.</span><span class="sxs-lookup"><span data-stu-id="60e12-1473">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="60e12-1474">Учет регистра поддерживается только в Bash для Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1474">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="60e12-1475">За пределами Bash NTFS будет отображать сведения о файлах правильно, но при взаимодействии с этими файлами из Windows может наблюдаться непредвиденное поведение.</span><span class="sxs-lookup"><span data-stu-id="60e12-1475">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="60e12-1476">Корень каждого тома (т. е. /mnt/c) не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="60e12-1476">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="60e12-1477">Дополнительные сведения об обработке этих файлов в Windows можно найти [здесь](https://support.microsoft.com/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="60e12-1477">More information on handling these files in Windows can be found [here](https://support.microsoft.com/kb/100625).</span></span>
- <span data-ttu-id="60e12-1478">Значительно улучшена поддержка pty и tty.</span><span class="sxs-lookup"><span data-stu-id="60e12-1478">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="60e12-1479">Теперь поддерживаются такие приложения, как tmux (GH 40).</span><span class="sxs-lookup"><span data-stu-id="60e12-1479">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="60e12-1480">Исправлена проблема с установкой, из-за которой учетные записи пользователей создавались не всегда.</span><span class="sxs-lookup"><span data-stu-id="60e12-1480">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="60e12-1481">Оптимизирована структура аргументов командной строки, которая позволяет получить очень длинный список аргументов.</span><span class="sxs-lookup"><span data-stu-id="60e12-1481">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="60e12-1482">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="60e12-1482">(GH #153)</span></span>
- <span data-ttu-id="60e12-1483">Теперь можно выполнять операции delete и chmod с файлами только для чтения в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-1483">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="60e12-1484">Исправлены некоторые экземпляры, в которых терминал при отключении переставал отвечать на запросы (GH 43).</span><span class="sxs-lookup"><span data-stu-id="60e12-1484">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="60e12-1485">Теперь на устройствах tty работает chmod и chown.</span><span class="sxs-lookup"><span data-stu-id="60e12-1485">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="60e12-1486">Разрешено подключение к 0.0.0.0 и :: как localhost (GH 388).</span><span class="sxs-lookup"><span data-stu-id="60e12-1486">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="60e12-1487">Теперь sendmsg и recvmsg обрабатывают векторы ввода-вывода длиной больше 1 (частично GH 376).</span><span class="sxs-lookup"><span data-stu-id="60e12-1487">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="60e12-1488">Теперь пользователи могут отказаться от автоматически создаваемого файла hosts (GH 398).</span><span class="sxs-lookup"><span data-stu-id="60e12-1488">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="60e12-1489">Автоматическое сопоставление языкового стандарта Linux с языковым стандартом NT во время установки (GH 11).</span><span class="sxs-lookup"><span data-stu-id="60e12-1489">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="60e12-1490">Добавлен файл /proc/sys/vm/swappiness (GH #306).</span><span class="sxs-lookup"><span data-stu-id="60e12-1490">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="60e12-1491">Теперь strace завершается правильно.</span><span class="sxs-lookup"><span data-stu-id="60e12-1491">strace now exits correctly</span></span>
- <span data-ttu-id="60e12-1492">Разрешено повторное открытие каналов через /proc/self/fd (GH 222).</span><span class="sxs-lookup"><span data-stu-id="60e12-1492">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="60e12-1493">Скрытие каталогов в %LOCALAPPDATA%\lxss из DrvFs (GH 270).</span><span class="sxs-lookup"><span data-stu-id="60e12-1493">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="60e12-1494">Улучшена обработка bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="60e12-1494">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="60e12-1495">Теперь поддерживаются такие команды, как bash ~ -c ls (GH 467).</span><span class="sxs-lookup"><span data-stu-id="60e12-1495">Commands like "bash ~ -c ls" now supported (GH #467)</span></span>
- <span data-ttu-id="60e12-1496">Сокеты теперь уведомляют epoll о доступе на чтение во время завершения (GH 271).</span><span class="sxs-lookup"><span data-stu-id="60e12-1496">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="60e12-1497">Команда lxrun /uninstall лучше удаляет файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="60e12-1497">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="60e12-1498">Исправлена команда ps -f (GH 246).</span><span class="sxs-lookup"><span data-stu-id="60e12-1498">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="60e12-1499">Улучшена поддержка приложений x11, таких как xEmacs (GH 481).</span><span class="sxs-lookup"><span data-stu-id="60e12-1499">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="60e12-1500">Обновлен начальный размер стека потока в соответствии с параметром Ubuntu по умолчанию. Теперь при системном вызове get_rlimit размер отображается правильно (GH 172, 258).</span><span class="sxs-lookup"><span data-stu-id="60e12-1500">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="60e12-1501">Улучшено отображение имен образов процессов Pico (например, для аудита).</span><span class="sxs-lookup"><span data-stu-id="60e12-1501">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="60e12-1502">Реализован файл /proc/mountinfo для команды df.</span><span class="sxs-lookup"><span data-stu-id="60e12-1502">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="60e12-1503">Исправлен код ошибки символической ссылки для дочернего имени.</span><span class="sxs-lookup"><span data-stu-id="60e12-1503">Fixed symlink error code for child name .</span></span> <span data-ttu-id="60e12-1504">И еще:</span><span class="sxs-lookup"><span data-stu-id="60e12-1504">and ..</span></span>
- <span data-ttu-id="60e12-1505">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1505">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1506">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1506">Syscall Support</span></span>
<span data-ttu-id="60e12-1507">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1507">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1508">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1508">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="60e12-1509">Сборка 14352</span><span class="sxs-lookup"><span data-stu-id="60e12-1509">Build 14352</span></span>
<span data-ttu-id="60e12-1510">Общие сведения о сборке Windows 14352 доступны в [блоге о Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="60e12-1510">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1511">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1511">Fixed</span></span>
- <span data-ttu-id="60e12-1512">Исправлена проблема, из-за которой большие файлы скачивались и создавались неправильно.</span><span class="sxs-lookup"><span data-stu-id="60e12-1512">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="60e12-1513">Это должно позволить использовать npm и реализовать другие сценарии (GH 3, GH 313).</span><span class="sxs-lookup"><span data-stu-id="60e12-1513">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="60e12-1514">Удалены некоторые экземпляры, в которых сокеты переставали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="60e12-1514">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="60e12-1515">Исправлены некоторые ошибки ptrace.</span><span class="sxs-lookup"><span data-stu-id="60e12-1515">Corrected some ptrace errors</span></span>
- <span data-ttu-id="60e12-1516">Исправлена проблема с WSL, и теперь можно использовать имена файлов длиннее 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="60e12-1516">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="60e12-1517">Улучшена поддержка знаков языков, отличных от английского.</span><span class="sxs-lookup"><span data-stu-id="60e12-1517">Improved support for non-English characters</span></span>
- <span data-ttu-id="60e12-1518">Добавление данных о текущем часовом поясе Windows и назначение его используемым по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="60e12-1518">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="60e12-1519">Уникальный идентификатор устройства для каждой точки подключения (исправление JRE — GH 49).</span><span class="sxs-lookup"><span data-stu-id="60e12-1519">Unique device id's for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="60e12-1520">Устранена ошибка с путями, содержащими . и .. (одну и две точки).</span><span class="sxs-lookup"><span data-stu-id="60e12-1520">Correct issue with paths containing "." and ".."</span></span>
- <span data-ttu-id="60e12-1521">Добавлена поддержка FIFO (GH 71).</span><span class="sxs-lookup"><span data-stu-id="60e12-1521">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="60e12-1522">Обновлен формат resolv.conf в соответствии с собственным форматом Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="60e12-1522">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="60e12-1523">Некоторая очистка procfs.</span><span class="sxs-lookup"><span data-stu-id="60e12-1523">Some procfs cleanup</span></span>
- <span data-ttu-id="60e12-1524">Включена проверка связи для консолей администратора (GH 18).</span><span class="sxs-lookup"><span data-stu-id="60e12-1524">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1525">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1525">Syscall Support</span></span>
<span data-ttu-id="60e12-1526">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1526">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1527">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1527">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="60e12-1528">Сборка 14342</span><span class="sxs-lookup"><span data-stu-id="60e12-1528">Build 14342</span></span>
<span data-ttu-id="60e12-1529">Общие сведения о сборке Windows 14342 доступны в [блоге о Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="60e12-1529">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="60e12-1530">Сведения о VolFs и DriveFs можно найти в [блоге о WSL](/archive/blogs/wsl/).</span><span class="sxs-lookup"><span data-stu-id="60e12-1530">Information on VolFs and DriveFs can be found on the [WSL Blog](/archive/blogs/wsl/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="60e12-1531">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1531">Fixed</span></span>
- <span data-ttu-id="60e12-1532">Исправлена проблема с установкой, возникавшая, когда в имени пользователя Windows присутствовали знаки Юникода.</span><span class="sxs-lookup"><span data-stu-id="60e12-1532">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="60e12-1533">Теперь обходное решение для обновления apt-get с помощью udev, приведенное в разделе часто задаваемых вопросов, предоставляется по умолчанию при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="60e12-1533">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="60e12-1534">Включены символические ссылки в каталогах DriveFs (/mnt/<drive>).</span><span class="sxs-lookup"><span data-stu-id="60e12-1534">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="60e12-1535">Теперь работают символические ссылки между DriveFs и VolFs.</span><span class="sxs-lookup"><span data-stu-id="60e12-1535">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="60e12-1536">Устранена проблема с анализом путей верхнего уровня. Теперь ls .// будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="60e12-1536">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="60e12-1537">Теперь работает установка npm в DriveFs и параметры -g.</span><span class="sxs-lookup"><span data-stu-id="60e12-1537">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="60e12-1538">Исправлена проблема, препятствующая запуску сервера PHP.</span><span class="sxs-lookup"><span data-stu-id="60e12-1538">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="60e12-1539">Обновлены значения среды по умолчанию, такие как $PATH, чтобы они больше соответствовали собственным переменным Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="60e12-1539">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="60e12-1540">Добавлена еженедельная задача обслуживания в Windows для обновления кэша пакетов apt.</span><span class="sxs-lookup"><span data-stu-id="60e12-1540">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="60e12-1541">Исправлена проблема с проверкой заголовков ELF. Теперь WSL поддерживает все параметры Melkor.</span><span class="sxs-lookup"><span data-stu-id="60e12-1541">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="60e12-1542">Оболочка Zsh работает.</span><span class="sxs-lookup"><span data-stu-id="60e12-1542">Zsh shell is functional</span></span>
- <span data-ttu-id="60e12-1543">Теперь поддерживаются предварительно скомпилированные двоичные файлы Go.</span><span class="sxs-lookup"><span data-stu-id="60e12-1543">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="60e12-1544">Теперь запросы при первом запуске bash.exe локализованы правильно.</span><span class="sxs-lookup"><span data-stu-id="60e12-1544">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="60e12-1545">Теперь /proc/meminfo возвращает правильные сведения.</span><span class="sxs-lookup"><span data-stu-id="60e12-1545">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="60e12-1546">Сокеты теперь поддерживаются в VFS.</span><span class="sxs-lookup"><span data-stu-id="60e12-1546">Sockets now supported in VFS</span></span>
- <span data-ttu-id="60e12-1547">Теперь /dev подключен как tempfs.</span><span class="sxs-lookup"><span data-stu-id="60e12-1547">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="60e12-1548">FIFO теперь поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60e12-1548">Fifo now supported</span></span>
- <span data-ttu-id="60e12-1549">Многоядерные системы теперь правильно отображаются в /proc/cpuinfo.</span><span class="sxs-lookup"><span data-stu-id="60e12-1549">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="60e12-1550">Дополнительные улучшения и сообщения об ошибках при скачивании во время первого запуска.</span><span class="sxs-lookup"><span data-stu-id="60e12-1550">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="60e12-1551">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="60e12-1551">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="60e12-1552">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="60e12-1552">Supported syscall list below.</span></span>
- <span data-ttu-id="60e12-1553">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1553">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="60e12-1554">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="60e12-1554">Known Issues</span></span>
- <span data-ttu-id="60e12-1555">Неправильное разрешение .. (две точки).</span><span class="sxs-lookup"><span data-stu-id="60e12-1555">Not resolving '..'</span></span> <span data-ttu-id="60e12-1556">в DriveFs в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="60e12-1556">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1557">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1557">Syscall Support</span></span>
<span data-ttu-id="60e12-1558">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1558">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="60e12-1559">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1559">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="60e12-1560">Сборка 14332</span><span class="sxs-lookup"><span data-stu-id="60e12-1560">Build 14332</span></span>

<span data-ttu-id="60e12-1561">Общие сведения о сборке Windows 14332 доступны в [блоге о Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="60e12-1561">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="60e12-1562">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1562">Fixed</span></span>
- <span data-ttu-id="60e12-1563">Улучшенное создание resolv.conf, включая определение приоритета записей DNS.</span><span class="sxs-lookup"><span data-stu-id="60e12-1563">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="60e12-1564">Проблема с перемещением файлов и каталогов между дисками в /mnt и прочими дисками.</span><span class="sxs-lookup"><span data-stu-id="60e12-1564">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="60e12-1565">Теперь можно создавать TAR-файлы с помощью символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="60e12-1565">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="60e12-1566">Добавлен каталог /run/lock по умолчанию, создаваемый при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="60e12-1566">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="60e12-1567">Обновлен файл /dev/null для возврата правильных сведений stat.</span><span class="sxs-lookup"><span data-stu-id="60e12-1567">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="60e12-1568">Дополнительные ошибки при скачивании во время первого запуска.</span><span class="sxs-lookup"><span data-stu-id="60e12-1568">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="60e12-1569">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="60e12-1569">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="60e12-1570">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="60e12-1570">Supported syscall list below.</span></span>
- <span data-ttu-id="60e12-1571">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1571">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1572">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1572">Syscall Support</span></span>
<span data-ttu-id="60e12-1573">Ниже приведен новый системный вызов, реализованный в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1573">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="60e12-1574">Системный вызов в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут поддерживаться не все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1574">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="60e12-1575">Сборка 14328</span><span class="sxs-lookup"><span data-stu-id="60e12-1575">Build 14328</span></span>

<span data-ttu-id="60e12-1576">Общие сведения о сборке Windows 14332 доступны в [блоге о Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="60e12-1576">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="60e12-1577">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="60e12-1577">New Features</span></span>
* <span data-ttu-id="60e12-1578">Теперь поддерживаются пользователи Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-1578">Now support Linux users.</span></span>  <span data-ttu-id="60e12-1579">При установке Bash для Ubuntu в Windows будет предложено создать пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="60e12-1579">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="60e12-1580">Дополнительные сведения: https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="60e12-1580">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="60e12-1581">В качестве имени узла теперь указывается имя компьютера Windows, а не @localhost.</span><span class="sxs-lookup"><span data-stu-id="60e12-1581">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="60e12-1582">Дополнительные сведения о сборке 14328: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="60e12-1582">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="60e12-1583">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="60e12-1583">Fixed</span></span>
* <span data-ttu-id="60e12-1584">Улучшения символьных ссылок для файлов вне каталога /mnt/<drive>.</span><span class="sxs-lookup"><span data-stu-id="60e12-1584">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="60e12-1585">Теперь установка npm работает.</span><span class="sxs-lookup"><span data-stu-id="60e12-1585">npm install now works</span></span>
    * <span data-ttu-id="60e12-1586">Теперь можно установить JDK или JRE с помощью [этих инструкций](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="60e12-1586">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="60e12-1587">Известная ошибка: символические ссылки не работали для подключений Windows.</span><span class="sxs-lookup"><span data-stu-id="60e12-1587">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="60e12-1588">Эта функция будет доступна в последующей сборке.</span><span class="sxs-lookup"><span data-stu-id="60e12-1588">Functionality will be available in a later build</span></span>
* <span data-ttu-id="60e12-1589">Теперь отображаются top и htop.</span><span class="sxs-lookup"><span data-stu-id="60e12-1589">top and htop now display</span></span>
* <span data-ttu-id="60e12-1590">Дополнительные сообщения об ошибке для некоторых сбоев при установке.</span><span class="sxs-lookup"><span data-stu-id="60e12-1590">Additional error messages for some install failures</span></span>
* <span data-ttu-id="60e12-1591">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="60e12-1591">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="60e12-1592">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="60e12-1592">Supported syscall list below.</span></span>
* <span data-ttu-id="60e12-1593">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="60e12-1593">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="60e12-1594">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="60e12-1594">Syscall Support</span></span>
<span data-ttu-id="60e12-1595">Ниже приведен список системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="60e12-1595">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="60e12-1596">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="60e12-1596">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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