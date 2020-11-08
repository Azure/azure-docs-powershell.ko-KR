---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 4d5ec07e7a068e1ab96f485ee67db0c1dd43f388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034350"
---
# <span data-ttu-id="cc27b-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="cc27b-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="cc27b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc27b-102">SYNOPSIS</span></span>

<span data-ttu-id="cc27b-103">백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="cc27b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc27b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc27b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc27b-105">DESCRIPTION</span></span>

<span data-ttu-id="cc27b-106">**AzRecoveryServicesBackupJob** cmdlet은 특정 자격 증명 모음에 대 한 Azure 백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="cc27b-107">-VaultId 매개 변수를 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="cc27b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cc27b-108">EXAMPLES</span></span>

### <span data-ttu-id="cc27b-109">예제 1: 진행 중인 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc27b-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="cc27b-110">첫 번째 명령은 진행 중인 작업의 상태를 배열로 가져온 다음이를 $Joblist 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="cc27b-111">두 번째 명령은 $Joblist 배열의 첫 번째 항목을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="cc27b-112">예제 2: 지난 7 일 동안 실패 한 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc27b-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="cc27b-113">이 명령은 자격 증명 모음의 마지막 주부터 실패 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="cc27b-114">*From* 매개 변수는 UTC에서 지정 된 지난 7 일의 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="cc27b-115">명령에서 *To* 매개 변수에 대 한 값을 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="cc27b-116">따라서 현재 시간에 대 한 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="cc27b-117">예제 3: 진행 중인 작업 가져오기 및 완료 대기</span><span class="sxs-lookup"><span data-stu-id="cc27b-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="cc27b-118">이 스크립트는 작업이 완료 될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="cc27b-119">참고: **Wait-AzRecoveryServicesBackupJob** cmdlet을 사용 하 여 while 루프 대신 Azure Backup 작업이 완료 될 때까지 대기할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="cc27b-120">변수</span><span class="sxs-lookup"><span data-stu-id="cc27b-120">PARAMETERS</span></span>

### <span data-ttu-id="cc27b-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="cc27b-121">-BackupManagementType</span></span>

<span data-ttu-id="cc27b-122">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="cc27b-123">현재는 Add-azurevm, AzureStorage만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="cc27b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc27b-124">-DefaultProfile</span></span>

<span data-ttu-id="cc27b-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc27b-126">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="cc27b-126">-From</span></span>

<span data-ttu-id="cc27b-127">이 cmdlet이 가져오는 작업에 대 한 시간 범위의 시작을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="cc27b-128">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="cc27b-129">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="cc27b-130">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="cc27b-131">-작업</span><span class="sxs-lookup"><span data-stu-id="cc27b-131">-Job</span></span>

<span data-ttu-id="cc27b-132">가져올 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="cc27b-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="cc27b-133">-JobId</span></span>

<span data-ttu-id="cc27b-134">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="cc27b-135">이 ID는 **Microsoft Azure.** . d m.-To-Commands 기본 개체의 JobId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="cc27b-136">-작업</span><span class="sxs-lookup"><span data-stu-id="cc27b-136">-Operation</span></span>

<span data-ttu-id="cc27b-137">이 cmdlet이 가져오는 작업의 연산을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="cc27b-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc27b-139">백업할</span><span class="sxs-lookup"><span data-stu-id="cc27b-139">Backup</span></span>
- <span data-ttu-id="cc27b-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="cc27b-140">ConfigureBackup</span></span>
- <span data-ttu-id="cc27b-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="cc27b-141">DeleteBackupData</span></span>
- <span data-ttu-id="cc27b-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="cc27b-142">DisableBackup</span></span>
- <span data-ttu-id="cc27b-143">복원한</span><span class="sxs-lookup"><span data-stu-id="cc27b-143">Restore</span></span>

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

### <span data-ttu-id="cc27b-144">-상태</span><span class="sxs-lookup"><span data-stu-id="cc27b-144">-Status</span></span>

<span data-ttu-id="cc27b-145">이 cmdlet이 가져오는 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="cc27b-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc27b-147">InProgress</span><span class="sxs-lookup"><span data-stu-id="cc27b-147">InProgress</span></span>
- <span data-ttu-id="cc27b-148">못함</span><span class="sxs-lookup"><span data-stu-id="cc27b-148">Failed</span></span>
- <span data-ttu-id="cc27b-149">되었습니다</span><span class="sxs-lookup"><span data-stu-id="cc27b-149">Cancelled</span></span>
- <span data-ttu-id="cc27b-150">...</span><span class="sxs-lookup"><span data-stu-id="cc27b-150">Cancelling</span></span>
- <span data-ttu-id="cc27b-151">완료</span><span class="sxs-lookup"><span data-stu-id="cc27b-151">Completed</span></span>
- <span data-ttu-id="cc27b-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="cc27b-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="cc27b-153">-To</span><span class="sxs-lookup"><span data-stu-id="cc27b-153">-To</span></span>

<span data-ttu-id="cc27b-154">이 cmdlet이 가져오는 작업에 대 한 시간 범위의 끝을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="cc27b-155">기본값은 현재 시스템 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-155">The default value is the current system time.</span></span>
<span data-ttu-id="cc27b-156">이 매개 변수를 지정 하는 경우 **-From** 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="cc27b-157">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="cc27b-158">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cc27b-158">-VaultId</span></span>

<span data-ttu-id="cc27b-159">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cc27b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc27b-160">CommonParameters</span></span>
<span data-ttu-id="cc27b-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc27b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc27b-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cc27b-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc27b-163">입력</span><span class="sxs-lookup"><span data-stu-id="cc27b-163">INPUTS</span></span>

### <span data-ttu-id="cc27b-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cc27b-164">System.String</span></span>

## <span data-ttu-id="cc27b-165">출력</span><span class="sxs-lookup"><span data-stu-id="cc27b-165">OUTPUTS</span></span>

### <span data-ttu-id="cc27b-166">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="cc27b-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="cc27b-167">상속자</span><span class="sxs-lookup"><span data-stu-id="cc27b-167">NOTES</span></span>

## <span data-ttu-id="cc27b-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc27b-168">RELATED LINKS</span></span>

[<span data-ttu-id="cc27b-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="cc27b-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="cc27b-170">중지-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="cc27b-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="cc27b-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="cc27b-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
