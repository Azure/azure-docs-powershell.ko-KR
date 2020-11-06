---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530810"
---
# <span data-ttu-id="730cd-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="730cd-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="730cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="730cd-102">SYNOPSIS</span></span>
<span data-ttu-id="730cd-103">일괄 처리 계정 또는 작업 일정에 대 한 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="730cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="730cd-104">SYNTAX</span></span>

### <span data-ttu-id="730cd-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="730cd-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="730cd-106">I</span><span class="sxs-lookup"><span data-stu-id="730cd-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730cd-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="730cd-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="730cd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="730cd-108">DESCRIPTION</span></span>
<span data-ttu-id="730cd-109">**Get-AzureBatchJob** Cmdlet은 *batchaccountcontext* 매개 변수에 지정 된 일괄 처리 계정에 대 한 Azure 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="730cd-110">*Id* 매개 변수를 사용 하 여 단일 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="730cd-111">*Filter* 매개 변수를 사용 하 여 OData (Open Data Protocol) 필터와 일치 하는 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="730cd-112">작업 일정 ID 또는 **Pscloudjobschedule** 인스턴스를 제공 하는 경우이 cmdlet은 해당 작업 일정에 대 한 작업만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="730cd-113">예제의</span><span class="sxs-lookup"><span data-stu-id="730cd-113">EXAMPLES</span></span>

### <span data-ttu-id="730cd-114">예제 1: ID를 기준으로 일괄 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="730cd-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="730cd-115">이 명령은 ID Job01 인 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="730cd-116">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="730cd-117">예제 2: 작업 일정에 대 한 모든 활성 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="730cd-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="730cd-118">이 명령은 ID JobSchedule27 인 작업 일정에 대 한 활성 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="730cd-119">예제 3: 파이프라인을 사용 하 여 작업 일정에 따라 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="730cd-120">이 명령은 Get-AzureBatchJobSchedule cmdlet을 사용 하 여 ID JobSchedule27 인 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="730cd-121">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업 일정을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="730cd-122">명령이 해당 작업 일정에 대 한 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="730cd-123">변수</span><span class="sxs-lookup"><span data-stu-id="730cd-123">PARAMETERS</span></span>

### <span data-ttu-id="730cd-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="730cd-124">-BatchContext</span></span>
<span data-ttu-id="730cd-125">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="730cd-126">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="730cd-127">-확장</span><span class="sxs-lookup"><span data-stu-id="730cd-127">-Expand</span></span>
<span data-ttu-id="730cd-128">OData (Open Data Protocol) expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="730cd-129">이 매개 변수에 대 한 값을 지정 하 여 가져올 기본 엔터티의 연결 된 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="730cd-130">-필터</span><span class="sxs-lookup"><span data-stu-id="730cd-130">-Filter</span></span>
<span data-ttu-id="730cd-131">작업에 대 한 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="730cd-132">필터를 지정 하지 않으면이 cmdlet은 일괄 처리 계정 또는 작업 일정에 대 한 모든 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="730cd-133">-Id</span><span class="sxs-lookup"><span data-stu-id="730cd-133">-Id</span></span>
<span data-ttu-id="730cd-134">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="730cd-135">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="730cd-136">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="730cd-136">-JobSchedule</span></span>
<span data-ttu-id="730cd-137">작업을 포함 하는 작업 일정을 나타내는 **Pscloudjobschedule** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="730cd-138">**Pscloudjobschedule** 개체를 얻으려면 Get-AzureBatchJobSchedule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="730cd-139">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="730cd-139">-JobScheduleId</span></span>
<span data-ttu-id="730cd-140">작업을 포함 하는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="730cd-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="730cd-141">-MaxCount</span></span>
<span data-ttu-id="730cd-142">반환할 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="730cd-143">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="730cd-144">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-144">The default value is 1000.</span></span>

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

### <span data-ttu-id="730cd-145">-선택</span><span class="sxs-lookup"><span data-stu-id="730cd-145">-Select</span></span>
<span data-ttu-id="730cd-146">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="730cd-147">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="730cd-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="730cd-148">-DefaultProfile</span></span>
<span data-ttu-id="730cd-149">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="730cd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="730cd-150">CommonParameters</span></span>
<span data-ttu-id="730cd-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="730cd-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="730cd-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="730cd-153">입력</span><span class="sxs-lookup"><span data-stu-id="730cd-153">INPUTS</span></span>

### <span data-ttu-id="730cd-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="730cd-154">BatchAccountContext</span></span>
<span data-ttu-id="730cd-155">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="730cd-156">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="730cd-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="730cd-157">' JobSchedule ' 매개 변수는 파이프라인에서 ' PSCloudJobSchedule ' 형식의 값을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="730cd-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="730cd-158">출력</span><span class="sxs-lookup"><span data-stu-id="730cd-158">OUTPUTS</span></span>

### <span data-ttu-id="730cd-159">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="730cd-159">PSCloudJob</span></span>

## <span data-ttu-id="730cd-160">상속자</span><span class="sxs-lookup"><span data-stu-id="730cd-160">NOTES</span></span>

## <span data-ttu-id="730cd-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="730cd-161">RELATED LINKS</span></span>

[<span data-ttu-id="730cd-162">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="730cd-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="730cd-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="730cd-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="730cd-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="730cd-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="730cd-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="730cd-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="730cd-166">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="730cd-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="730cd-167">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="730cd-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="730cd-168">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="730cd-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="730cd-169">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="730cd-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


