---
title: Начало работы с подключением диска Linux в WSL 2 (Предварительная версия)
description: Узнайте, как настроить подключение диска в WSL 2 и как получить к нему доступ.
keywords: WSL, Windows, виндовссубсистем, GNU, Linux, bash, диск, ext4, FileSystem, Mount
ms.date: 06/08/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 5d996586baf5e22cc557c27c6f54b2cb1a91dc4b
ms.sourcegitcommit: cc81ebc749cf84dd58e9f57ee4cc72b5c72be1fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "93352657"
---
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a><span data-ttu-id="93137-104">Начало работы с подключением диска Linux в WSL 2 (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="93137-104">Get started mounting a Linux disk in WSL 2 (preview)</span></span>

<span data-ttu-id="93137-105">Если вы хотите получить доступ к формату диска Linux, который не поддерживается Windows, можно использовать WSL 2 для подключения диска и доступа к его содержимому.</span><span class="sxs-lookup"><span data-stu-id="93137-105">If you want to access a Linux disk format that isn't supported by Windows, you can use WSL 2 to mount your disk and access its content.</span></span>

<span data-ttu-id="93137-106">В этом учебнике рассматриваются шаги по определению диска и раздела для подключения к WSL2, их подключению и доступу.</span><span class="sxs-lookup"><span data-stu-id="93137-106">This tutorial will cover the steps to identify the disk and partition to attach to WSL2, how to mount them, and how to access them.</span></span>

> [!NOTE]
> <span data-ttu-id="93137-107">Чтобы получить доступ к этой функции, необходимо использовать Windows 10 Build 20211 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="93137-107">You will need to be on Windows 10 Build 20211 or higher to access this feature.</span></span> <span data-ttu-id="93137-108">Вы можете присоединиться к [программе "предварительные оценки Windows](https://insider.windows.com/) " для получения последних предварительных сборок.</span><span class="sxs-lookup"><span data-stu-id="93137-108">You can join the [Windows Insiders Program](https://insider.windows.com/) to get the latest preview builds.</span></span>
> <span data-ttu-id="93137-109">Для подключения диска к WSL 2 требуется административный доступ.</span><span class="sxs-lookup"><span data-stu-id="93137-109">Administrator access is required to attach a disk to WSL 2.</span></span>

## <a name="identify-the-disk"></a><span data-ttu-id="93137-110">Указание диска</span><span class="sxs-lookup"><span data-stu-id="93137-110">Identify the disk</span></span>

<span data-ttu-id="93137-111">Чтобы получить список доступных дисков в Windows, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="93137-111">To list the available disks in Windows, run:</span></span>

```powershell
wmic diskdrive list brief
```

<span data-ttu-id="93137-112">Пути к дискам доступны в столбцах "DeviceID".</span><span class="sxs-lookup"><span data-stu-id="93137-112">The disks paths are available under the 'DeviceID' columns.</span></span> <span data-ttu-id="93137-113">Обычно под `\\.\PHYSICALDRIVE*` форматом.</span><span class="sxs-lookup"><span data-stu-id="93137-113">Usually under the `\\.\PHYSICALDRIVE*` format.</span></span>

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a><span data-ttu-id="93137-114">Список и выбор секций для подключения в WSL 2</span><span class="sxs-lookup"><span data-stu-id="93137-114">List and select the partitions to mount in WSL 2</span></span>

<span data-ttu-id="93137-115">После идентификации диска выполните:</span><span class="sxs-lookup"><span data-stu-id="93137-115">Once the disk is identified, run:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="93137-116">Это сделает диск доступным в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="93137-116">This will make the disk available in WSL 2.</span></span>

<span data-ttu-id="93137-117">После подключения раздел можно вывести в список, выполнив следующую команду в WSL 2:</span><span class="sxs-lookup"><span data-stu-id="93137-117">Once attached, the partition can be listed by running the following command inside WSL 2:</span></span>

```powershell
lsblk
```

<span data-ttu-id="93137-118">Будут отображены доступные блочные устройства и их разделы.</span><span class="sxs-lookup"><span data-stu-id="93137-118">This will display the available block devices and their partitions.</span></span>

<span data-ttu-id="93137-119">В Linux блочное устройство определяется как  `/dev/<Device><Partition>` .</span><span class="sxs-lookup"><span data-stu-id="93137-119">Inside Linux, a block device is identified as  `/dev/<Device><Partition>`.</span></span> <span data-ttu-id="93137-120">Например,/dev/sdb3 — это раздел номер 3 диска `sdb` .</span><span class="sxs-lookup"><span data-stu-id="93137-120">For example, /dev/sdb3, is the partition number 3 of disk `sdb`.</span></span>

<span data-ttu-id="93137-121">Выходные данные примера:</span><span class="sxs-lookup"><span data-stu-id="93137-121">Example output:</span></span>

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a><span data-ttu-id="93137-122">Определение типа файловой системы</span><span class="sxs-lookup"><span data-stu-id="93137-122">Identifying the filesystem type</span></span>

<span data-ttu-id="93137-123">Если вы не знакомы с типом файловой системы диска или раздела, можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="93137-123">If you don't know the type of filesystem of a disk or partition, you can use this command:</span></span>

```powershell
blkid <BlockDevice>
```

<span data-ttu-id="93137-124">Будет выведен обнаруженный тип файловой системы (в `TYPE="<Filesystem>"` формате).</span><span class="sxs-lookup"><span data-stu-id="93137-124">This will output the detected filesystem type (under the `TYPE="<Filesystem>"` format).</span></span>

## <a name="mount-the-selected-partitions"></a><span data-ttu-id="93137-125">Подключить выбранные секции</span><span class="sxs-lookup"><span data-stu-id="93137-125">Mount the selected partitions</span></span>

<span data-ttu-id="93137-126">Определив разделы, которые необходимо подключить, выполните следующую команду в каждом разделе:</span><span class="sxs-lookup"><span data-stu-id="93137-126">Once you have identified the partitions you want to mount, run this command on each partition:</span></span> 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> <span data-ttu-id="93137-127">Если вы хотите подключить весь диск как один том (т. е. Если диск не секционируется), `--partition` можно опустить.</span><span class="sxs-lookup"><span data-stu-id="93137-127">If you wish to mount the entire disk as a single volume (i.e. if the disk isn't partitioned), `--partition` can be omitted.</span></span>
> 
> <span data-ttu-id="93137-128">Если этот параметр опущен, то типом файловой системы по умолчанию будет «ext4».</span><span class="sxs-lookup"><span data-stu-id="93137-128">If omitted, the default filesystem type is "ext4".</span></span>

## <a name="access-the-disk-content"></a><span data-ttu-id="93137-129">Доступ к содержимому диска</span><span class="sxs-lookup"><span data-stu-id="93137-129">Access the disk content</span></span>

<span data-ttu-id="93137-130">После подключения доступ к диску можно получить по пути, на который указывает значение конфигурации: `automount.root` .</span><span class="sxs-lookup"><span data-stu-id="93137-130">Once mounted, the disk can be accessed under the path pointed to by the config value: `automount.root`.</span></span> <span data-ttu-id="93137-131">Значение по умолчанию — `/mnt/wsl`.</span><span class="sxs-lookup"><span data-stu-id="93137-131">The default value is `/mnt/wsl`.</span></span>

<span data-ttu-id="93137-132">В Windows доступ к диску можно получить из проводника, перейдя к: `\\wsl$\\<Distro>\\<Mountpoint>` (выберите любой дистрибутив Linux).</span><span class="sxs-lookup"><span data-stu-id="93137-132">From Windows, the disk can be accessed from File Explorer by navigating to: `\\wsl$\\<Distro>\\<Mountpoint>` (pick any Linux distribution).</span></span>

## <a name="unmount-the-disk"></a><span data-ttu-id="93137-133">Отключение диска.</span><span class="sxs-lookup"><span data-stu-id="93137-133">Unmount the disk</span></span>

<span data-ttu-id="93137-134">Если необходимо отключить диск от WSL 2 и отсоединить его от него, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="93137-134">If you want to unmount and detach the disk from WSL 2, run:</span></span>

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a><span data-ttu-id="93137-135">Справочник по командной строке</span><span class="sxs-lookup"><span data-stu-id="93137-135">Command line reference</span></span>

### <a name="mouting-a-specific-filesystem"></a><span data-ttu-id="93137-136">Маутинг определенную файловую систему</span><span class="sxs-lookup"><span data-stu-id="93137-136">Mouting a specific filesystem</span></span>

<span data-ttu-id="93137-137">По умолчанию WSL 2 будет пытаться подключить устройство как ext4.</span><span class="sxs-lookup"><span data-stu-id="93137-137">By default, WSL 2 will attempt to mount the device as ext4.</span></span> <span data-ttu-id="93137-138">Чтобы указать другую файловую систему, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="93137-138">To specify another filesystem, run:</span></span>

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

<span data-ttu-id="93137-139">Например, чтобы подключить диск в файловой системе FAT, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="93137-139">For example, to mount a disk as fat, run:</span></span>

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> <span data-ttu-id="93137-140">Чтобы получить список доступных файловых систем в WSL2, выполните команду: `cat /proc/filesystems`</span><span class="sxs-lookup"><span data-stu-id="93137-140">To list the available filesystems in WSL2, run: `cat /proc/filesystems`</span></span>

### <a name="mouting-a-specific-partition"></a><span data-ttu-id="93137-141">Маутинг определенную секцию</span><span class="sxs-lookup"><span data-stu-id="93137-141">Mouting a specific partition</span></span>

<span data-ttu-id="93137-142">По умолчанию WSL 2 пытается подключить весь диск.</span><span class="sxs-lookup"><span data-stu-id="93137-142">By default, WSL 2 attempts to mount the entire disk.</span></span> <span data-ttu-id="93137-143">Чтобы подключить конкретный раздел, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="93137-143">To mount a specific partition, run:</span></span>

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

<span data-ttu-id="93137-144">Это работает только в том случае, если диск является основной загрузочной записью (MBR) или GPT (таблица разделов GUID).</span><span class="sxs-lookup"><span data-stu-id="93137-144">This only works if the disk is either MBR (Master Boot Record) or GPT (GUID Partition Table).</span></span> <span data-ttu-id="93137-145">[Узнайте о стилях разделов — MBR и GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span><span class="sxs-lookup"><span data-stu-id="93137-145">[Read about partition styles - MBR and GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span></span>

### <a name="specifying-mount-options"></a><span data-ttu-id="93137-146">Указание параметров подключения</span><span class="sxs-lookup"><span data-stu-id="93137-146">Specifying mount options</span></span>

<span data-ttu-id="93137-147">Чтобы указать параметры подключения, выполните:</span><span class="sxs-lookup"><span data-stu-id="93137-147">To specify mount options, run:</span></span>

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

<span data-ttu-id="93137-148">Пример</span><span class="sxs-lookup"><span data-stu-id="93137-148">Example:</span></span>

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> <span data-ttu-id="93137-149">В настоящее время поддерживаются только параметры файловой системы.</span><span class="sxs-lookup"><span data-stu-id="93137-149">Only filesystem specific options are supported at this time.</span></span> <span data-ttu-id="93137-150">Универсальные параметры, такие как `ro, rw, noatime, ...` , не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93137-150">Generic options such as `ro, rw, noatime, ...` are not supported.</span></span>

### <a name="attaching-the-disk-without-mounting-it"></a><span data-ttu-id="93137-151">Подключение диска без подключения</span><span class="sxs-lookup"><span data-stu-id="93137-151">Attaching the disk without mounting it</span></span>

<span data-ttu-id="93137-152">Если схема диска не поддерживается ни одним из указанных выше параметров, можно подключить диск к WSL 2 без подключения к нему, выполнив:</span><span class="sxs-lookup"><span data-stu-id="93137-152">If the disk scheme isn't supported by any of the above options, you can attach the disk to WSL 2 without mounting it by running:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="93137-153">Это сделает блочное устройство доступным в WSL 2, чтобы его можно было подключить вручную.</span><span class="sxs-lookup"><span data-stu-id="93137-153">This will make the block device available inside WSL 2 so it can be mounted manually from there.</span></span> <span data-ttu-id="93137-154">Используйте `lsblk` для перечисления доступных блочных устройств в WSL 2.</span><span class="sxs-lookup"><span data-stu-id="93137-154">Use `lsblk` to list the available block devices inside WSL 2.</span></span>

### <a name="detaching-a-disk"></a><span data-ttu-id="93137-155">Отсоединение диска</span><span class="sxs-lookup"><span data-stu-id="93137-155">Detaching a disk</span></span>

<span data-ttu-id="93137-156">Чтобы отсоединить диск от WSL 2, выполните команду:</span><span class="sxs-lookup"><span data-stu-id="93137-156">To detach a disk from WSL 2, run:</span></span>

```powershell
wsl --unmount [DiskPath]
```

<span data-ttu-id="93137-157">Если `Diskpath` параметр не указан, все подключенные диски отключаются и отсоединяются.</span><span class="sxs-lookup"><span data-stu-id="93137-157">If `Diskpath` is omitted, all attached disks are unmounted and detached.</span></span>

> [!NOTE]
> <span data-ttu-id="93137-158">Если не удается отключить один диск, WSL 2 можно принудительно завершить, выполнив команду `wsl --shutdown` , которая отключит диск.</span><span class="sxs-lookup"><span data-stu-id="93137-158">If one disk fails to unmount, WSL 2 can be forced to exit by running `wsl --shutdown`, which will detach the disk.</span></span>

## <a name="mount-a-vhd-in-wsl"></a><span data-ttu-id="93137-159">Подключение виртуального жесткого диска в WSL</span><span class="sxs-lookup"><span data-stu-id="93137-159">Mount a VHD in WSL</span></span>

<span data-ttu-id="93137-160">Вы также можете подключить файлы виртуального жесткого диска (VHD) к WSL с помощью `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="93137-160">You can also mount virtual hard disk files (VHD) into WSL using `wsl --mount`.</span></span> <span data-ttu-id="93137-161">Для этого сначала необходимо подключить виртуальный жесткий диск к Windows с помощью [`Mount-VHD`](https://docs.microsoft.com/powershell/module/hyper-v/mount-vhd) команды в Windows.</span><span class="sxs-lookup"><span data-stu-id="93137-161">To do this, you first need to mount the VHD into Windows using the [`Mount-VHD`](https://docs.microsoft.com/powershell/module/hyper-v/mount-vhd) command in Windows.</span></span> <span data-ttu-id="93137-162">Не забудьте выполнить эту команду в окне с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="93137-162">Be sure to run this command in a window with administrator privileges.</span></span> <span data-ttu-id="93137-163">Ниже приведен пример, в котором мы используем эту команду, а также выводится путь к диску.</span><span class="sxs-lookup"><span data-stu-id="93137-163">Below is an example where we use this command, and also output the disk path</span></span> 

```powershell
Write-Output "\.\\PhysicalDrive$((Mount-VHD -Path .\ext4.vhdx -PassThru | Get-Disk).Number)"
```

<span data-ttu-id="93137-164">Вы можете использовать приведенные выше выходные данные, чтобы получить путь к диску для этого виртуального жесткого диска и подключить его к WSL, следуя инструкциям из предыдущего раздела.</span><span class="sxs-lookup"><span data-stu-id="93137-164">You can use the output above to obtain the disk path for this VHD and mount that into WSL following the instructions in the previous section.</span></span>

<span data-ttu-id="93137-165">Эту методику также можно использовать для подключения и взаимодействия с виртуальными жесткими дисками других WSL дистрибутивов, так как каждый WSL 2 дистрибутив хранится с помощью файла виртуального жесткого диска с именем: `ext4.vhdx` .</span><span class="sxs-lookup"><span data-stu-id="93137-165">You can also use this technique to mount and interact with the virtual hard disks of other WSL distros, as each WSL 2 distro is stored via a virtual hard disk file called: `ext4.vhdx`.</span></span> <span data-ttu-id="93137-166">По умолчанию виртуальные жесткие диски для WSL 2 дистрибутивов хранятся по этому пути: `C:\Users\[user]\AppData\Local\Packages\[distro]\LocalState\[distroPackageName]` , будьте внимательны при доступе к этим системным файлам, это рабочий процесс Power User.</span><span class="sxs-lookup"><span data-stu-id="93137-166">By default the VHDs for WSL 2 distros are stored in this path: `C:\Users\[user]\AppData\Local\Packages\[distro]\LocalState\[distroPackageName]`, please exercise caution accessing these system files, this is a power user workflow.</span></span>

## <a name="limitations"></a><span data-ttu-id="93137-167">Ограничения</span><span class="sxs-lookup"><span data-stu-id="93137-167">Limitations</span></span>

- <span data-ttu-id="93137-168">В настоящее время к WSL 2 можно подключить только целые диски. Это означает, что невозможно присоединить только один раздел.</span><span class="sxs-lookup"><span data-stu-id="93137-168">At this time, only entire disks can be attached to WSL 2, meaning that it's not possible to attach only a partition.</span></span> <span data-ttu-id="93137-169">В частности, это означает, что невозможно использовать `wsl --mount` для чтения раздела на устройстве загрузки, так как это устройство не может быть отсоединено от Windows.</span><span class="sxs-lookup"><span data-stu-id="93137-169">Concretely, this means that it's not possible to use `wsl --mount` to read a partition on the boot device, because that device can't be detached from Windows.</span></span>

- <span data-ttu-id="93137-170">Устройства USB Flash не поддерживаются в настоящее время и не подключаются к WSL 2.</span><span class="sxs-lookup"><span data-stu-id="93137-170">USB flash drives are not supported at this time and will fail to attach to WSL 2.</span></span> <span data-ttu-id="93137-171">Хотя диски USB поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93137-171">USB disks are supported though.</span></span>

- <span data-ttu-id="93137-172">Только системные системы, которые изначально поддерживаются в ядре, могут быть подключены `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="93137-172">Only filesystems that are natively supported in the kernel can be mounted by `wsl --mount`.</span></span> <span data-ttu-id="93137-173">Это означает, что невозможно использовать установленные драйверы FileSystem (например, NTFS-3G), вызвав `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="93137-173">This means that it's not possible to use installed filesystem drivers (such as ntfs-3g for example) by calling `wsl --mount`.</span></span>
