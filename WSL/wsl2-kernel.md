---
title: Обновление ядра Linux в WSL 2
description: Инструкции по обновлению ядра Linux в WSL 2 вручную
keywords: WSL, Windows, ядро Linux, подсистема Windows для Linux, ядро
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7bf2ef606d0bd23083f323117348aeea87c52b10
ms.sourcegitcommit: 609850fadd20687636b8486264e87af47c538111
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2020
ms.locfileid: "92444810"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="28512-104">Обновление ядра Linux в WSL 2</span><span class="sxs-lookup"><span data-stu-id="28512-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="28512-105">Чтобы вручную обновить ядро Linux в WSL 2, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="28512-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="28512-106">Если установщику не удается найти WSL 1, щелкните правой кнопкой мыши установщик обновления ядра Linux, а затем нажмите кнопку "Удалить" и запустите установщик повторно.</span><span class="sxs-lookup"><span data-stu-id="28512-106">If the installer can't find WSL 1, right-click the Linux kernel update installer and press "Uninstall", then rerun the installer.</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="28512-107">Скачивание пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="28512-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="28512-108">[Скачайте последнюю версию пакета обновления ядра Linux в WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) для 64-разрядных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="28512-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="28512-109">Если вы используете компьютер ARM64, вместо этого скачайте [пакет ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).</span><span class="sxs-lookup"><span data-stu-id="28512-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="28512-110">Установка пакета обновления ядра Linux</span><span class="sxs-lookup"><span data-stu-id="28512-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="28512-111">Чтобы установить пакет обновления ядра Linux:</span><span class="sxs-lookup"><span data-stu-id="28512-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="28512-112">Запустите пакет обновления, скачанный на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="28512-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="28512-113">Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.</span><span class="sxs-lookup"><span data-stu-id="28512-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="28512-114">По завершении установки можно приступить к использованию WSL 2.</span><span class="sxs-lookup"><span data-stu-id="28512-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="28512-115">Дальнейшие планы по обновлению ядра Linux в WSL 2</span><span class="sxs-lookup"><span data-stu-id="28512-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="28512-116">Дополнительные сведения см. в статье об [изменениях процесса установки обновления ядра Linux в WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), доступной в блоге, [посвященному командной строке Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="28512-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="28512-117">Диагностика</span><span class="sxs-lookup"><span data-stu-id="28512-117">Troubleshooting</span></span>

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a><span data-ttu-id="28512-118">Это обновление применяется только к компьютерам с подсистемой Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="28512-118">This update only applies to machines with the Windows Subsystem for Linux</span></span>
<span data-ttu-id="28512-119">Чтобы установить ядро MSI, сначала нужно включить WSL.</span><span class="sxs-lookup"><span data-stu-id="28512-119">To install MSI kernel, WSL is required and should be enabled first.</span></span> <span data-ttu-id="28512-120">В случае сбоя отображается следующее сообщение: `This update only applies to machines with the Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="28512-120">If it fails, it you will see the message: `This update only applies to machines with the Windows Subsystem for Linux`.</span></span> 

<span data-ttu-id="28512-121">Есть три возможные причины, по которым вы видите это сообщение:</span><span class="sxs-lookup"><span data-stu-id="28512-121">There are three possible reason you see this message:</span></span>

1. <span data-ttu-id="28512-122">Вы используете старую версию Windows, которая не поддерживает WSL 2.</span><span class="sxs-lookup"><span data-stu-id="28512-122">You are still in old version of Windows which doesn't support WSL 2.</span></span> <span data-ttu-id="28512-123">Проверьте [требования к WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) и выполните обновление, чтобы включить поддержку WSL 2.</span><span class="sxs-lookup"><span data-stu-id="28512-123">Please check the [WSL 2 requirements](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) and upgrade to use WSL 2.</span></span> 
2. <span data-ttu-id="28512-124">`Windows Subsystem for Linux` не включена.</span><span class="sxs-lookup"><span data-stu-id="28512-124">`Windows Subsystem for Linux` is not enabled.</span></span> <span data-ttu-id="28512-125">См. статью [Руководство по установке подсистемы Windows для Linux в Windows 10](https://docs.microsoft.com/windows/wsl/install-win10).</span><span class="sxs-lookup"><span data-stu-id="28512-125">Please follow the [Windows Subsystem for Linux Installation Guide](https://docs.microsoft.com/windows/wsl/install-win10).</span></span>
3. <span data-ttu-id="28512-126">После включения `Windows Subsystem for Linux` нужно перезагрузить компьютер. Сделайте это и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="28512-126">After you enabled `Windows Subsystem for Linux`, a reboot is required to take into effect, please reboot your machine and try again.</span></span>

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

<span data-ttu-id="28512-127">Если ядро отсутствует в %SystemRoot%\system32\lxss\tools\,, может возникнуть описанная выше ошибка.</span><span class="sxs-lookup"><span data-stu-id="28512-127">Each time kernel is missing in %SystemRoot%\system32\lxss\tools\, you may run into the above error.</span></span>

<span data-ttu-id="28512-128">Есть несколько способов устранения этой проблемы:</span><span class="sxs-lookup"><span data-stu-id="28512-128">Here are some possible ways to resolve it:</span></span>

1. <span data-ttu-id="28512-129">Установите ядро Linux вручную, следуя инструкциям на этой странице.</span><span class="sxs-lookup"><span data-stu-id="28512-129">Install the Linux kernel manually following the instructions on this page.</span></span>
2. <span data-ttu-id="28512-130">Перейдите к разделу "Установка и удаление программ", а затем удалите и снова установите MSI.</span><span class="sxs-lookup"><span data-stu-id="28512-130">Uninstall the MSI from 'Add or Remove Programs', and install it again.</span></span>