---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046467"
---
# <span data-ttu-id="45f18-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="45f18-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="45f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45f18-102">SYNOPSIS</span></span>
<span data-ttu-id="45f18-103">백업 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-103">Deletes a backup object.</span></span>

## <span data-ttu-id="45f18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45f18-104">SYNTAX</span></span>

### <span data-ttu-id="45f18-105">IdentifyById (기본값)</span><span class="sxs-lookup"><span data-stu-id="45f18-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="45f18-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="45f18-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="45f18-107">설명은</span><span class="sxs-lookup"><span data-stu-id="45f18-107">DESCRIPTION</span></span>
<span data-ttu-id="45f18-108">**Remove-AzureStorSimpleDeviceBackup** cmdlet은 단일 백업 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="45f18-109">이미 삭제 된 백업을 삭제 하려고 하면이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="45f18-110">예제의</span><span class="sxs-lookup"><span data-stu-id="45f18-110">EXAMPLES</span></span>

### <span data-ttu-id="45f18-111">예제 1: 장치에 대 한 백업 제거</span><span class="sxs-lookup"><span data-stu-id="45f18-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="45f18-112">이 명령은 Contoso63-AppVm 이라는 장치에 대해 지정 된 ID를 가진 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="45f18-113">이 명령은 **백업** 개체를 제거 하는 작업을 시작한 다음 **taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="45f18-114">작업의 상태를 보려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="45f18-115">예제 2: ID를 사용 하 여 장치에 대 한 첫 번째 백업 제거</span><span class="sxs-lookup"><span data-stu-id="45f18-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="45f18-116">첫 번째 명령은 Contoso63 이라는 장치에 대 한 백업을 가져온 다음 $Backup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="45f18-117">두 번째 명령은 Contoso63 이라는 장치에서 백업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="45f18-118">이 명령은 표준 점 표기법을 사용 하 여 $Backup 배열의 첫 번째 요소의 **InstanceId** 속성을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="45f18-119">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로이 명령은 작업이 완료 될 때까지 대기한 다음 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="45f18-120">예제 3: 파이프라인을 사용 하 여 디바이스의 첫 번째 백업 제거</span><span class="sxs-lookup"><span data-stu-id="45f18-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="45f18-121">첫 번째 명령은 Contoso63 이라는 장치에 대 한 백업을 가져온 다음 $Backup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="45f18-122">두 번째 명령은 $Backup 배열에 저장 된 첫 번째 개체를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="45f18-123">해당 cmdlet은 Contoso63 이라는 장치에서 해당 백업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="45f18-124">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로이 명령은 작업이 완료 될 때까지 대기한 다음 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="45f18-125">변수</span><span class="sxs-lookup"><span data-stu-id="45f18-125">PARAMETERS</span></span>

### <span data-ttu-id="45f18-126">-백업</span><span class="sxs-lookup"><span data-stu-id="45f18-126">-Backup</span></span>
<span data-ttu-id="45f18-127">삭제할 **백업** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="45f18-128">**백업** 개체를 얻으려면 **Get-AzureStorSimpleDeviceBackup** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45f18-129">-BackupId</span><span class="sxs-lookup"><span data-stu-id="45f18-129">-BackupId</span></span>
<span data-ttu-id="45f18-130">삭제할 백업의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="45f18-131">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="45f18-131">-DeviceName</span></span>
<span data-ttu-id="45f18-132">백업을 삭제할 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="45f18-133">-Force</span><span class="sxs-lookup"><span data-stu-id="45f18-133">-Force</span></span>
<span data-ttu-id="45f18-134">이 cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="45f18-135">-프로필</span><span class="sxs-lookup"><span data-stu-id="45f18-135">-Profile</span></span>
<span data-ttu-id="45f18-136">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="45f18-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="45f18-137">-WaitForComplete</span></span>
<span data-ttu-id="45f18-138">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="45f18-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f18-139">CommonParameters</span></span>
<span data-ttu-id="45f18-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f18-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45f18-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f18-142">입력</span><span class="sxs-lookup"><span data-stu-id="45f18-142">INPUTS</span></span>

### <span data-ttu-id="45f18-143">백업할</span><span class="sxs-lookup"><span data-stu-id="45f18-143">Backup</span></span>

## <span data-ttu-id="45f18-144">출력</span><span class="sxs-lookup"><span data-stu-id="45f18-144">OUTPUTS</span></span>

### <span data-ttu-id="45f18-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="45f18-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="45f18-146">이 cmdlet은 *Waitforcomplete* 매개 변수를 지정 하지 않으면 **TaskStatusInfo** 개체를 반환 합니다. 해당 매개 변수를 지정 하지 않으면 **taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f18-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="45f18-147">상속자</span><span class="sxs-lookup"><span data-stu-id="45f18-147">NOTES</span></span>

## <span data-ttu-id="45f18-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45f18-148">RELATED LINKS</span></span>

[<span data-ttu-id="45f18-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="45f18-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


