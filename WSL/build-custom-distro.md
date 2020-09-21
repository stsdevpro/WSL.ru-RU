---
title: Создание пользовательской дистрибутив Linux для WSL
description: Узнайте, как создать настраиваемый дистрибутив Linux для подсистемы Windows для Linux.
keywords: Башонвиндовс, bash, WSL, Windows, подсистема Windows, дистрибутив, настраиваемый
ms.date: 09/15/2020
ms.topic: article
ms.openlocfilehash: 2882cccac6c34cd52529dbf7e42c8d35907d8241
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818706"
---
# <a name="creating-a-custom-linux-distribution-for-wsl"></a>Создание пользовательского дистрибутива Linux для WSL

Используйте наш пример WSL с открытым исходным кодом для создания пакетов WSL дистрибутив для Microsoft Store и (или) для создания пользовательских пакетов Linux дистрибутив для загрузки неопубликованных приложений. [Репозиторий запуска дистрибутив](https://github.com/Microsoft/WSL-DistroLauncher) можно найти на сайте GitHub.

Этот проект включает:

- Служба поддержки распространения Linux для упаковки и отправки дистрибутива Linux в качестве appx-пакета, работающего на WSL
- Разработчики могут создавать настраиваемые дистрибутивы Linux, которые можно загруженные неопубликованные на свой компьютер разработки.

## <a name="background"></a>Фон

Мы распространяем дистрибутивов Linux для WSL как приложения UWP с помощью Microsoft Store. Можно установить приложения, которые будут запускаться на WSL — подсистему, расположенной в ядре Windows. Этот механизм доставки имеет много преимуществ, как описано в [предыдущей записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).

## <a name="sideloading-a-custom-linux-distro-package"></a>Неопубликованная загрузка пользовательского пакета дистрибутив для Linux

Вы можете создать пользовательский пакет дистрибутив для Linux в качестве приложения для загружать неопубликованные на личном компьютере. Обратите внимание, что пользовательский пакет не будет распространяться с помощью Microsoft Store, пока не будет отправлен в качестве обслуживания распространения.
Чтобы настроить компьютер для загружать неопубликованные приложений, его необходимо включить в параметрах системы в разделе "для разработчиков".  Убедитесь, что выбран режим разработчика или загружать неопубликованные приложения.

## <a name="for-linux-distro-maintainers"></a>Для дистрибутив обслуживания Linux

Для отправки в магазин необходимо работать с нами, чтобы получить утверждение публикации. Если вы являетесь владельцем дистрибутива Linux, который заинтересован в добавлении дистрибутива в Microsoft Store, обратитесь по адресу wslpartners@microsoft.com .

## <a name="getting-started"></a>Приступая к работе

Следуйте инструкциям в [репозитории GitHub дистрибутив Launcher](https://github.com/Microsoft/WSL-DistroLauncher) , чтобы создать пользовательский пакет дистрибутив для Linux.

## <a name="team-blogs"></a>Блоги группы

-  [Открытие источника. пример WSL для обслуживания распространения Linux и пользовательских дистрибутивов Linux для загрузки неопубликованных приложений](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
- [Блог командной строки](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Отзывы

- [Репозиторий GitHub дистрибутив Launcher](https://github.com/Microsoft/WSL-DistroLauncher)
- [Средство регистрации проблем GitHub для WSL](https://github.com/Microsoft/BashOnWindows/issues)
