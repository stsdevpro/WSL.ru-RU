---
title: Сравнение WSL 2 и WSL 1
description: 'Сравните версии 1 и 2 подсистемы Windows для Linux. Узнайте о новых возможностях WSL 2: актуальной версии ядра Linux, более высокой скорости работы, полной совместимости системных вызовов. WSL 1 лучше подходит для сценариев, когда файлы хранятся в разных операционных файловых системах. Вы можете увеличить размер виртуального жесткого диска (VHD) WSL 2.'
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux, ubuntu, debian, suse, windows 10, изменения взаимодействия с пользователем, WSL 2, ядро linux, сетевые приложения, localhost, IPv6, виртуальный жесткий диск, VHD, ограничения VHD, ошибка VHD
ms.date: 09/15/2020
ms.topic: conceptual
ms.localizationpriority: high
ms.custom: contperfq1
ms.openlocfilehash: ce68a19da519ddae5dd562c75c9ba2bac3659190
ms.sourcegitcommit: dee2bf22c0c9f5725122a155d2876fcb2b7427d0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "92211768"
---
# <a name="comparing-wsl-1-and-wsl-2"></a><span data-ttu-id="e66ad-107">Сравнение WSL 1 и WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-107">Comparing WSL 1 and WSL 2</span></span>

<span data-ttu-id="e66ad-108">Основные различия между подсистемами Windows для Linux WSL 1 и WSL 2 и причины обновления:</span><span class="sxs-lookup"><span data-stu-id="e66ad-108">The primary difference and reasons for updating the Windows Subsystem for Linux from WSL 1 to WSL 2 are to:</span></span>

- <span data-ttu-id="e66ad-109">**повышение производительности файловой системы;**</span><span class="sxs-lookup"><span data-stu-id="e66ad-109">**increase file system performance** ,</span></span>
- <span data-ttu-id="e66ad-110">**поддержка полной совместимости системных вызовов.**</span><span class="sxs-lookup"><span data-stu-id="e66ad-110">**support full system call compatibility** .</span></span>

<span data-ttu-id="e66ad-111">WSL 2 использует последнюю и самую новую технологию виртуализации для запуска ядра Linux внутри упрощенной служебной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e66ad-111">WSL 2 uses the latest and greatest in virtualization technology to run a Linux kernel inside of a lightweight utility virtual machine (VM).</span></span> <span data-ttu-id="e66ad-112">Однако WSL 2 не является традиционным функционалом виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e66ad-112">However, WSL 2 is not a traditional VM experience.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="e66ad-113">Установка WSL 1 и обновление до WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-113">Install WSL 1 and update to WSL 2</span></span>](install-win10.md)

## <a name="comparing-features"></a><span data-ttu-id="e66ad-114">Сравнение возможностей</span><span class="sxs-lookup"><span data-stu-id="e66ad-114">Comparing features</span></span>

<span data-ttu-id="e66ad-115">Функция</span><span class="sxs-lookup"><span data-stu-id="e66ad-115">Feature</span></span> | <span data-ttu-id="e66ad-116">WSL 1</span><span class="sxs-lookup"><span data-stu-id="e66ad-116">WSL 1</span></span> | <span data-ttu-id="e66ad-117">WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-117">WSL 2</span></span>
--- | --- | ---
 <span data-ttu-id="e66ad-118">Интеграция Windows и Linux</span><span class="sxs-lookup"><span data-stu-id="e66ad-118">Integration between Windows and Linux</span></span>| ✅|✅
 <span data-ttu-id="e66ad-119">Быстрый запуск</span><span class="sxs-lookup"><span data-stu-id="e66ad-119">Fast boot times</span></span>| ✅ | ✅
 <span data-ttu-id="e66ad-120">Незначительный расход ресурсов</span><span class="sxs-lookup"><span data-stu-id="e66ad-120">Small resource foot print</span></span>| ✅ |✅
 <span data-ttu-id="e66ad-121">Запуск с использованием текущих версий VMware и VirtualBox</span><span class="sxs-lookup"><span data-stu-id="e66ad-121">Runs with current versions of VMware and VirtualBox</span></span>| ✅ | ✅
 <span data-ttu-id="e66ad-122">Управляемая виртуальная машина</span><span class="sxs-lookup"><span data-stu-id="e66ad-122">Managed VM</span></span>| ❌ | ✅
 <span data-ttu-id="e66ad-123">Полнофункциональное ядро Linux</span><span class="sxs-lookup"><span data-stu-id="e66ad-123">Full Linux Kernel</span></span>| ❌ |✅
 <span data-ttu-id="e66ad-124">Полная совместимость системных вызовов</span><span class="sxs-lookup"><span data-stu-id="e66ad-124">Full system call compatibility</span></span>| ❌ | ✅
 <span data-ttu-id="e66ad-125">Производительность в файловых системах ОС</span><span class="sxs-lookup"><span data-stu-id="e66ad-125">Performance across OS file systems</span></span>| ✅ | ❌

<span data-ttu-id="e66ad-126">Как видно из приведенной выше таблицы, архитектура WSL 2 во многом превосходит архитектуру WSL 1, за исключением показателей производительности при работе с несколькими файловыми системами ОС.</span><span class="sxs-lookup"><span data-stu-id="e66ad-126">As you can tell from the comparison table above, the WSL 2 architecture outperforms WSL 1 in several ways, with the exception of performance across OS file systems.</span></span>

## <a name="performance-across-os-file-systems"></a><span data-ttu-id="e66ad-127">Производительность в файловых системах ОС</span><span class="sxs-lookup"><span data-stu-id="e66ad-127">Performance across OS file systems</span></span>

<span data-ttu-id="e66ad-128">Мы не рекомендуем работать с разными операционными системами, если на это нет особой причины.</span><span class="sxs-lookup"><span data-stu-id="e66ad-128">We recommend against working across operating systems with your files, unless you have a specific reason for doing so.</span></span> <span data-ttu-id="e66ad-129">Для ускорения производительности сохраняйте файлы в файловой системе WSL, если используете командную строку Linux (Ubuntu, OpenSUSE и т. д.).</span><span class="sxs-lookup"><span data-stu-id="e66ad-129">For the fastest performance speed, store your files in the WSL file system if you are working in a Linux command line (Ubuntu, OpenSUSE, etc).</span></span> <span data-ttu-id="e66ad-130">Если вы работаете в командной строке Windows (PowerShell, командной строке), сохраняйте файлы в файловой системе Windows.</span><span class="sxs-lookup"><span data-stu-id="e66ad-130">If you're working in a Windows command line (PowerShell, Command Prompt), store your files in the Windows file system.</span></span>

<span data-ttu-id="e66ad-131">Например, при хранении файлов проекта WSL:</span><span class="sxs-lookup"><span data-stu-id="e66ad-131">For example, when storing your WSL project files:</span></span>

- <span data-ttu-id="e66ad-132">Используйте корневой каталог файловой системы Linux: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`</span><span class="sxs-lookup"><span data-stu-id="e66ad-132">Use the Linux file system root directory: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`</span></span>
- <span data-ttu-id="e66ad-133">Не является корневым каталогом файловой системы Windows: `C:\Users\<user name>\Project`</span><span class="sxs-lookup"><span data-stu-id="e66ad-133">Not the Windows file system root directory: `C:\Users\<user name>\Project`</span></span>

<span data-ttu-id="e66ad-134">Доступ к корневой файловой системе Linux можно получить с помощью приложений и средств Windows, таких как проводник.</span><span class="sxs-lookup"><span data-stu-id="e66ad-134">You can access your Linux root file system with Windows apps and tools like File Explorer.</span></span> <span data-ttu-id="e66ad-135">Попробуйте открыть дистрибутив Linux (например, Ubuntu), убедитесь, что находитесь в домашнем каталоге Linux, введя следующую команду: `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="e66ad-135">Try opening a Linux distribution (like Ubuntu), be sure that you are in the Linux home directory by entering this command: `cd ~`.</span></span> <span data-ttu-id="e66ad-136">Затем откройте файловую систему Linux в проводнике, введя *(не забудьте точку в конце)* : `explorer.exe .`</span><span class="sxs-lookup"><span data-stu-id="e66ad-136">Then open your Linux file system in File Explorer by entering *(don't forget the period at the end)* : `explorer.exe .`</span></span>

<span data-ttu-id="e66ad-137">Подсистема WSL 2 доступна только в Windows 10 версии 1903, сборки 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="e66ad-137">WSL 2 is only available in Windows 10, Version 1903, Build 18362 or higher.</span></span> <span data-ttu-id="e66ad-138">Проверьте версию Windows, нажав **Windows + R** , введите **winver** , выберите **ОК** .</span><span class="sxs-lookup"><span data-stu-id="e66ad-138">Check your Windows version by selecting the **Windows logo key + R** , type **winver** , select **OK** .</span></span> <span data-ttu-id="e66ad-139">(Или введите команду `ver` в командной строке Windows).</span><span class="sxs-lookup"><span data-stu-id="e66ad-139">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="e66ad-140">Может потребоваться [выполнить обновление до последней версии Windows](ms-settings:windowsupdate).</span><span class="sxs-lookup"><span data-stu-id="e66ad-140">You may need to [update to the latest Windows version](ms-settings:windowsupdate).</span></span> <span data-ttu-id="e66ad-141">Для сборок ниже 18362 WSL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e66ad-141">For builds lower than 18362, WSL is not supported at all.</span></span>

> [!NOTE]
> <span data-ttu-id="e66ad-142">WSL 2 работает с [VMware 15.5.5 и более поздней версии](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) и [VirtualBox 6 и более поздней версии](https://www.virtualbox.org/wiki/Changelog-6.0).</span><span class="sxs-lookup"><span data-stu-id="e66ad-142">WSL 2 will work with [VMware 15.5.5+](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) and [VirtualBox 6+](https://www.virtualbox.org/wiki/Changelog-6.0).</span></span> <span data-ttu-id="e66ad-143">Дополнительные сведения см. в статье [Вопросы и ответы по WSL 2](./wsl2-faq.md#will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox).</span><span class="sxs-lookup"><span data-stu-id="e66ad-143">Learn more in our [WSL 2 FAQs.](./wsl2-faq.md#will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox)</span></span>

## <a name="whats-new-in-wsl-2"></a><span data-ttu-id="e66ad-144">Новые возможности в WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-144">What's new in WSL 2</span></span>

<span data-ttu-id="e66ad-145">WSL 2 — это основная модернизированная версия базовой архитектуры, которая использует технологию виртуализации и ядро Linux для реализации новых возможностей.</span><span class="sxs-lookup"><span data-stu-id="e66ad-145">WSL 2 is a major overhaul of the underlying architecture and uses virtualization technology and a Linux kernel to enable new features.</span></span> <span data-ttu-id="e66ad-146">Основные приоритеты этого обновления — увеличение производительности файловой системы и добавление полной совместимости системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="e66ad-146">The primary goals of this update are to increase file system performance and add full system call compatibility.</span></span>

- [<span data-ttu-id="e66ad-147">Системные требования WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-147">WSL 2 system requirements</span></span>](./install-win10.md#step-2---update-to-wsl-2)
- [<span data-ttu-id="e66ad-148">Обновление от WSL 1 до WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-148">Update from WSL 1 to WSL 2</span></span>](./install-win10.md#step-2---update-to-wsl-2)
- [<span data-ttu-id="e66ad-149">Часто задаваемые вопросы о WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-149">Frequently Asked Questions about WSL 2</span></span>](./wsl2-faq.md)

### <a name="wsl-2-architecture"></a><span data-ttu-id="e66ad-150">Архитектура WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-150">WSL 2 architecture</span></span>

<span data-ttu-id="e66ad-151">Во время обычной работы виртуальная машина может замедляться при загрузке, изолироваться, потреблять много ресурсов и требовать время для управления.</span><span class="sxs-lookup"><span data-stu-id="e66ad-151">A traditional VM experience can be slow to boot up, is isolated, consumes a lot of resources, and requires your time to manage it.</span></span> <span data-ttu-id="e66ad-152">В подсистеме WSL 2 нет таких проблем.</span><span class="sxs-lookup"><span data-stu-id="e66ad-152">WSL 2 does not have these attributes.</span></span>

<span data-ttu-id="e66ad-153">WSL 2 предоставляет преимущества WSL 1, включая простую интеграцию между Windows и Linux, быструю загрузку, незначительное потребление ресурсов и не требует настройки виртуальной машины или управления ею.</span><span class="sxs-lookup"><span data-stu-id="e66ad-153">WSL 2 provides the benefits of WSL 1, including seamless integration between Windows and Linux, fast boot times, a small resource footprint, and requires no VM configuration or management.</span></span> <span data-ttu-id="e66ad-154">Хотя WSL 2 использует виртуальную машину, она будет управляемой и будет работать в фоновом режиме, предоставляя тот же пользовательский интерфейс, что и WSL 1.</span><span class="sxs-lookup"><span data-stu-id="e66ad-154">While WSL 2 does use a VM, it is managed and run behind the scenes, leaving you with the same user experience as WSL 1.</span></span>

### <a name="full-linux-kernel"></a><span data-ttu-id="e66ad-155">Полнофункциональное ядро Linux</span><span class="sxs-lookup"><span data-stu-id="e66ad-155">Full Linux kernel</span></span>

<span data-ttu-id="e66ad-156">Ядро Linux в WSL 2 собрано собственными силами корпорации Майкрософт на основе последней стабильной ветви исходного кода, доступного по адресу kernel.org. Этот ядро специально настроено для WSL 2 путем оптимизации размера и производительности, чтобы обеспечить невероятное взаимодействие с Linux в Windows.</span><span class="sxs-lookup"><span data-stu-id="e66ad-156">The Linux kernel in WSL 2 is built by Microsoft from the latest stable branch, based on the source available at kernel.org. This kernel has been specially tuned for WSL 2, optimizing for size and performance to provide an amazing Linux experience on Windows.</span></span> <span data-ttu-id="e66ad-157">Ядро будет обслуживаться обновлениями Windows. Это означает, что вы получите новейшие исправления безопасности и улучшения ядра без необходимости заниматься этим самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="e66ad-157">The kernel will be serviced by Windows updates, which means you will get the latest security fixes and kernel improvements without needing to manage it yourself.</span></span>

<span data-ttu-id="e66ad-158">[Ядро Linux WSL 2 — это проект с открытым исходным кодом](https://github.com/microsoft/WSL2-Linux-Kernel).</span><span class="sxs-lookup"><span data-stu-id="e66ad-158">The [WSL 2 Linux kernel is open source](https://github.com/microsoft/WSL2-Linux-Kernel).</span></span> <span data-ttu-id="e66ad-159">Если вы хотите узнать больше, ознакомьтесь с записью блога [Реализация ядра Linux в Windows](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/), созданной группой, которая занималась сборкой ядра.</span><span class="sxs-lookup"><span data-stu-id="e66ad-159">If you'd like to learn more, check out the blog post [Shipping a Linux Kernel with Windows](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) written by the team that built it.</span></span>

### <a name="increased-file-io-performance"></a><span data-ttu-id="e66ad-160">Повышенная производительность операций ввода-вывода файлов</span><span class="sxs-lookup"><span data-stu-id="e66ad-160">Increased file IO performance</span></span>

<span data-ttu-id="e66ad-161">Команды для операций с большими объемами файлов, такие как git clone, npm install, apt update, apt upgrade и другие, с WSL 2 выполняются заметно быстрее.</span><span class="sxs-lookup"><span data-stu-id="e66ad-161">File intensive operations like git clone, npm install, apt update, apt upgrade, and more are all noticeably faster with WSL 2.</span></span>

<span data-ttu-id="e66ad-162">Фактическое увеличение скорости будет зависеть от того, какое приложение вы используете и как оно взаимодействует с файловой системой.</span><span class="sxs-lookup"><span data-stu-id="e66ad-162">The actual speed increase will depend on which app you're running and how it is interacting with the file system.</span></span> <span data-ttu-id="e66ad-163">Первоначальные версии WSL 2 запускаются в 20 раз быстрее по сравнению с WSL 1 при распаковке сжатого архива tarball и в 2–5 раз быстрее при использовании команд git clone, npm install и cmake в различных проектах.</span><span class="sxs-lookup"><span data-stu-id="e66ad-163">Initial versions of WSL 2 run up to 20x faster compared to WSL 1 when unpacking a zipped tarball, and around 2-5x faster when using git clone, npm install and cmake on various projects.</span></span>

### <a name="full-system-call-compatibility"></a><span data-ttu-id="e66ad-164">Полная совместимость системных вызовов</span><span class="sxs-lookup"><span data-stu-id="e66ad-164">Full system call compatibility</span></span>

<span data-ttu-id="e66ad-165">Двоичные файлы Linux используют системные вызовы для выполнения функций, таких как доступ к файлам, запрос памяти, создание процессов и многое другое.</span><span class="sxs-lookup"><span data-stu-id="e66ad-165">Linux binaries use system calls to perform functions such as accessing files, requesting memory, creating processes, and more.</span></span> <span data-ttu-id="e66ad-166">В то время как WSL 1 использует уровень перевода, созданный командой WSL, WSL 2 имеет собственное ядро Linux с полной совместимостью системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="e66ad-166">Whereas WSL 1 used a translation layer that was built by the WSL team, WSL 2 includes its own Linux kernel with full system call compatibility.</span></span> <span data-ttu-id="e66ad-167">Доступные преимущества:</span><span class="sxs-lookup"><span data-stu-id="e66ad-167">Benefits include:</span></span>

- <span data-ttu-id="e66ad-168">целый ряд новых приложений, которые можно запускать внутри WSL, например **[Docker](tutorials/wsl-containers.md)** и другие;</span><span class="sxs-lookup"><span data-stu-id="e66ad-168">A whole new set of apps that you can run inside of WSL, such as **[Docker](tutorials/wsl-containers.md)** and more.</span></span>

- <span data-ttu-id="e66ad-169">все обновления ядра Linux немедленно готовы к использованию.</span><span class="sxs-lookup"><span data-stu-id="e66ad-169">Any updates to the Linux kernel are immediately ready for use.</span></span> <span data-ttu-id="e66ad-170">(Вам не нужно ждать, пока специалисты WSL реализуют обновления и добавят изменения).</span><span class="sxs-lookup"><span data-stu-id="e66ad-170">(You don't have to wait for the WSL team to implement updates and add the changes).</span></span>

### <a name="wsl-2-uses-a-smaller-amount-of-memory-on-startup"></a><span data-ttu-id="e66ad-171">WSL 2 использует меньший объем памяти при запуске</span><span class="sxs-lookup"><span data-stu-id="e66ad-171">WSL 2 uses a smaller amount of memory on startup</span></span>

<span data-ttu-id="e66ad-172">WSL 2 использует упрощенную служебную виртуальную машину на реальном ядре Linux с небольшим потреблением памяти.</span><span class="sxs-lookup"><span data-stu-id="e66ad-172">WSL 2 uses a lightweight utility VM on a real Linux kernel with a small memory footprint.</span></span> <span data-ttu-id="e66ad-173">Эта программа будет выделять память с виртуальным адресом при запуске.</span><span class="sxs-lookup"><span data-stu-id="e66ad-173">The utility will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="e66ad-174">Она настроена на запуск с использованием незначительной доли общей памяти, которая требовалось для WSL 1.</span><span class="sxs-lookup"><span data-stu-id="e66ad-174">It is configured to start with a smaller proportion of your total memory that what was required for WSL 1.</span></span>

## <a name="exceptions-for-using-wsl-1-rather-than-wsl-2"></a><span data-ttu-id="e66ad-175">Исключения для использования WSL 1 вместо WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-175">Exceptions for using WSL 1 rather than WSL 2</span></span>

<span data-ttu-id="e66ad-176">Рекомендуется использовать WSL 2, так как он обеспечивает более высокую производительность и полную совместимость системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="e66ad-176">We recommend that you use WSL 2 as it offers faster performance and 100% system call compatibility.</span></span> <span data-ttu-id="e66ad-177">Однако существует несколько отдельных сценариев, в которых использовать WSL 1 может оказаться более предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="e66ad-177">However, there are a few specific scenarios where you might prefer using WSL 1.</span></span> <span data-ttu-id="e66ad-178">Рекомендуем использовать WSL 1, если:</span><span class="sxs-lookup"><span data-stu-id="e66ad-178">Consider using WSL 1 if:</span></span>

- <span data-ttu-id="e66ad-179">Файлы проекта должны храниться в файловой системе Windows.</span><span class="sxs-lookup"><span data-stu-id="e66ad-179">Your project files must be stored in the Windows file system.</span></span> <span data-ttu-id="e66ad-180">WSL 1 обеспечивает более быстрый доступ к файлам, подключенным из Windows.</span><span class="sxs-lookup"><span data-stu-id="e66ad-180">WSL 1 offers faster access to files mounted from Windows.</span></span>
  - <span data-ttu-id="e66ad-181">Если вы будете использовать дистрибутив Linux WSL для доступа к файлам проекта в файловой системе Windows, и эти файлы не могут храниться в файловой системе Linux, вы получите более высокую производительность в файловых системах ОС, используя WSL 1.</span><span class="sxs-lookup"><span data-stu-id="e66ad-181">If you will be using your WSL Linux distribution to access project files on the Windows file system, and these files cannot be stored on the Linux file system, you will achieve faster performance across the OS files systems by using WSL 1.</span></span>
- <span data-ttu-id="e66ad-182">Проект, для которого требуется перекрестная компиляция с использованием средств Windows и Linux на одних и тех же файлах.</span><span class="sxs-lookup"><span data-stu-id="e66ad-182">A project which requires cross-compilation using both Windows and Linux tools on the same files.</span></span>
  - <span data-ttu-id="e66ad-183">Операции с файлами в операционных системах Windows и Linux выполняются быстрее в WSL 1, чем на WSL 2. Поэтому если вы используете приложения Windows для доступа к файлам Linux, в настоящее время вы получите более высокую производительность при использовании WSL 1.</span><span class="sxs-lookup"><span data-stu-id="e66ad-183">File performance across the Windows and Linux operating systems is faster in WSL 1 than WSL 2, so if you are using Windows applications to access Linux files, you will currently achieve faster performance with WSL 1.</span></span>

> [!NOTE]
> <span data-ttu-id="e66ad-184">Попробуйте использовать [удаленное расширение WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) VS Code, чтобы хранить файлы проекта в файловой системе Linux, используя средства командной строки Linux. Также с помощью VS Code в Windows можно создавать, редактировать, отлаживать или запускать проекты в браузере без снижения производительности, связанной с работой в файловых системах Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="e66ad-184">Consider trying the VS Code [Remote WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) to enable you to store your project files on the Linux file system, using Linux command line tools, but also using VS Code on Windows to author, edit, debug, or run your project in an internet browser without any of the performance slow-downs associated with working across the Linux and Windows file systems.</span></span> <span data-ttu-id="e66ad-185">[Подробнее.](tutorials/wsl-vscode.md)</span><span class="sxs-lookup"><span data-stu-id="e66ad-185">[Learn more](tutorials/wsl-vscode.md).</span></span>

## <a name="accessing-network-applications"></a><span data-ttu-id="e66ad-186">Доступ к сетевым приложениям</span><span class="sxs-lookup"><span data-stu-id="e66ad-186">Accessing network applications</span></span>

### <a name="accessing-linux-networking-apps-from-windows-localhost"></a><span data-ttu-id="e66ad-187">Доступ к сетевым приложениям Linux из Windows (localhost)</span><span class="sxs-lookup"><span data-stu-id="e66ad-187">Accessing Linux networking apps from Windows (localhost)</span></span>

<span data-ttu-id="e66ad-188">Если вы создаете сетевое приложение (например, приложение, работающее на NodeJS или SQL Server) в дистрибутиве Linux, вы можете получить к нему доступ из приложения Windows (например, используя Microsoft Edge или Chrome) с помощью `localhost` (как обычно это и происходит).</span><span class="sxs-lookup"><span data-stu-id="e66ad-188">If you are building a networking app (for example an app running on a NodeJS or SQL server) in your Linux distribution, you can access it from a Windows app (like your Edge or Chrome internet browser) using `localhost` (just like you normally would).</span></span>

<span data-ttu-id="e66ad-189">Тем не менее, если вы используете более раннюю версию Windows (сборка 18945 или меньше), вам потребуется получить IP-адрес виртуальной машины узла Linux (или [обновить ее до последней версии Windows](ms-settings:windowsupdate)).</span><span class="sxs-lookup"><span data-stu-id="e66ad-189">However, if you are running an older version of Windows (Build 18945 or less), you will need to get the IP address of the Linux host VM (or [update to the latest Windows version](ms-settings:windowsupdate)).</span></span>

<span data-ttu-id="e66ad-190">Чтобы найти IP-адрес виртуальной машины, содержащей дистрибутив Linux, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e66ad-190">To find the IP address of the virtual machine powering your Linux distribution:</span></span>

- <span data-ttu-id="e66ad-191">В дистрибутиве WSL (напр., Ubuntu) выполните команду: `ip addr`</span><span class="sxs-lookup"><span data-stu-id="e66ad-191">From your WSL distribution (ie Ubuntu), run the command: `ip addr`</span></span>
- <span data-ttu-id="e66ad-192">Найдите и скопируйте адрес в значение `inet` интерфейса `eth0`.</span><span class="sxs-lookup"><span data-stu-id="e66ad-192">Find and copy the address under the `inet` value of the `eth0` interface.</span></span>
- <span data-ttu-id="e66ad-193">Если у вас установлено средство grep, найдите его с помощью команды: `ip addr | grep eth0`</span><span class="sxs-lookup"><span data-stu-id="e66ad-193">If you have the grep tool installed, find this more easily by filtering the output with the command: `ip addr | grep eth0`</span></span>
- <span data-ttu-id="e66ad-194">Подключитесь к серверу Linux, используя этот IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e66ad-194">Connect to your Linux server using this IP address.</span></span>

<span data-ttu-id="e66ad-195">На изображении ниже показан пример подключения к серверу Node.js с помощью браузера Edge.</span><span class="sxs-lookup"><span data-stu-id="e66ad-195">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![Подключение к серверу NodeJS с помощью Edge](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-networking-apps-from-linux-host-ip"></a><span data-ttu-id="e66ad-197">Доступ к сетевым приложениям Windows из Linux (IP-адрес основной системы)</span><span class="sxs-lookup"><span data-stu-id="e66ad-197">Accessing Windows networking apps from Linux (host IP)</span></span>

<span data-ttu-id="e66ad-198">Если вы хотите получить доступ к сетевому приложению, работающему в Windows (например, к приложению, работающему на NodeJS или SQL Server) из дистрибутива Linux (напр., Ubuntu), необходимо использовать IP-адрес основной системы.</span><span class="sxs-lookup"><span data-stu-id="e66ad-198">If you want to access a networking app running on Windows (for example an app running on a NodeJS or SQL server) from your Linux distribution (ie Ubuntu), then you need to use the IP address of your host machine.</span></span> <span data-ttu-id="e66ad-199">Хотя это происходит и нечасто, для этого можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e66ad-199">While this is not a common scenario, you can follow these steps to make it work.</span></span>
    - <span data-ttu-id="e66ad-200">Получите IP-адрес основной системы, выполнив следующую команду из дистрибутива Linux: `cat /etc/resolv.conf`</span><span class="sxs-lookup"><span data-stu-id="e66ad-200">Obtain the IP address of your host machine by running this command from your Linux distribution: `cat /etc/resolv.conf`</span></span>
    - <span data-ttu-id="e66ad-201">Скопируйте IP-адрес в строке, начинающейся с `nameserver`.</span><span class="sxs-lookup"><span data-stu-id="e66ad-201">Copy the IP address following the term: `nameserver`.</span></span>
    - <span data-ttu-id="e66ad-202">Подключитесь к любому серверу Windows, используя скопированный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e66ad-202">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="e66ad-203">На изображении ниже показан пример подключения к серверу Node.js под управлением Windows через cURL.</span><span class="sxs-lookup"><span data-stu-id="e66ad-203">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span>

![Подключение к серверу NodeJS в Windows с помощью cURL](media/wsl2-network-l2w.png)

### <a name="additional-networking-considerations"></a><span data-ttu-id="e66ad-205">Дополнительные рекомендации по работе с сетью</span><span class="sxs-lookup"><span data-stu-id="e66ad-205">Additional networking considerations</span></span>

#### <a name="connecting-via-remote-ip-addresses"></a><span data-ttu-id="e66ad-206">Подключение через удаленные IP-адреса</span><span class="sxs-lookup"><span data-stu-id="e66ad-206">Connecting via remote IP addresses</span></span>

<span data-ttu-id="e66ad-207">При использовании удаленных IP-адресов для подключения к приложениям они будут рассматриваться как подключения из локальной сети (LAN).</span><span class="sxs-lookup"><span data-stu-id="e66ad-207">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="e66ad-208">Это означает, что необходимо убедиться, что приложение может принимать подключения по локальной сети.</span><span class="sxs-lookup"><span data-stu-id="e66ad-208">This means that you will need to make sure your application can accept LAN connections.</span></span>

<span data-ttu-id="e66ad-209">Например, может потребоваться привязать приложение к `0.0.0.0` вместо `127.0.0.1`.</span><span class="sxs-lookup"><span data-stu-id="e66ad-209">For example, you may need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="e66ad-210">В примере приложения Python, использующего Flask, это можно сделать с помощью команды `app.run(host='0.0.0.0')`.</span><span class="sxs-lookup"><span data-stu-id="e66ad-210">In the example of a Python app using Flask, this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="e66ad-211">При внесении этих изменений не забывайте о безопасности, так как это позволит устанавливать подключения из вашей локальной сети.</span><span class="sxs-lookup"><span data-stu-id="e66ad-211">Please keep security in mind when making these changes as this will allow connections from your LAN.</span></span>

#### <a name="accessing-a-wsl-2-distribution-from-your-local-area-network-lan"></a><span data-ttu-id="e66ad-212">Доступ к дистрибутиву WSL 2 из локальной сети (LAN)</span><span class="sxs-lookup"><span data-stu-id="e66ad-212">Accessing a WSL 2 distribution from your local area network (LAN)</span></span>

<span data-ttu-id="e66ad-213">При использовании дистрибутива WSL 1, если к компьютеру можно получить доступ из локальной сети, то приложения, работающие в WSL, могут быть также доступны в локальной сети.</span><span class="sxs-lookup"><span data-stu-id="e66ad-213">When using a WSL 1 distribution, if your computer was set up to be accessed by your LAN, then applications run in WSL could be accessed on your LAN as well.</span></span>

<span data-ttu-id="e66ad-214">Это нетипичная ситуация в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="e66ad-214">This isn't the default case in WSL 2.</span></span> <span data-ttu-id="e66ad-215">В WSL 2 имеется виртуализированный адаптер Ethernet с собственным уникальным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="e66ad-215">WSL 2 has a virtualized ethernet adapter with its own unique IP address.</span></span> <span data-ttu-id="e66ad-216">В настоящее время для включения этого рабочего процесса необходимо выполнить те же действия, что и для обычной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e66ad-216">Currently, to enable this workflow you will need to go through the same steps as you would for a regular virtual machine.</span></span> <span data-ttu-id="e66ad-217">(Мы ищем способы улучшить это взаимодействие.)</span><span class="sxs-lookup"><span data-stu-id="e66ad-217">(We are looking into ways to improve this experience.)</span></span>

<span data-ttu-id="e66ad-218">Ниже приводится пример команды PowerShell, которая добавляет прокси-сервер портов, ожидающий передачи данных на порту узла 4000 и перенаправляющий все подключения на порт 4000 виртуальной машины WSL 2 с IP-адресом 192.168.101.100.</span><span class="sxs-lookup"><span data-stu-id="e66ad-218">Here's an example PowerShell command to add a port proxy that listens on port 4000 on the host and connects it to port 4000 to the WSL 2 VM with IP address 192.168.101.100.</span></span>

```powershell
netsh interface portproxy add v4tov4 listenport=4000 listenaddress=0.0.0.0 connectport=4000 connectaddress=192.168.101.100
```

#### <a name="ipv6-access"></a><span data-ttu-id="e66ad-219">Доступ по протоколу IPv6</span><span class="sxs-lookup"><span data-stu-id="e66ad-219">IPv6 access</span></span>

<span data-ttu-id="e66ad-220">В настоящее время дистрибутивы WSL 2 не могут обращаться к IPv6-адресам.</span><span class="sxs-lookup"><span data-stu-id="e66ad-220">WSL 2 distributions currently cannot reach IPv6-only addresses.</span></span> <span data-ttu-id="e66ad-221">Мы работаем над добавлением этой возможности.</span><span class="sxs-lookup"><span data-stu-id="e66ad-221">We are working on adding this feature.</span></span>

## <a name="expanding-the-size-of-your-wsl-2-virtual-hard-disk"></a><span data-ttu-id="e66ad-222">Увеличение размера виртуального жесткого диска WSL 2</span><span class="sxs-lookup"><span data-stu-id="e66ad-222">Expanding the size of your WSL 2 Virtual Hard Disk</span></span>

<span data-ttu-id="e66ad-223">Для хранения файлов Linux в WSL 2 используется виртуальный жесткий диск (VHD).</span><span class="sxs-lookup"><span data-stu-id="e66ad-223">WSL 2 uses a Virtual Hard Disk (VHD) to store your Linux files.</span></span> <span data-ttu-id="e66ad-224">В WSL 2 виртуальный жесткий диск существует в виде *VHDX* -файла на жестком диске Windows.</span><span class="sxs-lookup"><span data-stu-id="e66ad-224">In WSL 2, a VHD is represented on your Windows hard drive as a *.vhdx* file.</span></span>

<span data-ttu-id="e66ad-225">Виртуальный жесткий диск WSL 2 использует файловую систему ext4.</span><span class="sxs-lookup"><span data-stu-id="e66ad-225">The WSL 2 VHD uses the ext4 file system.</span></span> <span data-ttu-id="e66ad-226">Этот виртуальный жесткий диск имеет начальный максимальный размер 256 ГБ, и он автоматически изменяется по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="e66ad-226">This VHD automatically resizes to meet your storage needs and has an initial maximum size of 256GB.</span></span> <span data-ttu-id="e66ad-227">Если объем хранилища, необходимый для файлов Linux, превышает этот размер, вам следует увеличить его.</span><span class="sxs-lookup"><span data-stu-id="e66ad-227">If the storage space required by your Linux files exceeds this size you may need to expand it.</span></span> <span data-ttu-id="e66ad-228">Если размер дистрибутива превысил 256 ГБ, вы увидите сообщение о том, что закончилось место на диске.</span><span class="sxs-lookup"><span data-stu-id="e66ad-228">If your distribution grows in size to be greater than 256GB, you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="e66ad-229">Эту ошибку можно устранить, увеличив размер виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="e66ad-229">You can fix this error by expanding the VHD size.</span></span>

<span data-ttu-id="e66ad-230">Чтобы увеличить максимальный размер виртуального жесткого диска свыше 256 ГБ:</span><span class="sxs-lookup"><span data-stu-id="e66ad-230">To expand your maximum VHD size beyond 256GB:</span></span>

1. <span data-ttu-id="e66ad-231">Завершите работы всех экземпляров WSL с помощью команды `wsl --shutdown`.</span><span class="sxs-lookup"><span data-stu-id="e66ad-231">Terminate all WSL instances using the command: `wsl --shutdown`</span></span>

2. <span data-ttu-id="e66ad-232">Найдите имя пакета установки дистрибутива ("PackageFamilyName").</span><span class="sxs-lookup"><span data-stu-id="e66ad-232">Find your distribution installation package name ('PackageFamilyName')</span></span>
    - <span data-ttu-id="e66ad-233">С помощью PowerShell (где "distro" — имя дистрибутива) введите команду:</span><span class="sxs-lookup"><span data-stu-id="e66ad-233">Using PowerShell (where 'distro' is your distribution name) enter the command:</span></span>
    - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`

3. <span data-ttu-id="e66ad-234">Выберите VHD-файл `fullpath`, используемый в WSL 2. Здесь это будет `pathToVHD`:</span><span class="sxs-lookup"><span data-stu-id="e66ad-234">Locate the VHD file `fullpath` used by your WSL 2 installation, this will be your `pathToVHD`:</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`

4. <span data-ttu-id="e66ad-235">Измените размер VHD WSL 2, выполнив следующие команды.</span><span class="sxs-lookup"><span data-stu-id="e66ad-235">Resize your WSL 2 VHD by completing the following commands:</span></span>
   - <span data-ttu-id="e66ad-236">Откройте командную строку Windows с правами администратора и введите:</span><span class="sxs-lookup"><span data-stu-id="e66ad-236">Open Windows Command Prompt with admin privileges and enter:</span></span>

      ```powershell
      diskpart
      DISKPART> Select vdisk file="<pathToVHD>"
      DISKPART> detail vdisk
      ```

   - <span data-ttu-id="e66ad-237">Изучите выходные данные команды **detail** .</span><span class="sxs-lookup"><span data-stu-id="e66ad-237">Examine the output of the **detail** command.</span></span>  <span data-ttu-id="e66ad-238">Эти выходные данные будут содержать значение **Virtual size** (Объем виртуальной памяти).</span><span class="sxs-lookup"><span data-stu-id="e66ad-238">The output will include a value for **Virtual size** .</span></span>  <span data-ttu-id="e66ad-239">Это текущее максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="e66ad-239">This is the current maximum.</span></span>  <span data-ttu-id="e66ad-240">Переведите это значение в мегабайты.</span><span class="sxs-lookup"><span data-stu-id="e66ad-240">Convert this value to megabytes.</span></span>  <span data-ttu-id="e66ad-241">Новое значение после изменения размера должно быть больше полученного значения.</span><span class="sxs-lookup"><span data-stu-id="e66ad-241">The new value after resizing must be greater than this value.</span></span>  <span data-ttu-id="e66ad-242">Например, если команда **detail** возвращает значение **Virtual size: 256 GB** , необходимо предоставить значение больше, чем **256000** .</span><span class="sxs-lookup"><span data-stu-id="e66ad-242">For example, if the **detail** output shows **Virtual size: 256 GB** , then you must specify a value greater than **256000** .</span></span>  <span data-ttu-id="e66ad-243">Получив новый размер в мегабайтах, введите следующую команду в **diskpart** :</span><span class="sxs-lookup"><span data-stu-id="e66ad-243">Once you have your new size in megabytes, enter the following command in **diskpart** :</span></span>

      ```powershell
      DISKPART> expand vdisk maximum=<sizeInMegaBytes>
      ```

   - <span data-ttu-id="e66ad-244">Выход из **diskpart**</span><span class="sxs-lookup"><span data-stu-id="e66ad-244">Exit **diskpart**</span></span>

      ```powershell
      DISKPART> exit
      ```

5. <span data-ttu-id="e66ad-245">Запустите дистрибутив WSL (например, Ubuntu).</span><span class="sxs-lookup"><span data-stu-id="e66ad-245">Launch your WSL distribution (Ubuntu, for example).</span></span>

6. <span data-ttu-id="e66ad-246">Сообщите WSL, что можно увеличить размер файловой системы, выполнив следующие команды в командной строке дистрибутива Linux:</span><span class="sxs-lookup"><span data-stu-id="e66ad-246">Make WSL aware that it can expand its file system's size by running these commands from your Linux distribution command line.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e66ad-247">В ответ на первую команду **mount** может появиться такое сообщение: **/dev: none already mounted on /dev** (в этот момент устройство none уже подключено к /dev).</span><span class="sxs-lookup"><span data-stu-id="e66ad-247">You may see this message in response to the first **mount** command: **/dev: none already mounted on /dev** .</span></span>  <span data-ttu-id="e66ad-248">Это сообщение можно спокойно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="e66ad-248">This message can safely be ignored.</span></span>

   ```powershell
      sudo mount -t devtmpfs none /dev
      mount | grep ext4
   ```

   <span data-ttu-id="e66ad-249">Скопируйте имя этой записи, которая будет выглядеть следующим образом: `/dev/sdX` (где X обозначает любой символ).</span><span class="sxs-lookup"><span data-stu-id="e66ad-249">Copy the name of this entry, which will look like: `/dev/sdX` (with the X representing any other character).</span></span>  <span data-ttu-id="e66ad-250">В следующем примере значение **X** равно **b** :</span><span class="sxs-lookup"><span data-stu-id="e66ad-250">In the following example the value of **X** is **b** :</span></span>

   ```powershell
      sudo resize2fs /dev/sdb <sizeInMegabytes>M
   ```

   > [!NOTE]
   > <span data-ttu-id="e66ad-251">Возможно, придется установить приложение **resize2fs** .</span><span class="sxs-lookup"><span data-stu-id="e66ad-251">You may need to install **resize2fs** .</span></span>  <span data-ttu-id="e66ad-252">Для этого можно использовать такую команду: `sudo apt install resize2fs`.</span><span class="sxs-lookup"><span data-stu-id="e66ad-252">If so, you can use this command to install it:  `sudo apt install resize2fs`.</span></span>

   <span data-ttu-id="e66ad-253">Вывод имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="e66ad-253">The output will look similar to the following:</span></span>

   ```bash
      resize2fs 1.44.1 (24-Mar-2018)
      Filesystem at /dev/sdb is mounted on /; on-line resizing required
      old_desc_blocks = 32, new_desc_blocks = 38
      The filesystem on /dev/sdb is now 78643200 (4k) blocks long.
      ```

> [!NOTE]
> <span data-ttu-id="e66ad-254">Как правило, не следует изменять, перемещать файлы, связанные с WSL, расположенным внутри папки AppData, или получать к ним доступ с помощью инструментов или редакторов Windows.</span><span class="sxs-lookup"><span data-stu-id="e66ad-254">In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="e66ad-255">Это может привести к повреждению дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="e66ad-255">Doing so could cause your Linux distribution to become corrupted.</span></span>
