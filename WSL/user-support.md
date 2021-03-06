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
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a>Создание учетной записи пользователя и пароля для нового дистрибутива Linux

Когда вы [включите WSL и установите дистрибутив Linux из Microsoft Store](./install-win10.md), при открытии установленного дистрибутива Linux вам нужно будет сразу создать учетную запись и указать **имя пользователя** и **пароль**.

- Для каждого дистрибутива Linux используются свои **имя пользователя** и **пароль**, и они не связаны с именем пользователя Windows.

- После создания **имени пользователя** и **пароля** учетная запись будет использоваться по умолчанию для этого дистрибутива, и вы сможете автоматически входить в систему при запуске.

- Эта учетная запись будет считаться администратором Linux с возможностью запуска административных команд `sudo` (команд суперпользователя).

- Каждый дистрибутив Linux, работающий в подсистеме Windows для Linux, имеет собственные учетные записи пользователей Linux с паролями.  Учетную запись пользователя Linux нужно настраивать при каждом добавлении, переустановке или сбросе дистрибутива.

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a>Обновление и модификация пакетов

Большинство дистрибутивов поставляется с пустым или минимально наполненным каталогом пакетов. Мы настоятельно рекомендуем регулярно обновлять каталог пакетов и установленные пакеты с помощью предпочтительного диспетчера пакетов дистрибутива. Для Debian или Ubuntu используется функция apt.

```bash
sudo apt update && sudo apt upgrade
```

Windows не выполняет автоматическую установку обновлений или обновление дистрибутивов Linux. Это задача, выполнение которой большинство пользователей Linux предпочитают контролировать самостоятельно.

## <a name="reset-your-linux-password"></a>Сброс пароля Linux

Чтобы изменить пароль, откройте дистрибутив Linux (например, Ubuntu) и выполните команду `passwd`.

Вам будет предложено ввести текущий пароль, а затем появится запрос на ввод нового пароля, который нужно подтвердить.

## <a name="forgot-your-password"></a>Пароль утерян

Если вы забыли пароль для дистрибутива Linux, сделайте следующее.

1. Откройте PowerShell и перейдите в корень дистрибутива WSL по умолчанию с помощью команды `wsl -u root`.

    > Если вам нужно обновить забытый пароль в дистрибутиве, который не используется по умолчанию, используйте команду `wsl -d Debian -u root`, заменив `Debian` именем целевого дистрибутива.

2. Открыв дистрибутив WSL на корневом уровне в PowerShell, вы можете использовать для обновления пароля команду `passwd <WSLUsername>`, где `<WSLUsername>` — это имя пользователя для учетной записи в дистрибутиве, пароль к которой вы забыли.

3. Вам будет предложено ввести новый пароль UNIX, а затем подтвердить его. Когда пароль будет обновлен, закройте WSL в PowerShell, выполнив команду `exit`.

> [!NOTE]
> Если вы используете раннюю версию ОС Windows, например 1703 (Creators Update) или 1709 (Fall Creators Update), см. [архивный документ по обновлению такой учетной записи](./user-support-archived.md).
