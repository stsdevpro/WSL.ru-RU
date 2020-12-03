---
title: Устранение неполадок подсистемы Windows для Linux
description: Содержит подробные сведения о распространенных ошибках и проблемах, с которыми сталкиваются пользователи при выполнении Linux в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 09/28/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: f4040cbe9faf5d55324b56974dd5677052224dd1
ms.sourcegitcommit: d5d3dd8b91e93d46653f9512bceafd8b5340255f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96443748"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Устранение неполадок подсистемы Windows для Linux

Для получения поддержки по вопросам, связанным с WSL, изучите наш [репозиторий продукта WSL на сайте GitHub](https://github.com/Microsoft/wsl/issues).

## <a name="search-for-any-existing-issues-related-to-your-problem"></a>Поиск описанных проблем, связанных с вашей проблемой

При возникновении технических проблем используйте [репозиторий продукта](https://github.com/Microsoft/wsl/issues).

При возникновении проблем, связанных с содержимым этой документации, используйте [репозиторий документов](https://github.com/MicrosoftDocs/wsl/issues).

## <a name="submit-a-bug-report"></a>Отправка отчета об ошибке

При возникновении ошибок, связанных с функциями или компонентами WSL, отправьте сообщение о проблеме в репозитории продуктов: https://github.com/Microsoft/wsl/issues

## <a name="submit-a-feature-request"></a>Отправка запроса на добавление возможностей

Чтобы запросить новую возможность, связанную с функциональностью или совместимостью WSL, [создайте запрос в репозитории продуктов](https://github.com/Microsoft/wsl/issues).

## <a name="contribute-to-the-docs"></a>Участие в разработке документации

Чтобы внести изменения в документацию по WSL, отправьте запрос на вытягивание в репозитории документов: https://github.com/MicrosoftDocs/wsl/issues

## <a name="terminal-or-command-line"></a>Терминал или командная строка

Наконец, если ваша проблема связана с терминалом Windows, консолью Windows или интерфейсом командной строки, используйте репозиторий терминалов Windows: https://github.com/microsoft/terminal

## <a name="common-issues"></a>Распространенные проблемы

### <a name="im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2"></a>Я использую Windows 10 версии 1903, но не вижу параметры для WSL 2.

Скорее всего, это связано с тем, что на компьютере еще не установлены исправления для WSL 2. Чтобы решить эту проблему самым простым способом, перейдите в параметры Windows, нажмите кнопку "Проверить наличие обновлений" и установите последние обновления в системе. Изучите [полные инструкции по получению исправления для старой версии](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).

Если после нажатия кнопки "Проверить наличие обновлений" вы не получили обновление, можно [установить исправления KB4566116 вручную](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4566116).  

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a>Ошибка. 0x1bc, когда `wsl --set-default-version 2`

Это может произойти, если язык интерфейса или язык системы не является английским.

```powershell
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

Фактическая ошибка для `0x1bc`:

```powershell
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

См. сведения о проблеме [5749](https://github.com/microsoft/WSL/issues/5749).

### <a name="cannot-access-wsl-files-from-windows"></a>Не удается получить доступ к файлам WSL из Windows

Файловый сервер протокола 9p предоставляет службу на стороне Linux, которая позволяет Windows получить доступ к файловой системе Linux. Если вы не можете получить доступ к WSL с помощью `\\wsl$` в Windows, возможно, это вызвано неправильным запуском 9P.

Чтобы убедиться в этом, можно проверить журналы запуска с помощью команды `dmesg |grep 9p`. Если ошибки есть, отобразятся сведения о них. Вывод выглядит следующим образом:

```bash
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

Дополнительные сведения об этой ошибке см. в [этом потоке GitHub](https://github.com/microsoft/wsl/issues/5307).

### <a name="cant-start-wsl-2-distribution-and-only-see-wsl-2-in-output"></a>Не удается запустить дистрибутив WSL 2, а в выходных данных отображается только WSL 2.

Если язык интерфейса не английский, возможно, отображается усеченная версия текста ошибки.

```powershell
C:\Users\me>wsl
WSL 2
```

Чтобы устранить эту проблему, перейдите по адресу `https://aka.ms/wsl2kernel` и установите ядро вручную, следуя инструкциям на этой странице документации. 

### <a name="command-not-found-when-executing-windows-exe-in-linux"></a>Ошибка `command not found` при выполнении исполняемых файлов Windows в Linux

Пользователи могут запускать исполняемые файлы Windows, например notepad.exe, прямо в среде Linux. Но иногда это действие приводит к ошибке "Команда не найдена", как показано ниже: 

```Bash
$ notepad.exe
-bash: notepad.exe: command not found
```

Если в переменной $PATH нет обязательных путей Win32, подсистема взаимодействие не сможет найти EXE-файл.
Чтобы проверить это, выполните `echo $PATH` в среде Linux. В выходных данных вы должны увидеть путь к win32 (например, /mnt/c/Windows).
Если вы не видите эти пути Windows, скорее всего переменная PATH перезаписана оболочкой Linux. 

Ниже приведен пример файла /etc/profile на ОС Debian, который вызывал такую проблему:

```Bash
if [ "`id -u`" -eq 0 ]; then
  PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
else
  PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games"
fi
```

Чтобы решить эту проблему в среде Debian, нужно удалить приведенные выше строки.
Вы также можете добавить значения в переменную $PATH во время назначения, как показано ниже, но это может вызвать [другие проблемы](https://salsa.debian.org/debian/WSL/-/commit/7611edba482fd0b3f67143aa0fc1e2cc1d4100a6) с WSL и VSCode.

Дополнительные сведения см. в описании проблем [5296](https://github.com/microsoft/WSL/issues/5296) и [5779](https://github.com/microsoft/WSL/issues/5779).

### <a name="error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed"></a>"Ошибка: 0x80370102 The virtual machine could not be started because a required feature is not installed (Не удалось запустить виртуальную машину, так как не установлена необходимая функция).

Включите компонент платформы виртуальных машин Windows и убедитесь, что в BIOS включена виртуализация.

1. Проверка [требований к системе Hyper-V](/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)

2. Если компьютер является виртуальной машиной, включите [вложенную виртуализацию](./wsl2-faq.md#can-i-run-wsl-2-in-a-virtual-machine) вручную. Запустите PowerShell с правами администратора и выполните следующую команду:

    ```powershell
    Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
    ```

3. Следуйте рекомендациям производителя компьютера, чтобы включить виртуализацию. Как правило, для проверки того, что эти функции включены в ЦП, может использоваться BIOS системы. Инструкции для этого процесса могут быть разными для разных компьютеров, один из примеров вы можете изучить в [этой статье](https://www.bleepingcomputer.com/tutorials/how-to-enable-cpu-virtualization-in-your-computer-bios/) от Bleeping Computer.

4. Перезагрузите компьютер после включения дополнительного компонента `Virtual Machine Platform`.

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash утрачивает подключение к сети после подключения к сети VPN

Если после подключения к VPN в Windows оболочка Bash утрачивает подключение к сети, попробуйте воспользоваться этим обходным решением в Bash. Это решение позволит вручную переопределить разрешение DNS с помощью `/etc/resolv.conf`.

1. Запишите DNS-сервер виртуальной частной сети. Для этого выполните `ipconfig.exe /all`
2. Создайте копию существующего resolv.conf, выполнив `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Разорвите связь с текущим файлом resolv.conf, выполнив команду `sudo unlink /etc/resolv.conf`.
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Откройте `/etc/resolv.conf` и сделайте следующее. <br/>
   a. Удалите из файла первую строку с текстом "\# This file was automatically generated by WSL. To stop automatic generation of this file, remove this line." (Этот файл был автоматически создан WSL. Чтобы остановить автоматическое создание этого файла, удалите данную строку). <br/>
   b. Добавьте запись DNS из пункта 1 выше в качестве первой записи в списке DNS-серверов. <br/>
   c. Закройте файл. <br/>

После отключения VPN необходимо будет отменить изменения в `/etc/resolv.conf`. Для этого сделайте следующее.

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>При запуске WSL или установке дистрибутива возвращается код ошибки

Выполните [эти инструкции](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs), чтобы получить подробные журналы и сообщить о возникшей проблеме на портале GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Обновление Bash для Ubuntu в Windows

Два компонента Bash для Ubuntu в Windows могут требовать обновления.

1. Подсистема Windows для Linux
  
   Обновление этой части Bash для Ubuntu в Windows обеспечит применение всех новых исправлений, описанных в [заметках о выпуске](./release-notes.md). Убедитесь, что вы подписаны на Программу предварительной оценки Windows и что ваша сборка обновлена. Чтобы обеспечить более точное управление, включая сброс экземпляра Ubuntu, ознакомьтесь со [страницей справочных материалов по командам](./reference.md).

2. Двоичные файлы пользователя Ubuntu

   При обновлении этой части Bash для Ubuntu в Windows будут установлены все обновления двоичных файлов пользователя Ubuntu, включая приложения, установленные с помощью apt-get. Чтобы выполнить обновление, выполните следующие команды в Bash.
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Ошибки apt-get upgrade

Некоторые пакеты используют функции, которые еще не реализованы. Например, `udev`пока не поддерживается и вызывает несколько ошибок `apt-get upgrade`.

Чтобы устранить проблемы, связанные с `udev`, выполните следующие действия.

1. Введите приведенный ниже код в `/usr/sbin/policy-rc.d` и сохраните изменения.
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. Добавьте разрешения на выполнение в `/usr/sbin/policy-rc.d`:

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Выполните следующие команды:

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Ошибка: 0x80040306" при установке

Это связано с тем, что мы не поддерживаем устаревшую консоль.
Чтобы отключить устаревшую консоль, выполните следующие действия.

1. Выполните файл cmd.exe.
1. Щелкните правой кнопкой мыши строку заголовка и выберите "Свойства", затем снимите флажок "Использовать прежнюю версию консоли".
1. Нажмите кнопку "ОК".

### <a name="error-0x80040154-after-windows-update"></a>"Ошибка: 0x80040154" после обновления Windows

Компонент "Подсистема Windows для Linux" может быть отключен во время обновления Windows. В этом случае данную функцию Windows необходимо включить заново. Инструкции по включению подсистемы Windows для Linux можно найти в [руководстве по установке](./install-win10.md).

### <a name="changing-the-display-language"></a>Изменение отображаемого языка

Установщик WSL попытается автоматически изменить языковой стандарт Ubuntu в соответствии с языковым стандартом установки Windows.  Если это нежелательно, можно выполнить приведенную ниже команду, чтобы изменить языковой стандарт Ubuntu после завершения установки.  Чтобы это изменение вступило в силу, потребуется повторно запустить bash.exe.

В приведенном ниже примере языковой стандарт изменяется на EN-US.

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Проблемы установки после восстановления системы Windows

1. Удалите папку `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`. <br/>
  **Примечание. Не делайте этого, если дополнительный компонент полностью установлен и работает.**
2. Включите дополнительный компонент WSL (если он еще не включен).
3. Выполните перезагрузку.
4. Выполните команду lxrun /uninstall /full
5. Установите Bash.

### <a name="no-internet-access-in-wsl"></a>Нет доступа к Интернету в WSL

Некоторые пользователи сообщили о проблемах с определенными приложениями брандмауэра, блокирующими доступ к Интернету в WSL.  Сообщили о следующих брандмауэрах:

1. Kaspersky;
2. AVG;
3. Avast.

В некоторых случаях отключение брандмауэра обеспечивает доступ.  В некоторых случаях доступ блокируется просто при наличии установленного брандмауэра.

### <a name="permission-denied-error-when-using-ping"></a>Ошибка "Отказ в разрешении" при проверке связи

В выпуске [Windows Anniversary Update, версия 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update) для проверки связи в WSL требуются **права администратора**.  Чтобы выполнить проверку связи, запустите Bash для Ubuntu в Windows от имени администратора или запустите bash.exe из командной строки или сеанса PowerShell с привилегиями администратора.

В более поздних версиях Windows ([сборка 14926+](./release-notes.md#build-14926)) права администратора не требуются.

### <a name="bash-is-hung"></a>Bash перестал отвечать на запросы

Если при работе с Bash вы обнаружите, что Bash перестал отвечать на запросы (или взаимозаблокирован), помогите нам диагностировать проблему путем сбора и передачи дампа памяти. Обратите внимание на то, что выполнение этих действий приведет к сбою системы. Не делайте этого, если вас это не устраивает, либо предварительно сохраните результаты своей работы.

Сбор дампа памяти

1. Измените тип дампа памяти на "Полный дамп памяти". При изменении типа дампа запишите текущий тип.

2. Выполните [эти действия](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809), чтобы настроить аварийное завершение с помощью клавиатуры.

3. Воспроизведите взаимоблокировку или прекращение ответа на запросы.

4. Выполните аварийное завершение системы с помощью последовательности клавиш из пункта 2.

5. Произойдет аварийное завершение системы и будет собран дамп памяти.

6. После перезагрузки системы отправьте memory.dmp на адрес электронной почты secure@microsoft.com. По умолчанию файл дампа находится в папке %SystemRoot%\memory.dmp или C:\Windows\memory.dmp, если C: является системным диском. В письме укажите, что дамп предназначен для команды разработчиков WSL или Bash в Windows.

7. Восстановите исходное значение типа дампа памяти.

### <a name="check-your-build-number"></a>Проверка номера сборки

Чтобы узнать архитектуру компьютера и номер сборки Windows, выберите  
**Параметры** > **Система** > **О программе**

Найдите поля **Сборка ОС** и **Тип системы**.  
    ![Снимок экрана с полями "Сборка ОС" и "Тип системы"](media/system.png)

Чтобы найти номер сборки Windows Server, выполните в PowerShell следующую команду.  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Подтверждение включения WSL

Вы можете убедиться, что подсистема Windows для Linux включена, выполнив в PowerShell следующую команду.  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Проблемы с подключением к серверу OpenSSH

Попытка подключения к серверу SSH завершается следующей ошибкой: "Connection closed by 127.0.0.1 port 22" (Подключение закрыто узлом 127.0.0.1 через порт 22).

1. Убедитесь, что сервер OpenSSH работает

   ```bash
   sudo service ssh status
   ```

   и вы следовали указаниям в этом руководстве: https://ubuntu.com/server/docs/service-openssh.

2. Завершите работу службы sshd и запустите sshd в режиме отладки.

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. Проверьте журналы запуска и убедитесь, что ключи сервера доступны и в журнале нет сообщений, как показано ниже.

   ```BASH
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

Если вы видите такие сообщения и в разделе `/etc/ssh/` отсутствуют ключи, потребуется повторно создать ключи или просто очистить и установить сервер OpenSSH.

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a>"Указанная сборка не найдена". Это сообщение может появиться при включении дополнительного компонента WSL.

Данная ошибка связана с неправильным состоянием установки. Чтобы устранить эту проблему, выполните следующие действия.

- Если вы используете команду включения компонента WSL в PowerShell, попробуйте использовать графический пользовательский интерфейс. Для этого откройте меню "Пуск", выполните поиск фразы "Включение или отключение компонентов Windows", а затем из списка выберите "Подсистема Windows для Linux". Этот дополнительный компонент будет установлен.

- Обновите версию Windows, выбрав "Параметры" > "Обновления" и щелкнув "Проверить наличие обновлений".

- Если оба способа не помогли и вам нужно использовать WSL, рассмотрите возможность обновления на месте, переустановив Windows 10 с установочного носителя и выбрав параметр "Сохранить все", чтобы сохранить свои приложения и файлы. Инструкции по такой установке можно найти на странице [Переустановка Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).

### <a name="correct-ssh-related-permission-errors"></a>Правильные (связанные с SSH) ошибки разрешений

Если вы видите эту ошибку:

```bash
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

Чтобы устранить эту проблему, добавьте следующий текст в файл ```/etc/wsl.conf```:

```bash
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

Обратите внимание, что добавление этой команды будет включать метаданные и изменять разрешения для файлов Windows, показанных в WSL. См. сведения о [разрешениях файловой системы](./file-permissions.md).

### <a name="running-windows-commands-fails-inside-a-distribution"></a>Выполнение команд Windows завершается сбоем в дистрибутиве

Некоторые дистрибутивы, [доступные в Microsoft Store](install-win10.md#step-6---install-your-linux-distribution-of-choice), еще не полностью поддерживают возможность выполнения команд Windows в [Терминале](https://en.wikipedia.org/wiki/Linux_console). Если при выполнении `powershell.exe /c start .` или любой другой команды Windows возникает ошибка `-bash: powershell.exe: command not found`, ее можно устранить, выполнив следующие действия:

1. В дистрибутиве WSL выполните `echo $PATH`.  
   Если `/mnt/c/Windows/system32` отсутствует, что-то переопределяет стандартную переменную PATH.
2. Проверьте параметры профиля с помощью `cat /etc/profile`.  
   Если присутствует назначение переменной PATH, измените файл, чтобы закомментировать блок назначения PATH, используя символ **#** .
3. Проверьте, существует ли файл wsl.conf (`cat /etc/wsl.conf`), и убедитесь, что он не содержит `appendWindowsPath=false`. В противном случае закомментируйте эту строку.
4. Перезапустите дистрибутив, введя `wsl -t `, после чего следует имя дистрибутива, либо выполните `wsl --shutdown` в cmd или PowerShell.

### <a name="unable-to-boot-after-installing-wsl-2"></a>Не удается выполнить загрузку после установки WSL 2

Мы осведомлены о проблемах, из-за которых пользователям не удается выполнить загрузку после установки WSL 2. Пока мы полностью диагностировали эту проблему, от пользователей поступали сообщения о том, что помочь в ее устранении может [изменение размера буфера](https://github.com/microsoft/WSL/issues/4784#issuecomment-639219363) или [установка правильных драйверов](https://github.com/microsoft/WSL/issues/4784#issuecomment-675702244). Просматривайте новейшие сведения об этой [проблеме на сайте GitHub](https://github.com/microsoft/WSL/issues/4784). 
