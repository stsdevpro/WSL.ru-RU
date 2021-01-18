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
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a>Заметки о выпуске подсистемы Windows для ядра Linux

Включена поддержка дистрибутивов WSL 2, [использующих полнофункциональное ядро Linux](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/). Это ядро Linux имеет открытый кодом. Исходный код доступен в репозитории [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel). Это ядро Linux доставляется на компьютер через Центр обновления Майкрософт в соответствии с отдельным графиком выпуска подсистемы Windows для Linux (поставляется в составе образа Windows).

## <a name="5472"></a>5.4.72
*Дата выпуска:* Предварительный выпуск — 10.11.2020

[Ссылка на официальный выпуск GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.72)

* Исправлена конфигурация для версии 5.4.72.

## <a name="5451-microsoft-standard"></a>5.4.51-microsoft-standard
*Дата выпуска:* Предварительный выпуск — 22.10.2020

[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51)

* Стабильный выпуск 5.4.51

## <a name="419128-microsoft-standard"></a>4.19.128-microsoft-standard
*Дата выпуска:* 15.09.2020

[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard)

* Это стабильный выпуск 4.19.128
* Исправление повреждения памяти IOCTL драйвера dxgkrnl

## <a name="419121-microsoft-standard"></a>4.19.121-microsoft-standard
*Дата выпуска:* Предварительный выпуск

[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard)

* Drivers: hv: vmbus: hook up dxgkrnl
* Включена поддержка вычислений GPU

## <a name="419104-microsoft-standard"></a>4.19.104-microsoft-standard
*Дата выпуска:* 09.06.2020 

[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard)

* Обновление конфигурации WSL для выпуска 4.19.104

## <a name="41984-microsoft-standard"></a>4.19.84-microsoft-standard
*Дата выпуска:* 12.11.2019 

[Официальная ссылка на выпуск GitHub.](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard)

* Это стабильный выпуск 4.19.84

