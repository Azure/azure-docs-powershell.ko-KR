---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045852"
---
# <span data-ttu-id="b453d-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b453d-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="b453d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b453d-102">SYNOPSIS</span></span>
<span data-ttu-id="b453d-103">기존 백업 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="b453d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b453d-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b453d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b453d-105">DESCRIPTION</span></span>
<span data-ttu-id="b453d-106">**Set-AzureStorSimpleDeviceBackupPolicy** cmdlet은 기존 백업 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="b453d-107">정책의 이름을 바꾸고, 일정을 추가, 업데이트 또는 삭제 하 고, 정책과 연결 된 볼륨을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="b453d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b453d-108">EXAMPLES</span></span>

### <span data-ttu-id="b453d-109">예제 1: 백업 정책의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="b453d-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="b453d-110">이 명령은 지정 된 ID를 포함 하는 백업 정책의 이름을 UpdatedGeneralPolicy07로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="b453d-111">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로 명령이 작업을 완료 한 다음 작업에 대 한 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="b453d-112">예제 2: 백업 정책에 대 한 일정 업데이트</span><span class="sxs-lookup"><span data-stu-id="b453d-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="b453d-113">첫 번째 명령은 **새 AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet을 사용 하 여 업데이트 구성 개체를 만든 다음 $UpdateConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="b453d-114">두 번째 명령은 $UpdateArray 라는 새 배열 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="b453d-115">다음 명령은 $UpdateConfig에 저장 된 업데이트를 해당 배열에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="b453d-116">배열에 업데이트를 두 개 이상 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="b453d-117">마지막 명령은 Contoso63 이라는 장치에서 지정 된 ID를 갖는 백업 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="b453d-118">이제 정책에 업데이트 된 일정이 $UpdateArray에 저장 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="b453d-119">변수</span><span class="sxs-lookup"><span data-stu-id="b453d-119">PARAMETERS</span></span>

### <span data-ttu-id="b453d-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="b453d-120">-BackupPolicyId</span></span>
<span data-ttu-id="b453d-121">업데이트할 **Backuppolicy** 개체의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

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

### <span data-ttu-id="b453d-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="b453d-122">-BackupPolicyName</span></span>
<span data-ttu-id="b453d-123">백업 정책의 새 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-123">Specifies a new name for the backup policy.</span></span>

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

### <span data-ttu-id="b453d-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="b453d-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="b453d-125">삭제할 **Backupschedule** 개체의 인스턴스 id 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b453d-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="b453d-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="b453d-127">정책에 추가할 **BackupScheduleBase** 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="b453d-128">**BackupScheduleBase** 개체를 얻으려면 **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b453d-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="b453d-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="b453d-130">업데이트할 **BackupScheduleUpdateRequest** 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="b453d-131">**BackupScheduleUpdateRequest** 개체를 얻으려면 **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b453d-132">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="b453d-132">-DeviceName</span></span>
<span data-ttu-id="b453d-133">백업 정책을 업데이트할 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

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

### <span data-ttu-id="b453d-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="b453d-134">-NewName</span></span>
<span data-ttu-id="b453d-135">디바이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-135">Specifies a name for the device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b453d-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="b453d-136">-Profile</span></span>
<span data-ttu-id="b453d-137">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b453d-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="b453d-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="b453d-139">백업 정책을 업데이트할 볼륨의 Id 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b453d-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b453d-140">-WaitForComplete</span></span>
<span data-ttu-id="b453d-141">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b453d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b453d-142">CommonParameters</span></span>
<span data-ttu-id="b453d-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b453d-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b453d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b453d-145">입력</span><span class="sxs-lookup"><span data-stu-id="b453d-145">INPUTS</span></span>

### <span data-ttu-id="b453d-146">않아야</span><span class="sxs-lookup"><span data-stu-id="b453d-146">None</span></span>

## <span data-ttu-id="b453d-147">출력</span><span class="sxs-lookup"><span data-stu-id="b453d-147">OUTPUTS</span></span>

### <span data-ttu-id="b453d-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="b453d-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="b453d-149">*Waitforcomplete* 매개 변수를 지정 하면이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="b453d-150">해당 매개 변수를 지정 하지 않으면 **Taskresponse** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b453d-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="b453d-151">상속자</span><span class="sxs-lookup"><span data-stu-id="b453d-151">NOTES</span></span>

## <span data-ttu-id="b453d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b453d-152">RELATED LINKS</span></span>

[<span data-ttu-id="b453d-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b453d-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="b453d-154">새로운 AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b453d-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="b453d-155">제거-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b453d-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="b453d-156">새로운 AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="b453d-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


