---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 5e6555095563fd5c0589835b28ad293f395fffaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526720"
---
# <span data-ttu-id="29a9b-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="29a9b-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="29a9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="29a9b-103">백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29a9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29a9b-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29a9b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="29a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="29a9b-106">**AzureRmRecoveryServicesBackupJob** cmdlet은 특정 자격 증명 모음에 대 한 Azure 백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="29a9b-107">현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="29a9b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="29a9b-108">EXAMPLES</span></span>

### <span data-ttu-id="29a9b-109">예제 1: 진행 중인 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="29a9b-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="29a9b-110">첫 번째 명령은 진행 중인 작업의 상태를 배열로 가져온 다음이를 $Joblist 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="29a9b-111">두 번째 명령은 $Joblist 배열의 첫 번째 항목을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="29a9b-112">예제 2: 지난 7 일 동안 실패 한 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="29a9b-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="29a9b-113">이 명령은 자격 증명 모음의 마지막 주부터 실패 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="29a9b-114">*From* 매개 변수는 UTC에서 지정 된 지난 7 일의 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="29a9b-115">명령에서 *To* 매개 변수에 대 한 값을 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="29a9b-116">따라서 현재 시간에 대 한 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="29a9b-117">예제 3: 진행 중인 작업 가져오기 및 완료 대기</span><span class="sxs-lookup"><span data-stu-id="29a9b-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="29a9b-118">이 스크립트는 작업이 완료 될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="29a9b-119">변수</span><span class="sxs-lookup"><span data-stu-id="29a9b-119">PARAMETERS</span></span>

### <span data-ttu-id="29a9b-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="29a9b-120">-BackupManagementType</span></span>
<span data-ttu-id="29a9b-121">백업 관리 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="29a9b-122">현재는 Add-azurevm만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a9b-123">-DefaultProfile</span></span>
<span data-ttu-id="29a9b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9b-125">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="29a9b-125">-From</span></span>
<span data-ttu-id="29a9b-126">이 cmdlet이 가져오는 작업에 대 한 시간 범위의 시작을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="29a9b-127">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="29a9b-128">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="29a9b-129">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-129">Use UTC format for dates.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9b-130">-작업</span><span class="sxs-lookup"><span data-stu-id="29a9b-130">-Job</span></span>
<span data-ttu-id="29a9b-131">가져올 백업 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-131">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9b-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="29a9b-132">-JobId</span></span>
<span data-ttu-id="29a9b-133">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="29a9b-134">ID는 **AzureRmRecoveryServicesBackupJob** 개체의 InstanceId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="29a9b-135">**AzureRmRecoveryServicesBackupJob** 개체를 얻으려면 AzureRmRecoveryServicesBackupJob를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9b-136">-작업</span><span class="sxs-lookup"><span data-stu-id="29a9b-136">-Operation</span></span>
<span data-ttu-id="29a9b-137">이 cmdlet이 가져오는 작업의 연산을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="29a9b-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29a9b-139">백업할</span><span class="sxs-lookup"><span data-stu-id="29a9b-139">Backup</span></span>
- <span data-ttu-id="29a9b-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="29a9b-140">ConfigureBackup</span></span>
- <span data-ttu-id="29a9b-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="29a9b-141">DeleteBackupData</span></span>
- <span data-ttu-id="29a9b-142">등록이</span><span class="sxs-lookup"><span data-stu-id="29a9b-142">Register</span></span>
- <span data-ttu-id="29a9b-143">복원한</span><span class="sxs-lookup"><span data-stu-id="29a9b-143">Restore</span></span>
- <span data-ttu-id="29a9b-144">문서</span><span class="sxs-lookup"><span data-stu-id="29a9b-144">UnProtect</span></span>
- <span data-ttu-id="29a9b-145">을</span><span class="sxs-lookup"><span data-stu-id="29a9b-145">Unregister</span></span>

```yaml
Type: JobOperation
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9b-146">-상태</span><span class="sxs-lookup"><span data-stu-id="29a9b-146">-Status</span></span>
<span data-ttu-id="29a9b-147">이 cmdlet이 가져오는 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="29a9b-148">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29a9b-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="29a9b-149">InProgress</span></span>
- <span data-ttu-id="29a9b-150">못함</span><span class="sxs-lookup"><span data-stu-id="29a9b-150">Failed</span></span>
- <span data-ttu-id="29a9b-151">되었습니다</span><span class="sxs-lookup"><span data-stu-id="29a9b-151">Cancelled</span></span>
- <span data-ttu-id="29a9b-152">...</span><span class="sxs-lookup"><span data-stu-id="29a9b-152">Cancelling</span></span>
- <span data-ttu-id="29a9b-153">완료</span><span class="sxs-lookup"><span data-stu-id="29a9b-153">Completed</span></span>
- <span data-ttu-id="29a9b-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="29a9b-154">CompletedWithWarnings</span></span>

```yaml
Type: JobStatus
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9b-155">-To</span><span class="sxs-lookup"><span data-stu-id="29a9b-155">-To</span></span>
<span data-ttu-id="29a9b-156">이 cmdlet이 가져오는 작업에 대 한 시간 범위의 끝을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="29a9b-157">기본값은 현재 시스템 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-157">The default value is the current system time.</span></span>
<span data-ttu-id="29a9b-158">이 매개 변수를 지정 하는 경우에도 *From* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="29a9b-159">날짜에 UTC 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-159">Use UTC format for dates.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a9b-160">CommonParameters</span></span>
<span data-ttu-id="29a9b-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a9b-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a9b-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a9b-163">입력</span><span class="sxs-lookup"><span data-stu-id="29a9b-163">INPUTS</span></span>

### <span data-ttu-id="29a9b-164">않아야</span><span class="sxs-lookup"><span data-stu-id="29a9b-164">None</span></span>
<span data-ttu-id="29a9b-165">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29a9b-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29a9b-166">출력</span><span class="sxs-lookup"><span data-stu-id="29a9b-166">OUTPUTS</span></span>

### <span data-ttu-id="29a9b-167">Microsoft Azure.. i m.. i a m.</span><span class="sxs-lookup"><span data-stu-id="29a9b-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="29a9b-168">System.webserver. IList ' 1 [Microsoft Azure. Commands. e-유틸리티의 JobBase]</span><span class="sxs-lookup"><span data-stu-id="29a9b-168">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="29a9b-169">상속자</span><span class="sxs-lookup"><span data-stu-id="29a9b-169">NOTES</span></span>

## <span data-ttu-id="29a9b-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29a9b-170">RELATED LINKS</span></span>

[<span data-ttu-id="29a9b-171">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="29a9b-171">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="29a9b-172">중지-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="29a9b-172">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="29a9b-173">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="29a9b-173">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


