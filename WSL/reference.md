---
title: Справочные материалы по командам подсистемы Windows для Linux
description: См. список команд, управляющих подсистемой Windows для Linux, включая аргументы для выполнения команд Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: fc5c9e06c597092a3790ba7f9eb06054a33450c1
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866131"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="51ee6-104">Справочные материалы по командам подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="51ee6-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="51ee6-105">Лучший способ взаимодействовать с подсистемой Windows для Linux — использовать команду `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="51ee6-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span>

## <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="51ee6-106">Задать WSL 2 в качестве версии по умолчанию</span><span class="sxs-lookup"><span data-stu-id="51ee6-106">Set WSL 2 as your default version</span></span>

<span data-ttu-id="51ee6-107">Выполните следующую команду в PowerShell, чтобы задать WSL 2 в качестве версии по умолчанию при установке нового дистрибутива Linux:</span><span class="sxs-lookup"><span data-stu-id="51ee6-107">Run the following command in Powershell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="51ee6-108">Установите вашу версию дистрибутива на WSL 1 или WSL 2</span><span class="sxs-lookup"><span data-stu-id="51ee6-108">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="51ee6-109">Вы можете проверить версию WSL, назначенную каждому из установленных дистрибутивов Linux, открыв командную строку PowerShell и введя команду (доступна только в [сборке Windows 19041](ms-settings:windowsupdate) или более поздней версии): `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="51ee6-109">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```bash
wsl --list --verbose
```

<span data-ttu-id="51ee6-110">Чтобы настроить дистрибутив для одной из версий WSL, выполните:</span><span class="sxs-lookup"><span data-stu-id="51ee6-110">To set a distribution to be backed by either version of WSL please run:</span></span>

```bash
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="51ee6-111">Не забудьте заменить `<distribution name>` на фактическое имя дистрибутива и `<versionNumber>` с номером "1" или "2".</span><span class="sxs-lookup"><span data-stu-id="51ee6-111">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="51ee6-112">Вы можете всегда вернуться к WSL версии 1, выполнив эту команду и заменив "2" на "1".</span><span class="sxs-lookup"><span data-stu-id="51ee6-112">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="51ee6-113">Кроме того, если вы хотите сделать WSL 2 архитектурой по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="51ee6-113">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```bash
wsl --set-default-version 2
```

<span data-ttu-id="51ee6-114">Будет установлена версия любого нового дистрибутива, установленного в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="51ee6-114">This will set the version of any new distribution installed to WSL 2.</span></span>

## `wsl.exe`

<span data-ttu-id="51ee6-115">Ниже приведен список, содержащий все параметры `wsl.exe` при использовании в Windows версии 1903.</span><span class="sxs-lookup"><span data-stu-id="51ee6-115">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="51ee6-116">Использование: `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="51ee6-116">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-commands"></a><span data-ttu-id="51ee6-117">Аргументы для выполнения команд Linux</span><span class="sxs-lookup"><span data-stu-id="51ee6-117">Arguments for running Linux commands</span></span>

* <span data-ttu-id="51ee6-118">**Без аргументов**</span><span class="sxs-lookup"><span data-stu-id="51ee6-118">**Without arguments**</span></span>

  <span data-ttu-id="51ee6-119">Если командная строка не указана, wsl.exe запускает оболочку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51ee6-119">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="51ee6-120">**--exec, -e \<CommandLine>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-120">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="51ee6-121">Выполнение указанной команды без использования оболочки Linux по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51ee6-121">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="51ee6-122">Остальная часть командной строки передается "как есть".</span><span class="sxs-lookup"><span data-stu-id="51ee6-122">Pass the remaining command line as is.</span></span>

<span data-ttu-id="51ee6-123">Приведенные выше команды также принимают следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="51ee6-123">The above commands also accept the following options:</span></span>

* <span data-ttu-id="51ee6-124">**--distribution, -d \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-124">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="51ee6-125">Запуск указанного дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="51ee6-125">Run the specified distribution.</span></span>

* <span data-ttu-id="51ee6-126">**--user, -u \<UserName>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-126">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="51ee6-127">Выполнение от имени указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="51ee6-127">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="51ee6-128">Аргументы для управления подсистемой Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="51ee6-128">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="51ee6-129">**--export \<Distro> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-129">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="51ee6-130">Экспорт дистрибутива в TAR-файл.</span><span class="sxs-lookup"><span data-stu-id="51ee6-130">Exports the distribution to a tar file.</span></span> <span data-ttu-id="51ee6-131">Именем файла может быть "-" для стандартного вывода.</span><span class="sxs-lookup"><span data-stu-id="51ee6-131">The filename can be - for standard output.</span></span>

* <span data-ttu-id="51ee6-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="51ee6-133">Импорт указанного TAR-файла в качестве нового дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="51ee6-133">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="51ee6-134">Именем файла может быть "-" для стандартного ввода.</span><span class="sxs-lookup"><span data-stu-id="51ee6-134">The filename can be - for standard input.</span></span>

* <span data-ttu-id="51ee6-135">**--list, -l [параметры]**</span><span class="sxs-lookup"><span data-stu-id="51ee6-135">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="51ee6-136">Вывод списка дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="51ee6-136">Lists distributions.</span></span>

  <span data-ttu-id="51ee6-137">Параметры:</span><span class="sxs-lookup"><span data-stu-id="51ee6-137">Options:</span></span>
  * <span data-ttu-id="51ee6-138">**--all**</span><span class="sxs-lookup"><span data-stu-id="51ee6-138">**--all**</span></span>

    <span data-ttu-id="51ee6-139">Вывод списка всех дистрибутивов, включая дистрибутивы, которые сейчас устанавливаются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="51ee6-139">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="51ee6-140">**--running**</span><span class="sxs-lookup"><span data-stu-id="51ee6-140">**--running**</span></span>

    <span data-ttu-id="51ee6-141">Вывод списка всех дистрибутивов, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="51ee6-141">List only distributions that are currently running.</span></span>

* <span data-ttu-id="51ee6-142">**--set-default, -s \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-142">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="51ee6-143">Указание дистрибутива, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51ee6-143">Sets the distribution as the default.</span></span>

* <span data-ttu-id="51ee6-144">**--terminate, -t \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-144">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="51ee6-145">Завершение указанного дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="51ee6-145">Terminates the specified distribution.</span></span>

* <span data-ttu-id="51ee6-146">**--unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-146">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="51ee6-147">Отмените регистрацию дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="51ee6-147">Un-register the distribution.</span></span>

* <span data-ttu-id="51ee6-148">**--help** отображает сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="51ee6-148">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="51ee6-149">Дополнительные команды</span><span class="sxs-lookup"><span data-stu-id="51ee6-149">Additional Commands</span></span>

<span data-ttu-id="51ee6-150">Доступны также устоявшиеся команды для взаимодействия с подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="51ee6-150">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="51ee6-151">Их функциональные возможности реализованы в `wsl.exe`, но эти команды по-прежнему можно использовать.</span><span class="sxs-lookup"><span data-stu-id="51ee6-151">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span>

### `wslconfig.exe`

<span data-ttu-id="51ee6-152">Эта команда позволяет настроить дистрибутив WSL.</span><span class="sxs-lookup"><span data-stu-id="51ee6-152">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="51ee6-153">Ниже приводится список ее параметров.</span><span class="sxs-lookup"><span data-stu-id="51ee6-153">Below is a list of its options.</span></span>

<span data-ttu-id="51ee6-154">Использование: `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="51ee6-154">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="51ee6-155">Аргументы</span><span class="sxs-lookup"><span data-stu-id="51ee6-155">Arguments</span></span>

* <span data-ttu-id="51ee6-156">**/l, /list [параметры]**</span><span class="sxs-lookup"><span data-stu-id="51ee6-156">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="51ee6-157">Вывод списка зарегистрированных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="51ee6-157">Lists registered distributions.</span></span>
  
<span data-ttu-id="51ee6-158">Параметры:</span><span class="sxs-lookup"><span data-stu-id="51ee6-158">Options:</span></span>

* <span data-ttu-id="51ee6-159">**/all** Дополнительный вывод списка всех дистрибутивов, включая дистрибутивы, которые сейчас устанавливаются или удаляются.</span><span class="sxs-lookup"><span data-stu-id="51ee6-159">**/all** Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

* <span data-ttu-id="51ee6-160">**/running** Вывод списка всех дистрибутивов, выполняемых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="51ee6-160">**/running** List only distributions that are currently running.</span></span>

* <span data-ttu-id="51ee6-161">**/s, /setdefault \<Distro>** Задание дистрибутива, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51ee6-161">**/s, /setdefault \<Distro>** Sets the distribution as the default.</span></span>

* <span data-ttu-id="51ee6-162">**/t, /terminate \<Distro>** Завершение работы дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="51ee6-162">**/t, /terminate \<Distro>** Terminates the distribution.</span></span>

* <span data-ttu-id="51ee6-163">**/u, /unregister \<Distro>** Отмена регистрации дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="51ee6-163">**/u, /unregister \<Distro>** Un-registers the distribution.</span></span>

* <span data-ttu-id="51ee6-164">**/upgrade \<Distro>** Обновление дистрибутива до файловой системы WslFs.</span><span class="sxs-lookup"><span data-stu-id="51ee6-164">**/upgrade \<Distro>** Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="51ee6-165">Эта команда используется для запуска оболочки Bash.</span><span class="sxs-lookup"><span data-stu-id="51ee6-165">This command is used to start a bash shell.</span></span> <span data-ttu-id="51ee6-166">Ниже приведены параметры, которые можно использовать с этой командой.</span><span class="sxs-lookup"><span data-stu-id="51ee6-166">Below are the options you can use with this command.</span></span>

<span data-ttu-id="51ee6-167">Использование: `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="51ee6-167">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="51ee6-168">**Параметр не задан**</span><span class="sxs-lookup"><span data-stu-id="51ee6-168">**No Option given**</span></span>
  
  <span data-ttu-id="51ee6-169">Запуск оболочки Bash в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="51ee6-169">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="51ee6-170">Если оболочка Bash не установлена, автоматически запускается `lxrun /install`.</span><span class="sxs-lookup"><span data-stu-id="51ee6-170">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="51ee6-171">Команда `bash ~` запускает оболочку Bash в корневом каталоге пользователя.</span><span class="sxs-lookup"><span data-stu-id="51ee6-171">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="51ee6-172">Это аналог команды `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="51ee6-172">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="51ee6-173">**-c \<command>**</span><span class="sxs-lookup"><span data-stu-id="51ee6-173">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="51ee6-174">Выполнение команды, вывод выходных данных и возврат в командную строку Windows.</span><span class="sxs-lookup"><span data-stu-id="51ee6-174">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>

  <span data-ttu-id="51ee6-175">Пример: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="51ee6-175">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="51ee6-176">Нерекомендуемые команды</span><span class="sxs-lookup"><span data-stu-id="51ee6-176">Deprecated Commands</span></span>

<span data-ttu-id="51ee6-177">Команда `lxrun.exe` была первой командой, используемой для установки подсистемы Windows для Linux и управления ею.</span><span class="sxs-lookup"><span data-stu-id="51ee6-177">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="51ee6-178">Она считается нерекомендуемой в Windows 10 версии 1803 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="51ee6-178">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="51ee6-179">С помощью команды `lxrun.exe` можно взаимодействовать с [подсистемой Windows для Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) напрямую.</span><span class="sxs-lookup"><span data-stu-id="51ee6-179">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="51ee6-180">Эти команды устанавливаются в каталог `\Windows\System32` и могут выполняться в командной строке Windows или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="51ee6-180">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="51ee6-181">Команда</span><span class="sxs-lookup"><span data-stu-id="51ee6-181">Command</span></span>                     | <span data-ttu-id="51ee6-182">Описание</span><span class="sxs-lookup"><span data-stu-id="51ee6-182">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="51ee6-183">Команда lxrun используется для управления экземпляром WSL.</span><span class="sxs-lookup"><span data-stu-id="51ee6-183">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="51ee6-184">Запускает процесс скачивания и установки.</span><span class="sxs-lookup"><span data-stu-id="51ee6-184">Starts the download and install process.</span></span> <br/> <span data-ttu-id="51ee6-185">Можно добавить параметр **/y** для обхода всех запросов.</span><span class="sxs-lookup"><span data-stu-id="51ee6-185">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="51ee6-186">Запрос на подтверждение будет принят автоматически, а в качестве привилегированного пользователя будет задан пользователь по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51ee6-186">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="51ee6-187">Удаляет дистрибутив и образ Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="51ee6-187">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="51ee6-188">По умолчанию это не приводит к удалению корневого каталога пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="51ee6-188">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="51ee6-189">Можно добавить параметр **/y** для автоматического принятия запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="51ee6-189">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="51ee6-190">Параметр **/full** позволяет удалить дистрибутив вместе с корневым каталогом пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="51ee6-190">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="51ee6-191">Задает использование Bash по умолчанию для пользователя Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="51ee6-191">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="51ee6-192">Запрашивает пароль, если указанный пользователь не существует.</span><span class="sxs-lookup"><span data-stu-id="51ee6-192">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="51ee6-193">Дополнительные сведения: https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="51ee6-193">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="51ee6-194">Параметр **/y** позволяет обойти запрос пароля.</span><span class="sxs-lookup"><span data-stu-id="51ee6-194">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="51ee6-195">Пользователь будет создан без пароля.</span><span class="sxs-lookup"><span data-stu-id="51ee6-195">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="51ee6-196">Обновляет индекс пакетов подсистемы.</span><span class="sxs-lookup"><span data-stu-id="51ee6-196">Updates the subsystem's package index</span></span>          |
