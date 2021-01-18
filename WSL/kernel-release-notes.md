---
title: Заметки о выпуске подсистемы Windows для ядра Linux
description: Заметки о выпуске подсистемы Windows для Linux.  Обновляется ежемесячно.
keywords: заметки о выпуске, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, ядро
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 07488d61ad1c01f85c1d78789274aa3afbc9e1d8
ms.sourcegitcommit: e2d586925b314ce4517773b9c78736450a9f75d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "97977109"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="da4b8-105">Заметки о выпуске подсистемы Windows для ядра Linux</span><span class="sxs-lookup"><span data-stu-id="da4b8-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="da4b8-106">Включена поддержка дистрибутивов WSL 2, [использующих полнофункциональное ядро Linux](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="da4b8-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="da4b8-107">Это ядро Linux имеет открытый кодом. Исходный код доступен в репозитории [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel).</span><span class="sxs-lookup"><span data-stu-id="da4b8-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="da4b8-108">Это ядро Linux доставляется на компьютер через Центр обновления Майкрософт в соответствии с отдельным графиком выпуска подсистемы Windows для Linux (поставляется в составе образа Windows).</span><span class="sxs-lookup"><span data-stu-id="da4b8-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="5472"></a><span data-ttu-id="da4b8-109">5.4.72</span><span class="sxs-lookup"><span data-stu-id="da4b8-109">5.4.72</span></span>
<span data-ttu-id="da4b8-110">*Дата выпуска:* Предварительный выпуск — 10.11.2020</span><span class="sxs-lookup"><span data-stu-id="da4b8-110">*Release Date*: Prerelease - 11/10/2020</span></span>

[<span data-ttu-id="da4b8-111">Ссылка на официальный выпуск GitHub</span><span class="sxs-lookup"><span data-stu-id="da4b8-111">Official Github release link</span></span>](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.72)

* <span data-ttu-id="da4b8-112">Исправлена конфигурация для версии 5.4.72.</span><span class="sxs-lookup"><span data-stu-id="da4b8-112">Fix config for 5.4.72</span></span>

## <a name="5451-microsoft-standard"></a><span data-ttu-id="da4b8-113">5.4.51-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="da4b8-113">5.4.51-microsoft-standard</span></span>
<span data-ttu-id="da4b8-114">*Дата выпуска:* Предварительный выпуск — 22.10.2020</span><span class="sxs-lookup"><span data-stu-id="da4b8-114">*Release Date*: Prerelease - 10/22/2020</span></span>

<span data-ttu-id="da4b8-115">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51)</span><span class="sxs-lookup"><span data-stu-id="da4b8-115">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51).</span></span>

* <span data-ttu-id="da4b8-116">Стабильный выпуск 5.4.51</span><span class="sxs-lookup"><span data-stu-id="da4b8-116">Stable release of 5.4.51</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="da4b8-117">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="da4b8-117">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="da4b8-118">*Дата выпуска:* 15.09.2020</span><span class="sxs-lookup"><span data-stu-id="da4b8-118">*Release Date*: 09/15/2020</span></span>

<span data-ttu-id="da4b8-119">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="da4b8-119">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="da4b8-120">Это стабильный выпуск 4.19.128</span><span class="sxs-lookup"><span data-stu-id="da4b8-120">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="da4b8-121">Исправление повреждения памяти IOCTL драйвера dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="da4b8-121">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="da4b8-122">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="da4b8-122">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="da4b8-123">*Дата выпуска:* Предварительный выпуск</span><span class="sxs-lookup"><span data-stu-id="da4b8-123">*Release Date*: Prerelease</span></span>

<span data-ttu-id="da4b8-124">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="da4b8-124">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="da4b8-125">Drivers: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="da4b8-125">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="da4b8-126">Включена поддержка вычислений GPU</span><span class="sxs-lookup"><span data-stu-id="da4b8-126">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="da4b8-127">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="da4b8-127">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="da4b8-128">*Дата выпуска:* 09.06.2020</span><span class="sxs-lookup"><span data-stu-id="da4b8-128">*Release Date*: 06/09/2020</span></span> 

<span data-ttu-id="da4b8-129">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="da4b8-129">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="da4b8-130">Обновление конфигурации WSL для выпуска 4.19.104</span><span class="sxs-lookup"><span data-stu-id="da4b8-130">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="da4b8-131">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="da4b8-131">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="da4b8-132">*Дата выпуска:* 12.11.2019</span><span class="sxs-lookup"><span data-stu-id="da4b8-132">*Release Date*: 11/12/2019</span></span> 

<span data-ttu-id="da4b8-133">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="da4b8-133">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="da4b8-134">Это стабильный выпуск 4.19.84</span><span class="sxs-lookup"><span data-stu-id="da4b8-134">This is the 4.19.84 stable release</span></span>

