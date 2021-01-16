---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: b0709c7b839ca992d415cd5ba9fff58e769120fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368936"
---
# <span data-ttu-id="26e8e-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26e8e-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="26e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="26e8e-103">Batch 계정 또는 작업 일정에 대한 Batch 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="26e8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="26e8e-104">SYNTAX</span></span>

### <span data-ttu-id="26e8e-105">ODataFilter(기본값)</span><span class="sxs-lookup"><span data-stu-id="26e8e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26e8e-106">ID</span><span class="sxs-lookup"><span data-stu-id="26e8e-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26e8e-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="26e8e-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26e8e-108">설명</span><span class="sxs-lookup"><span data-stu-id="26e8e-108">DESCRIPTION</span></span>
<span data-ttu-id="26e8e-109">**Get-AzBatchJob** cmdlet은 *BatchAccountContext* 매개 변수로 지정된 Batch 계정에 대한 Azure Batch 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="26e8e-110">ID 매개 *변수를 사용하여* 단일 작업을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="26e8e-111">Filter 매개  변수를 사용하여 OData(Open Data Protocol) 필터와 일치하는 작업을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="26e8e-112">작업 일정 ID 또는 **PSCloudJobSchedule** 인스턴스를 제공하면 이 cmdlet은 해당 작업 일정에 대한 작업만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="26e8e-113">예제</span><span class="sxs-lookup"><span data-stu-id="26e8e-113">EXAMPLES</span></span>

### <span data-ttu-id="26e8e-114">예제 1: ID로 Batch 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="26e8e-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="26e8e-115">이 명령은 ID Job01이 있는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="26e8e-116">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="26e8e-117">예제 2: 작업 일정에 대한 모든 활성 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="26e8e-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="26e8e-118">이 명령은 ID JobSchedule27이 있는 작업 일정에 대한 활성 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="26e8e-119">예제 3: 파이프라인을 사용하여 작업 일정에 따라 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="26e8e-120">이 명령은 Get-AzBatchJobSchedule cmdlet을 사용하여 ID JobSchedule27이 있는 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="26e8e-121">이 명령은 파이프라인 연산자를 사용하여 작업 일정을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="26e8e-122">이 명령은 작업 일정에 대한 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="26e8e-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26e8e-123">PARAMETERS</span></span>

### <span data-ttu-id="26e8e-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="26e8e-124">-BatchContext</span></span>
<span data-ttu-id="26e8e-125">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="26e8e-126">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="26e8e-127">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="26e8e-128">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="26e8e-129">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="26e8e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e8e-130">-DefaultProfile</span></span>
<span data-ttu-id="26e8e-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26e8e-132">-Expand</span><span class="sxs-lookup"><span data-stu-id="26e8e-132">-Expand</span></span>
<span data-ttu-id="26e8e-133">OData(Open Data Protocol) expand 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="26e8e-134">이 매개 변수에 대한 값을 지정하여 얻을 주 엔터티의 관련 엔터티를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="26e8e-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="26e8e-135">-Filter</span></span>
<span data-ttu-id="26e8e-136">작업의 OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="26e8e-137">필터를 지정하지 않으면 이 cmdlet은 Batch 계정 또는 작업 일정에 대한 모든 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="26e8e-138">-Id</span><span class="sxs-lookup"><span data-stu-id="26e8e-138">-Id</span></span>
<span data-ttu-id="26e8e-139">이 cmdlet이 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="26e8e-140">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="26e8e-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="26e8e-141">-JobSchedule</span></span>
<span data-ttu-id="26e8e-142">작업을 포함하는 작업 일정을 나타내는 **PSCloudJobSchedule** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="26e8e-143">**PSCloudJobSchedule** 개체를 얻습니다. Get-AzBatchJobSchedule cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="26e8e-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="26e8e-144">-JobScheduleId</span></span>
<span data-ttu-id="26e8e-145">작업을 포함하는 작업 일정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="26e8e-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="26e8e-146">-MaxCount</span></span>
<span data-ttu-id="26e8e-147">반환할 작업의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="26e8e-148">0 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="26e8e-149">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="26e8e-150">-Select</span><span class="sxs-lookup"><span data-stu-id="26e8e-150">-Select</span></span>
<span data-ttu-id="26e8e-151">OData select 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="26e8e-152">이 매개 변수에 대한 값을 지정하여 모든 개체 속성이 아닌 특정 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="26e8e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e8e-153">CommonParameters</span></span>
<span data-ttu-id="26e8e-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26e8e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e8e-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26e8e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e8e-156">입력</span><span class="sxs-lookup"><span data-stu-id="26e8e-156">INPUTS</span></span>

### <span data-ttu-id="26e8e-157">System.String</span><span class="sxs-lookup"><span data-stu-id="26e8e-157">System.String</span></span>

### <span data-ttu-id="26e8e-158">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="26e8e-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="26e8e-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="26e8e-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="26e8e-160">출력</span><span class="sxs-lookup"><span data-stu-id="26e8e-160">OUTPUTS</span></span>

### <span data-ttu-id="26e8e-161">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="26e8e-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="26e8e-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26e8e-162">NOTES</span></span>

## <span data-ttu-id="26e8e-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26e8e-163">RELATED LINKS</span></span>

[<span data-ttu-id="26e8e-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26e8e-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="26e8e-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26e8e-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="26e8e-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="26e8e-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="26e8e-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="26e8e-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="26e8e-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26e8e-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="26e8e-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26e8e-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="26e8e-170">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="26e8e-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="26e8e-171">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26e8e-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)