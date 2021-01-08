---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Узнайте, как установить дистрибутивы Linux (включая Ubuntu, Debian, SUSE, Kali, Fedora, Pengwin и Alpine) на компьютере под управлением Windows 10 с помощью терминала Bash.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка, включить, WSL2, версия 2
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: cbfd1f1aab99bc1965e569c4e818bd1663aa2878
ms.sourcegitcommit: f5b14630947ee9cf3438e9ba502bfbe85ed72cd1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "97957695"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="884e1-104">Руководство по установке подсистемы Windows для Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="884e1-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

<span data-ttu-id="884e1-105">Возможны два варианта установки подсистемы Windows для Linux (WSL):</span><span class="sxs-lookup"><span data-stu-id="884e1-105">There are two options available for installing Windows Subsystem for Linux (WSL):</span></span>

- <span data-ttu-id="884e1-106">**[Упрощенная установка](#simplified-installation-for-windows-insiders)** *(предварительный выпуск)* : `wsl --install`.</span><span class="sxs-lookup"><span data-stu-id="884e1-106">**[Simplified install](#simplified-installation-for-windows-insiders)** *(preview release)*: `wsl --install`</span></span>

    <span data-ttu-id="884e1-107">Для выполнения упрощенной команды установки `wsl --install` нужно присоединиться к [Программе предварительной оценки Windows](https://insider.windows.com/getting-started) и установить предварительную сборку Windows 10 (сборка ОС 20262 или более поздняя). При этом вам не потребуется выполнять шаги установки вручную.</span><span class="sxs-lookup"><span data-stu-id="884e1-107">The `wsl --install` simplified install command requires that you join the [Windows Insiders Program](https://insider.windows.com/getting-started) and install a preview build of Windows 10 (OS build 20262 or higher), but eliminates the need to follow the manual install steps.</span></span> <span data-ttu-id="884e1-108">Все что нужно сделать — это открыть окно командной строки с правами администратора и запустить команду `wsl --install`. После перезапуска вы сможете использовать WSL.</span><span class="sxs-lookup"><span data-stu-id="884e1-108">All you need to do is open a command window with administrator privileges and run `wsl --install`, after a restart you will be ready to use WSL.</span></span>

- <span data-ttu-id="884e1-109">**[Установка вручную](#manual-installation-steps)** : выполните приведенные ниже шаги.</span><span class="sxs-lookup"><span data-stu-id="884e1-109">**[Manual install](#manual-installation-steps)**: Follow the six steps listed below.</span></span>

    <span data-ttu-id="884e1-110">Ниже указаны шаги по установке WSL вручную, которые также можно использовать для установки Linux в любой версии Windows 10.</span><span class="sxs-lookup"><span data-stu-id="884e1-110">The manual install steps for WSL are listed below and can be used to install Linux on any version of Windows 10.</span></span>

## <a name="simplified-installation-for-windows-insiders"></a><span data-ttu-id="884e1-111">Упрощенная установка для участников программы предварительной оценки Windows</span><span class="sxs-lookup"><span data-stu-id="884e1-111">Simplified Installation for Windows Insiders</span></span>

<span data-ttu-id="884e1-112">Процесс установки подсистемы Windows для Linux был значительно улучшен в последних предварительных сборках Windows 10 для участников программы предварительной оценки Windows — приведенные ниже шаги, которые выполняются вручную, были заменены одной командой.</span><span class="sxs-lookup"><span data-stu-id="884e1-112">The installation process for Windows Subsystem for Linux has been significantly improved in the latest Windows Insiders preview builds of Windows 10, replacing the manual steps below with a single command.</span></span>

<span data-ttu-id="884e1-113">Чтобы использовать упрощенную команду установки `wsl --install`, вы должны:</span><span class="sxs-lookup"><span data-stu-id="884e1-113">In order to use the `wsl --install` simplified install command, you must:</span></span>

- <span data-ttu-id="884e1-114">присоединиться к [Программе предварительной оценки Windows](https://insider.windows.com/getting-started);</span><span class="sxs-lookup"><span data-stu-id="884e1-114">Join the [Windows Insiders Program](https://insider.windows.com/getting-started)</span></span>
- <span data-ttu-id="884e1-115">установить предварительную сборку Windows 10 (сборка ОС 20262 или более поздней версии);</span><span class="sxs-lookup"><span data-stu-id="884e1-115">Install a preview build of Windows 10 (OS build 20262 or higher).</span></span>
- <span data-ttu-id="884e1-116">открыть окно командной строки от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="884e1-116">Open a command line windows with Administrator privileges</span></span>

<span data-ttu-id="884e1-117">Если эти требования выполнены, выполните следующие действия, чтобы установить WSL:</span><span class="sxs-lookup"><span data-stu-id="884e1-117">Once those requirements are met, to install WSL:</span></span>

- <span data-ttu-id="884e1-118">В командной строке, открытой в режиме администратора, выполните команду `wsl.exe --install`.</span><span class="sxs-lookup"><span data-stu-id="884e1-118">Enter this command in the command line you've opened in Admin mode: `wsl.exe --install`</span></span>
- <span data-ttu-id="884e1-119">Перезапустите компьютер.</span><span class="sxs-lookup"><span data-stu-id="884e1-119">Restart your machine</span></span>

<span data-ttu-id="884e1-120">При первом запуске недавно установленного дистрибутива Linux откроется окно консоли, и вам будет предложено подождать, чтобы файлы распаковались и сохранились на компьютере.</span><span class="sxs-lookup"><span data-stu-id="884e1-120">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="884e1-121">Все будущие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="884e1-121">All future launches should take less than a second.</span></span>

<span data-ttu-id="884e1-122">Затем необходимо будет [создать учетную запись пользователя и пароль для нового дистрибутива Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="884e1-122">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

<span data-ttu-id="884e1-123">**Поздравляем! Вы успешно установили и настроили дистрибутив Linux, который полностью интегрирован с операционной системой Windows.**</span><span class="sxs-lookup"><span data-stu-id="884e1-123">**CONGRATULATIONS! You've successfully installed and set up a Linux distribution that is completely integrated with your Windows operating system!**</span></span>

<span data-ttu-id="884e1-124">Команда --install выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="884e1-124">The --install command performs the following actions:</span></span>

- <span data-ttu-id="884e1-125">включает дополнительные компоненты WSL и платформы виртуальных машин;</span><span class="sxs-lookup"><span data-stu-id="884e1-125">Enables the optional WSL and Virtual Machine Platform components</span></span>
- <span data-ttu-id="884e1-126">скачивает и устанавливает последнюю версию ядра Linux;</span><span class="sxs-lookup"><span data-stu-id="884e1-126">Downloads and installs the latest Linux kernel</span></span>
- <span data-ttu-id="884e1-127">задает WSL 2 в качестве среды по умолчанию;</span><span class="sxs-lookup"><span data-stu-id="884e1-127">Sets WSL 2 as the default</span></span>
- <span data-ttu-id="884e1-128">скачивает и устанавливает дистрибутив Linux *(может потребоваться перезагрузка)* .</span><span class="sxs-lookup"><span data-stu-id="884e1-128">Downloads and installs a Linux distribution *(reboot may be required)*</span></span>

<span data-ttu-id="884e1-129">По умолчанию в качестве устанавливаемого дистрибутива Linux используется Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="884e1-129">By default, the installed Linux distribution will be Ubuntu.</span></span> <span data-ttu-id="884e1-130">Чтобы изменить дистрибутив, используйте команду `wsl --install -d <Distribution Name>`.</span><span class="sxs-lookup"><span data-stu-id="884e1-130">This can be changed using `wsl --install -d <Distribution Name>`.</span></span> <span data-ttu-id="884e1-131">*(Замените `<Distribution Name>` именем нужного дистрибутива.)* Дополнительные дистрибутивы Linux можно добавить на компьютер после первоначальной установки — для этого выполните команду `wsl --install -d <Distribution Name>`.</span><span class="sxs-lookup"><span data-stu-id="884e1-131">*(Replacing `<Distribution Name>` with the name of your desired distribution.)* Additional Linux distributions may be added to your machine after the initial install using the `wsl --install -d <Distribution Name>` command.</span></span>

<span data-ttu-id="884e1-132">Чтобы просмотреть список доступных дистрибутивов Linux, введите `wsl --list --online`.</span><span class="sxs-lookup"><span data-stu-id="884e1-132">To see a list of available Linux distributions, enter `wsl --list --online`.</span></span>

## <a name="manual-installation-steps"></a><span data-ttu-id="884e1-133">Шаги по установке вручную</span><span class="sxs-lookup"><span data-stu-id="884e1-133">Manual Installation Steps</span></span>

<span data-ttu-id="884e1-134">Если вы не используете сборку для участников программы предварительной оценки Windows, компоненты, необходимые для WSL, потребуется включить вручную. Для этого выполните приведенные ниже шаги.</span><span class="sxs-lookup"><span data-stu-id="884e1-134">If you are not on a Windows Insiders build, the features required for WSL will need to be enabled manually following the steps below.</span></span>

## <a name="step-1---enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="884e1-135">Шаг 1. Включение подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="884e1-135">Step 1 - Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="884e1-136">Перед установкой дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux".</span><span class="sxs-lookup"><span data-stu-id="884e1-136">You must first enable the "Windows Subsystem for Linux" optional feature before installing any Linux distributions on Windows.</span></span>

<span data-ttu-id="884e1-137">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="884e1-137">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="884e1-138">Теперь перейдите к шагу 2 и выполните обновление до WSL 2. Если вы хотите установить только WSL 1, вы можете **перезагрузить** компьютер и перейти к разделу [Шаг 6. Установка дистрибутива Linux по выбору](./install-win10.md#step-6---install-your-linux-distribution-of-choice).</span><span class="sxs-lookup"><span data-stu-id="884e1-138">We recommend now moving on to step #2, updating to WSL 2, but if you wish to only install WSL 1, you can now **restart** your machine and move on to [Step 6 - Install your Linux distribution of choice](./install-win10.md#step-6---install-your-linux-distribution-of-choice).</span></span> <span data-ttu-id="884e1-139">Чтобы выполнить обновление до WSL 2, **дождитесь перезагрузки** компьютера и перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="884e1-139">To update to WSL 2, **wait to restart** your machine and move on to the next step.</span></span>

## <a name="step-2---check-requirements-for-running-wsl-2"></a><span data-ttu-id="884e1-140">Шаг 2. Проверка требований для запуска WSL 2</span><span class="sxs-lookup"><span data-stu-id="884e1-140">Step 2 - Check requirements for running WSL 2</span></span>

<span data-ttu-id="884e1-141">Для обновления до WSL 2 требуется Windows 10.</span><span class="sxs-lookup"><span data-stu-id="884e1-141">To update to WSL 2, you must be running Windows 10.</span></span>

- <span data-ttu-id="884e1-142">Для 64-разрядных систем: **версия 1903** или более поздняя со **сборкой 18362** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="884e1-142">For x64 systems: **Version 1903** or higher, with **Build 18362** or higher.</span></span>
- <span data-ttu-id="884e1-143">Для систем ARM64: **версия 2004** или более поздняя со **сборкой 19041** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="884e1-143">For ARM64 systems: **Version 2004** or higher, with **Build 19041** or higher.</span></span>
- <span data-ttu-id="884e1-144">Сборки ниже 18362 не поддерживают WSL 2.</span><span class="sxs-lookup"><span data-stu-id="884e1-144">Builds lower than 18362 do not support WSL 2.</span></span> <span data-ttu-id="884e1-145">Для обновления версии Windows используйте [помощник по обновлению Windows](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="884e1-145">Use the [Windows Update Assistant](https://www.microsoft.com/software-download/windows10) to update your version of Windows.</span></span>

<span data-ttu-id="884e1-146">Чтобы проверить версию и номер сборки, нажмите клавиши **Windows+R**, введите **winver** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="884e1-146">To check your version and build number, select **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="884e1-147">(Или введите команду `ver` в командной строке Windows).</span><span class="sxs-lookup"><span data-stu-id="884e1-147">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="884e1-148">В меню "Параметры" [выполните обновление до последней версии Windows](ms-settings:windowsupdate).</span><span class="sxs-lookup"><span data-stu-id="884e1-148">[Update to the latest Windows version](ms-settings:windowsupdate) in the Settings menu.</span></span>

> [!NOTE]
> <span data-ttu-id="884e1-149">Если вы используете Windows 10 версии 1903 или 1909, в меню Windows откройте меню "Параметры", перейдите к разделу "Обновления и безопасность" и выберите "Проверить наличие обновлений".</span><span class="sxs-lookup"><span data-stu-id="884e1-149">If you are running Windows 10 version 1903 or 1909, open "Settings" from your Windows menu, navigate to "Update & Security" and select "Check for Updates".</span></span> <span data-ttu-id="884e1-150">Номер сборки должен быть 18362.1049 и выше или 18363.1049 и выше с номером дополнительной сборки не ниже 1049.</span><span class="sxs-lookup"><span data-stu-id="884e1-150">Your Build number must be 18362.1049+ or 18363.1049+, with the minor build # over .1049.</span></span> <span data-ttu-id="884e1-151">Подробнее: [поддержка WSL 2 вскоре будет реализована в Windows 10 версий 1903 и 1909](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/).</span><span class="sxs-lookup"><span data-stu-id="884e1-151">Read more: [WSL 2 Support is coming to Windows 10 Versions 1903 and 1909](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/).</span></span> <span data-ttu-id="884e1-152">См. [инструкции по устранению неполадок](./troubleshooting.md#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).</span><span class="sxs-lookup"><span data-stu-id="884e1-152">See the [troubleshooting instructions](./troubleshooting.md#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).</span></span>

## <a name="step-3---enable-virtual-machine-feature"></a><span data-ttu-id="884e1-153">Шаг 3. Включение компонента виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="884e1-153">Step 3 - Enable Virtual Machine feature</span></span>

<span data-ttu-id="884e1-154">Перед установкой WSL 2 необходимо включить необязательный компонент **Платформа виртуальных машин**.</span><span class="sxs-lookup"><span data-stu-id="884e1-154">Before installing WSL 2, you must enable the **Virtual Machine Platform** optional feature.</span></span>

<span data-ttu-id="884e1-155">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="884e1-155">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="884e1-156">**Перезапустите** компьютер, чтобы завершить установку и обновление WSL до WSL 2.</span><span class="sxs-lookup"><span data-stu-id="884e1-156">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

## <a name="step-4---download-the-linux-kernel-update-package"></a><span data-ttu-id="884e1-157">Шаг 4. Скачивание пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="884e1-157">Step 4 - Download the Linux kernel update package</span></span>

1. <span data-ttu-id="884e1-158">Скачайте пакет последней версии:</span><span class="sxs-lookup"><span data-stu-id="884e1-158">Download the latest package:</span></span>
    - [<span data-ttu-id="884e1-159">Пакет обновления ядра Linux в WSL 2 для 64-разрядных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="884e1-159">WSL2 Linux kernel update package for x64 machines</span></span>](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

    > [!NOTE]
    > <span data-ttu-id="884e1-160">Если вы используете компьютер ARM64, вместо этого скачайте [пакет ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).</span><span class="sxs-lookup"><span data-stu-id="884e1-160">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span> <span data-ttu-id="884e1-161">Если вы не знаете, какой тип компьютера используете, откройте командную строку или PowerShell и введите `systeminfo | find "System Type"`.</span><span class="sxs-lookup"><span data-stu-id="884e1-161">If you're not sure what kind of machine you have, open Command Prompt or PowerShell and enter: `systeminfo | find "System Type"`.</span></span>

2. <span data-ttu-id="884e1-162">Запустите пакет обновления, скачанный на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="884e1-162">Run the update package downloaded in the previous step.</span></span> <span data-ttu-id="884e1-163">(Для запуска щелкните дважды. Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.)</span><span class="sxs-lookup"><span data-stu-id="884e1-163">(Double-click to run - you will be prompted for elevated permissions, select ‘yes’ to approve this installation.)</span></span>

<span data-ttu-id="884e1-164">Когда установка завершится, перейдите к следующему шагу — выбору WSL 2 в качестве версии по умолчанию при установке новых дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="884e1-164">Once the installation is complete, move on to the next step - setting WSL 2 as your default version when installing new Linux distributions.</span></span> <span data-ttu-id="884e1-165">(Пропустите этот шаг, если вы хотите, чтобы новые дистрибутивы Linux были установлены в WSL 1).</span><span class="sxs-lookup"><span data-stu-id="884e1-165">(Skip this step if you want your new Linux installs to be set to WSL 1).</span></span>

> [!NOTE]
> <span data-ttu-id="884e1-166">Дополнительные сведения см. в статье об [изменениях процесса установки обновления ядра Linux в WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), доступной в блоге, [посвященному командной строке Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="884e1-166">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>

## <a name="step-5---set-wsl-2-as-your-default-version"></a><span data-ttu-id="884e1-167">Шаг 5. Выбор WSL 2 в качестве версии по умолчанию</span><span class="sxs-lookup"><span data-stu-id="884e1-167">Step 5 - Set WSL 2 as your default version</span></span>

<span data-ttu-id="884e1-168">Откройте PowerShell и выполните следующую команду, чтобы задать WSL 2 в качестве версии по умолчанию при установке нового дистрибутива Linux:</span><span class="sxs-lookup"><span data-stu-id="884e1-168">Open PowerShell and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

## <a name="step-6---install-your-linux-distribution-of-choice"></a><span data-ttu-id="884e1-169">Шаг 6. Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="884e1-169">Step 6 - Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="884e1-170">Откройте [Microsoft Store](https://aka.ms/wslstore) и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="884e1-170">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="884e1-172">Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="884e1-172">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="884e1-173">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="884e1-173">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="884e1-174">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="884e1-174">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="884e1-175">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="884e1-175">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="884e1-176">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="884e1-176">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="884e1-177">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="884e1-177">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="884e1-178">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="884e1-178">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="884e1-179">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="884e1-179">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="884e1-180">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="884e1-180">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="884e1-181">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="884e1-181">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="884e1-182">Pengwin</span><span class="sxs-lookup"><span data-stu-id="884e1-182">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="884e1-183">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="884e1-183">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="884e1-184">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="884e1-184">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="884e1-185">На странице дистрибутива щелкните "Получить".</span><span class="sxs-lookup"><span data-stu-id="884e1-185">From the distribution's page, select "Get".</span></span>

    ![Дистрибутивы Linux в Microsoft Store](media/UbuntuStore.png)

<span data-ttu-id="884e1-187">При первом запуске недавно установленного дистрибутива Linux откроется окно консоли, и вам будет предложено подождать минуту или две, чтобы файлы распаковались и сохранились на компьютере.</span><span class="sxs-lookup"><span data-stu-id="884e1-187">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="884e1-188">Все будущие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="884e1-188">All future launches should take less than a second.</span></span>

<span data-ttu-id="884e1-189">Затем необходимо будет [создать учетную запись пользователя и пароль для нового дистрибутива Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="884e1-189">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

<span data-ttu-id="884e1-191">**Поздравляем! Вы успешно установили и настроили дистрибутив Linux, который полностью интегрирован с операционной системой Windows.**</span><span class="sxs-lookup"><span data-stu-id="884e1-191">**CONGRATULATIONS! You've successfully installed and set up a Linux distribution that is completely integrated with your Windows operating system!**</span></span>

## <a name="install-windows-terminal-optional"></a><span data-ttu-id="884e1-192">Установка Терминала Windows (необязательно)</span><span class="sxs-lookup"><span data-stu-id="884e1-192">Install Windows Terminal (optional)</span></span>

<span data-ttu-id="884e1-193">В Терминале Windows можно использовать несколько вкладок (чтобы быстро переходить между несколькими командными строками Linux, командной строкой Windows, PowerShell, Azure CLI и пр.), создавать пользовательские сочетания клавиш (для открытия и закрытия вкладок, копирования и вставки и пр.), а также применять функцию поиска и пользовательские темы (цветовые схемы, стили и размеры шрифтов, а также фоновое изображение, размытие и прозрачность).</span><span class="sxs-lookup"><span data-stu-id="884e1-193">Windows Terminal enables multiple tabs (quickly switch between multiple Linux command lines, Windows Command Prompt, PowerShell, Azure CLI, etc), create custom key bindings (shortcut keys for opening or closing tabs, copy+paste, etc.), use the search feature, and custom themes (color schemes, font styles and sizes, background image/blur/transparency).</span></span> [<span data-ttu-id="884e1-194">Подробнее.</span><span class="sxs-lookup"><span data-stu-id="884e1-194">Learn more.</span></span>](/windows/terminal)

<span data-ttu-id="884e1-195">[Установка Терминала Windows](/windows/terminal/get-started)</span><span class="sxs-lookup"><span data-stu-id="884e1-195">[Install Windows Terminal](/windows/terminal/get-started).</span></span>

  ![Терминал Windows](media/terminal.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="884e1-197">Установите вашу версию дистрибутива на WSL 1 или WSL 2</span><span class="sxs-lookup"><span data-stu-id="884e1-197">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="884e1-198">Вы можете проверить версию WSL, назначенную каждому из установленных дистрибутивов Linux, открыв командную строку PowerShell и введя команду (доступна только в [сборке Windows 18362](ms-settings:windowsupdate) или выше): `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="884e1-198">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 18362 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="884e1-199">Чтобы настроить дистрибутив для одной из версий WSL, выполните:</span><span class="sxs-lookup"><span data-stu-id="884e1-199">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="884e1-200">Не забудьте заменить `<distribution name>` на фактическое имя дистрибутива и `<versionNumber>` с номером "1" или "2".</span><span class="sxs-lookup"><span data-stu-id="884e1-200">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="884e1-201">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="884e1-201">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

> [!NOTE]
> <span data-ttu-id="884e1-202">Обновление с WSL 1 до WSL 2 может занять несколько минут в зависимости от размера целевого дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="884e1-202">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="884e1-203">Если вы используете устаревшую установку WSL 1 из Юбилейного обновления Windows 10 или обновления Creators Update, может возникнуть ошибка обновления.</span><span class="sxs-lookup"><span data-stu-id="884e1-203">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="884e1-204">Выполните эти инструкции, чтобы [удалить устаревшие дистрибутивы](./install-legacy.md#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="884e1-204">Follow these instructions to [uninstall and remove any legacy distributions](./install-legacy.md#uninstallingremoving-the-legacy-distro).</span></span>
>
> <span data-ttu-id="884e1-205">Если `wsl --set-default-version` выполняется как недопустимая команда, введите `wsl --help`.</span><span class="sxs-lookup"><span data-stu-id="884e1-205">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="884e1-206">Если `--set-default-version` нет в списке, это указывает на отсутствие поддержки в ОС. Вам нужно выполнить обновление до версии 1903, сборки 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="884e1-206">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 1903, Build 18362 or higher.</span></span>
>
> <span data-ttu-id="884e1-207">После выполнения команды может появиться следующее сообщение: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="884e1-207">If you see this message after running the command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="884e1-208">Это значит, что вам по-прежнему нужно установить пакет обновления MSI для ядра Linux.</span><span class="sxs-lookup"><span data-stu-id="884e1-208">You still need to install the MSI Linux kernel update package.</span></span>

<span data-ttu-id="884e1-209">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="884e1-209">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="884e1-210">Будет установлена версия любого нового дистрибутива, установленного в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="884e1-210">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="884e1-211">Устранение неполадок установки</span><span class="sxs-lookup"><span data-stu-id="884e1-211">Troubleshooting installation</span></span>

<span data-ttu-id="884e1-212">Ниже перечислены возможные ошибки и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="884e1-212">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="884e1-213">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="884e1-213">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="884e1-214">**Сбой установки с ошибкой 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="884e1-214">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="884e1-215">Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`).</span><span class="sxs-lookup"><span data-stu-id="884e1-215">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="884e1-216">Убедитесь, что дистрибутивы хранятся на системном диске.</span><span class="sxs-lookup"><span data-stu-id="884e1-216">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="884e1-217">Выберите **Параметры** -> \*\*Система --> **Хранилище** -> **Другие параметры хранилища: Изменить место сохранения нового содержимого**.
    ![Изображение параметров системы для установки приложений на диске C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="884e1-217">Open **Settings** -> \*\*System --> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="884e1-218">**Сбой WslRegisterDistribution с ошибкой 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="884e1-218">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="884e1-219">Дополнительный компонент "Подсистема Windows для Linux" не включен.</span><span class="sxs-lookup"><span data-stu-id="884e1-219">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="884e1-220">Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="884e1-220">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="884e1-221">**Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**</span><span class="sxs-lookup"><span data-stu-id="884e1-221">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="884e1-222">Убедитесь, что в BIOS вашего компьютера включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="884e1-222">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="884e1-223">Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.</span><span class="sxs-lookup"><span data-stu-id="884e1-223">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="884e1-224">**При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**</span><span class="sxs-lookup"><span data-stu-id="884e1-224">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="884e1-225">Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="884e1-225">Enure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18362 or higher.</span></span> <span data-ttu-id="884e1-226">Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="884e1-226">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span>

- <span data-ttu-id="884e1-227">**Запрошенную операцию не удалось выполнить из-за ограничения системы виртуального диска. Файлы виртуального жесткого диска должны быть распакованными, незашифрованными и не разреженными.**</span><span class="sxs-lookup"><span data-stu-id="884e1-227">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="884e1-228">Снимите флажок Compress contents (Сжимать содержимое) (а также флажок Encrypt contents (Шифровать содержимое), если он установлен), открыв папку профиля для дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="884e1-228">Deselect “Compress contents” (as well as “Encrypt contents” if that’s checked) by opening the profile folder for your Linux distribution.</span></span> <span data-ttu-id="884e1-229">Он должен находиться в подпапке файловой системы Windows, для примера: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.</span><span class="sxs-lookup"><span data-stu-id="884e1-229">It should be located in a folder on your Windows file system, something like: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`</span></span>
  - <span data-ttu-id="884e1-230">В этом профиле дистрибутива Linux должна находиться папка LocalState.</span><span class="sxs-lookup"><span data-stu-id="884e1-230">In this Linux distro profile, there should be a LocalState folder.</span></span> <span data-ttu-id="884e1-231">Щелкните эту папку правой кнопкой мыши, чтобы отобразить меню параметров.</span><span class="sxs-lookup"><span data-stu-id="884e1-231">Right-click this folder to display a menu of options.</span></span> <span data-ttu-id="884e1-232">Выберите Properties (Свойства) > Advanced (Дополнительно) и убедитесь, что флажки Compress contents to save disk space (Сжимать содержимое для экономии места на диске) и Encrypt contents to secure data (Шифровать содержимое для защиты данных) не установлены.</span><span class="sxs-lookup"><span data-stu-id="884e1-232">Select Properties > Advanced and then ensure that the “Compress contents to save disk space” and “Encrypt contents to secure data” checkboxes are unselected (not checked).</span></span> <span data-ttu-id="884e1-233">Если вы увидите запрос на применение параметров к текущей папке или ко всем вложенным папкам и файлам, выберите вариант только для текущей папки, так как вы очищаете только флаг сжатия.</span><span class="sxs-lookup"><span data-stu-id="884e1-233">If you are asked whether to apply this to just to the current folder or to all subfolders and files, select “just this folder” because you are only clearing the compress flag.</span></span> <span data-ttu-id="884e1-234">После этого команда `wsl --set-version` будет работать правильно.</span><span class="sxs-lookup"><span data-stu-id="884e1-234">After this, the `wsl --set-version` command should work.</span></span>

![Снимок экрана с параметрами свойств дистрибутива WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> <span data-ttu-id="884e1-236">В этом примере папка LocalState для дистрибутива Ubuntu 18.04 расположена по адресу C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span><span class="sxs-lookup"><span data-stu-id="884e1-236">In my case, the LocalState folder for my Ubuntu 18.04 distribution was located at C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span></span>
>
> <span data-ttu-id="884e1-237">Чтобы получать обновленные сведения, проверьте [ветку № 4103 в документации GitHub WSL](https://github.com/microsoft/WSL/issues/4103), где отслеживается эта проблема.</span><span class="sxs-lookup"><span data-stu-id="884e1-237">Check [WSL Docs GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="884e1-238">**Термин WSL не распознан как имя командлета, функции, файла скрипта или действующей программы.**</span><span class="sxs-lookup"><span data-stu-id="884e1-238">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="884e1-239">Убедитесь, что установлен дополнительный компонент [Подсистема Windows для Linux](./install-win10.md#step-3---enable-virtual-machine-feature).</span><span class="sxs-lookup"><span data-stu-id="884e1-239">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#step-3---enable-virtual-machine-feature).</span></span> <span data-ttu-id="884e1-240">Кроме того, эта ошибка возникнет, если вы используете устройство ARM64 и выполняете эту команду в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="884e1-240">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="884e1-241">Вместо этого запустите `wsl.exe` из [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) или командной строки.</span><span class="sxs-lookup"><span data-stu-id="884e1-241">Instead run `wsl.exe` from [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows), or Command Prompt.</span></span>

- <span data-ttu-id="884e1-242">**Error: This update only applies to machines with the Windows Subsystem for Linux** (Ошибка. Это обновление применяется только к компьютерам с подсистемой Windows для Linux).</span><span class="sxs-lookup"><span data-stu-id="884e1-242">**Error: This update only applies to machines with the Windows Subsystem for Linux.**</span></span>
  - <span data-ttu-id="884e1-243">Чтобы установить пакет обновления MSI для ядра Linux, нужно сначала включить WSL.</span><span class="sxs-lookup"><span data-stu-id="884e1-243">To install the Linux kernel update MSI package, WSL is required and should be enabled first.</span></span> <span data-ttu-id="884e1-244">В случае сбоя отображается следующее сообщение: `This update only applies to machines with the Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="884e1-244">If it fails, it you will see the message: `This update only applies to machines with the Windows Subsystem for Linux`.</span></span>
  - <span data-ttu-id="884e1-245">Есть три возможные причины, по которым вы видите это сообщение:</span><span class="sxs-lookup"><span data-stu-id="884e1-245">There are three possible reason you see this message:</span></span>

  1. <span data-ttu-id="884e1-246">Вы используете старую версию Windows, которая не поддерживает WSL 2.</span><span class="sxs-lookup"><span data-stu-id="884e1-246">You are still in old version of Windows which doesn't support WSL 2.</span></span> <span data-ttu-id="884e1-247">Требования к версиям и ссылки пакеты обновления см. на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="884e1-247">See step #2 for version requirements and links to update.</span></span>

  2. <span data-ttu-id="884e1-248">Компонент WSL не включен.</span><span class="sxs-lookup"><span data-stu-id="884e1-248">WSL is not enabled.</span></span> <span data-ttu-id="884e1-249">Необходимо вернуться к шагу 1 и убедиться, что на компьютере включен необязательный компонент WSL.</span><span class="sxs-lookup"><span data-stu-id="884e1-249">You will need to return to step #1 and ensure that the optional WSL feature is enabled on your machine.</span></span>

  3. <span data-ttu-id="884e1-250">Когда он будет включен, перезагрузите компьютер, чтобы изменения вступили в силу, и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="884e1-250">After you enabled WSL, a reboot is required for it to take effect, reboot your machine and try again.</span></span>

- <span data-ttu-id="884e1-251">**Error: WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel .** (Ошибка. Для WSL 2 требуется обновление компонента ядра. Дополнительные сведения см. здесь: https://aka.ms/wsl2kernel ).</span><span class="sxs-lookup"><span data-stu-id="884e1-251">**Error: WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel .**</span></span>
  - <span data-ttu-id="884e1-252">Эта ошибка возникает, если пакет ядра Linux отсутствует в папке %SystemRoot%\system32\lxss\tools.</span><span class="sxs-lookup"><span data-stu-id="884e1-252">If the Linux kernel package is missing in the %SystemRoot%\system32\lxss\tools folder, you will encounter this error.</span></span> <span data-ttu-id="884e1-253">Чтобы устранить ошибку, установите пакет обновления MSI для ядра Linux, как описано на шаге 4 в этих инструкциях по установке.</span><span class="sxs-lookup"><span data-stu-id="884e1-253">Resolve it by installing the Linux kernel update MSI package in step #4 of these installation instructions.</span></span> <span data-ttu-id="884e1-254">Возможно, вам потребуется удалить пакет MSI в разделе [Установка и удаление программ](ms-settings:appsfeatures-app), а затем снова установить его.</span><span class="sxs-lookup"><span data-stu-id="884e1-254">You may need to uninstall the MSI from ['Add or Remove Programs'](ms-settings:appsfeatures-app), and install it again.</span></span>
