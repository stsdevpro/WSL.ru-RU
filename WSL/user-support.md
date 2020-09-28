---
title: Создание и обновление учетных записей пользователей для дистрибутивов Linux
description: Справочные материалы по управлению учетными записями пользователей и разрешениями для подсистемы Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, учетные записи пользователей
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7f1ad56a6f4261ad0455ee93bdeb5e31d0ed10d1
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818726"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a><span data-ttu-id="6d90e-104">Создание учетной записи пользователя и пароля для нового дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="6d90e-104">Create a user account and password for your new Linux distribution</span></span>

<span data-ttu-id="6d90e-105">Когда вы [включите WSL и установите дистрибутив Linux из Microsoft Store](./install-win10.md), при открытии установленного дистрибутива Linux вам нужно будет сразу создать учетную запись и указать **имя пользователя** и **пароль**.</span><span class="sxs-lookup"><span data-stu-id="6d90e-105">Once you have [enabled WSL and installed a Linux distribution from the Microsoft Store](./install-win10.md), the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="6d90e-106">Для каждого дистрибутива Linux используются свои **имя пользователя** и **пароль**, и они не связаны с именем пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="6d90e-106">This **User Name** and **Password** is specific to each separate Linux distribution that you install and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="6d90e-107">После создания **имени пользователя** и **пароля** учетная запись будет использоваться по умолчанию для этого дистрибутива, и вы сможете автоматически входить в систему при запуске.</span><span class="sxs-lookup"><span data-stu-id="6d90e-107">Once you create a **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="6d90e-108">Эта учетная запись будет считаться администратором Linux с возможностью запуска административных команд `sudo` (команд суперпользователя).</span><span class="sxs-lookup"><span data-stu-id="6d90e-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="6d90e-109">Каждый дистрибутив Linux, работающий в подсистеме Windows для Linux, имеет собственные учетные записи пользователей Linux с паролями.</span><span class="sxs-lookup"><span data-stu-id="6d90e-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="6d90e-110">Учетную запись пользователя Linux нужно настраивать при каждом добавлении, переустановке или сбросе дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="6d90e-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a><span data-ttu-id="6d90e-112">Обновление и модификация пакетов</span><span class="sxs-lookup"><span data-stu-id="6d90e-112">Update and upgrade packages</span></span>

<span data-ttu-id="6d90e-113">Большинство дистрибутивов поставляется с пустым или минимально наполненным каталогом пакетов.</span><span class="sxs-lookup"><span data-stu-id="6d90e-113">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="6d90e-114">Мы настоятельно рекомендуем регулярно обновлять каталог пакетов и установленные пакеты с помощью предпочтительного диспетчера пакетов дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="6d90e-114">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distribution's preferred package manager.</span></span> <span data-ttu-id="6d90e-115">Для Debian или Ubuntu используется функция apt.</span><span class="sxs-lookup"><span data-stu-id="6d90e-115">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="6d90e-116">Windows не выполняет автоматическую установку обновлений или обновление дистрибутивов Linux.</span><span class="sxs-lookup"><span data-stu-id="6d90e-116">Windows does not automatically update or upgrade your Linux distribution(s).</span></span> <span data-ttu-id="6d90e-117">Это задача, выполнение которой большинство пользователей Linux предпочитают контролировать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="6d90e-117">This is a task that most Linux users prefer to control themselves.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="6d90e-118">Сброс пароля Linux</span><span class="sxs-lookup"><span data-stu-id="6d90e-118">Reset your Linux password</span></span>

<span data-ttu-id="6d90e-119">Чтобы изменить пароль, откройте дистрибутив Linux (например, Ubuntu) и выполните команду `passwd`.</span><span class="sxs-lookup"><span data-stu-id="6d90e-119">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="6d90e-120">Вам будет предложено ввести текущий пароль, а затем появится запрос на ввод нового пароля, который нужно подтвердить.</span><span class="sxs-lookup"><span data-stu-id="6d90e-120">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

## <a name="forgot-your-password"></a><span data-ttu-id="6d90e-121">Пароль утерян</span><span class="sxs-lookup"><span data-stu-id="6d90e-121">Forgot your password</span></span>

<span data-ttu-id="6d90e-122">Если вы забыли пароль для дистрибутива Linux, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="6d90e-122">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="6d90e-123">Откройте PowerShell и перейдите в корень дистрибутива WSL по умолчанию с помощью команды `wsl -u root`.</span><span class="sxs-lookup"><span data-stu-id="6d90e-123">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

    > <span data-ttu-id="6d90e-124">Если вам нужно обновить забытый пароль в дистрибутиве, который не используется по умолчанию, используйте команду `wsl -d Debian -u root`, заменив `Debian` именем целевого дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="6d90e-124">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="6d90e-125">Открыв дистрибутив WSL на корневом уровне в PowerShell, вы можете использовать для обновления пароля команду `passwd <WSLUsername>`, где `<WSLUsername>` — это имя пользователя для учетной записи в дистрибутиве, пароль к которой вы забыли.</span><span class="sxs-lookup"><span data-stu-id="6d90e-125">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd <WSLUsername>` where `<WSLUsername>` is the username of the account in the DISTRO whose password you've forgotten.</span></span>

3. <span data-ttu-id="6d90e-126">Вам будет предложено ввести новый пароль UNIX, а затем подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6d90e-126">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="6d90e-127">Когда пароль будет обновлен, закройте WSL в PowerShell, выполнив команду `exit`.</span><span class="sxs-lookup"><span data-stu-id="6d90e-127">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="6d90e-128">Если вы используете раннюю версию ОС Windows, например 1703 (Creators Update) или 1709 (Fall Creators Update), см. [архивный документ по обновлению такой учетной записи](./user-support-archived.md).</span><span class="sxs-lookup"><span data-stu-id="6d90e-128">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
