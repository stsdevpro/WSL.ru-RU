---
title: Установка подсистемы Linux в Windows Server
description: Узнайте, как установить подсистему Linux на Windows Server. WSL предоставляется для установки на Windows Server 2019 (версия 1709) и более поздних версий.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 501bbf78c2d9f59dad945af9c30571317240b79f
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866148"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="61893-105">Руководство по установке Windows Server</span><span class="sxs-lookup"><span data-stu-id="61893-105">Windows Server Installation Guide</span></span>

<span data-ttu-id="61893-106">Подсистема Windows для Linux доступна для установки на Windows Server 2019 (версия 1709) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="61893-106">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="61893-107">В этом руководстве рассматриваются действия по включению WSL на компьютере.</span><span class="sxs-lookup"><span data-stu-id="61893-107">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="61893-108">Включение подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="61893-108">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="61893-109">Перед запуском дистрибутивов Linux в Windows необходимо включить дополнительный компонент "Подсистема Windows для Linux" и перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="61893-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="61893-110">Запустите PowerShell с правами администратора и выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="61893-110">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="61893-111">Скачивание дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="61893-111">Download a Linux distribution</span></span>

<span data-ttu-id="61893-112">Выполните [эти инструкции](install-manual.md), чтобы скачать избранный дистрибутив Linux.</span><span class="sxs-lookup"><span data-stu-id="61893-112">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="61893-113">Извлечение и установка дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="61893-113">Extract and install a Linux distribution</span></span>

<span data-ttu-id="61893-114">После загрузки дистрибутива Linux для извлечения его содержимого и установки вручную выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="61893-114">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="61893-115">Извлеките содержимое пакета `<distro>.appx`, с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="61893-115">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="61893-116">Запустите средство запуска приложения дистрибутива в целевой папке.</span><span class="sxs-lookup"><span data-stu-id="61893-116">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="61893-117">Средство запуска обычно называется `<distro>.exe` (например, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="61893-117">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Расширенный дистрибутив Ubuntu в Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="61893-119">**Сбой установки с ошибкой 0x8007007e**. При возникновении этой ошибки система не поддерживает WSL.</span><span class="sxs-lookup"><span data-stu-id="61893-119">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="61893-120">Убедитесь, что вы используете сборку Windows 16215 или более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="61893-120">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="61893-121">[Проверьте используемую сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="61893-121">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="61893-122">Также убедитесь, [что WSL включен](troubleshooting.md#confirm-wsl-is-enabled) и ваш компьютер перезагружен после включения этой функции.</span><span class="sxs-lookup"><span data-stu-id="61893-122">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="61893-123">3. Добавьте путь дистрибутива в путь среды Windows (в этом примере: `C:\Users\Administrator\Ubuntu`), с помощью PowerShell:</span><span class="sxs-lookup"><span data-stu-id="61893-123">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="61893-124">Теперь вы можете запустить дистрибутив из любого пути, введя `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="61893-124">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="61893-125">Например: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="61893-125">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="61893-126">После установки необходимо [инициализировать новый экземпляр дистрибутива](initialize-distro.md), прежде чем его можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="61893-126">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
