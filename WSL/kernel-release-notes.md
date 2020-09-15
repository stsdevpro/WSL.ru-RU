---
title: Заметки о выпуске подсистемы Windows для ядра Linux
description: Заметки о выпуске подсистемы Windows для Linux.  Обновляется ежемесячно.
keywords: заметки о выпуске, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, ядро
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 32b65bcde3df01b25f0361493a172e754e78e101
ms.sourcegitcommit: 43d4056eefe0c71ecd9a0fbd5a7a58dd18fa9829
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "89615551"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="dde1f-105">Заметки о выпуске подсистемы Windows для ядра Linux</span><span class="sxs-lookup"><span data-stu-id="dde1f-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="dde1f-106">Включена поддержка дистрибутивов WSL 2, [использующих полнофункциональное ядро Linux](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="dde1f-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="dde1f-107">Это ядро Linux имеет открытый кодом. Исходный код доступен в репозитории [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel).</span><span class="sxs-lookup"><span data-stu-id="dde1f-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="dde1f-108">Это ядро Linux доставляется на компьютер через Центр обновления Майкрософт в соответствии с отдельным графиком выпуска подсистемы Windows для Linux (поставляется в составе образа Windows).</span><span class="sxs-lookup"><span data-stu-id="dde1f-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="dde1f-109">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="dde1f-109">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="dde1f-110">*Дата выпуска:* предварительный выпуск и версии, доступные для установки вручную.</span><span class="sxs-lookup"><span data-stu-id="dde1f-110">*Release Date*: Prerelease and available via manual install</span></span>

<span data-ttu-id="dde1f-111">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="dde1f-111">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="dde1f-112">Это стабильный выпуск 4.19.128</span><span class="sxs-lookup"><span data-stu-id="dde1f-112">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="dde1f-113">Исправление повреждения памяти IOCTL драйвера dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="dde1f-113">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="dde1f-114">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="dde1f-114">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="dde1f-115">*Дата выпуска:* Предварительный выпуск</span><span class="sxs-lookup"><span data-stu-id="dde1f-115">*Release Date*: Prerelease</span></span>

<span data-ttu-id="dde1f-116">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="dde1f-116">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="dde1f-117">Drivers: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="dde1f-117">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="dde1f-118">Включена поддержка вычислений GPU</span><span class="sxs-lookup"><span data-stu-id="dde1f-118">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="dde1f-119">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="dde1f-119">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="dde1f-120">*Дата выпуска:* 09.06.2020</span><span class="sxs-lookup"><span data-stu-id="dde1f-120">*Release Date*: 06/09/2020</span></span> 

<span data-ttu-id="dde1f-121">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="dde1f-121">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="dde1f-122">Обновление конфигурации WSL для выпуска 4.19.104</span><span class="sxs-lookup"><span data-stu-id="dde1f-122">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="dde1f-123">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="dde1f-123">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="dde1f-124">*Дата выпуска:* 12.11.2019</span><span class="sxs-lookup"><span data-stu-id="dde1f-124">*Release Date*: 11/12/2019</span></span> 

<span data-ttu-id="dde1f-125">[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard)</span><span class="sxs-lookup"><span data-stu-id="dde1f-125">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="dde1f-126">Это стабильный выпуск 4.19.84</span><span class="sxs-lookup"><span data-stu-id="dde1f-126">This is the 4.19.84 stable release</span></span>

