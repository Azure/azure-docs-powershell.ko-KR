---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: b16939cdce5a4be471e1ae8133271349884e63a7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880249"
---
# <span data-ttu-id="6b77e-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b77e-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="6b77e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b77e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b77e-103">작업에 대 한 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="6b77e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b77e-104">SYNTAX</span></span>

### <span data-ttu-id="6b77e-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b77e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b77e-106">I</span><span class="sxs-lookup"><span data-stu-id="6b77e-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b77e-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="6b77e-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b77e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6b77e-108">DESCRIPTION</span></span>
<span data-ttu-id="6b77e-109">**AzBatchTask** Cmdlet은 일괄 작업에 대 한 Azure 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="6b77e-110">*JobId* 매개 변수 또는 *작업* 매개 변수 중 하나를 통해 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="6b77e-111">단일 작업을 가져오려면 *Id* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="6b77e-112">*Filter* 매개 변수를 지정 하 여 OData (Open Data Protocol) 필터와 일치 하는 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="6b77e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6b77e-113">EXAMPLES</span></span>

### <span data-ttu-id="6b77e-114">예제 1: ID로 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b77e-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 : 
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="6b77e-115">이 명령은 작업 Job01에서 ID Task03를 사용 하 여 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="6b77e-116">Get-AzBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6b77e-117">예제 2: 지정한 작업에서 완료 된 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b77e-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         : 
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               : 
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="6b77e-118">이 명령은 ID Job02가 있는 작업에서 완료 된 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="6b77e-119">변수</span><span class="sxs-lookup"><span data-stu-id="6b77e-119">PARAMETERS</span></span>

### <span data-ttu-id="6b77e-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b77e-120">-BatchContext</span></span>
<span data-ttu-id="6b77e-121">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b77e-122">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6b77e-123">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-123">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6b77e-124">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6b77e-125">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6b77e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b77e-126">-DefaultProfile</span></span>
<span data-ttu-id="6b77e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b77e-128">-확장</span><span class="sxs-lookup"><span data-stu-id="6b77e-128">-Expand</span></span>
<span data-ttu-id="6b77e-129">OData expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="6b77e-130">가져올 주 엔터티의 연결 된 엔터티를 가져오려면이 매개 변수에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="6b77e-131">-필터</span><span class="sxs-lookup"><span data-stu-id="6b77e-131">-Filter</span></span>
<span data-ttu-id="6b77e-132">작업에 대 한 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="6b77e-133">필터를 지정 하지 않으면이 cmdlet은 일괄 처리 계정 또는 작업에 대 한 모든 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="6b77e-134">-Id</span><span class="sxs-lookup"><span data-stu-id="6b77e-134">-Id</span></span>
<span data-ttu-id="6b77e-135">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="6b77e-136">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b77e-137">-작업</span><span class="sxs-lookup"><span data-stu-id="6b77e-137">-Job</span></span>
<span data-ttu-id="6b77e-138">이 cmdlet이 가져오는 작업을 포함 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="6b77e-139">**Pscloudjob** 개체를 가져오려면 Get-AzBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b77e-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="6b77e-140">-JobId</span></span>
<span data-ttu-id="6b77e-141">이 cmdlet이 가져오는 작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b77e-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6b77e-142">-MaxCount</span></span>
<span data-ttu-id="6b77e-143">반환할 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="6b77e-144">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6b77e-145">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="6b77e-146">-선택</span><span class="sxs-lookup"><span data-stu-id="6b77e-146">-Select</span></span>
<span data-ttu-id="6b77e-147">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="6b77e-148">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="6b77e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b77e-149">CommonParameters</span></span>
<span data-ttu-id="6b77e-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b77e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b77e-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b77e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b77e-152">입력</span><span class="sxs-lookup"><span data-stu-id="6b77e-152">INPUTS</span></span>

### <span data-ttu-id="6b77e-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6b77e-153">System.String</span></span>

### <span data-ttu-id="6b77e-154">Microsoft.Azure.Commands.Batch. PSCloudJob 모델</span><span class="sxs-lookup"><span data-stu-id="6b77e-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="6b77e-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b77e-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6b77e-156">출력</span><span class="sxs-lookup"><span data-stu-id="6b77e-156">OUTPUTS</span></span>

### <span data-ttu-id="6b77e-157">Microsoft.Azure.Commands.Batch. PSCloudTask에 대 한 모델</span><span class="sxs-lookup"><span data-stu-id="6b77e-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="6b77e-158">상속자</span><span class="sxs-lookup"><span data-stu-id="6b77e-158">NOTES</span></span>

## <span data-ttu-id="6b77e-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b77e-159">RELATED LINKS</span></span>

[<span data-ttu-id="6b77e-160">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6b77e-160">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6b77e-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="6b77e-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="6b77e-162">새로운 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b77e-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="6b77e-163">제거-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b77e-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="6b77e-164">중지-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b77e-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="6b77e-165">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6b77e-165">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


