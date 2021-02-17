---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc8b9017180c431caabc31970877d9fe0e4c346a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183921"
---
# <span data-ttu-id="29d62-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="29d62-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="29d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d62-102">SYNOPSIS</span></span>

<span data-ttu-id="29d62-103">Backup 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="29d62-104">구문</span><span class="sxs-lookup"><span data-stu-id="29d62-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29d62-105">설명</span><span class="sxs-lookup"><span data-stu-id="29d62-105">DESCRIPTION</span></span>

<span data-ttu-id="29d62-106">**Get-AzRecoveryServicesBackupJob** cmdlet은 특정 자격 증명 모음에 대한 Azure Backup 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="29d62-107">-VaultId 매개 변수를 사용하여 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="29d62-108">예제</span><span class="sxs-lookup"><span data-stu-id="29d62-108">EXAMPLES</span></span>

### <span data-ttu-id="29d62-109">예제 1: 진행 중 작업 모두를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="29d62-110">첫 번째 명령은 진행 중 작업의 상태를 배열로 하여 $Joblist 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="29d62-111">두 번째 명령은 배열의 첫 번째 $Joblist 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="29d62-112">예제 2: 지난 7일 동안 실패한 모든 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="29d62-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="29d62-113">이 명령은 자격 증명 모음의 지난 주에서 실패한 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="29d62-114">From  매개 변수는 과거 7일 동안의 시간을 UTC로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="29d62-115">이 명령은 To 매개 변수에 대한 값을 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="29d62-116">따라서 현재 시간의 기본값을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="29d62-117">예제 3: 진행 중 작업 및 완료 대기</span><span class="sxs-lookup"><span data-stu-id="29d62-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="29d62-118">이 스크립트는 작업이 완료될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="29d62-119">참고: **Wait-AzRecoveryServicesBackupJob** cmdlet을 사용하여 While 루프 대신 Azure Backup 작업이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="29d62-120">예제 4: 성공적으로 완료된 지난 2일 동안 모든 AzureVM 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="29d62-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="29d62-121">첫 번째 cmdlet은 자격 증명 모음 개체를 페치합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="29d62-122">두 번째 cmdlet은 지난 2일 동안 완료된 모든 AzureVM 작업을 해당 자격 증명 모음에 $jobs.</span><span class="sxs-lookup"><span data-stu-id="29d62-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="29d62-123">MAB 에이전트 작업을 페치하기 위해 BackupManagementType 매개 변수 값을 MAB로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="29d62-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29d62-124">PARAMETERS</span></span>

### <span data-ttu-id="29d62-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="29d62-125">-BackupManagementType</span></span>

<span data-ttu-id="29d62-126">보호되는 리소스의 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-126">The class of resources being protected.</span></span> <span data-ttu-id="29d62-127">현재 이 cmdlet에 지원되는 값은 AzureVM, AzureStorage, AzureWorkload, MAB입니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d62-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d62-128">-DefaultProfile</span></span>

<span data-ttu-id="29d62-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29d62-130">-From</span><span class="sxs-lookup"><span data-stu-id="29d62-130">-From</span></span>

<span data-ttu-id="29d62-131">이 cmdlet에서 얻을 작업의 시간 범위의 시작을 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="29d62-132">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="29d62-133">**DateTime** 개체에 대한 자세한 내용은 .를 입력합니다. `Get-Help Get-Date`</span><span class="sxs-lookup"><span data-stu-id="29d62-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="29d62-134">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="29d62-135">-Job</span><span class="sxs-lookup"><span data-stu-id="29d62-135">-Job</span></span>

<span data-ttu-id="29d62-136">얻을 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="29d62-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="29d62-137">-JobId</span></span>

<span data-ttu-id="29d62-138">이 cmdlet이 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="29d62-139">ID는 **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** 개체의 JobId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="29d62-140">-Operation</span><span class="sxs-lookup"><span data-stu-id="29d62-140">-Operation</span></span>

<span data-ttu-id="29d62-141">이 cmdlet에서 얻을 작업의 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="29d62-142">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="29d62-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29d62-143">Backup</span><span class="sxs-lookup"><span data-stu-id="29d62-143">Backup</span></span>
- <span data-ttu-id="29d62-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="29d62-144">ConfigureBackup</span></span>
- <span data-ttu-id="29d62-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="29d62-145">DeleteBackupData</span></span>
- <span data-ttu-id="29d62-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="29d62-146">DisableBackup</span></span>
- <span data-ttu-id="29d62-147">복원</span><span class="sxs-lookup"><span data-stu-id="29d62-147">Restore</span></span>
- <span data-ttu-id="29d62-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="29d62-148">BackupDataMove</span></span>

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

### <span data-ttu-id="29d62-149">-Status</span><span class="sxs-lookup"><span data-stu-id="29d62-149">-Status</span></span>

<span data-ttu-id="29d62-150">이 cmdlet이 얻을 작업의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="29d62-151">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="29d62-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29d62-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="29d62-152">InProgress</span></span>
- <span data-ttu-id="29d62-153">실패</span><span class="sxs-lookup"><span data-stu-id="29d62-153">Failed</span></span>
- <span data-ttu-id="29d62-154">Cancelled</span><span class="sxs-lookup"><span data-stu-id="29d62-154">Cancelled</span></span>
- <span data-ttu-id="29d62-155">취소</span><span class="sxs-lookup"><span data-stu-id="29d62-155">Cancelling</span></span>
- <span data-ttu-id="29d62-156">완료</span><span class="sxs-lookup"><span data-stu-id="29d62-156">Completed</span></span>
- <span data-ttu-id="29d62-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="29d62-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="29d62-158">-To</span><span class="sxs-lookup"><span data-stu-id="29d62-158">-To</span></span>

<span data-ttu-id="29d62-159">이 cmdlet에서 얻을 작업의 시간 범위의 끝을 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="29d62-160">기본값은 현재 시스템 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-160">The default value is the current system time.</span></span>
<span data-ttu-id="29d62-161">이 매개 변수를 지정하는 경우 -From 매개 **변수도 지정해야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="29d62-162">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="29d62-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="29d62-163">-VaultId</span></span>

<span data-ttu-id="29d62-164">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="29d62-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d62-165">CommonParameters</span></span>
<span data-ttu-id="29d62-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29d62-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d62-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29d62-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d62-168">입력</span><span class="sxs-lookup"><span data-stu-id="29d62-168">INPUTS</span></span>

### <span data-ttu-id="29d62-169">System.String</span><span class="sxs-lookup"><span data-stu-id="29d62-169">System.String</span></span>

## <span data-ttu-id="29d62-170">출력</span><span class="sxs-lookup"><span data-stu-id="29d62-170">OUTPUTS</span></span>

### <span data-ttu-id="29d62-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="29d62-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="29d62-172">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29d62-172">NOTES</span></span>

## <span data-ttu-id="29d62-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29d62-173">RELATED LINKS</span></span>

[<span data-ttu-id="29d62-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="29d62-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="29d62-175">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="29d62-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="29d62-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="29d62-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
