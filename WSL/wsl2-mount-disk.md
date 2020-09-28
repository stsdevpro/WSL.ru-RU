---
title: Начало работы с подключением диска Linux в WSL 2 (Предварительная версия)
description: Узнайте, как настроить подключение диска в WSL 2 и как получить к нему доступ.
keywords: WSL, Windows, виндовссубсистем, GNU, Linux, bash, диск, ext4, FileSystem, Mount
ms.date: 06/08/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 5ea7d7adae42a44b040408575e7345c456f3acac
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413285"
---
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a><span data-ttu-id="1e9d1-104">Начало работы с подключением диска Linux в WSL 2 (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="1e9d1-104">Get started mounting a linux disk in WSL 2 (preview)</span></span>

<span data-ttu-id="1e9d1-105">Если вы хотите получить доступ к формату диска Linux, который не поддерживается Windows, можно использовать WSL 2 для подключения диска и доступа к его содержимому.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-105">If you want to access a Linux disk format that isn't supported by Windows, you can use WSL 2 to mount your disk and access its content.</span></span>

<span data-ttu-id="1e9d1-106">В этом учебнике рассматриваются шаги по определению диска и раздела для подключения к WSL2, их подключению и доступу.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-106">This tutorial will cover the steps to identify the disk and partition to attach to WSL2, how to mount them, and how to access them.</span></span>

> [!NOTE]
> <span data-ttu-id="1e9d1-107">Для подключения диска к WSL 2 требуется административный доступ.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-107">Administrator access is required to attach a disk to WSL 2.</span></span>

## <a name="identify-the-disk"></a><span data-ttu-id="1e9d1-108">Указание диска</span><span class="sxs-lookup"><span data-stu-id="1e9d1-108">Identify the disk</span></span>

<span data-ttu-id="1e9d1-109">Чтобы получить список доступных дисков в Windows, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-109">To list the available disks in Windows, run:</span></span>

```powershell
wmic diskdrive list brief
```

<span data-ttu-id="1e9d1-110">Пути к дискам доступны в столбцах "DeviceID".</span><span class="sxs-lookup"><span data-stu-id="1e9d1-110">The disks paths are available under the 'DeviceID' columns.</span></span> <span data-ttu-id="1e9d1-111">Обычно под `\\.\PHYSICALDRIVE*` форматом.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-111">Usually under the `\\.\PHYSICALDRIVE*` format.</span></span>

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a><span data-ttu-id="1e9d1-112">Список и выбор секций для подключения в WSL 2</span><span class="sxs-lookup"><span data-stu-id="1e9d1-112">List and select the partitions to mount in WSL 2</span></span>

<span data-ttu-id="1e9d1-113">После идентификации диска выполните:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-113">Once the disk is identified, run:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="1e9d1-114">Это сделает диск доступным в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-114">This will make the disk available in WSL 2.</span></span>

<span data-ttu-id="1e9d1-115">После подключения раздел можно вывести в список, выполнив следующую команду в WSL 2:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-115">Once attached, the partition can be listed by running the following command inside WSL 2:</span></span>

```powershell
lsblk
```

<span data-ttu-id="1e9d1-116">Будут отображены доступные блочные устройства и их разделы.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-116">This will display the available block devices and their partitions.</span></span>

<span data-ttu-id="1e9d1-117">В Linux блочное устройство определяется как  `/dev/<Device><Partition>` .</span><span class="sxs-lookup"><span data-stu-id="1e9d1-117">Inside Linux, a block device is identified as  `/dev/<Device><Partition>`.</span></span> <span data-ttu-id="1e9d1-118">Например,/dev/sdb3 — это раздел номер 3 диска `sdb` .</span><span class="sxs-lookup"><span data-stu-id="1e9d1-118">For example, /dev/sdb3, is the partition number 3 of disk `sdb`.</span></span>

<span data-ttu-id="1e9d1-119">Выходные данные примера:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-119">Example output:</span></span>

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a><span data-ttu-id="1e9d1-120">Определение типа файловой системы</span><span class="sxs-lookup"><span data-stu-id="1e9d1-120">Identifying the filesystem type</span></span>

<span data-ttu-id="1e9d1-121">Если вы не знакомы с типом файловой системы диска или раздела, можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-121">If you don't know the type of filesystem of a disk or partition, you can use this command:</span></span>

```powershell
blkid <BlockDevice>
```

<span data-ttu-id="1e9d1-122">Будет выведен обнаруженный тип файловой системы (в `TYPE="<Filesystem>"` формате).</span><span class="sxs-lookup"><span data-stu-id="1e9d1-122">This will output the detected filesystem type (under the `TYPE="<Filesystem>"` format).</span></span>

## <a name="mount-the-selected-partitions"></a><span data-ttu-id="1e9d1-123">Подключить выбранные секции</span><span class="sxs-lookup"><span data-stu-id="1e9d1-123">Mount the selected partitions</span></span>

<span data-ttu-id="1e9d1-124">Определив разделы, которые необходимо подключить, выполните следующую команду в каждом разделе:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-124">Once you have identified the partitions you want to mount, run this command on each partition:</span></span> 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> <span data-ttu-id="1e9d1-125">Если вы хотите подключить весь диск как один том (т. е. Если диск не секционируется), `--partition` можно опустить.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-125">If you wish to mount the entire disk as a single volume (i.e. if the disk isn't partitioned), `--partition` can be omitted.</span></span>
> 
> <span data-ttu-id="1e9d1-126">Если этот параметр опущен, то типом файловой системы по умолчанию будет «ext4».</span><span class="sxs-lookup"><span data-stu-id="1e9d1-126">If omitted, the default filesystem type is "ext4".</span></span>

## <a name="access-the-disk-content"></a><span data-ttu-id="1e9d1-127">Доступ к содержимому диска</span><span class="sxs-lookup"><span data-stu-id="1e9d1-127">Access the disk content</span></span>

<span data-ttu-id="1e9d1-128">После подключения доступ к диску можно получить по пути, на который указывает значение конфигурации: `automount.root` .</span><span class="sxs-lookup"><span data-stu-id="1e9d1-128">Once mounted, the disk can be accessed under the path pointed to by the config value: `automount.root`.</span></span> <span data-ttu-id="1e9d1-129">Значение по умолчанию — `/mnt/wsl`.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-129">The default value is `/mnt/wsl`.</span></span>

<span data-ttu-id="1e9d1-130">В Windows доступ к диску можно получить из проводника, перейдя к: `\\wsl$\\<Distro>\\<Mountpoint>` (выберите любой дистрибутив Linux).</span><span class="sxs-lookup"><span data-stu-id="1e9d1-130">From Windows, the disk can be accessed from File Explorer by navigating to: `\\wsl$\\<Distro>\\<Mountpoint>` (pick any Linux distribution).</span></span>

## <a name="unmount-the-disk"></a><span data-ttu-id="1e9d1-131">Отключение диска.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-131">Unmount the disk</span></span>

<span data-ttu-id="1e9d1-132">Если необходимо отключить диск от WSL 2 и отсоединить его от него, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-132">If you want to unmount and detach the disk from WSL 2, run:</span></span>

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a><span data-ttu-id="1e9d1-133">Справочник по командной строке</span><span class="sxs-lookup"><span data-stu-id="1e9d1-133">Command line reference</span></span>

### <a name="mouting-a-specific-filesystem"></a><span data-ttu-id="1e9d1-134">Маутинг определенную файловую систему</span><span class="sxs-lookup"><span data-stu-id="1e9d1-134">Mouting a specific filesystem</span></span>

<span data-ttu-id="1e9d1-135">По умолчанию WSL 2 будет пытаться подключить устройство как ext4.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-135">By default, WSL 2 will attempt to mount the device as ext4.</span></span> <span data-ttu-id="1e9d1-136">Чтобы указать другую файловую систему, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-136">To specify another filesystem, run:</span></span>

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

<span data-ttu-id="1e9d1-137">Например, чтобы подключить диск в файловой системе FAT, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-137">For example, to mount a disk as fat, run:</span></span>

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> <span data-ttu-id="1e9d1-138">Чтобы получить список доступных файловых систем в WSL2, выполните команду: `cat /proc/filesystems`</span><span class="sxs-lookup"><span data-stu-id="1e9d1-138">To list the available filesystems in WSL2, run: `cat /proc/filesystems`</span></span>

### <a name="mouting-a-specific-partition"></a><span data-ttu-id="1e9d1-139">Маутинг определенную секцию</span><span class="sxs-lookup"><span data-stu-id="1e9d1-139">Mouting a specific partition</span></span>

<span data-ttu-id="1e9d1-140">По умолчанию WSL 2 пытается подключить весь диск.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-140">By default, WSL 2 attempts to mount the entire disk.</span></span> <span data-ttu-id="1e9d1-141">Чтобы подключить конкретный раздел, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-141">To mount a specific partition, run:</span></span>

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

<span data-ttu-id="1e9d1-142">Это работает только в том случае, если диск является основной загрузочной записью (MBR) или GPT (таблица разделов GUID).</span><span class="sxs-lookup"><span data-stu-id="1e9d1-142">This only works if the disk is either MBR (Master Boot Record) or GPT (GUID Partition Table).</span></span> <span data-ttu-id="1e9d1-143">[Узнайте о стилях разделов — MBR и GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span><span class="sxs-lookup"><span data-stu-id="1e9d1-143">[Read about partition styles - MBR and GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span></span>

### <a name="specifying-mount-options"></a><span data-ttu-id="1e9d1-144">Указание параметров подключения</span><span class="sxs-lookup"><span data-stu-id="1e9d1-144">Specifying mount options</span></span>

<span data-ttu-id="1e9d1-145">Чтобы указать параметры подключения, выполните:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-145">To specify mount options, run:</span></span>

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

<span data-ttu-id="1e9d1-146">Пример:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-146">Example:</span></span>

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> <span data-ttu-id="1e9d1-147">В настоящее время поддерживаются только параметры файловой системы.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-147">Only filesystem specific options are supported at this time.</span></span> <span data-ttu-id="1e9d1-148">Универсальные параметры, такие как `ro, rw, noatime, ...` , не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-148">Generic options such as `ro, rw, noatime, ...` are not supported.</span></span>

### <a name="attaching-the-disk-without-mounting-it"></a><span data-ttu-id="1e9d1-149">Подключение диска без подключения</span><span class="sxs-lookup"><span data-stu-id="1e9d1-149">Attaching the disk without mounting it</span></span>

<span data-ttu-id="1e9d1-150">Если схема диска не поддерживается ни одним из указанных выше параметров, можно подключить диск к WSL 2 без подключения к нему, выполнив:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-150">If the disk scheme isn't supported by any of the above options, you can attach the disk to WSL 2 without mounting it by running:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="1e9d1-151">Это сделает блочное устройство доступным в WSL 2, чтобы его можно было подключить вручную.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-151">This will make the block device available inside WSL 2 so it can be mounted manually from there.</span></span> <span data-ttu-id="1e9d1-152">Используйте `lsblk` для перечисления доступных блочных устройств в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-152">Use `lsblk` to list the available block devices inside WSL 2.</span></span>

### <a name="detaching-a-disk"></a><span data-ttu-id="1e9d1-153">Отсоединение диска</span><span class="sxs-lookup"><span data-stu-id="1e9d1-153">Detaching a disk</span></span>

<span data-ttu-id="1e9d1-154">Чтобы отсоединить диск от WSL 2, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="1e9d1-154">To detach a disk from WSL 2, run:</span></span>

```powershell
wsl --unmount [DiskPath]
```

<span data-ttu-id="1e9d1-155">Если `Diskpath` параметр не указан, все подключенные диски отключаются и отсоединяются.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-155">If `Diskpath` is omitted, all attached disks are unmounted and detached.</span></span>

> [!NOTE]
> <span data-ttu-id="1e9d1-156">Если не удается отключить один диск, WSL 2 можно принудительно завершить, выполнив команду `wsl --shutdown` , которая отключит диск.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-156">If one disk fails to unmount, WSL 2 can be forced to exit by running `wsl --shutdown`, which will detach the disk.</span></span>

## <a name="limitations"></a><span data-ttu-id="1e9d1-157">Ограничения</span><span class="sxs-lookup"><span data-stu-id="1e9d1-157">Limitations</span></span>

- <span data-ttu-id="1e9d1-158">В настоящее время к WSL 2 можно подключить только целые диски. Это означает, что невозможно присоединить только один раздел.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-158">At this time, only entire disks can be attached to WSL 2, meaning that it's not possible to attach only a partition.</span></span> <span data-ttu-id="1e9d1-159">В частности, это означает, что невозможно использовать `wsl --mount` для чтения раздела на устройстве загрузки, так как это устройство не может быть отсоединено от Windows.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-159">Concretely, this means that it's not possible to use `wsl --mount` to read a partition on the boot device, because that device can't be detached from Windows.</span></span>

- <span data-ttu-id="1e9d1-160">Устройства USB Flash не поддерживаются в настоящее время и не подключаются к WSL 2.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-160">USB flash drives are not supported at this time and will fail to attach to WSL 2.</span></span> <span data-ttu-id="1e9d1-161">Хотя диски USB поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e9d1-161">USB disks are supported though.</span></span>

- <span data-ttu-id="1e9d1-162">Только системные системы, которые изначально поддерживаются в ядре, могут быть подключены `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="1e9d1-162">Only filesystems that are natively supported in the kernel can be mounted by `wsl --mount`.</span></span> <span data-ttu-id="1e9d1-163">Это означает, что невозможно использовать установленные драйверы FileSystem (например, NTFS-3G), вызвав `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="1e9d1-163">This means that it's not possible to use installed filesystem drivers (such as ntfs-3g for example) by calling `wsl --mount`.</span></span>