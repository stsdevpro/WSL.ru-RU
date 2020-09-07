---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Узнайте, как установить подсистему Windows для Linux в Windows 10. Windows 10 необходимо обновить до версии 2004, сборки 19041 или выше.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка, включить, WSL2, версия 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 14e1697d1f2ac7a1efa17368be830a5c22973bc6
ms.sourcegitcommit: 910845e9b3f980b2c5b9b4968331a706720603c6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2020
ms.locfileid: "89058499"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="bcdd1-105">Руководство по установке подсистемы Windows для Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="bcdd1-105">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="bcdd1-106">Установка подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="bcdd1-106">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="bcdd1-107">Перед установкой дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux".</span><span class="sxs-lookup"><span data-stu-id="bcdd1-107">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="bcdd1-108">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-108">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="bcdd1-109">Чтобы установить только WSL 1, необходимо перезагрузить компьютер и перейти к пункту [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice) (Установить дистрибутив Linux), в противном случае дождитесь перезапуска и переходите к обновлению до WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-109">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="bcdd1-110">Узнайте больше о [сравнении WSL 2 и WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-110">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="bcdd1-111">Обновление до WSL 2</span><span class="sxs-lookup"><span data-stu-id="bcdd1-111">Update to WSL 2</span></span>

<span data-ttu-id="bcdd1-112">Чтобы выполнить обновление до WSL 2, необходимо выполнить следующие условия:</span><span class="sxs-lookup"><span data-stu-id="bcdd1-112">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="bcdd1-113">Использовать Windows 10 с [обновлением до версии 1903 или выше](ms-settings:windowsupdate), **сборкой 18362** или выше для систем x64.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-113">Running Windows 10, [updated to version 1903 or higher](ms-settings:windowsupdate), **Build 18362** or higher for x64 systems.</span></span>
- <span data-ttu-id="bcdd1-114">Использовать Windows 10 с обновлением до версии 2004 или выше и **сборкой 19041** или выше для систем ARM64.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-114">Running Windows 10, updated to version 2004 or higher, **build 19041**, for ARM64 systems.</span></span>
- <span data-ttu-id="bcdd1-115">Обратите внимание, что, если вы работаете с Windows 10 версии 1903 или 1909, необходимо убедиться, что используется надлежащее обновление. Инструкции можно [найти здесь](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-115">Please note if you are on Windows 10 version 1903 or 1909 you will need to ensure that you have the proper backport, instructions can be [found here](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span></span> 

- <span data-ttu-id="bcdd1-116">Проверьте версию Windows, нажав **Windows + R**, введите **winver**, выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-116">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="bcdd1-117">(Или введите команду `ver` в командной строке Windows).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-117">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="bcdd1-118">[Обновите последнюю версию Windows](ms-settings:windowsupdate), если сборка ниже 18361.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-118">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 18361.</span></span> <span data-ttu-id="bcdd1-119">[Получите помощник по Центру обновления Windows](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-119">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="bcdd1-120">Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)</span><span class="sxs-lookup"><span data-stu-id="bcdd1-120">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="bcdd1-121">Перед установкой WSL 2 необходимо включить необязательный компонент "Virtual Machine Platform" (Платформа виртуальных машин).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-121">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="bcdd1-122">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-122">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="bcdd1-123">**Перезапустите** компьютер, чтобы завершить установку и обновление WSL до WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-123">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="bcdd1-124">Задать WSL 2 в качестве версии по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bcdd1-124">Set WSL 2 as your default version</span></span>

<span data-ttu-id="bcdd1-125">Откройте PowerShell от имени администратора и выполните следующую команду, чтобы задать WSL 2 в качестве версии по умолчанию при установке нового дистрибутива Linux:</span><span class="sxs-lookup"><span data-stu-id="bcdd1-125">Open PowerShell as Administrator and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="bcdd1-126">После выполнения этой команды может появиться следующее сообщение: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-126">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="bcdd1-127">Перейдите по ссылке ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) и установите MSI-файл с этой страницы документации, чтобы установить на компьютере ядро Linux для WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-127">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="bcdd1-128">После установки ядра выполните команду еще раз. Она должна успешно завершиться без отображения сообщения.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-128">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="bcdd1-129">Обновление с WSL 1 до WSL 2 может занять несколько минут в зависимости от размера целевого дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-129">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="bcdd1-130">Если вы используете устаревшую установку WSL 1 из Юбилейного обновления Windows 10 или обновления Creators Update, может возникнуть ошибка обновления.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-130">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="bcdd1-131">Выполните эти инструкции, чтобы [удалить устаревшие дистрибутивы](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-131">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span> 
>
> <span data-ttu-id="bcdd1-132">Если `wsl --set-default-version` выполняется как недопустимая команда, введите `wsl --help`.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-132">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="bcdd1-133">Если `--set-default-version` нет в списке, это указывает на отсутствие поддержки в ОС. Вам нужно выполнить обновление до версии 1903, сборки 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-133">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 1903, Build 18362 or higher.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="bcdd1-134">Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="bcdd1-134">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="bcdd1-135">Откройте [Microsoft Store](https://aka.ms/wslstore) и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-135">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="bcdd1-137">Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="bcdd1-137">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="bcdd1-138">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="bcdd1-138">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="bcdd1-139">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="bcdd1-139">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="bcdd1-140">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="bcdd1-140">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="bcdd1-141">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="bcdd1-141">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="bcdd1-142">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="bcdd1-142">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="bcdd1-143">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="bcdd1-143">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="bcdd1-144">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="bcdd1-144">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="bcdd1-145">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="bcdd1-145">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="bcdd1-146">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="bcdd1-146">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="bcdd1-147">Pengwin</span><span class="sxs-lookup"><span data-stu-id="bcdd1-147">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="bcdd1-148">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="bcdd1-148">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="bcdd1-149">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="bcdd1-149">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="bcdd1-150">На странице дистрибутива щелкните "Получить".</span><span class="sxs-lookup"><span data-stu-id="bcdd1-150">From the distribution's page, select "Get".</span></span>

    ![Дистрибутивы Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="bcdd1-152">Настройка нового дистрибутива</span><span class="sxs-lookup"><span data-stu-id="bcdd1-152">Set up a new distribution</span></span>

<span data-ttu-id="bcdd1-153">При первом запуске недавно установленного дистрибутива Linux откроется окно консоли, и вам будет предложено подождать минуту или две, чтобы файлы распаковались и сохранились на компьютере.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-153">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="bcdd1-154">Все будущие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-154">All future launches should take less than a second.</span></span>

<span data-ttu-id="bcdd1-155">Затем необходимо будет [создать учетную запись пользователя и пароль для нового дистрибутива Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-155">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="bcdd1-157">Установите вашу версию дистрибутива на WSL 1 или WSL 2</span><span class="sxs-lookup"><span data-stu-id="bcdd1-157">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="bcdd1-158">Вы можете проверить версию WSL, назначенную каждому из установленных дистрибутивов Linux, открыв командную строку PowerShell и введя команду (доступна только в [сборке Windows 18362](ms-settings:windowsupdate) или выше): `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-158">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 18362 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="bcdd1-159">Чтобы настроить дистрибутив для одной из версий WSL, выполните:</span><span class="sxs-lookup"><span data-stu-id="bcdd1-159">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="bcdd1-160">Не забудьте заменить `<distribution name>` на фактическое имя дистрибутива и `<versionNumber>` с номером "1" или "2".</span><span class="sxs-lookup"><span data-stu-id="bcdd1-160">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="bcdd1-161">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="bcdd1-161">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="bcdd1-162">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bcdd1-162">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="bcdd1-163">Будет установлена версия любого нового дистрибутива, установленного в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-163">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="bcdd1-164">Устранение неполадок установки</span><span class="sxs-lookup"><span data-stu-id="bcdd1-164">Troubleshooting installation</span></span>

<span data-ttu-id="bcdd1-165">Ниже перечислены возможные ошибки и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-165">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="bcdd1-166">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-166">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="bcdd1-167">**Сбой установки с ошибкой 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="bcdd1-167">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="bcdd1-168">Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-168">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="bcdd1-169">Убедитесь, что дистрибутивы хранятся на системном диске.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-169">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="bcdd1-170">Выберите **Параметры** -> **Хранилище** -> **More Storage Settings: (Другие параметры хранилища:) Изменить место сохранения нового содержимого**.
    ![Изображение параметров системы для установки приложений на диске C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="bcdd1-170">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="bcdd1-171">**Сбой WslRegisterDistribution с ошибкой 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="bcdd1-171">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="bcdd1-172">Дополнительный компонент "Подсистема Windows для Linux" не включен.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-172">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="bcdd1-173">Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-173">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="bcdd1-174">**Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**</span><span class="sxs-lookup"><span data-stu-id="bcdd1-174">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="bcdd1-175">Убедитесь, что в BIOS вашего компьютера включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-175">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="bcdd1-176">Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-176">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="bcdd1-177">**При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**</span><span class="sxs-lookup"><span data-stu-id="bcdd1-177">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="bcdd1-178">Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-178">Enure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18362 or higher.</span></span> <span data-ttu-id="bcdd1-179">Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-179">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span>

- <span data-ttu-id="bcdd1-180">**Запрошенную операцию не удалось выполнить из-за ограничения системы виртуального диска. Файлы виртуального жесткого диска должны быть распакованными, незашифрованными и не разреженными.**</span><span class="sxs-lookup"><span data-stu-id="bcdd1-180">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="bcdd1-181">Снимите флажок Compress contents (Сжимать содержимое) (а также флажок Encrypt contents (Шифровать содержимое), если он установлен), открыв папку профиля для дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-181">Deselect “Compress contents” (as well as “Encrypt contents” if that’s checked) by opening the profile folder for your Linux distribution.</span></span> <span data-ttu-id="bcdd1-182">Он должен находиться в подпапке файловой системы Windows, для примера: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-182">It should be located in a folder on your Windows file system, something like: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`</span></span>
  - <span data-ttu-id="bcdd1-183">В этом профиле дистрибутива Linux должна находиться папка LocalState.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-183">In this Linux distro profile, there should be a LocalState folder.</span></span> <span data-ttu-id="bcdd1-184">Щелкните эту папку правой кнопкой мыши, чтобы отобразить меню параметров.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-184">Right-click this folder to display a menu of options.</span></span> <span data-ttu-id="bcdd1-185">Выберите Properties (Свойства) > Advanced (Дополнительно) и убедитесь, что флажки Compress contents to save disk space (Сжимать содержимое для экономии места на диске) и Encrypt contents to secure data (Шифровать содержимое для защиты данных) не установлены.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-185">Select Properties > Advanced and then ensure that the “Compress contents to save disk space” and “Encrypt contents to secure data” checkboxes are unselected (not checked).</span></span> <span data-ttu-id="bcdd1-186">Если вы увидите запрос на применение параметров к текущей папке или ко всем вложенным папкам и файлам, выберите вариант только для текущей папки, так как вы очищаете только флаг сжатия.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-186">If you are asked whether to apply this to just to the current folder or to all subfolders and files, select “just this folder” because you are only clearing the compress flag.</span></span> <span data-ttu-id="bcdd1-187">После этого команда `wsl –set-version` будет работать правильно.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-187">After this, the `wsl –set-version` command should work.</span></span>

![Снимок экрана с параметрами свойств дистрибутива WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> <span data-ttu-id="bcdd1-189">В этом примере папка LocalState для дистрибутива Ubuntu 18.04 расположена по адресу C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span><span class="sxs-lookup"><span data-stu-id="bcdd1-189">In my case, the LocalState folder for my Ubuntu 18.04 distribution was located at C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span></span>
>
> <span data-ttu-id="bcdd1-190">Чтобы получать обновленные сведения, проверьте [ветку № 4103 в документации GitHub WSL](https://github.com/microsoft/WSL/issues/4103), где отслеживается эта проблема.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-190">Check [WSL Docs GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="bcdd1-191">**Термин WSL не распознан как имя командлета, функции, файла скрипта или действующей программы.**</span><span class="sxs-lookup"><span data-stu-id="bcdd1-191">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="bcdd1-192">Убедитесь, что установлен дополнительный компонент [Подсистема Windows для Linux](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="bcdd1-192">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="bcdd1-193">Кроме того, эта ошибка возникнет, если вы используете устройство ARM64 и выполняете эту команду в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-193">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="bcdd1-194">Вместо этого запустите `wsl.exe` из [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) или командной строки.</span><span class="sxs-lookup"><span data-stu-id="bcdd1-194">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
