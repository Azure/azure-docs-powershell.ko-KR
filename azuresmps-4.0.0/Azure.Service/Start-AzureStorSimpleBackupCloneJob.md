---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045748"
---
# <span data-ttu-id="1c9e3-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="1c9e3-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="1c9e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9e3-103">장치에서 백업을 복제 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="1c9e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c9e3-104">SYNTAX</span></span>

### <span data-ttu-id="1c9e3-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1c9e3-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1c9e3-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="1c9e3-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1c9e3-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="1c9e3-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1c9e3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1c9e3-108">DESCRIPTION</span></span>
<span data-ttu-id="1c9e3-109">**AzureStorSimpleBackupCloneJob** Cmdlet은 StorSimple 장치에서 기존 백업을 복제 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="1c9e3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1c9e3-110">EXAMPLES</span></span>

### <span data-ttu-id="1c9e3-111">예제 1: 장치 이름을 사용 하 여 다른 볼륨으로 백업 복제</span><span class="sxs-lookup"><span data-stu-id="1c9e3-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="1c9e3-112">첫 번째 명령은 **AzureStorSimpleDeviceBackup** cmdlet을 사용 하 여 ContosoDev07 이라는 장치에 대 한 첫 번째 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="1c9e3-113">이 명령은 $Backup 변수에 해당 백업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="1c9e3-114">두 번째 명령은 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 액세스 제어 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="1c9e3-115">명령이 $Acrs 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="1c9e3-116">마지막 명령은 장치의 볼륨에 대 한 지정 된 백업을 같은 장치의 다른 볼륨에 복제 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="1c9e3-117">이 예제에서는 이름을 기준으로 디바이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-117">This example specifies the device by name.</span></span>
<span data-ttu-id="1c9e3-118">이 명령은 $Backup 및 $Acrs에 저장 된 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="1c9e3-119">명령에서 작업의 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="1c9e3-120">예제 2: 장치 Id를 사용 하 여 다른 볼륨으로 백업 복제</span><span class="sxs-lookup"><span data-stu-id="1c9e3-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="1c9e3-121">첫 번째 명령은 **AzureStorSimpleDeviceBackup** cmdlet을 사용 하 여 ContosoDev07 이라는 장치에 대 한 첫 번째 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="1c9e3-122">이 명령은 $Backup 변수에 해당 백업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="1c9e3-123">두 번째 명령은 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 액세스 제어 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="1c9e3-124">명령이 $Acrs 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="1c9e3-125">마지막 명령은 장치의 볼륨에 대 한 지정 된 백업을 같은 장치의 다른 볼륨에 복제 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="1c9e3-126">이 예제에서는 장치 ID를 기준으로 디바이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="1c9e3-127">이 명령은 $Backup 및 $Acrs에 저장 된 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="1c9e3-128">명령에서 작업의 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="1c9e3-129">예제 3: 장치 이름을 사용 하 여 다른 장치의 볼륨에 백업 복제</span><span class="sxs-lookup"><span data-stu-id="1c9e3-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="1c9e3-130">첫 번째 명령은 **AzureStorSimpleDeviceBackup** cmdlet을 사용 하 여 ContosoDev07 이라는 장치에 대 한 첫 번째 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="1c9e3-131">이 명령은 $Backup 변수에 해당 백업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="1c9e3-132">두 번째 명령은 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 액세스 제어 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="1c9e3-133">명령이 $Acrs 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="1c9e3-134">마지막 명령은 장치의 볼륨에 대 한 지정 된 백업을 다른 장치의 볼륨에 복제 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="1c9e3-135">이 예제에서는 이름을 기준으로 디바이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="1c9e3-136">이 명령은 $Backup 및 $Acrs에 저장 된 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="1c9e3-137">명령에서 작업의 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="1c9e3-138">예제 4: 장치 이름과 파이프라인 연산자를 사용 하 여 다른 볼륨으로 백업 복제</span><span class="sxs-lookup"><span data-stu-id="1c9e3-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="1c9e3-139">첫 번째 명령은 **AzureStorSimpleDeviceBackup** cmdlet을 사용 하 여 ContosoDev07 이라는 장치에 대 한 첫 번째 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="1c9e3-140">이 명령은 $Backup 변수에 해당 백업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="1c9e3-141">두 번째 명령은 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 액세스 제어 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="1c9e3-142">이 명령은 파이프라인 연산자를 사용 하 여 결과를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1c9e3-143">현재 cmdlet은 장치의 볼륨에 대해 지정 된 백업을 같은 장치의 다른 볼륨에 복제 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="1c9e3-144">이 예제에서는 이름을 기준으로 디바이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-144">This example specifies the device by name.</span></span>
<span data-ttu-id="1c9e3-145">이 명령은 $Backup에 저장 된 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="1c9e3-146">명령은 파이프라인에서 *Targetaccesscontrolrecords* 매개 변수 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="1c9e3-147">명령에서 작업의 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="1c9e3-148">변수</span><span class="sxs-lookup"><span data-stu-id="1c9e3-148">PARAMETERS</span></span>

### <span data-ttu-id="1c9e3-149">-BackupId</span><span class="sxs-lookup"><span data-stu-id="1c9e3-149">-BackupId</span></span>
<span data-ttu-id="1c9e3-150">복제할 백업의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-150">Specifies the instance ID of the backup to clone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="1c9e3-151">-CloneVolumeName</span></span>
<span data-ttu-id="1c9e3-152">대상 장치에서 복제 된 새 볼륨의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-152">Specifies the name for the new cloned volume on the target device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-153">-Force</span><span class="sxs-lookup"><span data-stu-id="1c9e3-153">-Force</span></span>
<span data-ttu-id="1c9e3-154">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-154">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-155">-프로필</span><span class="sxs-lookup"><span data-stu-id="1c9e3-155">-Profile</span></span>
<span data-ttu-id="1c9e3-156">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-156">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-157">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="1c9e3-157">-Snapshot</span></span>
<span data-ttu-id="1c9e3-158">이 cmdlet이 복제 하는 스냅숏 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="1c9e3-159">-SourceDeviceId</span></span>
<span data-ttu-id="1c9e3-160">원본 장치의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="1c9e3-161">이 cmdlet은 원본 장치에서 다시 복제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-161">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-162">-SourceDeviceName 이름</span><span class="sxs-lookup"><span data-stu-id="1c9e3-162">-SourceDeviceName</span></span>
<span data-ttu-id="1c9e3-163">원본 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="1c9e3-164">이 cmdlet은 원본 장치에서 다시 복제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="1c9e3-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="1c9e3-166">액세스 제어 레코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="1c9e3-167">-TargetDeviceId</span></span>
<span data-ttu-id="1c9e3-168">대상 장치의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-168">Specifies the instance ID of the target device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-169">-TargetDeviceName 이름</span><span class="sxs-lookup"><span data-stu-id="1c9e3-169">-TargetDeviceName</span></span>
<span data-ttu-id="1c9e3-170">이 cmdlet이 백업을 복제 하는 디바이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9e3-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9e3-171">CommonParameters</span></span>
<span data-ttu-id="1c9e3-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9e3-173">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9e3-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9e3-174">입력</span><span class="sxs-lookup"><span data-stu-id="1c9e3-174">INPUTS</span></span>

### <span data-ttu-id="1c9e3-175">스냅샷, AccessControlRecord 목록</span><span class="sxs-lookup"><span data-stu-id="1c9e3-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="1c9e3-176">이 cmdlet에 대 한 **Accesscontrolrecord** 개체의 목록을 파이프 **스냅샷** 개체 또는 목록으로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c9e3-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="1c9e3-177">출력</span><span class="sxs-lookup"><span data-stu-id="1c9e3-177">OUTPUTS</span></span>

## <span data-ttu-id="1c9e3-178">상속자</span><span class="sxs-lookup"><span data-stu-id="1c9e3-178">NOTES</span></span>

## <span data-ttu-id="1c9e3-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c9e3-179">RELATED LINKS</span></span>

[<span data-ttu-id="1c9e3-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="1c9e3-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="1c9e3-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="1c9e3-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


