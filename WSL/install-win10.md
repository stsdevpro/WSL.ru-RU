---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Узнайте, как установить дистрибутивы Linux (включая Ubuntu, Debian, SUSE, Kali, Fedora, Pengwin и Alpine) на компьютере под управлением Windows 10 с помощью терминала Bash.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка, включить, WSL2, версия 2
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 74a5960609e058b2f2da6160ecd04dc48f666a69
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413117"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="be0ca-104">Руководство по установке подсистемы Windows для Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="be0ca-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-windows-subsystem-for-linux"></a><span data-ttu-id="be0ca-105">Установка подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="be0ca-105">Install Windows Subsystem for Linux</span></span>

<span data-ttu-id="be0ca-106">Существует две версии подсистемы Windows для Linux (WSL), которые можно выбрать при установке.</span><span class="sxs-lookup"><span data-stu-id="be0ca-106">Windows Subsystem for Linux has two different versions to choose between during the installation process.</span></span> <span data-ttu-id="be0ca-107">WSL 2 обеспечивает более высокую общую производительность. Мы рекомендуем использовать ее.</span><span class="sxs-lookup"><span data-stu-id="be0ca-107">WSL 2 has better overall performance and we recommend using it.</span></span> <span data-ttu-id="be0ca-108">Если ваша система не поддерживает WSL 2 или у вас особый случай, когда требуется использовать межсистемное хранилище файлов, возможно, вы захотите выбрать WSL 1.</span><span class="sxs-lookup"><span data-stu-id="be0ca-108">If your system does not support WSL 2, or you have a specific situation that requires cross-system file storage, then you may want to stick with WSL 1.</span></span> <span data-ttu-id="be0ca-109">Узнайте больше о [сравнении WSL 2 и WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="be0ca-109">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="step-1---enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="be0ca-110">Шаг 1. Включение подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="be0ca-110">Step 1 - Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="be0ca-111">Перед установкой дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux".</span><span class="sxs-lookup"><span data-stu-id="be0ca-111">You must first enable the "Windows Subsystem for Linux" optional feature before installing any Linux distributions on Windows.</span></span>

<span data-ttu-id="be0ca-112">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="be0ca-112">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="be0ca-113">Теперь перейдите к шагу 2 и выполните обновление до WSL 2. Если вы хотите установить только WSL 1, вы можете перезагрузить компьютер и перейти к разделу [Шаг 6. Установка дистрибутива Linux по выбору](./install-win10.md#step-6---install-your-linux-distribution-of-choice).</span><span class="sxs-lookup"><span data-stu-id="be0ca-113">We recommend now moving on to step #2, updating to WSL 2, but if you wish to only install WSL 1, you can now restart your machine and move on to [Step 6 - Install your Linux distribution of choice](./install-win10.md#step-6---install-your-linux-distribution-of-choice).</span></span> <span data-ttu-id="be0ca-114">Чтобы выполнить обновление до WSL 2, дождитесь перезагрузки компьютера и перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="be0ca-114">To update to WSL 2, wait to restart your machine and move on to the next step.</span></span>

## <a name="step-2---update-to-wsl-2"></a><span data-ttu-id="be0ca-115">Шаг 2. Обновление до WSL 2</span><span class="sxs-lookup"><span data-stu-id="be0ca-115">Step 2 - Update to WSL 2</span></span>

<span data-ttu-id="be0ca-116">Для обновления до WSL 2 требуется Windows 10.</span><span class="sxs-lookup"><span data-stu-id="be0ca-116">To update to WSL 2, you must be running Windows 10.</span></span>

### <a name="requirements"></a><span data-ttu-id="be0ca-117">Требования</span><span class="sxs-lookup"><span data-stu-id="be0ca-117">Requirements</span></span>

- <span data-ttu-id="be0ca-118">Для 64-разрядных систем: **версия 1903** или более поздняя со **сборкой 18362** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="be0ca-118">For x64 systems: **Version 1903** or higher, with **Build 18362** or higher.</span></span>
- <span data-ttu-id="be0ca-119">Для систем ARM64: **версия 2004** или более поздняя со **сборкой 19041** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="be0ca-119">For ARM64 systems: **Version 2004** or higher, with **Build 19041** or higher.</span></span>
- <span data-ttu-id="be0ca-120">Сборки ниже 18362 не поддерживают WSL 2.</span><span class="sxs-lookup"><span data-stu-id="be0ca-120">Builds lower than 18362 do not support WSL 2.</span></span> <span data-ttu-id="be0ca-121">Для обновления версии Windows используйте [помощник по обновлению Windows](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="be0ca-121">Use the [Windows Update Assistant](https://www.microsoft.com/software-download/windows10) to update your version of Windows.</span></span>

<span data-ttu-id="be0ca-122">Чтобы проверить версию и номер сборки, нажмите клавиши **Windows+R**, введите **winver** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="be0ca-122">To check your version and build number, select **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="be0ca-123">(Или введите команду `ver` в командной строке Windows).</span><span class="sxs-lookup"><span data-stu-id="be0ca-123">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="be0ca-124">В меню "Параметры" [выполните обновление до последней версии Windows](ms-settings:windowsupdate).</span><span class="sxs-lookup"><span data-stu-id="be0ca-124">[Update to the latest Windows version](ms-settings:windowsupdate) in the Settings menu.</span></span>

> [!NOTE]
> <span data-ttu-id="be0ca-125">Если вы используете Windows 10 версии 1903 или 1909, в меню Windows откройте меню "Параметры", перейдите к разделу "Обновления и безопасность" и выберите "Проверить наличие обновлений".</span><span class="sxs-lookup"><span data-stu-id="be0ca-125">If you are running Windows 10 version 1903 or 1909, open "Settings" from your Windows menu, navigate to "Update & Security" and select "Check for Updates".</span></span> <span data-ttu-id="be0ca-126">Номер сборки должен быть 18362.1049 и выше или 18363.1049 и выше с номером дополнительной сборки не ниже 1049.</span><span class="sxs-lookup"><span data-stu-id="be0ca-126">Your Build number must be 18362.1049+ or 18363.1049+, with the minor build # over .1049.</span></span> <span data-ttu-id="be0ca-127">Подробнее: [поддержка WSL 2 вскоре будет реализована в Windows 10 версий 1903 и 1909](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/).</span><span class="sxs-lookup"><span data-stu-id="be0ca-127">Read more: [WSL 2 Support is coming to Windows 10 Versions 1903 and 1909](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/).</span></span> <span data-ttu-id="be0ca-128">См. [инструкции по устранению неполадок](./troubleshooting.md#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).</span><span class="sxs-lookup"><span data-stu-id="be0ca-128">See the [troubleshooting instructions](./troubleshooting.md#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).</span></span>

## <a name="step-3---enable-virtual-machine-feature"></a><span data-ttu-id="be0ca-129">Шаг 3. Включение компонента виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="be0ca-129">Step 3 - Enable Virtual Machine feature</span></span>

<span data-ttu-id="be0ca-130">Перед установкой WSL 2 необходимо включить необязательный компонент **Платформа виртуальных машин**.</span><span class="sxs-lookup"><span data-stu-id="be0ca-130">Before installing WSL 2, you must enable the **Virtual Machine Platform** optional feature.</span></span>

<span data-ttu-id="be0ca-131">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="be0ca-131">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="be0ca-132">**Перезапустите** компьютер, чтобы завершить установку и обновление WSL до WSL 2.</span><span class="sxs-lookup"><span data-stu-id="be0ca-132">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

## <a name="step-4---download-the-linux-kernel-update-package"></a><span data-ttu-id="be0ca-133">Шаг 4. Скачивание пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="be0ca-133">Step 4 - Download the Linux kernel update package</span></span>

1. <span data-ttu-id="be0ca-134">Скачайте пакет последней версии:</span><span class="sxs-lookup"><span data-stu-id="be0ca-134">Download the latest package:</span></span>
    - [<span data-ttu-id="be0ca-135">Пакет обновления ядра Linux в WSL 2 для 64-разрядных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="be0ca-135">WSL2 Linux kernel update package for x64 machines</span></span>](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

    > [!NOTE]
    > <span data-ttu-id="be0ca-136">Если вы используете компьютер ARM64, вместо этого скачайте [пакет ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).</span><span class="sxs-lookup"><span data-stu-id="be0ca-136">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span> <span data-ttu-id="be0ca-137">Если вы не знаете, какой тип компьютера используете, откройте командную строку или PowerShell и введите `systeminfo | find "System Type"`.</span><span class="sxs-lookup"><span data-stu-id="be0ca-137">If you're not sure what kind of machine you have, open Command Prompt or PowerShell and enter: `systeminfo | find "System Type"`.</span></span>

2. <span data-ttu-id="be0ca-138">Запустите пакет обновления, скачанный на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="be0ca-138">Run the update package downloaded in the previous step.</span></span> <span data-ttu-id="be0ca-139">(Для запуска щелкните дважды. Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.)</span><span class="sxs-lookup"><span data-stu-id="be0ca-139">(Double-click to run - you will be prompted for elevated permissions, select ‘yes’ to approve this installation.)</span></span>

<span data-ttu-id="be0ca-140">Когда установка завершится, перейдите к следующему шагу — выбору WSL 2 в качестве версии по умолчанию при установке новых дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="be0ca-140">Once the installation is complete, move on to the next step - setting WSL 2 as your default version when installing new Linux distributions.</span></span> <span data-ttu-id="be0ca-141">(Пропустите этот шаг, если вы хотите, чтобы новые дистрибутивы Linux были установлены в WSL 1).</span><span class="sxs-lookup"><span data-stu-id="be0ca-141">(Skip this step if you want your new Linux installs to be set to WSL 1).</span></span>

> [!NOTE]
> <span data-ttu-id="be0ca-142">Дополнительные сведения см. в статье об [изменениях процесса установки обновления ядра Linux в WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), доступной в блоге, [посвященному командной строке Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="be0ca-142">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>

## <a name="step-5---set-wsl-2-as-your-default-version"></a><span data-ttu-id="be0ca-143">Шаг 5. Выбор WSL 2 в качестве версии по умолчанию</span><span class="sxs-lookup"><span data-stu-id="be0ca-143">Step 5 - Set WSL 2 as your default version</span></span>

<span data-ttu-id="be0ca-144">Откройте PowerShell от имени администратора и выполните следующую команду, чтобы задать WSL 2 в качестве версии по умолчанию при установке нового дистрибутива Linux:</span><span class="sxs-lookup"><span data-stu-id="be0ca-144">Open PowerShell as Administrator and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

> [!NOTE]
> <span data-ttu-id="be0ca-145">Обновление с WSL 1 до WSL 2 может занять несколько минут в зависимости от размера целевого дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="be0ca-145">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="be0ca-146">Если вы используете устаревшую установку WSL 1 из Юбилейного обновления Windows 10 или обновления Creators Update, может возникнуть ошибка обновления.</span><span class="sxs-lookup"><span data-stu-id="be0ca-146">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="be0ca-147">Выполните эти инструкции, чтобы [удалить устаревшие дистрибутивы](./install-legacy.md#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="be0ca-147">Follow these instructions to [uninstall and remove any legacy distributions](./install-legacy.md#uninstallingremoving-the-legacy-distro).</span></span>
>
> <span data-ttu-id="be0ca-148">Если `wsl --set-default-version` выполняется как недопустимая команда, введите `wsl --help`.</span><span class="sxs-lookup"><span data-stu-id="be0ca-148">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="be0ca-149">Если `--set-default-version` нет в списке, это указывает на отсутствие поддержки в ОС. Вам нужно выполнить обновление до версии 1903, сборки 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="be0ca-149">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 1903, Build 18362 or higher.</span></span>
>
> <span data-ttu-id="be0ca-150">После выполнения команды может появиться следующее сообщение: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="be0ca-150">If you see this message after running the command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="be0ca-151">Это значит, что вам по-прежнему нужно установить пакет обновления MSI для ядра Linux.</span><span class="sxs-lookup"><span data-stu-id="be0ca-151">You still need to install the MSI Linux kernel update package.</span></span>

## <a name="step-6---install-your-linux-distribution-of-choice"></a><span data-ttu-id="be0ca-152">Шаг 6. Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="be0ca-152">Step 6 - Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="be0ca-153">Откройте [Microsoft Store](https://aka.ms/wslstore) и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="be0ca-153">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="be0ca-155">Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="be0ca-155">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="be0ca-156">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="be0ca-156">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="be0ca-157">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="be0ca-157">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="be0ca-158">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="be0ca-158">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="be0ca-159">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="be0ca-159">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="be0ca-160">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="be0ca-160">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="be0ca-161">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="be0ca-161">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="be0ca-162">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="be0ca-162">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="be0ca-163">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="be0ca-163">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="be0ca-164">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="be0ca-164">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="be0ca-165">Pengwin</span><span class="sxs-lookup"><span data-stu-id="be0ca-165">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="be0ca-166">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="be0ca-166">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="be0ca-167">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="be0ca-167">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="be0ca-168">На странице дистрибутива щелкните "Получить".</span><span class="sxs-lookup"><span data-stu-id="be0ca-168">From the distribution's page, select "Get".</span></span>

    ![Дистрибутивы Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="step-7---set-up-a-new-distribution"></a><span data-ttu-id="be0ca-170">Шаг 7. Настройка нового дистрибутива</span><span class="sxs-lookup"><span data-stu-id="be0ca-170">Step 7 - Set up a new distribution</span></span>

<span data-ttu-id="be0ca-171">При первом запуске недавно установленного дистрибутива Linux откроется окно консоли, и вам будет предложено подождать минуту или две, чтобы файлы распаковались и сохранились на компьютере.</span><span class="sxs-lookup"><span data-stu-id="be0ca-171">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="be0ca-172">Все будущие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="be0ca-172">All future launches should take less than a second.</span></span>

<span data-ttu-id="be0ca-173">Затем необходимо будет [создать учетную запись пользователя и пароль для нового дистрибутива Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="be0ca-173">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

<span data-ttu-id="be0ca-175">**Поздравляем! Вы успешно установили и настроили дистрибутив Linux, который полностью интегрирован с операционной системой Windows.**</span><span class="sxs-lookup"><span data-stu-id="be0ca-175">**CONGRATULATIONS! You've successfully installed and set up a Linux distribution that is completely integrated with your Windows operating system!**</span></span>

## <a name="install-windows-terminal-optional"></a><span data-ttu-id="be0ca-176">Установка Терминала Windows (необязательно)</span><span class="sxs-lookup"><span data-stu-id="be0ca-176">Install Windows Terminal (optional)</span></span>

<span data-ttu-id="be0ca-177">В Терминале Windows можно использовать несколько вкладок (чтобы быстро переходить между несколькими командными строками Linux, командной строкой Windows, PowerShell, Azure CLI и пр.), создавать пользовательские сочетания клавиш (для открытия и закрытия вкладок, копирования и вставки и пр.), а также применять функцию поиска и пользовательские темы (цветовые схемы, стили и размеры шрифтов, а также фоновое изображение, размытие и прозрачность).</span><span class="sxs-lookup"><span data-stu-id="be0ca-177">Windows Terminal enables multiple tabs (quickly switch between multiple Linux command lines, Windows Command Prompt, PowerShell, Azure CLI, etc), create custom key bindings (shortcut keys for opening or closing tabs, copy+paste, etc.), use the search feature, and custom themes (color schemes, font styles and sizes, background image/blur/transparency).</span></span> [<span data-ttu-id="be0ca-178">Подробнее.</span><span class="sxs-lookup"><span data-stu-id="be0ca-178">Learn more.</span></span>](/windows/terminal)

<span data-ttu-id="be0ca-179">[Установка Терминала Windows](/windows/terminal/get-started)</span><span class="sxs-lookup"><span data-stu-id="be0ca-179">[Install Windows Terminal](/windows/terminal/get-started).</span></span>

  ![Терминал Windows](media/terminal.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="be0ca-181">Установите вашу версию дистрибутива на WSL 1 или WSL 2</span><span class="sxs-lookup"><span data-stu-id="be0ca-181">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="be0ca-182">Вы можете проверить версию WSL, назначенную каждому из установленных дистрибутивов Linux, открыв командную строку PowerShell и введя команду (доступна только в [сборке Windows 18362](ms-settings:windowsupdate) или выше): `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="be0ca-182">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 18362 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="be0ca-183">Чтобы настроить дистрибутив для одной из версий WSL, выполните:</span><span class="sxs-lookup"><span data-stu-id="be0ca-183">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="be0ca-184">Не забудьте заменить `<distribution name>` на фактическое имя дистрибутива и `<versionNumber>` с номером "1" или "2".</span><span class="sxs-lookup"><span data-stu-id="be0ca-184">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="be0ca-185">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="be0ca-185">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="be0ca-186">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="be0ca-186">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="be0ca-187">Будет установлена версия любого нового дистрибутива, установленного в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="be0ca-187">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="be0ca-188">Устранение неполадок установки</span><span class="sxs-lookup"><span data-stu-id="be0ca-188">Troubleshooting installation</span></span>

<span data-ttu-id="be0ca-189">Ниже перечислены возможные ошибки и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="be0ca-189">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="be0ca-190">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="be0ca-190">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="be0ca-191">**Сбой установки с ошибкой 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="be0ca-191">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="be0ca-192">Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`).</span><span class="sxs-lookup"><span data-stu-id="be0ca-192">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="be0ca-193">Убедитесь, что дистрибутивы хранятся на системном диске.</span><span class="sxs-lookup"><span data-stu-id="be0ca-193">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="be0ca-194">Выберите **Параметры** -> **Хранилище** -> **More Storage Settings: (Другие параметры хранилища:) Изменить место сохранения нового содержимого**.
    ![Изображение параметров системы для установки приложений на диске C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="be0ca-194">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="be0ca-195">**Сбой WslRegisterDistribution с ошибкой 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="be0ca-195">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="be0ca-196">Дополнительный компонент "Подсистема Windows для Linux" не включен.</span><span class="sxs-lookup"><span data-stu-id="be0ca-196">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="be0ca-197">Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="be0ca-197">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="be0ca-198">**Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**</span><span class="sxs-lookup"><span data-stu-id="be0ca-198">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="be0ca-199">Убедитесь, что в BIOS вашего компьютера включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="be0ca-199">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="be0ca-200">Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.</span><span class="sxs-lookup"><span data-stu-id="be0ca-200">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="be0ca-201">**При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**</span><span class="sxs-lookup"><span data-stu-id="be0ca-201">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="be0ca-202">Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="be0ca-202">Enure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18362 or higher.</span></span> <span data-ttu-id="be0ca-203">Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="be0ca-203">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span>

- <span data-ttu-id="be0ca-204">**Запрошенную операцию не удалось выполнить из-за ограничения системы виртуального диска. Файлы виртуального жесткого диска должны быть распакованными, незашифрованными и не разреженными.**</span><span class="sxs-lookup"><span data-stu-id="be0ca-204">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="be0ca-205">Снимите флажок Compress contents (Сжимать содержимое) (а также флажок Encrypt contents (Шифровать содержимое), если он установлен), открыв папку профиля для дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="be0ca-205">Deselect “Compress contents” (as well as “Encrypt contents” if that’s checked) by opening the profile folder for your Linux distribution.</span></span> <span data-ttu-id="be0ca-206">Он должен находиться в подпапке файловой системы Windows, для примера: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.</span><span class="sxs-lookup"><span data-stu-id="be0ca-206">It should be located in a folder on your Windows file system, something like: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`</span></span>
  - <span data-ttu-id="be0ca-207">В этом профиле дистрибутива Linux должна находиться папка LocalState.</span><span class="sxs-lookup"><span data-stu-id="be0ca-207">In this Linux distro profile, there should be a LocalState folder.</span></span> <span data-ttu-id="be0ca-208">Щелкните эту папку правой кнопкой мыши, чтобы отобразить меню параметров.</span><span class="sxs-lookup"><span data-stu-id="be0ca-208">Right-click this folder to display a menu of options.</span></span> <span data-ttu-id="be0ca-209">Выберите Properties (Свойства) > Advanced (Дополнительно) и убедитесь, что флажки Compress contents to save disk space (Сжимать содержимое для экономии места на диске) и Encrypt contents to secure data (Шифровать содержимое для защиты данных) не установлены.</span><span class="sxs-lookup"><span data-stu-id="be0ca-209">Select Properties > Advanced and then ensure that the “Compress contents to save disk space” and “Encrypt contents to secure data” checkboxes are unselected (not checked).</span></span> <span data-ttu-id="be0ca-210">Если вы увидите запрос на применение параметров к текущей папке или ко всем вложенным папкам и файлам, выберите вариант только для текущей папки, так как вы очищаете только флаг сжатия.</span><span class="sxs-lookup"><span data-stu-id="be0ca-210">If you are asked whether to apply this to just to the current folder or to all subfolders and files, select “just this folder” because you are only clearing the compress flag.</span></span> <span data-ttu-id="be0ca-211">После этого команда `wsl --set-version` будет работать правильно.</span><span class="sxs-lookup"><span data-stu-id="be0ca-211">After this, the `wsl --set-version` command should work.</span></span>

![Снимок экрана с параметрами свойств дистрибутива WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> <span data-ttu-id="be0ca-213">В этом примере папка LocalState для дистрибутива Ubuntu 18.04 расположена по адресу C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span><span class="sxs-lookup"><span data-stu-id="be0ca-213">In my case, the LocalState folder for my Ubuntu 18.04 distribution was located at C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span></span>
>
> <span data-ttu-id="be0ca-214">Чтобы получать обновленные сведения, проверьте [ветку № 4103 в документации GitHub WSL](https://github.com/microsoft/WSL/issues/4103), где отслеживается эта проблема.</span><span class="sxs-lookup"><span data-stu-id="be0ca-214">Check [WSL Docs GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="be0ca-215">**Термин WSL не распознан как имя командлета, функции, файла скрипта или действующей программы.**</span><span class="sxs-lookup"><span data-stu-id="be0ca-215">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="be0ca-216">Убедитесь, что установлен дополнительный компонент [Подсистема Windows для Linux](./install-win10.md#step-3---enable-virtual-machine-feature).</span><span class="sxs-lookup"><span data-stu-id="be0ca-216">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#step-3---enable-virtual-machine-feature).</span></span> <span data-ttu-id="be0ca-217">Кроме того, эта ошибка возникнет, если вы используете устройство ARM64 и выполняете эту команду в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="be0ca-217">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="be0ca-218">Вместо этого запустите `wsl.exe` из [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) или командной строки.</span><span class="sxs-lookup"><span data-stu-id="be0ca-218">Instead run `wsl.exe` from [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows), or Command Prompt.</span></span>

- <span data-ttu-id="be0ca-219">**Error: This update only applies to machines with the Windows Subsystem for Linux** (Ошибка. Это обновление применяется только к компьютерам с подсистемой Windows для Linux).</span><span class="sxs-lookup"><span data-stu-id="be0ca-219">**Error: This update only applies to machines with the Windows Subsystem for Linux.**</span></span>
  - <span data-ttu-id="be0ca-220">Чтобы установить пакет обновления MSI для ядра Linux, нужно сначала включить WSL.</span><span class="sxs-lookup"><span data-stu-id="be0ca-220">To install the Linux kernel update MSI package, WSL is required and should be enabled first.</span></span> <span data-ttu-id="be0ca-221">В случае сбоя отображается следующее сообщение: `This update only applies to machines with the Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="be0ca-221">If it fails, it you will see the message: `This update only applies to machines with the Windows Subsystem for Linux`.</span></span>
  - <span data-ttu-id="be0ca-222">Есть три возможные причины, по которым вы видите это сообщение:</span><span class="sxs-lookup"><span data-stu-id="be0ca-222">There are three possible reason you see this message:</span></span>

  1. <span data-ttu-id="be0ca-223">Вы используете старую версию Windows, которая не поддерживает WSL 2.</span><span class="sxs-lookup"><span data-stu-id="be0ca-223">You are still in old version of Windows which doesn't support WSL 2.</span></span> <span data-ttu-id="be0ca-224">Требования к версиям и ссылки пакеты обновления см. на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="be0ca-224">See step #2 for version requirements and links to update.</span></span>

  2. <span data-ttu-id="be0ca-225">Компонент WSL не включен.</span><span class="sxs-lookup"><span data-stu-id="be0ca-225">WSL is not enabled.</span></span> <span data-ttu-id="be0ca-226">Необходимо вернуться к шагу 1 и убедиться, что на компьютере включен необязательный компонент WSL.</span><span class="sxs-lookup"><span data-stu-id="be0ca-226">You will need to return to step #1 and ensure that the optional WSL feature is enabled on your machine.</span></span>

  3. <span data-ttu-id="be0ca-227">Когда он будет включен, перезагрузите компьютер, чтобы изменения вступили в силу, и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="be0ca-227">After you enabled WSL, a reboot is required for it to take effect, reboot your machine and try again.</span></span>

- <span data-ttu-id="be0ca-228">**Error: WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel .** (Ошибка. Для WSL 2 требуется обновление компонента ядра. Дополнительные сведения см. здесь: https://aka.ms/wsl2kernel ).</span><span class="sxs-lookup"><span data-stu-id="be0ca-228">**Error: WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel .**</span></span>
  - <span data-ttu-id="be0ca-229">Эта ошибка возникает, если пакет ядра Linux отсутствует в папке %SystemRoot%\system32\lxss\tools.</span><span class="sxs-lookup"><span data-stu-id="be0ca-229">If the Linux kernel package is missing in the %SystemRoot%\system32\lxss\tools folder, you will encounter this error.</span></span> <span data-ttu-id="be0ca-230">Чтобы устранить ошибку, установите пакет обновления MSI для ядра Linux, как описано на шаге 4 в этих инструкциях по установке.</span><span class="sxs-lookup"><span data-stu-id="be0ca-230">Resolve it by installing the Linux kernel update MSI package in step #4 of these installation instructions.</span></span> <span data-ttu-id="be0ca-231">Возможно, вам потребуется удалить пакет MSI в разделе [Установка и удаление программ](ms-settings:appsfeatures-app), а затем снова установить его.</span><span class="sxs-lookup"><span data-stu-id="be0ca-231">You may need to uninstall the MSI from ['Add or Remove Programs'](ms-settings:appsfeatures-app), and install it again.</span></span>