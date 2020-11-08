---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046464"
---
# <span data-ttu-id="0fc3b-101">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0fc3b-101">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="0fc3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc3b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc3b-103">기존 백업 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-103">Removes an existing backup policy.</span></span>

## <span data-ttu-id="0fc3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fc3b-104">SYNTAX</span></span>

### <span data-ttu-id="0fc3b-105">IdentifyById (기본값)</span><span class="sxs-lookup"><span data-stu-id="0fc3b-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0fc3b-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="0fc3b-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0fc3b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0fc3b-107">DESCRIPTION</span></span>
<span data-ttu-id="0fc3b-108">**Remove-AzureStorSimpleDeviceBackupPolicy** cmdlet은 기존 **backuppolicy** 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-108">The **Remove-AzureStorSimpleDeviceBackupPolicy** cmdlet removes an existing **BackupPolicy** object.</span></span>
<span data-ttu-id="0fc3b-109">백업 정책을 제거 하면 해당 정책에 따라 더 이상 백업이 수행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-109">After you remove a backup policy, no further backups take place based on that policy.</span></span>
<span data-ttu-id="0fc3b-110">이 cmdlet는 삭제 된 정책과 연결 된 모든 일정도 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-110">This cmdlet also deletes all schedules associated with the deleted policy.</span></span>

## <span data-ttu-id="0fc3b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0fc3b-111">EXAMPLES</span></span>

### <span data-ttu-id="0fc3b-112">예제 1: 백업 정책 제거</span><span class="sxs-lookup"><span data-stu-id="0fc3b-112">Example 1: Remove a backup policy</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

<span data-ttu-id="0fc3b-113">이 명령은이 정책을 기반으로 더 이상 백업이 만들어지지 않도록 인스턴스 ID 03710b4c-82c1-40ca-be5c-40289dc49642 인 **Backuppolicy** 를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-113">This command removes the **BackupPolicy** that has the instance ID 03710b4c-82c1-40ca-be5c-40289dc49642, so that no more backups are made based on this policy.</span></span>
<span data-ttu-id="0fc3b-114">이 명령으로이 정책과 연결 된 모든 일정이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-114">The command also deletes all schedules associated with this policy.</span></span>
<span data-ttu-id="0fc3b-115">이 명령은 **Backuppolicy** 개체를 제거 하는 작업을 시작한 다음 **taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-115">The command starts the operation that removes the **BackupPolicy** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="0fc3b-116">작업의 상태를 보려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="0fc3b-117">예제 2: 장치에 대 한 백업 정책의 첫 번째 제거</span><span class="sxs-lookup"><span data-stu-id="0fc3b-117">Example 2: Remove the first of the backup policies for a device</span></span>
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

<span data-ttu-id="0fc3b-118">첫 번째 명령은 Contoso63 이라는 장치에 대 한 백업 정책을 가져온 다음이를 $Policies 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-118">The first command gets the backup policies for the device named Contoso63-AppVm, and then stores them in the $Policies variable.</span></span>

<span data-ttu-id="0fc3b-119">두 번째 명령은 Contoso63에서 첫 번째 백업 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-119">The second command removes the first backup policy from Contoso63-AppVm.</span></span>
<span data-ttu-id="0fc3b-120">명령에서는 표준 도트 구문을 사용 하 여 $Policies에서 첫 번째 항목의 **InstanceId** 속성을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-120">The command uses standard dot syntax to identify the **InstanceId** property of the first item in $Policies.</span></span>
<span data-ttu-id="0fc3b-121">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로 명령이 작업을 완료 한 다음 작업에 대 한 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-121">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="0fc3b-122">예제 3: 파이프라인을 사용 하 여 백업 정책 제거</span><span class="sxs-lookup"><span data-stu-id="0fc3b-122">Example 3: Remove a backup policy by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

<span data-ttu-id="0fc3b-123">이 명령은 **Get-AzureStorSimpleDeviceBackupPolicy** 를 사용 하 여 **backuppolicydetails** 개체를 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-123">This command gets a **BackupPolicyDetails** object by using **Get-AzureStorSimpleDeviceBackupPolicy** , and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0fc3b-124">현재 cmdlet은 TSQAVolume01_Default 라는 백업 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-124">The current cmdlet removes the backup policy named TSQAVolume01_Default.</span></span>

## <span data-ttu-id="0fc3b-125">변수</span><span class="sxs-lookup"><span data-stu-id="0fc3b-125">PARAMETERS</span></span>

### <span data-ttu-id="0fc3b-126">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0fc3b-126">-BackupPolicy</span></span>
<span data-ttu-id="0fc3b-127">삭제할 **Backuppolicydetails** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-127">Specifies the **BackupPolicyDetails** object to delete.</span></span>
<span data-ttu-id="0fc3b-128">**Backuppolicydetails** 개체를 가져오려면 **AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-128">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc3b-129">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="0fc3b-129">-BackupPolicyId</span></span>
<span data-ttu-id="0fc3b-130">삭제할 **Backuppolicy** 개체의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-130">Specifies the instance ID of the **BackupPolicy** object to delete.</span></span>

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

### <span data-ttu-id="0fc3b-131">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="0fc3b-131">-DeviceName</span></span>
<span data-ttu-id="0fc3b-132">백업 정책을 삭제할 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-132">Specifies the name of the StorSimple device on which to delete the backup policy.</span></span>

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

### <span data-ttu-id="0fc3b-133">-Force</span><span class="sxs-lookup"><span data-stu-id="0fc3b-133">-Force</span></span>
<span data-ttu-id="0fc3b-134">이 cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="0fc3b-135">-프로필</span><span class="sxs-lookup"><span data-stu-id="0fc3b-135">-Profile</span></span>
<span data-ttu-id="0fc3b-136">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0fc3b-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="0fc3b-137">-WaitForComplete</span></span>
<span data-ttu-id="0fc3b-138">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="0fc3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc3b-139">CommonParameters</span></span>
<span data-ttu-id="0fc3b-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc3b-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fc3b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc3b-142">입력</span><span class="sxs-lookup"><span data-stu-id="0fc3b-142">INPUTS</span></span>

### <span data-ttu-id="0fc3b-143">BackupPolicyDetails</span><span class="sxs-lookup"><span data-stu-id="0fc3b-143">BackupPolicyDetails</span></span>
<span data-ttu-id="0fc3b-144">이 cmdlet은 **Backuppolicydetails** 개체를 수락 하 여 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-144">This cmdlet accepts a **BackupPolicyDetails** object to delete.</span></span>

## <span data-ttu-id="0fc3b-145">출력</span><span class="sxs-lookup"><span data-stu-id="0fc3b-145">OUTPUTS</span></span>

### <span data-ttu-id="0fc3b-146">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="0fc3b-146">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="0fc3b-147">*Waitforcomplete* 매개 변수를 지정 하면이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-147">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="0fc3b-148">해당 매개 변수를 지정 하지 않으면 **Taskresponse** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fc3b-148">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="0fc3b-149">상속자</span><span class="sxs-lookup"><span data-stu-id="0fc3b-149">NOTES</span></span>

## <span data-ttu-id="0fc3b-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fc3b-150">RELATED LINKS</span></span>

[<span data-ttu-id="0fc3b-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0fc3b-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="0fc3b-152">새로운 AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0fc3b-152">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="0fc3b-153">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0fc3b-153">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="0fc3b-154">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="0fc3b-154">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


