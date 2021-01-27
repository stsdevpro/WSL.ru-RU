---
title: WSL для предприятий
description: Ресурсы и инструкции для оптимального использования WSL в корпоративной среде.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, корпоративный, развертывание, автономный, упаковка, магазин, распространение, установка, установить
ms.date: 12/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a210268fb460a793fec2047c6d6678f92869ea16
ms.sourcegitcommit: 0523e6a2ca99f5f3b188d526afed3ce6ad7e3abb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2021
ms.locfileid: "98766857"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="7993d-104">Подсистема Windows для Linux для предприятий</span><span class="sxs-lookup"><span data-stu-id="7993d-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="7993d-105">Администратор или менеджер может потребовать от всех разработчиков использовать одно и то же одобренное программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="7993d-105">As an administrator or manager, you may require all developers to use the same approved software.</span></span> <span data-ttu-id="7993d-106">Такая согласованность помогает создать четко определенную рабочую среду.</span><span class="sxs-lookup"><span data-stu-id="7993d-106">This consistency helps to create a well-defined work environment.</span></span> <span data-ttu-id="7993d-107">Подсистема Windows для Linux (WSL) помогает обеспечить такую согласованность, позволяя импортировать и экспортировать пользовательские образы WSL с одного компьютера на другой.</span><span class="sxs-lookup"><span data-stu-id="7993d-107">The Windows Subsystem for Linux aids in this consistency by allowing you to import and export custom WSL images from one machine to the next.</span></span> <span data-ttu-id="7993d-108">Ознакомьтесь с разделами ниже:</span><span class="sxs-lookup"><span data-stu-id="7993d-108">Read the guide below to learn more about:</span></span>

* [<span data-ttu-id="7993d-109">Создание пользовательского образа WSL</span><span class="sxs-lookup"><span data-stu-id="7993d-109">Creating a custom WSL image</span></span>](#creating-a-custom-wsl-image)
* [<span data-ttu-id="7993d-110">Распространение образа WSL</span><span class="sxs-lookup"><span data-stu-id="7993d-110">Distributing a WSL image</span></span>](#distributing-your-wsl-image)
* [<span data-ttu-id="7993d-111">Обновление и исправление дистрибутивов и пакетов Linux</span><span class="sxs-lookup"><span data-stu-id="7993d-111">Update and patch Linux distributions and packages</span></span>](#update-and-patch-linux-distributions-and-packages)
* [<span data-ttu-id="7993d-112">Варианты защиты предприятия и управления им</span><span class="sxs-lookup"><span data-stu-id="7993d-112">Enterprise security and control options</span></span>](#enterprise-security-and-control-options)

## <a name="creating-a-custom-wsl-image"></a><span data-ttu-id="7993d-113">Создание пользовательского образа WSL</span><span class="sxs-lookup"><span data-stu-id="7993d-113">Creating a custom WSL image</span></span>

<span data-ttu-id="7993d-114">То, что часто называют образом, представляет собой просто моментальный снимок программного обеспечения и его компонентов, сохраненный в файле.</span><span class="sxs-lookup"><span data-stu-id="7993d-114">What is commonly referred to as an "image", is simply a snapshot of your software and its components saved to a file.</span></span> <span data-ttu-id="7993d-115">В случае Подсистемы Windows для Linux образ будет состоять из подсистемы, ее дистрибутивов, а также установленных программ и пакетов в дистрибутиве.</span><span class="sxs-lookup"><span data-stu-id="7993d-115">In the case of the Windows Subsystem for Linux, your image would consist of the subsystem, its distributions, and whatever software and packages are installed on the distribution.</span></span>

<span data-ttu-id="7993d-116">Чтобы приступить к созданию образа WSL, сначала [установите Подсистему Windows для Linux](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="7993d-116">To begin creating your WSL image, first [install the Windows Subsystem for Linux](./install-win10.md).</span></span>

<span data-ttu-id="7993d-117">После установки перейдите в Microsoft Store для бизнеса, чтобы скачать и установить дистрибутив Linux, который вам подходит.</span><span class="sxs-lookup"><span data-stu-id="7993d-117">Once installed, use The Microsoft Store for Business to download and install the Linux distribution that’s right for you.</span></span> <span data-ttu-id="7993d-118">Создание учетной записи с [помощью Microsoft Store для бизнеса](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business.)</span><span class="sxs-lookup"><span data-stu-id="7993d-118">Create an account with the [Microsoft Store for Business](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business.)</span></span>

### <a name="exporting-your-wsl-image"></a><span data-ttu-id="7993d-119">Экспорт образа WSL</span><span class="sxs-lookup"><span data-stu-id="7993d-119">Exporting your WSL image</span></span>

<span data-ttu-id="7993d-120">Экспортируйте пользовательский образ WSL, выполнив команду wsl --export `<Distro> <FileName>`, которая упакует образ в файл с расширением .tar и подготовит его для распространения на другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="7993d-120">Export your custom WSL image by running wsl --export `<Distro> <FileName>`, which will wrap your image in a tar file and make it ready for distribution on to other machines.</span></span>

## <a name="distributing-your-wsl-image"></a><span data-ttu-id="7993d-121">Распространение образа WSL</span><span class="sxs-lookup"><span data-stu-id="7993d-121">Distributing your WSL image</span></span>

<span data-ttu-id="7993d-122">Распространите образ WSL из общей папки или устройства хранения, выполнив команду wsl --import `<Distro> <InstallLocation> <FileName>`, которая импортирует указанный файл с расширением .tar в качестве нового дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="7993d-122">Distribute the WSL image from a share or storage device by running wsl --import `<Distro> <InstallLocation> <FileName>`, which will import the specified tar file as a new distribution.</span></span>

## <a name="update-and-patch-linux-distributions-and-packages"></a><span data-ttu-id="7993d-123">Обновление и исправление дистрибутивов и пакетов Linux</span><span class="sxs-lookup"><span data-stu-id="7993d-123">Update and patch Linux distributions and packages</span></span>

<span data-ttu-id="7993d-124">Настоятельно рекомендуется использовать средства диспетчера конфигурации Linux для мониторинга пространства пользователя Linux и управления им.</span><span class="sxs-lookup"><span data-stu-id="7993d-124">Using Linux configuration manager tools is strongly recommended for monitoring and managing Linux user space.</span></span> <span data-ttu-id="7993d-125">Есть много диспетчеров конфигурации Linux.</span><span class="sxs-lookup"><span data-stu-id="7993d-125">There are a host of Linux configuration managers to choose from.</span></span> <span data-ttu-id="7993d-126">Ознакомьтесь с этой [записью блога](http://www.craigloewen.com/blog/2019/12/04/running-puppet-quickly-in-wsl2/) о том, как установить Puppet в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="7993d-126">Check out this [blog post](http://www.craigloewen.com/blog/2019/12/04/running-puppet-quickly-in-wsl2/) on how to install Puppet in WSL 2.</span></span>

## <a name="enterprise-security-and-control-options"></a><span data-ttu-id="7993d-127">Варианты защиты предприятия и управления им</span><span class="sxs-lookup"><span data-stu-id="7993d-127">Enterprise security and control options</span></span>

<span data-ttu-id="7993d-128">В настоящее время WSL предлагает ограниченные механизмы управления в отношении изменения взаимодействия с пользователем в корпоративном сценарии.</span><span class="sxs-lookup"><span data-stu-id="7993d-128">Currently, WSL offers limited control mechanisms in regard to modifying the user experience in an Enterprise scenario.</span></span> <span data-ttu-id="7993d-129">Корпоративные функции продолжают разрабатываться. Ниже перечислены области поддерживаемых и неподдерживаемых функций.</span><span class="sxs-lookup"><span data-stu-id="7993d-129">Enterprise features continue in development however, below are the areas of supported and unsupported features.</span></span> <span data-ttu-id="7993d-130">Чтобы запросить новую функцию, не описанную в этом списке, отправьте соответствующее сообщение в [репозиторий GitHub](https://github.com/microsoft/WSL/issues?q=is%3Aissue+is%3Aopen+enterprise).</span><span class="sxs-lookup"><span data-stu-id="7993d-130">To request a new feature not covered in this list, file an issue in our [GitHub repo](https://github.com/microsoft/WSL/issues?q=is%3Aissue+is%3Aopen+enterprise).</span></span>

### <a name="supported"></a><span data-ttu-id="7993d-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7993d-131">Supported</span></span>

* <span data-ttu-id="7993d-132">Совместное использование утвержденного образа с помощью `wsl --import` и `wsl --export`</span><span class="sxs-lookup"><span data-stu-id="7993d-132">Sharing an approved image internally using `wsl --import` and `wsl --export`</span></span>
* <span data-ttu-id="7993d-133">Создание собственного дистрибутива WSL для предприятия с помощью репозитория [WSL Distro Launcher](https://github.com/microsoft/WSL-DistroLauncher).</span><span class="sxs-lookup"><span data-stu-id="7993d-133">Creating your own WSL distro for your Enterprise using the [WSL Distro Launcher repo](https://github.com/microsoft/WSL-DistroLauncher)</span></span>

<span data-ttu-id="7993d-134">Ниже приведен список функций, которые пока не поддерживаются, но изучаются.</span><span class="sxs-lookup"><span data-stu-id="7993d-134">Here's a list of features for which we don't yet have support for, but are investigating.</span></span>

### <a name="unsupported"></a><span data-ttu-id="7993d-135">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7993d-135">Unsupported</span></span>

* <span data-ttu-id="7993d-136">Синхронизация пользователя в WSL с пользователем Windows на хост-компьютере</span><span class="sxs-lookup"><span data-stu-id="7993d-136">Synchronizing the user inside WSL with the Windows user on the host machine</span></span>
* <span data-ttu-id="7993d-137">Управление обновлениями и установка исправлений для дистрибутивов и пакетов Linux с помощью средств Windows</span><span class="sxs-lookup"><span data-stu-id="7993d-137">Managing updates and patching of the Linux distributions and packages using Windows tools</span></span>
* <span data-ttu-id="7993d-138">Обновление содержимого WSL также обновляет содержимое дистрибутива в Windows</span><span class="sxs-lookup"><span data-stu-id="7993d-138">Having Windows update also update WSL distro contents</span></span>
* <span data-ttu-id="7993d-139">Управление тем, к каким дистрибутивам могут получить доступ пользователи вашего предприятия</span><span class="sxs-lookup"><span data-stu-id="7993d-139">Controlling which distributions users in your Enterprise can access</span></span>
* <span data-ttu-id="7993d-140">Запуск обязательных служб (ведение журнала или мониторинг) в WSL</span><span class="sxs-lookup"><span data-stu-id="7993d-140">Running mandatory services (logging or monitoring) inside of WSL</span></span>
* <span data-ttu-id="7993d-141">Мониторинг экземпляров Linux с помощью таких средств Windows Configuration Manager, как SCCM или Intune</span><span class="sxs-lookup"><span data-stu-id="7993d-141">Monitoring Linux instances using Windows configuration manager tools such as SCCM or Intune</span></span>
* <span data-ttu-id="7993d-142">Поддержка McAfee</span><span class="sxs-lookup"><span data-stu-id="7993d-142">McAfee support</span></span>
