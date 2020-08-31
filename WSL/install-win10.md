---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Узнайте, как установить подсистему Windows для Linux в Windows 10. Windows 10 необходимо обновить до версии 2004, сборки 19041 или выше.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка, включить, WSL2, версия 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 23c72c0e82c90c23fc0406b56dbf8accad0e39df
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866164"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="efa04-105">Руководство по установке подсистемы Windows для Linux в Windows 10</span><span class="sxs-lookup"><span data-stu-id="efa04-105">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="efa04-106">Установка подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="efa04-106">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="efa04-107">Перед установкой дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux".</span><span class="sxs-lookup"><span data-stu-id="efa04-107">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="efa04-108">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="efa04-108">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="efa04-109">Чтобы установить только WSL 1, необходимо перезагрузить компьютер и перейти к пункту [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice) (Установить дистрибутив Linux), в противном случае дождитесь перезапуска и переходите к обновлению до WSL 2.</span><span class="sxs-lookup"><span data-stu-id="efa04-109">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="efa04-110">Узнайте больше о [сравнении WSL 2 и WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="efa04-110">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="efa04-111">Обновление до WSL 2</span><span class="sxs-lookup"><span data-stu-id="efa04-111">Update to WSL 2</span></span>

<span data-ttu-id="efa04-112">Чтобы выполнить обновление до WSL 2, необходимо выполнить следующие условия:</span><span class="sxs-lookup"><span data-stu-id="efa04-112">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="efa04-113">Использовать Windows 10 с [обновлением до версии 1903 или выше](ms-settings:windowsupdate), **сборкой 18362 или выше**.</span><span class="sxs-lookup"><span data-stu-id="efa04-113">Running Windows 10, [updated to version 1903 or higher](ms-settings:windowsupdate), **Build 18362** or higher.</span></span>

- <span data-ttu-id="efa04-114">Проверьте версию Windows, нажав **Windows + R**, введите **winver**, выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="efa04-114">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="efa04-115">(Или введите команду `ver` в командной строке Windows).</span><span class="sxs-lookup"><span data-stu-id="efa04-115">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="efa04-116">[Обновите последнюю версию Windows](ms-settings:windowsupdate), если сборка ниже 18361.</span><span class="sxs-lookup"><span data-stu-id="efa04-116">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 18361.</span></span> <span data-ttu-id="efa04-117">[Получите помощник по Центру обновления Windows](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="efa04-117">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="efa04-118">Включение необязательного компонента "Virtual Machine Platform" (Платформа виртуальной машины)</span><span class="sxs-lookup"><span data-stu-id="efa04-118">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="efa04-119">Перед установкой WSL 2 необходимо включить необязательный компонент "Virtual Machine Platform" (Платформа виртуальных машин).</span><span class="sxs-lookup"><span data-stu-id="efa04-119">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="efa04-120">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="efa04-120">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="efa04-121">**Перезапустите** компьютер, чтобы завершить установку и обновление WSL до WSL 2.</span><span class="sxs-lookup"><span data-stu-id="efa04-121">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="efa04-122">Задать WSL 2 в качестве версии по умолчанию</span><span class="sxs-lookup"><span data-stu-id="efa04-122">Set WSL 2 as your default version</span></span>

<span data-ttu-id="efa04-123">Откройте PowerShell от имени администратора и выполните следующую команду, чтобы задать WSL 2 в качестве версии по умолчанию при установке нового дистрибутива Linux:</span><span class="sxs-lookup"><span data-stu-id="efa04-123">Open PowerShell as Administrator and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="efa04-124">После выполнения этой команды может появиться следующее сообщение: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="efa04-124">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="efa04-125">Перейдите по ссылке ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) и установите MSI-файл с этой страницы документации, чтобы установить на компьютере ядро Linux для WSL 2.</span><span class="sxs-lookup"><span data-stu-id="efa04-125">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="efa04-126">После установки ядра выполните команду еще раз. Она должна успешно завершиться без отображения сообщения.</span><span class="sxs-lookup"><span data-stu-id="efa04-126">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="efa04-127">Обновление с WSL 1 до WSL 2 может занять несколько минут в зависимости от размера целевого дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="efa04-127">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="efa04-128">Если вы используете устаревшую установку WSL 1 из Юбилейного обновления Windows 10 или обновления Creators Update, может возникнуть ошибка обновления.</span><span class="sxs-lookup"><span data-stu-id="efa04-128">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="efa04-129">Выполните эти инструкции, чтобы [удалить устаревшие дистрибутивы](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="efa04-129">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span> 
>
> <span data-ttu-id="efa04-130">Если `wsl --set-default-version` выполняется как недопустимая команда, введите `wsl --help`.</span><span class="sxs-lookup"><span data-stu-id="efa04-130">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="efa04-131">Если `--set-default-version` нет в списке, это указывает на отсутствие поддержки в ОС. Вам нужно выполнить обновление до версии 1903, сборки 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="efa04-131">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 1903, Build 18362 or higher.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="efa04-132">Установка дистрибутива Linux по выбору</span><span class="sxs-lookup"><span data-stu-id="efa04-132">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="efa04-133">Откройте [Microsoft Store](https://aka.ms/wslstore) и выберите предпочтительный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="efa04-133">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    <span data-ttu-id="efa04-135">Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:</span><span class="sxs-lookup"><span data-stu-id="efa04-135">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="efa04-136">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="efa04-136">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="efa04-137">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="efa04-137">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="efa04-138">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="efa04-138">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="efa04-139">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="efa04-139">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="efa04-140">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="efa04-140">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="efa04-141">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="efa04-141">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="efa04-142">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="efa04-142">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="efa04-143">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="efa04-143">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="efa04-144">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="efa04-144">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="efa04-145">Pengwin</span><span class="sxs-lookup"><span data-stu-id="efa04-145">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="efa04-146">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="efa04-146">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="efa04-147">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="efa04-147">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="efa04-148">На странице дистрибутива щелкните "Получить".</span><span class="sxs-lookup"><span data-stu-id="efa04-148">From the distribution's page, select "Get".</span></span>

    ![Дистрибутивы Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="efa04-150">Настройка нового дистрибутива</span><span class="sxs-lookup"><span data-stu-id="efa04-150">Set up a new distribution</span></span>

<span data-ttu-id="efa04-151">При первом запуске недавно установленного дистрибутива Linux откроется окно консоли, и вам будет предложено подождать минуту или две, чтобы файлы распаковались и сохранились на компьютере.</span><span class="sxs-lookup"><span data-stu-id="efa04-151">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="efa04-152">Все будущие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="efa04-152">All future launches should take less than a second.</span></span>

<span data-ttu-id="efa04-153">Затем необходимо будет [создать учетную запись пользователя и пароль для нового дистрибутива Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="efa04-153">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="efa04-155">Установите вашу версию дистрибутива на WSL 1 или WSL 2</span><span class="sxs-lookup"><span data-stu-id="efa04-155">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="efa04-156">Вы можете проверить версию WSL, назначенную каждому из установленных дистрибутивов Linux, открыв командную строку PowerShell и введя команду (доступна только в [сборке Windows 18362](ms-settings:windowsupdate) или выше): `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="efa04-156">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 18362 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="efa04-157">Чтобы настроить дистрибутив для одной из версий WSL, выполните:</span><span class="sxs-lookup"><span data-stu-id="efa04-157">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="efa04-158">Не забудьте заменить `<distribution name>` на фактическое имя дистрибутива и `<versionNumber>` с номером "1" или "2".</span><span class="sxs-lookup"><span data-stu-id="efa04-158">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="efa04-159">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="efa04-159">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="efa04-160">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="efa04-160">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="efa04-161">Будет установлена версия любого нового дистрибутива, установленного в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="efa04-161">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="efa04-162">Устранение неполадок установки</span><span class="sxs-lookup"><span data-stu-id="efa04-162">Troubleshooting installation</span></span>

<span data-ttu-id="efa04-163">Ниже перечислены возможные ошибки и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="efa04-163">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="efa04-164">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="efa04-164">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="efa04-165">**Сбой установки с ошибкой 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="efa04-165">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="efa04-166">Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`).</span><span class="sxs-lookup"><span data-stu-id="efa04-166">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="efa04-167">Убедитесь, что дистрибутивы хранятся на системном диске.</span><span class="sxs-lookup"><span data-stu-id="efa04-167">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="efa04-168">Выберите **Параметры** -> **Хранилище** -> **More Storage Settings: (Другие параметры хранилища:) Изменить место сохранения нового содержимого**.
    ![Изображение параметров системы для установки приложений на диске C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="efa04-168">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="efa04-169">**Сбой WslRegisterDistribution с ошибкой 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="efa04-169">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="efa04-170">Дополнительный компонент "Подсистема Windows для Linux" не включен.</span><span class="sxs-lookup"><span data-stu-id="efa04-170">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="efa04-171">Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="efa04-171">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="efa04-172">**Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**</span><span class="sxs-lookup"><span data-stu-id="efa04-172">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="efa04-173">Убедитесь, что в BIOS вашего компьютера включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="efa04-173">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="efa04-174">Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.</span><span class="sxs-lookup"><span data-stu-id="efa04-174">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="efa04-175">**При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**</span><span class="sxs-lookup"><span data-stu-id="efa04-175">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="efa04-176">Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 18362 или выше.</span><span class="sxs-lookup"><span data-stu-id="efa04-176">Enure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18362 or higher.</span></span> <span data-ttu-id="efa04-177">Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="efa04-177">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span>

- <span data-ttu-id="efa04-178">**Запрошенную операцию не удалось выполнить из-за ограничения системы виртуального диска. Файлы виртуального жесткого диска должны быть распакованными, незашифрованными и не разреженными.**</span><span class="sxs-lookup"><span data-stu-id="efa04-178">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="efa04-179">Снимите флажок Compress contents (Сжимать содержимое) (а также флажок Encrypt contents (Шифровать содержимое), если он установлен), открыв папку профиля для дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="efa04-179">Deselect “Compress contents” (as well as “Encrypt contents” if that’s checked) by opening the profile folder for your Linux distribution.</span></span> <span data-ttu-id="efa04-180">Он должен находиться в подпапке файловой системы Windows, для примера: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.</span><span class="sxs-lookup"><span data-stu-id="efa04-180">It should be located in a folder on your Windows file system, something like: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`</span></span>
  - <span data-ttu-id="efa04-181">В этом профиле дистрибутива Linux должна находиться папка LocalState.</span><span class="sxs-lookup"><span data-stu-id="efa04-181">In this Linux distro profile, there should be a LocalState folder.</span></span> <span data-ttu-id="efa04-182">Щелкните эту папку правой кнопкой мыши, чтобы отобразить меню параметров.</span><span class="sxs-lookup"><span data-stu-id="efa04-182">Right-click this folder to display a menu of options.</span></span> <span data-ttu-id="efa04-183">Выберите Properties (Свойства) > Advanced (Дополнительно) и убедитесь, что флажки Compress contents to save disk space (Сжимать содержимое для экономии места на диске) и Encrypt contents to secure data (Шифровать содержимое для защиты данных) не установлены.</span><span class="sxs-lookup"><span data-stu-id="efa04-183">Select Properties > Advanced and then ensure that the “Compress contents to save disk space” and “Encrypt contents to secure data” checkboxes are unselected (not checked).</span></span> <span data-ttu-id="efa04-184">Если вы увидите запрос на применение параметров к текущей папке или ко всем вложенным папкам и файлам, выберите вариант только для текущей папки, так как вы очищаете только флаг сжатия.</span><span class="sxs-lookup"><span data-stu-id="efa04-184">If you are asked whether to apply this to just to the current folder or to all subfolders and files, select “just this folder” because you are only clearing the compress flag.</span></span> <span data-ttu-id="efa04-185">После этого команда `wsl –set-version` будет работать правильно.</span><span class="sxs-lookup"><span data-stu-id="efa04-185">After this, the `wsl –set-version` command should work.</span></span>

![Снимок экрана с параметрами свойств дистрибутива WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> <span data-ttu-id="efa04-187">В этом примере папка LocalState для дистрибутива Ubuntu 18.04 расположена по адресу C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span><span class="sxs-lookup"><span data-stu-id="efa04-187">In my case, the LocalState folder for my Ubuntu 18.04 distribution was located at C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span></span>
>
> <span data-ttu-id="efa04-188">Чтобы получать обновленные сведения, проверьте [ветку № 4103 в документации GitHub WSL](https://github.com/microsoft/WSL/issues/4103), где отслеживается эта проблема.</span><span class="sxs-lookup"><span data-stu-id="efa04-188">Check [WSL Docs GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="efa04-189">**Термин WSL не распознан как имя командлета, функции, файла скрипта или действующей программы.**</span><span class="sxs-lookup"><span data-stu-id="efa04-189">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="efa04-190">Убедитесь, что установлен дополнительный компонент [Подсистема Windows для Linux](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="efa04-190">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="efa04-191">Кроме того, эта ошибка возникнет, если вы используете устройство ARM64 и выполняете эту команду в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="efa04-191">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="efa04-192">Вместо этого запустите `wsl.exe` из [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) или командной строки.</span><span class="sxs-lookup"><span data-stu-id="efa04-192">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
