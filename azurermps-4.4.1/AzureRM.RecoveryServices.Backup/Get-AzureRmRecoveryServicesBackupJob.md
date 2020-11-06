---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537031"
---
# <span data-ttu-id="5f382-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5f382-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="5f382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f382-102">SYNOPSIS</span></span>
<span data-ttu-id="5f382-103">백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f382-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f382-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f382-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f382-105">DESCRIPTION</span></span>
<span data-ttu-id="5f382-106">**AzureRmRecoveryServicesBackupJob** cmdlet은 특정 자격 증명 모음에 대 한 Azure 백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="5f382-107">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5f382-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5f382-108">EXAMPLES</span></span>

### <span data-ttu-id="5f382-109">예제 1: 진행 중인 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="5f382-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="5f382-110">첫 번째 명령은 진행 중인 작업의 상태를 배열로 가져온 다음이를 $Joblist 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="5f382-111">두 번째 명령은 $Joblist 배열의 첫 번째 항목을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="5f382-112">예제 2: 지난 7 일 동안 실패 한 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="5f382-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="5f382-113">이 명령은 자격 증명 모음의 마지막 주부터 실패 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="5f382-114">*From* 매개 변수는 UTC에서 지정 된 지난 7 일의 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="5f382-115">명령에서 *To* 매개 변수에 대 한 값을 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="5f382-116">따라서 현재 시간에 대 한 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="5f382-117">예제 3: 진행 중인 작업 가져오기 및 완료 대기</span><span class="sxs-lookup"><span data-stu-id="5f382-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="5f382-118">이 스크립트는 작업이 완료 될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="5f382-119">변수</span><span class="sxs-lookup"><span data-stu-id="5f382-119">PARAMETERS</span></span>

### <span data-ttu-id="5f382-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5f382-120">-BackupManagementType</span></span>
<span data-ttu-id="5f382-121">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="5f382-122">현재는 Add-azurevm만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f382-123">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="5f382-123">-From</span></span>
<span data-ttu-id="5f382-124">이 cmdlet이 가져오는 작업에 대 한 시간 범위의 시작을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-124">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5f382-125">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-125">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="5f382-126">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-126">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="5f382-127">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-127">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f382-128">-작업</span><span class="sxs-lookup"><span data-stu-id="5f382-128">-Job</span></span>
<span data-ttu-id="5f382-129">가져올 백업 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-129">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f382-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="5f382-130">-JobId</span></span>
<span data-ttu-id="5f382-131">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-131">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="5f382-132">ID는 **AzureRmRecoveryServicesBackupJob** 개체의 InstanceId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-132">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="5f382-133">**AzureRmRecoveryServicesBackupJob** 개체를 얻으려면 AzureRmRecoveryServicesBackupJob를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-133">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f382-134">-작업</span><span class="sxs-lookup"><span data-stu-id="5f382-134">-Operation</span></span>
<span data-ttu-id="5f382-135">이 cmdlet이 가져오는 작업의 연산을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-135">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5f382-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f382-137">백업할</span><span class="sxs-lookup"><span data-stu-id="5f382-137">Backup</span></span>
- <span data-ttu-id="5f382-138">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="5f382-138">ConfigureBackup</span></span>
- <span data-ttu-id="5f382-139">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="5f382-139">DeleteBackupData</span></span>
- <span data-ttu-id="5f382-140">등록이</span><span class="sxs-lookup"><span data-stu-id="5f382-140">Register</span></span>
- <span data-ttu-id="5f382-141">복원한</span><span class="sxs-lookup"><span data-stu-id="5f382-141">Restore</span></span>
- <span data-ttu-id="5f382-142">문서</span><span class="sxs-lookup"><span data-stu-id="5f382-142">UnProtect</span></span>
- <span data-ttu-id="5f382-143">을</span><span class="sxs-lookup"><span data-stu-id="5f382-143">Unregister</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f382-144">-상태</span><span class="sxs-lookup"><span data-stu-id="5f382-144">-Status</span></span>
<span data-ttu-id="5f382-145">이 cmdlet이 가져오는 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5f382-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f382-147">InProgress</span><span class="sxs-lookup"><span data-stu-id="5f382-147">InProgress</span></span>
- <span data-ttu-id="5f382-148">못함</span><span class="sxs-lookup"><span data-stu-id="5f382-148">Failed</span></span>
- <span data-ttu-id="5f382-149">되었습니다</span><span class="sxs-lookup"><span data-stu-id="5f382-149">Cancelled</span></span>
- <span data-ttu-id="5f382-150">...</span><span class="sxs-lookup"><span data-stu-id="5f382-150">Cancelling</span></span>
- <span data-ttu-id="5f382-151">완료</span><span class="sxs-lookup"><span data-stu-id="5f382-151">Completed</span></span>
- <span data-ttu-id="5f382-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="5f382-152">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f382-153">-To</span><span class="sxs-lookup"><span data-stu-id="5f382-153">-To</span></span>
<span data-ttu-id="5f382-154">이 cmdlet이 가져오는 작업에 대 한 시간 범위의 끝을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5f382-155">기본값은 현재 시스템 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-155">The default value is the current system time.</span></span>
<span data-ttu-id="5f382-156">이 매개 변수를 지정 하는 경우에도 *From* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-156">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="5f382-157">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-157">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f382-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f382-158">-DefaultProfile</span></span>
<span data-ttu-id="5f382-159">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f382-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f382-160">CommonParameters</span></span>
<span data-ttu-id="5f382-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f382-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f382-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f382-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f382-163">입력</span><span class="sxs-lookup"><span data-stu-id="5f382-163">INPUTS</span></span>

## <span data-ttu-id="5f382-164">출력</span><span class="sxs-lookup"><span data-stu-id="5f382-164">OUTPUTS</span></span>

### <span data-ttu-id="5f382-165">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="5f382-165">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="5f382-166">System.webserver. IList ' 1 [Microsoft Azure. Commands. e-유틸리티의 JobBase]</span><span class="sxs-lookup"><span data-stu-id="5f382-166">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="5f382-167">상속자</span><span class="sxs-lookup"><span data-stu-id="5f382-167">NOTES</span></span>

## <span data-ttu-id="5f382-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f382-168">RELATED LINKS</span></span>

[<span data-ttu-id="5f382-169">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="5f382-169">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="5f382-170">중지-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5f382-170">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="5f382-171">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5f382-171">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


