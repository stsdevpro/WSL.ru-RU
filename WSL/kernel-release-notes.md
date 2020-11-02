---
title: Заметки о выпуске подсистемы Windows для ядра Linux
description: Заметки о выпуске подсистемы Windows для Linux.  Обновляется ежемесячно.
keywords: заметки о выпуске, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, ядро
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 0ab1e7e85ce9d601bd8eb602d98e3487e8202e03
ms.sourcegitcommit: 609850fadd20687636b8486264e87af47c538111
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2020
ms.locfileid: "92444822"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="41fc0-105">Заметки о выпуске подсистемы Windows для ядра Linux</span><span class="sxs-lookup"><span data-stu-id="41fc0-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="41fc0-106">Включена поддержка дистрибутивов WSL 2, [использующих полнофункциональное ядро Linux](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="41fc0-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="41fc0-107">Это ядро Linux имеет открытый кодом. Исходный код доступен в репозитории [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel).</span><span class="sxs-lookup"><span data-stu-id="41fc0-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="41fc0-108">Это ядро Linux доставляется на компьютер через Центр обновления Майкрософт в соответствии с отдельным графиком выпуска подсистемы Windows для Linux (поставляется в составе образа Windows).</span><span class="sxs-lookup"><span data-stu-id="41fc0-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="5451-microsoft-standard"></a><span data-ttu-id="41fc0-109">5.4.51-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="41fc0-109">5.4.51-microsoft-standard</span></span>
<span data-ttu-id="41fc0-110">*Дата выпуска:* Предварительный выпуск — 22.10.2020</span><span class="sxs-lookup"><span data-stu-id="41fc0-110">*Release Date* : Prerelease - 10/22/2020</span></span>

<span data-ttu-id="41fc0-111">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51)</span><span class="sxs-lookup"><span data-stu-id="41fc0-111">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51).</span></span>

* <span data-ttu-id="41fc0-112">Стабильный выпуск 5.4.51</span><span class="sxs-lookup"><span data-stu-id="41fc0-112">Stable release of 5.4.51</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="41fc0-113">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="41fc0-113">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="41fc0-114">*Дата выпуска:* 15.09.2020</span><span class="sxs-lookup"><span data-stu-id="41fc0-114">*Release Date* : 09/15/2020</span></span>

<span data-ttu-id="41fc0-115">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="41fc0-115">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="41fc0-116">Это стабильный выпуск 4.19.128</span><span class="sxs-lookup"><span data-stu-id="41fc0-116">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="41fc0-117">Исправление повреждения памяти IOCTL драйвера dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="41fc0-117">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="41fc0-118">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="41fc0-118">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="41fc0-119">*Дата выпуска:* Предварительный выпуск</span><span class="sxs-lookup"><span data-stu-id="41fc0-119">*Release Date* : Prerelease</span></span>

<span data-ttu-id="41fc0-120">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="41fc0-120">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="41fc0-121">Drivers: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="41fc0-121">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="41fc0-122">Включена поддержка вычислений GPU</span><span class="sxs-lookup"><span data-stu-id="41fc0-122">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="41fc0-123">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="41fc0-123">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="41fc0-124">*Дата выпуска:* 09.06.2020</span><span class="sxs-lookup"><span data-stu-id="41fc0-124">*Release Date* : 06/09/2020</span></span> 

<span data-ttu-id="41fc0-125">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="41fc0-125">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="41fc0-126">Обновление конфигурации WSL для выпуска 4.19.104</span><span class="sxs-lookup"><span data-stu-id="41fc0-126">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="41fc0-127">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="41fc0-127">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="41fc0-128">*Дата выпуска:* 12.11.2019</span><span class="sxs-lookup"><span data-stu-id="41fc0-128">*Release Date* : 11/12/2019</span></span> 

<span data-ttu-id="41fc0-129">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="41fc0-129">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="41fc0-130">Это стабильный выпуск 4.19.84</span><span class="sxs-lookup"><span data-stu-id="41fc0-130">This is the 4.19.84 stable release</span></span>

