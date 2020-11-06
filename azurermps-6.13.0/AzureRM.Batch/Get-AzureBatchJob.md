---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: 1a5f971e52da27eb2abeca02c4362eee9b9755c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531456"
---
# <span data-ttu-id="23860-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="23860-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="23860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23860-102">SYNOPSIS</span></span>
<span data-ttu-id="23860-103">일괄 처리 계정 또는 작업 일정에 대 한 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23860-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23860-104">SYNTAX</span></span>

### <span data-ttu-id="23860-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="23860-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23860-106">I</span><span class="sxs-lookup"><span data-stu-id="23860-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23860-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="23860-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23860-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23860-108">DESCRIPTION</span></span>
<span data-ttu-id="23860-109">**Get-AzureBatchJob** Cmdlet은 *batchaccountcontext* 매개 변수에 지정 된 일괄 처리 계정에 대 한 Azure 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="23860-110">*Id* 매개 변수를 사용 하 여 단일 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23860-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="23860-111">*Filter* 매개 변수를 사용 하 여 OData (Open Data Protocol) 필터와 일치 하는 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23860-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="23860-112">작업 일정 ID 또는 **Pscloudjobschedule** 인스턴스를 제공 하는 경우이 cmdlet은 해당 작업 일정에 대 한 작업만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="23860-113">예제의</span><span class="sxs-lookup"><span data-stu-id="23860-113">EXAMPLES</span></span>

### <span data-ttu-id="23860-114">예제 1: ID를 기준으로 일괄 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="23860-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="23860-115">이 명령은 ID Job01 인 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="23860-116">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="23860-117">예제 2: 작업 일정에 대 한 모든 활성 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="23860-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="23860-118">이 명령은 ID JobSchedule27 인 작업 일정에 대 한 활성 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="23860-119">예제 3: 파이프라인을 사용 하 여 작업 일정에 따라 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="23860-120">이 명령은 Get-AzureBatchJobSchedule cmdlet을 사용 하 여 ID JobSchedule27 인 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="23860-121">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업 일정을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23860-122">명령이 해당 작업 일정에 대 한 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="23860-123">변수</span><span class="sxs-lookup"><span data-stu-id="23860-123">PARAMETERS</span></span>

### <span data-ttu-id="23860-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="23860-124">-BatchContext</span></span>
<span data-ttu-id="23860-125">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="23860-126">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23860-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="23860-127">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="23860-128">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23860-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="23860-129">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23860-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23860-130">-DefaultProfile</span></span>
<span data-ttu-id="23860-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23860-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23860-132">-확장</span><span class="sxs-lookup"><span data-stu-id="23860-132">-Expand</span></span>
<span data-ttu-id="23860-133">OData (Open Data Protocol) expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="23860-134">이 매개 변수에 대 한 값을 지정 하 여 가져올 기본 엔터티의 연결 된 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23860-135">-필터</span><span class="sxs-lookup"><span data-stu-id="23860-135">-Filter</span></span>
<span data-ttu-id="23860-136">작업에 대 한 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="23860-137">필터를 지정 하지 않으면이 cmdlet은 일괄 처리 계정 또는 작업 일정에 대 한 모든 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23860-138">-Id</span><span class="sxs-lookup"><span data-stu-id="23860-138">-Id</span></span>
<span data-ttu-id="23860-139">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="23860-140">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="23860-140">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23860-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="23860-141">-JobSchedule</span></span>
<span data-ttu-id="23860-142">작업을 포함 하는 작업 일정을 나타내는 **Pscloudjobschedule** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="23860-143">**Pscloudjobschedule** 개체를 얻으려면 Get-AzureBatchJobSchedule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23860-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="23860-144">-JobScheduleId</span></span>
<span data-ttu-id="23860-145">작업을 포함 하는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23860-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="23860-146">-MaxCount</span></span>
<span data-ttu-id="23860-147">반환할 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="23860-148">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23860-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="23860-149">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="23860-149">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23860-150">-선택</span><span class="sxs-lookup"><span data-stu-id="23860-150">-Select</span></span>
<span data-ttu-id="23860-151">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="23860-152">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23860-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23860-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23860-153">CommonParameters</span></span>
<span data-ttu-id="23860-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23860-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23860-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23860-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23860-156">입력</span><span class="sxs-lookup"><span data-stu-id="23860-156">INPUTS</span></span>

### <span data-ttu-id="23860-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23860-157">System.String</span></span>

### <span data-ttu-id="23860-158">Microsoft.Azure.Commands.Batch. PSCloudJobSchedule 모델</span><span class="sxs-lookup"><span data-stu-id="23860-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="23860-159">매개 변수: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23860-159">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="23860-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="23860-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="23860-161">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23860-161">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="23860-162">출력</span><span class="sxs-lookup"><span data-stu-id="23860-162">OUTPUTS</span></span>

### <span data-ttu-id="23860-163">Microsoft.Azure.Commands.Batch. PSCloudJob 모델</span><span class="sxs-lookup"><span data-stu-id="23860-163">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="23860-164">상속자</span><span class="sxs-lookup"><span data-stu-id="23860-164">NOTES</span></span>

## <span data-ttu-id="23860-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23860-165">RELATED LINKS</span></span>

[<span data-ttu-id="23860-166">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="23860-166">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="23860-167">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="23860-167">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="23860-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="23860-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="23860-169">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="23860-169">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="23860-170">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="23860-170">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="23860-171">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="23860-171">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="23860-172">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="23860-172">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="23860-173">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="23860-173">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


