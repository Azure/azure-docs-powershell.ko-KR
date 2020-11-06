---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529028"
---
# <span data-ttu-id="35d8a-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="35d8a-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="35d8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="35d8a-103">백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35d8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35d8a-104">SYNTAX</span></span>

### <span data-ttu-id="35d8a-105">FiltersSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="35d8a-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35d8a-106">Joblistfilter</span><span class="sxs-lookup"><span data-stu-id="35d8a-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35d8a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35d8a-107">DESCRIPTION</span></span>
<span data-ttu-id="35d8a-108">**AzureRmBackupJob** cmdlet은 특정 자격 증명 모음에 대 한 Azure 백업 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="35d8a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35d8a-109">EXAMPLES</span></span>

### <span data-ttu-id="35d8a-110">예제 1: 백업 자격 증명 모음의 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="35d8a-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="35d8a-111">첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="35d8a-112">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="35d8a-113">두 번째 명령은 $Vault의 자격 증명 모음에 대 한 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="35d8a-114">예제 2: 완료 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="35d8a-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="35d8a-115">이 명령은 $Vault의 자격 증명 모음에서 완료 된 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="35d8a-116">예제 3: 지난 주에 실패 한 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="35d8a-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="35d8a-117">이 명령은 $Vault의 자격 증명 모음에서 지난 주에 실패 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="35d8a-118">*From* 매개 변수는 지난 7 일의 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="35d8a-119">명령에서 *To* 매개 변수에 대 한 값을 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="35d8a-120">따라서 현재 시간에 대 한 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="35d8a-121">예제 4: 완료 되는 진행 중인 작업에 대 한 백업 폴링</span><span class="sxs-lookup"><span data-stu-id="35d8a-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="35d8a-122">이 스크립트는 작업이 완료 될 때까지 현재 진행 중인 첫 번째 작업을 폴링합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="35d8a-123">스크립트의 첫 번째 줄은 진행 중인 $Vault의 모든 작업을 가져온 다음 해당 작업을 $Jobs 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="35d8a-124">두 번째 줄은 $Jobs 배열의 첫 번째 작업을 $Job 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="35d8a-125">세 번째 줄은 작업이 완료 될 때까지 작업의 현재 상태를 확인 하는 **while** 루프를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="35d8a-126">**While** 키워드에 대 한 자세한 내용은를 입력 `Get-Help about_While` 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="35d8a-127">**While** 루프는 콘솔에 메시지를 기록 하 고 10 초 동안 대기한 다음 $Job 변수를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="35d8a-128">이 스크립트는 기존 $Job 값을 사용 하 여 $Job 변수를 업데이트 하 고 현재 cmdlet을 통해 작업의 현재 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="35d8a-129">Windows PowerShell cmdlet에 대 한 자세한 내용은 및를 입력 `Get-Help Write-Host` `Get-Help Start-Sleep` 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="35d8a-130">스크립트의 마지막 줄에서 스크립트가 완료 되었음을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="35d8a-131">변수</span><span class="sxs-lookup"><span data-stu-id="35d8a-131">PARAMETERS</span></span>

### <span data-ttu-id="35d8a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d8a-132">-DefaultProfile</span></span>
<span data-ttu-id="35d8a-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="35d8a-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35d8a-134">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="35d8a-134">-From</span></span>
<span data-ttu-id="35d8a-135">이 cmdlet이 가져오는 작업에 대 한 시간 범위의 시작을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="35d8a-136">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="35d8a-137">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8a-138">-작업</span><span class="sxs-lookup"><span data-stu-id="35d8a-138">-Job</span></span>
<span data-ttu-id="35d8a-139">이 cmdlet이 가져오는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="35d8a-140">**AzureRmBackupJob** 개체를 가져오려면 Get-AzureRmBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8a-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="35d8a-141">-JobId</span></span>
<span data-ttu-id="35d8a-142">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="35d8a-143">ID는 **AzureRmBackupJob** 개체의 **InstanceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="35d8a-144">**AzureRmBackupJob** 개체를 얻으려면 AzureRmBackupJob를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8a-145">-작업</span><span class="sxs-lookup"><span data-stu-id="35d8a-145">-Operation</span></span>
<span data-ttu-id="35d8a-146">이 cmdlet이 가져오는 작업의 연산을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="35d8a-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35d8a-148">백업할</span><span class="sxs-lookup"><span data-stu-id="35d8a-148">Backup</span></span> 
- <span data-ttu-id="35d8a-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="35d8a-149">ConfigureBackup</span></span> 
- <span data-ttu-id="35d8a-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="35d8a-150">DeleteBackupData</span></span> 
- <span data-ttu-id="35d8a-151">등록이</span><span class="sxs-lookup"><span data-stu-id="35d8a-151">Register</span></span> 
- <span data-ttu-id="35d8a-152">복원한</span><span class="sxs-lookup"><span data-stu-id="35d8a-152">Restore</span></span> 
- <span data-ttu-id="35d8a-153">문서</span><span class="sxs-lookup"><span data-stu-id="35d8a-153">UnProtect</span></span> 
- <span data-ttu-id="35d8a-154">을</span><span class="sxs-lookup"><span data-stu-id="35d8a-154">Unregister</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8a-155">-상태</span><span class="sxs-lookup"><span data-stu-id="35d8a-155">-Status</span></span>
<span data-ttu-id="35d8a-156">이 cmdlet이 가져오는 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="35d8a-157">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35d8a-158">InProgress</span><span class="sxs-lookup"><span data-stu-id="35d8a-158">InProgress</span></span>
- <span data-ttu-id="35d8a-159">못함</span><span class="sxs-lookup"><span data-stu-id="35d8a-159">Failed</span></span>
- <span data-ttu-id="35d8a-160">되었습니다</span><span class="sxs-lookup"><span data-stu-id="35d8a-160">Cancelled</span></span>
- <span data-ttu-id="35d8a-161">...</span><span class="sxs-lookup"><span data-stu-id="35d8a-161">Cancelling</span></span>
- <span data-ttu-id="35d8a-162">완료</span><span class="sxs-lookup"><span data-stu-id="35d8a-162">Completed</span></span>
- <span data-ttu-id="35d8a-163">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="35d8a-163">CompletedWithWarnings</span></span> 

<span data-ttu-id="35d8a-164">이 매개 변수를 지정 하 여 진행 중인 모든 작업 또는 실패 한 모든 작업을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-164">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8a-165">-To</span><span class="sxs-lookup"><span data-stu-id="35d8a-165">-To</span></span>
<span data-ttu-id="35d8a-166">이 cmdlet이 가져오는 작업에 대 한 시간 범위의 끝을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-166">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="35d8a-167">기본값은 현재 시스템 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-167">The default value is the current system time.</span></span>
<span data-ttu-id="35d8a-168">이 매개 변수를 지정 하는 경우에도 *From* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-168">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8a-169">-Type</span><span class="sxs-lookup"><span data-stu-id="35d8a-169">-Type</span></span>
<span data-ttu-id="35d8a-170">이 cmdlet이 백업 작업을 가져오는 컨테이너 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-170">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="35d8a-171">현재만 지원 되는 값은 Add-azurevm입니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-171">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d8a-172">-저장실</span><span class="sxs-lookup"><span data-stu-id="35d8a-172">-Vault</span></span>
<span data-ttu-id="35d8a-173">이 cmdlet이 작업을 가져오는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-173">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="35d8a-174">**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-174">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35d8a-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d8a-175">CommonParameters</span></span>
<span data-ttu-id="35d8a-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d8a-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d8a-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d8a-178">입력</span><span class="sxs-lookup"><span data-stu-id="35d8a-178">INPUTS</span></span>

### <span data-ttu-id="35d8a-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="35d8a-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="35d8a-180">출력</span><span class="sxs-lookup"><span data-stu-id="35d8a-180">OUTPUTS</span></span>

### <span data-ttu-id="35d8a-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="35d8a-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="35d8a-182">이 cmdlet은 하나 이상의 백업 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d8a-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="35d8a-183">상속자</span><span class="sxs-lookup"><span data-stu-id="35d8a-183">NOTES</span></span>
* <span data-ttu-id="35d8a-184">않아야</span><span class="sxs-lookup"><span data-stu-id="35d8a-184">None</span></span>

## <span data-ttu-id="35d8a-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35d8a-185">RELATED LINKS</span></span>

[<span data-ttu-id="35d8a-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="35d8a-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="35d8a-187">중지-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="35d8a-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="35d8a-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="35d8a-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


