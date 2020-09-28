---
title: Установка подсистемы Windows для Linux (WSL) в Windows 10
description: Узнайте, как установить дистрибутивы Linux (включая Ubuntu, Debian, SUSE, Kali, Fedora, Pengwin и Alpine) на компьютере под управлением Windows 10 с помощью терминала Bash.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, установка, включить, WSL2, версия 2
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: f617f006ae8067da8adbe1449bfcfe5bf32e73a3
ms.sourcegitcommit: 1232d3b3becc4ceaa113f8ffb0b935c5550f99a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "90777655"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Руководство по установке подсистемы Windows для Linux в Windows 10

## <a name="install-windows-subsystem-for-linux"></a>Установка подсистемы Windows для Linux

Существует две версии подсистемы Windows для Linux (WSL), которые можно выбрать при установке. WSL 2 обеспечивает более высокую общую производительность. Мы рекомендуем использовать ее. Если ваша система не поддерживает WSL 2 или у вас особый случай, когда требуется использовать межсистемное хранилище файлов, возможно, вы захотите выбрать WSL 1. Узнайте больше о [сравнении WSL 2 и WSL 1](./compare-versions.md).

## <a name="step-1---enable-the-windows-subsystem-for-linux"></a>Шаг 1. Включение подсистемы Windows для Linux

Перед установкой дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux".

Запустите PowerShell с правами администратора и выполните следующую команду.

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

Теперь перейдите к шагу 2 и выполните обновление до WSL 2. Если вы хотите установить только WSL 1, вы можете перезагрузить компьютер и перейти к разделу [Шаг 6. Установка дистрибутива Linux по выбору](./install-win10.md#step-6---install-your-linux-distribution-of-choice). Чтобы выполнить обновление до WSL 2, дождитесь перезагрузки компьютера и перейдите к следующему шагу.

## <a name="step-2---update-to-wsl-2"></a>Шаг 2. Обновление до WSL 2

Для обновления до WSL 2 требуется Windows 10.

### <a name="requirements"></a>Требования

- Для 64-разрядных систем: **версия 1903** или более поздняя со **сборкой 18362** или более поздней версии.
- Для систем ARM64: **версия 2004** или более поздняя со **сборкой 19041** или более поздней версии.
- Сборки ниже 18362 не поддерживают WSL 2. Для обновления версии Windows используйте [помощник по обновлению Windows](https://www.microsoft.com/software-download/windows10).

Чтобы проверить версию и номер сборки, нажмите клавиши **Windows+R**, введите **winver** и нажмите кнопку **ОК**. (Или введите команду `ver` в командной строке Windows). В меню "Параметры" [выполните обновление до последней версии Windows](ms-settings:windowsupdate).

> [!NOTE]
> Если вы используете Windows 10 версии 1903 или 1909, в меню Windows откройте меню "Параметры", перейдите к разделу "Обновления и безопасность" и выберите "Проверить наличие обновлений". Номер сборки должен быть 18362.1049 и выше или 18363.1049 и выше с номером дополнительной сборки не ниже 1049. Подробнее: [поддержка WSL 2 вскоре будет реализована в Windows 10 версий 1903 и 1909](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/). См. [инструкции по устранению неполадок](https://docs.microsoft.com/windows/wsl/troubleshooting#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).

## <a name="step-3---enable-virtual-machine-feature"></a>Шаг 3. Включение компонента виртуальных машин

Перед установкой WSL 2 необходимо включить необязательный компонент **Платформа виртуальных машин**.

Запустите PowerShell с правами администратора и выполните следующую команду.

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

**Перезапустите** компьютер, чтобы завершить установку и обновление WSL до WSL 2.

## <a name="step-4---download-the-linux-kernel-update-package"></a>Шаг 4. Скачивание пакета обновления ядра Linux

1. Скачайте пакет последней версии:
    - [Пакет обновления ядра Linux в WSL 2 для 64-разрядных компьютеров.](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

    > [!NOTE]
    > Если вы используете компьютер ARM64, вместо этого скачайте [пакет ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi). Если вы не знаете, какой тип компьютера используете, откройте командную строку или PowerShell и введите `systeminfo | find "System Type"`.

2. Запустите пакет обновления, скачанный на предыдущем этапе. (Для запуска щелкните дважды. Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.)

Когда установка завершится, перейдите к следующему шагу — выбору WSL 2 в качестве версии по умолчанию при установке новых дистрибутивов Linux. (Пропустите этот шаг, если вы хотите, чтобы новые дистрибутивы Linux были установлены в WSL 1).

> [!NOTE]
> Дополнительные сведения см. в статье об [изменениях процесса установки обновления ядра Linux в WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), доступной в блоге, [посвященному командной строке Windows](https://aka.ms/cliblog).

## <a name="step-5---set-wsl-2-as-your-default-version"></a>Шаг 5. Выбор WSL 2 в качестве версии по умолчанию

Откройте PowerShell от имени администратора и выполните следующую команду, чтобы задать WSL 2 в качестве версии по умолчанию при установке нового дистрибутива Linux:

```powershell
wsl --set-default-version 2
```

> [!NOTE]
> Обновление с WSL 1 до WSL 2 может занять несколько минут в зависимости от размера целевого дистрибутива. Если вы используете устаревшую установку WSL 1 из Юбилейного обновления Windows 10 или обновления Creators Update, может возникнуть ошибка обновления. Выполните эти инструкции, чтобы [удалить устаревшие дистрибутивы](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).
>
> Если `wsl --set-default-version` выполняется как недопустимая команда, введите `wsl --help`. Если `--set-default-version` нет в списке, это указывает на отсутствие поддержки в ОС. Вам нужно выполнить обновление до версии 1903, сборки 18362 или выше.
>
> После выполнения команды может появиться следующее сообщение: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`. Это значит, что вам по-прежнему нужно установить пакет обновления MSI для ядра Linux.

## <a name="step-6---install-your-linux-distribution-of-choice"></a>Шаг 6. Установка дистрибутива Linux по выбору

1. Откройте [Microsoft Store](https://aka.ms/wslstore) и выберите предпочтительный дистрибутив Linux.

    ![Представление дистрибутивов Linux в Microsoft Store](media/store.png)

    Ниже приведены ссылки на страницы Microsoft Store для каждого дистрибутива:

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [Ubuntu 20.04 LTS](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [openSUSE Leap 15.1](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [SUSE Linux Enterprise Server 12 SP5](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [SUSE Linux Enterprise Server 15 SP1](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

2. На странице дистрибутива щелкните "Получить".

    ![Дистрибутивы Linux в Microsoft Store](media/UbuntuStore.png)

## <a name="step-7---set-up-a-new-distribution"></a>Шаг 7. Настройка нового дистрибутива

При первом запуске недавно установленного дистрибутива Linux откроется окно консоли, и вам будет предложено подождать минуту или две, чтобы файлы распаковались и сохранились на компьютере. Все будущие запуски должны занимать меньше секунды.

Затем необходимо будет [создать учетную запись пользователя и пароль для нового дистрибутива Linux](./user-support.md).

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

**Поздравляем! Вы успешно установили и настроили дистрибутив Linux, который полностью интегрирован с операционной системой Windows.**

## <a name="install-windows-terminal-optional"></a>Установка Терминала Windows (необязательно)

В Терминале Windows можно использовать несколько вкладок (чтобы быстро переходить между несколькими командными строками Linux, командной строкой Windows, PowerShell, Azure CLI и пр.), создавать пользовательские сочетания клавиш (для открытия и закрытия вкладок, копирования и вставки и пр.), а также применять функцию поиска и пользовательские темы (цветовые схемы, стили и размеры шрифтов, а также фоновое изображение, размытие и прозрачность). [Подробнее.](https://docs.microsoft.com/windows/terminal)

[Установка Терминала Windows](https://docs.microsoft.com/windows/terminal/get-started)

  ![Терминал Windows](media/terminal.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>Установите вашу версию дистрибутива на WSL 1 или WSL 2

Вы можете проверить версию WSL, назначенную каждому из установленных дистрибутивов Linux, открыв командную строку PowerShell и введя команду (доступна только в [сборке Windows 18362](ms-settings:windowsupdate) или выше): `wsl -l -v`.

```powershell
wsl --list --verbose
```

Чтобы настроить дистрибутив для одной из версий WSL, выполните:

```powershell
wsl --set-version <distribution name> <versionNumber>
```

Не забудьте заменить `<distribution name>` на фактическое имя дистрибутива и `<versionNumber>` с номером "1" или "2". Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".

Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:

```powershell
wsl --set-default-version 2
```

Будет установлена версия любого нового дистрибутива, установленного в WSL 2.

## <a name="troubleshooting-installation"></a>Устранение неполадок установки

Ниже перечислены возможные ошибки и способы их устранения. Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).

- **Сбой установки с ошибкой 0x80070003**
  - Подсистема Windows для Linux работает только на системном диске (обычно это диск `C:`). Убедитесь, что дистрибутивы хранятся на системном диске.  
  - Выберите **Параметры** -> **Хранилище** -> **More Storage Settings: (Другие параметры хранилища:) Изменить место сохранения нового содержимого**.
    ![Изображение параметров системы для установки приложений на диске C:](media/AppStorage.png)

- **Сбой WslRegisterDistribution с ошибкой 0x8007019e**
  - Дополнительный компонент "Подсистема Windows для Linux" не включен.
  - Выберите **Панель управления** -> **Программы и компоненты** -> **Включение или отключение компонентов Windows** и установите флажок **Подсистема Windows для Linux** или используйте командлет PowerShell, упомянутый в начале этой статьи.

- **Сбой установки с ошибкой 0x80070003 или ошибкой 0x80370102.**
  - Убедитесь, что в BIOS вашего компьютера включена виртуализация. Расположение этого параметра зависит от компьютера, но обычно он находится в разделе настроек ЦП в BIOS.

- **При попытке обновления возникает ошибка `Invalid command line option: wsl --set-version Ubuntu 2`.**
  - Убедитесь, что у вас включена подсистема Windows для Linux и используется сборка Windows 18362 или выше. Чтобы включить WSL, выполните эту команду в командной строке PowerShell с правами администратора: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.

- **Запрошенную операцию не удалось выполнить из-за ограничения системы виртуального диска. Файлы виртуального жесткого диска должны быть распакованными, незашифрованными и не разреженными.**
  - Снимите флажок Compress contents (Сжимать содержимое) (а также флажок Encrypt contents (Шифровать содержимое), если он установлен), открыв папку профиля для дистрибутива Linux. Он должен находиться в подпапке файловой системы Windows, для примера: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.
  - В этом профиле дистрибутива Linux должна находиться папка LocalState. Щелкните эту папку правой кнопкой мыши, чтобы отобразить меню параметров. Выберите Properties (Свойства) > Advanced (Дополнительно) и убедитесь, что флажки Compress contents to save disk space (Сжимать содержимое для экономии места на диске) и Encrypt contents to secure data (Шифровать содержимое для защиты данных) не установлены. Если вы увидите запрос на применение параметров к текущей папке или ко всем вложенным папкам и файлам, выберите вариант только для текущей папки, так как вы очищаете только флаг сжатия. После этого команда `wsl --set-version` будет работать правильно.

![Снимок экрана с параметрами свойств дистрибутива WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> В этом примере папка LocalState для дистрибутива Ubuntu 18.04 расположена по адресу C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc
>
> Чтобы получать обновленные сведения, проверьте [ветку № 4103 в документации GitHub WSL](https://github.com/microsoft/WSL/issues/4103), где отслеживается эта проблема.

- **Термин WSL не распознан как имя командлета, функции, файла скрипта или действующей программы.**
  - Убедитесь, что установлен дополнительный компонент [Подсистема Windows для Linux](./install-win10.md#step-3---enable-virtual-machine-feature). Кроме того, эта ошибка возникнет, если вы используете устройство ARM64 и выполняете эту команду в PowerShell. Вместо этого запустите `wsl.exe` из [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) или командной строки.

- **Error: This update only applies to machines with the Windows Subsystem for Linux** (Ошибка. Это обновление применяется только к компьютерам с подсистемой Windows для Linux).
  - Чтобы установить пакет обновления MSI для ядра Linux, нужно сначала включить WSL. В случае сбоя отображается следующее сообщение: `This update only applies to machines with the Windows Subsystem for Linux`.
  - Есть три возможные причины, по которым вы видите это сообщение:

  1. Вы используете старую версию Windows, которая не поддерживает WSL 2. Требования к версиям и ссылки пакеты обновления см. на шаге 2.

  2. Компонент WSL не включен. Необходимо вернуться к шагу 1 и убедиться, что на компьютере включен необязательный компонент WSL.

  3. Когда он будет включен, перезагрузите компьютер, чтобы изменения вступили в силу, и повторите попытку.

- **Error: WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel .** (Ошибка. Для WSL 2 требуется обновление компонента ядра. Дополнительные сведения см. здесь: https://aka.ms/wsl2kernel ).
  - Эта ошибка возникает, если пакет ядра Linux отсутствует в папке %SystemRoot%\system32\lxss\tools. Чтобы устранить ошибку, установите пакет обновления MSI для ядра Linux, как описано на шаге 4 в этих инструкциях по установке. Возможно, вам потребуется удалить пакет MSI в разделе [Установка и удаление программ](ms-settings:appsfeatures-app), а затем снова установить его.
