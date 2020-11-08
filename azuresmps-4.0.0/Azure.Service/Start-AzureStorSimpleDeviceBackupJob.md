---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046027"
---
# <span data-ttu-id="224d8-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="224d8-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="224d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="224d8-102">SYNOPSIS</span></span>
<span data-ttu-id="224d8-103">기존 백업 정책에서 백업을 만드는 새 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="224d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="224d8-104">SYNTAX</span></span>

### <span data-ttu-id="224d8-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="224d8-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="224d8-106">지정 된 backuptype</span><span class="sxs-lookup"><span data-stu-id="224d8-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="224d8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="224d8-107">DESCRIPTION</span></span>
<span data-ttu-id="224d8-108">**AzureStorSimpleDeviceBackupJob** Cmdlet은 StorSimple 장치의 기존 백업 정책에서 백업을 만드는 새 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="224d8-109">기본적으로이 cmdlet은 로컬 스냅숏 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="224d8-110">클라우드 백업을 만들려면 *Backuptype* 매개 변수에 대해 cloudsnapshot의 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="224d8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="224d8-111">EXAMPLES</span></span>

### <span data-ttu-id="224d8-112">예제 1: 로컬 스냅샷 백업 만들기</span><span class="sxs-lookup"><span data-stu-id="224d8-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="224d8-113">이 명령은 지정 된 정책 ID에 대 한 로컬 스냅숏 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="224d8-114">이 명령은 작업을 시작한 다음 **Taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="224d8-115">작업 상태를 확인 하려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="224d8-116">예제 2: 클라우드 스냅숏 백업 만들기 및 완료 대기</span><span class="sxs-lookup"><span data-stu-id="224d8-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="224d8-117">이 명령은 지정 된 정책 ID에 대 한 클라우드 스냅숏 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="224d8-118">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로 명령이 작업을 완료 한 다음 작업에 대 한 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="224d8-119">변수</span><span class="sxs-lookup"><span data-stu-id="224d8-119">PARAMETERS</span></span>

### <span data-ttu-id="224d8-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="224d8-120">-BackupPolicyId</span></span>
<span data-ttu-id="224d8-121">백업을 만드는 데 사용할 백업 정책의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="224d8-122">-BackupType</span><span class="sxs-lookup"><span data-stu-id="224d8-122">-BackupType</span></span>
<span data-ttu-id="224d8-123">백업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-123">Specifies the backup type.</span></span>
<span data-ttu-id="224d8-124">유효한 값은 LocalSnapshot 및 CloudSnapshot입니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="224d8-125">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="224d8-125">-DeviceName</span></span>
<span data-ttu-id="224d8-126">백업 작업을 시작할 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="224d8-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="224d8-127">-Profile</span></span>
<span data-ttu-id="224d8-128">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="224d8-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="224d8-129">-WaitForComplete</span></span>
<span data-ttu-id="224d8-130">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="224d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224d8-131">CommonParameters</span></span>
<span data-ttu-id="224d8-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224d8-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="224d8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224d8-134">입력</span><span class="sxs-lookup"><span data-stu-id="224d8-134">INPUTS</span></span>

### <span data-ttu-id="224d8-135">않아야</span><span class="sxs-lookup"><span data-stu-id="224d8-135">None</span></span>

## <span data-ttu-id="224d8-136">출력</span><span class="sxs-lookup"><span data-stu-id="224d8-136">OUTPUTS</span></span>

### <span data-ttu-id="224d8-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="224d8-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="224d8-138">*Waitforcomplete* 매개 변수를 지정 하면이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="224d8-139">해당 매개 변수를 지정 하지 않으면 **Taskresponse** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="224d8-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="224d8-140">상속자</span><span class="sxs-lookup"><span data-stu-id="224d8-140">NOTES</span></span>

## <span data-ttu-id="224d8-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="224d8-141">RELATED LINKS</span></span>

[<span data-ttu-id="224d8-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="224d8-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="224d8-143">시작-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="224d8-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


