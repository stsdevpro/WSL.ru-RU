---
title: Скачивание дистрибутивов подсистемы Windows для Linux (WSL) вручную
description: Инструкции по скачиванию дистрибутивов подсистемы Windows для Linux вручную.
keywords: wsl, подсистема windows для linux, установка вручную, microsoft store, windows 10s, curl, add-appxpackage, long-term servicing, ltsc
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: b94c7eb2f9e70a79f47853dac44badde58667315
ms.sourcegitcommit: f5b14630947ee9cf3438e9ba502bfbe85ed72cd1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "97957665"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="939d9-104">Скачивание пакетов дистрибутива подсистемы Windows для Linux вручную</span><span class="sxs-lookup"><span data-stu-id="939d9-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="939d9-105">Существует несколько сценариев, в которых вы не сможете (или не захотите) устанавливать дистрибутивы WSL Linux с помощью Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="939d9-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="939d9-106">В частности, вы можете использовать номер SKU классической ОС Windows Server или Long-Term Servicing (LTSC), который не поддерживает Microsoft Store, или политики корпоративной сети и административные параметры, запрещающие использовать Microsoft Store в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="939d9-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="939d9-107">В таких случаях, когда подсистема WSL доступна, как скачать и установить дистрибутивы Linux в WSL, если нет доступа к магазину?</span><span class="sxs-lookup"><span data-stu-id="939d9-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="939d9-108">Примечание. **Среды оболочки командной строки, в том числе дистрибутивы Linux/WSL, Cmd и PowerShell не могут выполняться в S-режиме Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="939d9-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="939d9-109">Это ограничение существует, чтобы обеспечить целостность и безопасность, которые предоставляет S-режим. Дополнительные сведения см. в [этой записи блога](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/).</span><span class="sxs-lookup"><span data-stu-id="939d9-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distributions"></a><span data-ttu-id="939d9-110">Скачивание дистрибутивов</span><span class="sxs-lookup"><span data-stu-id="939d9-110">Downloading distributions</span></span>

<span data-ttu-id="939d9-111">Если приложение Microsoft Store недоступно, вы можете скачать и вручную установить дистрибутивы Linux, щелкнув следующие ссылки:</span><span class="sxs-lookup"><span data-stu-id="939d9-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="939d9-112">Ubuntu 20.04</span><span class="sxs-lookup"><span data-stu-id="939d9-112">Ubuntu 20.04</span></span>](https://aka.ms/wslubuntu2004)
* [<span data-ttu-id="939d9-113">Ubuntu 20.04 ARM</span><span class="sxs-lookup"><span data-stu-id="939d9-113">Ubuntu 20.04 ARM</span></span>](https://aka.ms/wslubuntu2004arm)
* [<span data-ttu-id="939d9-114">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="939d9-114">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="939d9-115">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="939d9-115">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="939d9-116">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="939d9-116">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="939d9-117">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="939d9-117">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="939d9-118">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="939d9-118">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="939d9-119">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="939d9-119">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="939d9-120">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="939d9-120">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="939d9-121">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="939d9-121">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="939d9-122">Это приведет к скачиванию пакетов `<distro>.appx` в выбранную папку.</span><span class="sxs-lookup"><span data-stu-id="939d9-122">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="939d9-123">Следуйте [инструкциям по установке](#installing-your-distro) скачанных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="939d9-123">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="939d9-124">Скачивание дистрибутивов с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="939d9-124">Downloading distros via the command line</span></span>

<span data-ttu-id="939d9-125">При желании вы также можете скачать предпочтительные дистрибутивы с помощью командной строки.</span><span class="sxs-lookup"><span data-stu-id="939d9-125">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="939d9-126">Скачивание с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="939d9-126">Download using PowerShell</span></span>

 <span data-ttu-id="939d9-127">Чтобы скачать дистрибутивы с помощью PowerShell, используйте командлет [Invoke-WebRequest](/powershell/module/microsoft.powershell.utility/invoke-webrequest).</span><span class="sxs-lookup"><span data-stu-id="939d9-127">To download distros using PowerShell, use the [Invoke-WebRequest](/powershell/module/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="939d9-128">Ниже приведены инструкции по скачиванию Ubuntu 16.04.</span><span class="sxs-lookup"><span data-stu-id="939d9-128">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="939d9-129">Если загрузка занимает много времени, выключите индикатор выполнения, задав `$ProgressPreference = 'SilentlyContinue'`.</span><span class="sxs-lookup"><span data-stu-id="939d9-129">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="939d9-130">Скачивание с помощью cURL</span><span class="sxs-lookup"><span data-stu-id="939d9-130">Download using curl</span></span>
<span data-ttu-id="939d9-131">Обновление Windows 10 Spring 2018 (или более поздней версии) содержит популярную [служебную программу командной строки cURL](https://curl.haxx.se/), с помощью которой можно вызывать веб-запросы (например, команды HTTP GET, POST, PUT и т. д.) из командной строки.</span><span class="sxs-lookup"><span data-stu-id="939d9-131">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="939d9-132">Вы можете использовать `curl.exe`, чтобы скачать приведенные выше дистрибутивы:</span><span class="sxs-lookup"><span data-stu-id="939d9-132">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="939d9-133">В приведенном выше примере выполняется `curl.exe` (а не только `curl`), чтобы убедиться, что в PowerShell вызывается реальный исполняемый файл cURL, а не его псевдоним для [Invoke-WebRequest](/powershell/module/microsoft.powershell.utility/invoke-webrequest).</span><span class="sxs-lookup"><span data-stu-id="939d9-133">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](/powershell/module/microsoft.powershell.utility/invoke-webrequest)</span></span>

> <span data-ttu-id="939d9-134">Примечание. Использование `curl` может быть предпочтительным, если необходимо вызвать или создать сценарий для скачивания с помощью командлетов командной строки и сценариев `.bat` / `.cmd`.</span><span class="sxs-lookup"><span data-stu-id="939d9-134">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="939d9-135">Установка дистрибутива</span><span class="sxs-lookup"><span data-stu-id="939d9-135">Installing your distro</span></span>

<span data-ttu-id="939d9-136">Если вы используете Windows 10, вы можете установить дистрибутив с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="939d9-136">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="939d9-137">Просто перейдите в папку, содержащую скачанный выше дистрибутив, и в этом каталоге выполните следующую команду, в которой `app_name` — это имя APPX-файла дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="939d9-137">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="939d9-138">Если вы используете сервер Windows, инструкции по установке можно найти на странице документации [Windows Server](install-on-server.md).</span><span class="sxs-lookup"><span data-stu-id="939d9-138">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="939d9-139">После установки дистрибутива следуйте обычным инструкциям по \* [обновлению WSL 1 до WSL 2](./install-win10.md#set-your-distribution-version-to-wsl-1-or-wsl-2) или [создайте новую учетную запись пользователя и пароль](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="939d9-139">Once your distribution is installed, follow the normal instructions to \* [Update from WSL 1 to WSL 2](./install-win10.md#set-your-distribution-version-to-wsl-1-or-wsl-2) or [create a new user account and password](./user-support.md).</span></span>
