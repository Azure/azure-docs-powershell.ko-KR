---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045747"
---
# <span data-ttu-id="ec9e4-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="ec9e4-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="ec9e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9e4-103">StorSimple 장치에서 백업을 복원 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="ec9e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec9e4-104">SYNTAX</span></span>

### <span data-ttu-id="ec9e4-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ec9e4-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec9e4-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="ec9e4-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec9e4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ec9e4-107">DESCRIPTION</span></span>
<span data-ttu-id="ec9e4-108">**AzureStorSimpleDeviceBackupRestoreJob** Cmdlet은 StorSimple 장치에서 백업을 복원 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="ec9e4-109">백업 ID와 선택적 스냅숏 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="ec9e4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ec9e4-110">EXAMPLES</span></span>

### <span data-ttu-id="ec9e4-111">예제 1: 백업을 복원 하는 작업 시작</span><span class="sxs-lookup"><span data-stu-id="ec9e4-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="ec9e4-112">이 명령은 지정 된 ID와 관련 스냅샷이 있는 백업 개체를 Contoso63 이라는 장치에서 복원 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="ec9e4-113">명령에서 *Waitforcomplete* 매개 변수를 지정 하므로 작업이 완료 된 후 cmdlet가 콘솔에 컨트롤을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="ec9e4-114">예제 2: 특정 스냅숏을 복원 하는 작업 시작</span><span class="sxs-lookup"><span data-stu-id="ec9e4-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="ec9e4-115">이 명령은 지정 된 ID의 백업 스냅숏을 복원 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="ec9e4-116">명령은 Contoso63 이라는 장치에서 ID를 기준으로 백업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="ec9e4-117">명령에서 *Force* 매개 변수를 지정 하므로 확인 메시지를 표시 하지 않고 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="ec9e4-118">변수</span><span class="sxs-lookup"><span data-stu-id="ec9e4-118">PARAMETERS</span></span>

### <span data-ttu-id="ec9e4-119">-BackupId</span><span class="sxs-lookup"><span data-stu-id="ec9e4-119">-BackupId</span></span>
<span data-ttu-id="ec9e4-120">복원할 백업의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="ec9e4-121">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="ec9e4-121">-DeviceName</span></span>
<span data-ttu-id="ec9e4-122">백업이 있는 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="ec9e4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ec9e4-123">-Force</span></span>
<span data-ttu-id="ec9e4-124">이 cmdlet이 확인을 묻는 메시지를 표시 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="ec9e4-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="ec9e4-125">-Profile</span></span>
<span data-ttu-id="ec9e4-126">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ec9e4-127">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="ec9e4-127">-SnapshotId</span></span>
<span data-ttu-id="ec9e4-128">복원할 스냅숏의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-128">Specifies the instance ID of the snapshot to restore.</span></span>

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

### <span data-ttu-id="ec9e4-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="ec9e4-129">-WaitForComplete</span></span>
<span data-ttu-id="ec9e4-130">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ec9e4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9e4-131">CommonParameters</span></span>
<span data-ttu-id="ec9e4-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9e4-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec9e4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9e4-134">입력</span><span class="sxs-lookup"><span data-stu-id="ec9e4-134">INPUTS</span></span>

### <span data-ttu-id="ec9e4-135">않아야</span><span class="sxs-lookup"><span data-stu-id="ec9e4-135">None</span></span>

## <span data-ttu-id="ec9e4-136">출력</span><span class="sxs-lookup"><span data-stu-id="ec9e4-136">OUTPUTS</span></span>

### <span data-ttu-id="ec9e4-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="ec9e4-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="ec9e4-138">*Waitforcomplete* 매개 변수를 지정 하면이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="ec9e4-139">해당 매개 변수를 지정 하지 않으면 **Taskresponse** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec9e4-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="ec9e4-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ec9e4-140">NOTES</span></span>

## <span data-ttu-id="ec9e4-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec9e4-141">RELATED LINKS</span></span>

[<span data-ttu-id="ec9e4-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="ec9e4-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="ec9e4-143">시작-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="ec9e4-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


