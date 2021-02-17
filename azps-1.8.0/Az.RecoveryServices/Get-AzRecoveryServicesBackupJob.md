---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399824"
---
# <span data-ttu-id="cbdca-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="cbdca-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="cbdca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbdca-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdca-103">Backup 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="cbdca-104">구문</span><span class="sxs-lookup"><span data-stu-id="cbdca-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbdca-105">설명</span><span class="sxs-lookup"><span data-stu-id="cbdca-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdca-106">**Get-AzRecoveryServicesBackupJob** cmdlet은 특정 자격 증명 모음에 대한 Azure Backup 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="cbdca-107">현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="cbdca-108">예제</span><span class="sxs-lookup"><span data-stu-id="cbdca-108">EXAMPLES</span></span>

### <span data-ttu-id="cbdca-109">예제 1: 진행 중 작업 모두를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="cbdca-110">첫 번째 명령은 진행 중 작업의 상태를 배열로 하여 $Joblist 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="cbdca-111">두 번째 명령은 배열의 첫 번째 $Joblist 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="cbdca-112">예제 2: 지난 7일 동안 실패한 모든 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="cbdca-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="cbdca-113">이 명령은 자격 증명 모음의 지난 주에서 실패한 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="cbdca-114">From  매개 변수는 과거 7일의 시간을 UTC로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="cbdca-115">이 명령은 To 매개 변수에 대한 값을 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="cbdca-116">따라서 현재 시간의 기본값을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="cbdca-117">예제 3: 진행 중 작업 및 완료 대기</span><span class="sxs-lookup"><span data-stu-id="cbdca-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="cbdca-118">이 스크립트는 작업이 완료될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="cbdca-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbdca-119">PARAMETERS</span></span>

### <span data-ttu-id="cbdca-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="cbdca-120">-BackupManagementType</span></span>
<span data-ttu-id="cbdca-121">Backup 관리 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="cbdca-122">현재 AzureVM, AzureStorage만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdca-123">-DefaultProfile</span></span>
<span data-ttu-id="cbdca-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbdca-125">-From</span><span class="sxs-lookup"><span data-stu-id="cbdca-125">-From</span></span>
<span data-ttu-id="cbdca-126">이 cmdlet에서 얻을 작업의 시간 범위의 시작을 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="cbdca-127">**DateTime 개체를** 얻습니다. Get-Date cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="cbdca-128">**DateTime** 개체에 대한 자세한 내용은 `Get-Help Get-Date` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="cbdca-129">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="cbdca-130">-Job</span><span class="sxs-lookup"><span data-stu-id="cbdca-130">-Job</span></span>
<span data-ttu-id="cbdca-131">얻을 Backup 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="cbdca-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="cbdca-132">-JobId</span></span>
<span data-ttu-id="cbdca-133">이 cmdlet이 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="cbdca-134">ID는 **AzureRmRecoveryServicesBackupJob** 개체의 InstanceId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="cbdca-135">**AzureRmRecoveryServicesBackupJob** 개체를 얻습니다. Get-AzRecoveryServicesBackupJob을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="cbdca-136">-Operation</span><span class="sxs-lookup"><span data-stu-id="cbdca-136">-Operation</span></span>
<span data-ttu-id="cbdca-137">이 cmdlet에서 얻을 작업의 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="cbdca-138">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="cbdca-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cbdca-139">Backup</span><span class="sxs-lookup"><span data-stu-id="cbdca-139">Backup</span></span>
- <span data-ttu-id="cbdca-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="cbdca-140">ConfigureBackup</span></span>
- <span data-ttu-id="cbdca-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="cbdca-141">DeleteBackupData</span></span>
- <span data-ttu-id="cbdca-142">등록</span><span class="sxs-lookup"><span data-stu-id="cbdca-142">Register</span></span>
- <span data-ttu-id="cbdca-143">복원</span><span class="sxs-lookup"><span data-stu-id="cbdca-143">Restore</span></span>
- <span data-ttu-id="cbdca-144">UnProtect</span><span class="sxs-lookup"><span data-stu-id="cbdca-144">UnProtect</span></span>
- <span data-ttu-id="cbdca-145">등록을 등록하지 않은 경우</span><span class="sxs-lookup"><span data-stu-id="cbdca-145">Unregister</span></span>

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

### <span data-ttu-id="cbdca-146">-Status</span><span class="sxs-lookup"><span data-stu-id="cbdca-146">-Status</span></span>
<span data-ttu-id="cbdca-147">이 cmdlet이 얻을 작업의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="cbdca-148">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="cbdca-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cbdca-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="cbdca-149">InProgress</span></span>
- <span data-ttu-id="cbdca-150">실패</span><span class="sxs-lookup"><span data-stu-id="cbdca-150">Failed</span></span>
- <span data-ttu-id="cbdca-151">Cancelled</span><span class="sxs-lookup"><span data-stu-id="cbdca-151">Cancelled</span></span>
- <span data-ttu-id="cbdca-152">취소</span><span class="sxs-lookup"><span data-stu-id="cbdca-152">Cancelling</span></span>
- <span data-ttu-id="cbdca-153">완료</span><span class="sxs-lookup"><span data-stu-id="cbdca-153">Completed</span></span>
- <span data-ttu-id="cbdca-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="cbdca-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="cbdca-155">-To</span><span class="sxs-lookup"><span data-stu-id="cbdca-155">-To</span></span>
<span data-ttu-id="cbdca-156">이 cmdlet에서 얻을 작업의 시간 범위의 끝을 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="cbdca-157">기본값은 현재 시스템 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-157">The default value is the current system time.</span></span>
<span data-ttu-id="cbdca-158">이 매개 변수를 지정하는 경우 From 매개 변수도 *지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="cbdca-159">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="cbdca-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cbdca-160">-VaultId</span></span>
<span data-ttu-id="cbdca-161">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-161">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbdca-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdca-162">CommonParameters</span></span>
<span data-ttu-id="cbdca-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdca-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdca-164">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cbdca-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdca-165">입력</span><span class="sxs-lookup"><span data-stu-id="cbdca-165">INPUTS</span></span>

### <span data-ttu-id="cbdca-166">System.String</span><span class="sxs-lookup"><span data-stu-id="cbdca-166">System.String</span></span>

## <span data-ttu-id="cbdca-167">출력</span><span class="sxs-lookup"><span data-stu-id="cbdca-167">OUTPUTS</span></span>

### <span data-ttu-id="cbdca-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="cbdca-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="cbdca-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cbdca-169">NOTES</span></span>

## <span data-ttu-id="cbdca-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbdca-170">RELATED LINKS</span></span>


[<span data-ttu-id="cbdca-171">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="cbdca-171">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="cbdca-172">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="cbdca-172">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


