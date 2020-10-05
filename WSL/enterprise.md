---
title: Подсистема Windows для Linux для предприятий
description: Ресурсы и инструкции для оптимального использования подсистемы Windows для Linux в корпоративной среде.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10, корпоративный, развертывание, автономный, упаковка, магазин, распространение, установка, установить
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ac0025257ae70547c5b20d89535510a8b8bb006c
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413105"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a><span data-ttu-id="156c9-104">Настройка подсистемы Windows для Linux для вашего предприятия</span><span class="sxs-lookup"><span data-stu-id="156c9-104">Set up Windows Subsystem for Linux for your enterprise company</span></span>

<span data-ttu-id="156c9-105">Microsoft Store для бизнеса предлагает различные решения для предприятий, которые хотят развернуть WSL в своей компании.</span><span class="sxs-lookup"><span data-stu-id="156c9-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="156c9-106">Документация [Microsoft Store для бизнеса и образования](/microsoft-store/) является отличным ресурсом для поиска общих сведений о магазине.</span><span class="sxs-lookup"><span data-stu-id="156c9-106">The [Microsoft Store for Business and Education docs](/microsoft-store/) are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="156c9-107">Если вы представляете компанию, которая только собирается начать установку WSL, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="156c9-107">If you're a company that's just looking to get set up to start deploying WSL, follow these steps:</span></span>

* [<span data-ttu-id="156c9-108">Зарегистрируйтесь в Microsoft Store для бизнеса и приступайте к работе</span><span class="sxs-lookup"><span data-stu-id="156c9-108">Sign up for the Microsoft Store for Business and get started</span></span>](/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="156c9-109">[Получите сведения об управлении своими продуктами и услугами (включая тем, кто может получать доступ к каким приложениям в вашем личном магазине)](/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="156c9-109">[Manage your products and services (including who can access which apps in your private store)](/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="156c9-110">Здесь вы можете добавлять дистрибутивы WSL в свое хранилище и контролировать, кто может их устанавливать</span><span class="sxs-lookup"><span data-stu-id="156c9-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="156c9-111">Используйте выбранный метод распространения для развертывания программного обеспечения в компании</span><span class="sxs-lookup"><span data-stu-id="156c9-111">Use a distribution method of your choice to deploy the software to your company</span></span>](/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="156c9-112">Свяжитесь с сотрудниками вашей компании, чтобы они могли использовать эту ссылку на эту документацию для установки WSL: [Установка подсистемы Windows для Linux](./install-win10.md)</span><span class="sxs-lookup"><span data-stu-id="156c9-112">Communicate to the employees of your company that they can use this documentation link to install WSL: [Install the Windows Subsystem for Linux](./install-win10.md)</span></span>

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a><span data-ttu-id="156c9-113">Как распределять дистрибутив Linux в Windows в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="156c9-113">How to distribute a Linux distribution on Windows offline</span></span>

<span data-ttu-id="156c9-114">Если компьютеры в вашей организации не имеют доступа к Microsoft Store или Microsoft Store для бизнеса, можно скачать установщик дистрибутива Linux с автономной лицензией, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="156c9-114">If the computers in your company don't have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distribution that has an offline license by following these steps.</span></span>

### <a name="set-up-an-azure-active-directory-account"></a><span data-ttu-id="156c9-115">Настройка учетной записи Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="156c9-115">Set up an Azure Active Directory account</span></span>

<span data-ttu-id="156c9-116">Чтобы получить установщик приложений Microsoft Store необходимо [зарегистрироваться для использования учетной записи Azure AD](/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) и быть глобальным администратором организации.</span><span class="sxs-lookup"><span data-stu-id="156c9-116">You need to [sign up for an Azure AD account](/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="156c9-117">Если у вас уже есть учетная запись, этот шаг можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="156c9-117">If you already have an account, you can skip this step.</span></span>

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a><span data-ttu-id="156c9-118">Настройка WSL с помощью учетной записи Microsoft Store для бизнеса</span><span class="sxs-lookup"><span data-stu-id="156c9-118">Set up WSL using your Microsoft Store for Business account</span></span>

<span data-ttu-id="156c9-119">Инструкции по регистрации учетной записи можно найти здесь: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="156c9-119">The instructions to register an account are found here: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business</span></span>

1. <span data-ttu-id="156c9-120">Войдите в Store для бизнеса и перейдите на домашнюю страницу: https://www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="156c9-120">Sign into the Store for Business and go to the homepage: https://www.microsoft.com/business-store</span></span>

    ![Домашняя страница MS Store для бизнеса](media/offlineinstallscreens/1-screen.png)

2. <span data-ttu-id="156c9-122">Перейдите в меню "Управление" > "Настройки" и включите параметр Show offline apps (Показывать автономные приложения).</span><span class="sxs-lookup"><span data-stu-id="156c9-122">Go to Manage > Settings and enable 'Show offline apps'.</span></span>

    ![Страница параметров MS Store для бизнеса](media/offlineinstallscreens/2-screen.png)

3. <span data-ttu-id="156c9-124">Вернитесь на главную страницу, выбрав "Магазин для моей группы".</span><span class="sxs-lookup"><span data-stu-id="156c9-124">Go back to the main page by selecting 'Shop for my group'.</span></span>

    ![Домашняя страница MS Store для бизнеса](media/offlineinstallscreens/1-screen.png)

4. <span data-ttu-id="156c9-126">Найдите нужный дистрибутив и выберите его.</span><span class="sxs-lookup"><span data-stu-id="156c9-126">Search for your desired distribution and select it.</span></span>

    ![Домашняя страница MS Store для бизнеса с активным поиском](media/offlineinstallscreens/3-screen.png)

5. <span data-ttu-id="156c9-128">Выберите "Автономная" лицензия в раскрывающемся меню "Тип лицензии" и выберите "Получить приложение".</span><span class="sxs-lookup"><span data-stu-id="156c9-128">Select an 'Offline' license in the License type dropdown menu and select 'Get the app'.</span></span> <span data-ttu-id="156c9-129">(Некоторые дистрибутивы Linux могут не предоставлять автономную лицензию).</span><span class="sxs-lookup"><span data-stu-id="156c9-129">(Some Linux distributions may elect not to provide an offline license).</span></span>

    ![Выбор параметра автономной лицензии для Ubuntu в MS Store для бизнеса](media/offlineinstallscreens/4-screen.png)

6. <span data-ttu-id="156c9-131">Нажмите кнопку "Управление", чтобы перейти на страницу продукта приложения.</span><span class="sxs-lookup"><span data-stu-id="156c9-131">Select the 'Manage' button to get to the app's product page.</span></span>

    ![Выбор параметра управления для Ubuntu в MS Store для бизнеса](media/offlineinstallscreens/5-screen.png)

7. <span data-ttu-id="156c9-133">Выберите архитектуру и скачайте пакет для использования в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="156c9-133">Select your architecture and download the package for offline use.</span></span>

    ![Выбор параметра архитектуры для Ubuntu в MS Store для бизнеса](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="156c9-135">Затем этот установщик можно распространить на любой компьютер, на который необходимо установить WSL.</span><span class="sxs-lookup"><span data-stu-id="156c9-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>
