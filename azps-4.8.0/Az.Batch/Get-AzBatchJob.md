---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: b0709c7b839ca992d415cd5ba9fff58e769120fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056556"
---
# <span data-ttu-id="d9d78-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9d78-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="d9d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d78-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d78-103">일괄 처리 계정 또는 작업 일정에 대 한 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="d9d78-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9d78-104">SYNTAX</span></span>

### <span data-ttu-id="d9d78-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="d9d78-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9d78-106">I</span><span class="sxs-lookup"><span data-stu-id="d9d78-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9d78-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="d9d78-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9d78-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d9d78-108">DESCRIPTION</span></span>
<span data-ttu-id="d9d78-109">**AzBatchJob** Cmdlet은 *batchaccountcontext* 매개 변수에서 지정 하는 일괄 처리 계정에 대 한 Azure 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="d9d78-110">*Id* 매개 변수를 사용 하 여 단일 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="d9d78-111">*Filter* 매개 변수를 사용 하 여 OData (Open Data Protocol) 필터와 일치 하는 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="d9d78-112">작업 일정 ID 또는 **Pscloudjobschedule** 인스턴스를 제공 하는 경우이 cmdlet은 해당 작업 일정에 대 한 작업만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="d9d78-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d9d78-113">EXAMPLES</span></span>

### <span data-ttu-id="d9d78-114">예제 1: ID를 기준으로 일괄 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9d78-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
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

<span data-ttu-id="d9d78-115">이 명령은 ID Job01 인 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="d9d78-116">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d9d78-117">예제 2: 작업 일정에 대 한 모든 활성 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9d78-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="d9d78-118">이 명령은 ID JobSchedule27 인 작업 일정에 대 한 활성 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="d9d78-119">예제 3: 파이프라인을 사용 하 여 작업 일정에 따라 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
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

<span data-ttu-id="d9d78-120">이 명령은 Get-AzBatchJobSchedule cmdlet을 사용 하 여 ID JobSchedule27 인 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="d9d78-121">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업 일정을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d9d78-122">명령이 해당 작업 일정에 대 한 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="d9d78-123">변수</span><span class="sxs-lookup"><span data-stu-id="d9d78-123">PARAMETERS</span></span>

### <span data-ttu-id="d9d78-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d9d78-124">-BatchContext</span></span>
<span data-ttu-id="d9d78-125">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d9d78-126">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d9d78-127">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d9d78-128">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d9d78-129">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d9d78-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d78-130">-DefaultProfile</span></span>
<span data-ttu-id="d9d78-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9d78-132">-확장</span><span class="sxs-lookup"><span data-stu-id="d9d78-132">-Expand</span></span>
<span data-ttu-id="d9d78-133">OData (Open Data Protocol) expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="d9d78-134">이 매개 변수에 대 한 값을 지정 하 여 가져올 기본 엔터티의 연결 된 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="d9d78-135">-필터</span><span class="sxs-lookup"><span data-stu-id="d9d78-135">-Filter</span></span>
<span data-ttu-id="d9d78-136">작업에 대 한 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="d9d78-137">필터를 지정 하지 않으면이 cmdlet은 일괄 처리 계정 또는 작업 일정에 대 한 모든 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="d9d78-138">-Id</span><span class="sxs-lookup"><span data-stu-id="d9d78-138">-Id</span></span>
<span data-ttu-id="d9d78-139">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="d9d78-140">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d9d78-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="d9d78-141">-JobSchedule</span></span>
<span data-ttu-id="d9d78-142">작업을 포함 하는 작업 일정을 나타내는 **Pscloudjobschedule** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="d9d78-143">**Pscloudjobschedule** 개체를 얻으려면 Get-AzBatchJobSchedule cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="d9d78-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="d9d78-144">-JobScheduleId</span></span>
<span data-ttu-id="d9d78-145">작업을 포함 하는 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="d9d78-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d9d78-146">-MaxCount</span></span>
<span data-ttu-id="d9d78-147">반환할 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="d9d78-148">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="d9d78-149">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="d9d78-150">-선택</span><span class="sxs-lookup"><span data-stu-id="d9d78-150">-Select</span></span>
<span data-ttu-id="d9d78-151">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="d9d78-152">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="d9d78-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d78-153">CommonParameters</span></span>
<span data-ttu-id="d9d78-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9d78-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d78-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9d78-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d78-156">입력</span><span class="sxs-lookup"><span data-stu-id="d9d78-156">INPUTS</span></span>

### <span data-ttu-id="d9d78-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d9d78-157">System.String</span></span>

### <span data-ttu-id="d9d78-158">Microsoft.Azure.Commands.Batch. PSCloudJobSchedule 모델</span><span class="sxs-lookup"><span data-stu-id="d9d78-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="d9d78-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d9d78-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d9d78-160">출력</span><span class="sxs-lookup"><span data-stu-id="d9d78-160">OUTPUTS</span></span>

### <span data-ttu-id="d9d78-161">Microsoft.Azure.Commands.Batch. PSCloudJob 모델</span><span class="sxs-lookup"><span data-stu-id="d9d78-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="d9d78-162">상속자</span><span class="sxs-lookup"><span data-stu-id="d9d78-162">NOTES</span></span>

## <span data-ttu-id="d9d78-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9d78-163">RELATED LINKS</span></span>

[<span data-ttu-id="d9d78-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9d78-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="d9d78-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9d78-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="d9d78-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d9d78-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d9d78-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d9d78-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="d9d78-168">새로운 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9d78-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="d9d78-169">제거-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9d78-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="d9d78-170">중지-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d9d78-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="d9d78-171">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d9d78-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
