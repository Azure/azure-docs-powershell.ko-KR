---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: 1a177f0987f27f81f0ab27d5e35db11df17ae005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527096"
---
# <span data-ttu-id="112e7-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="112e7-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="112e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="112e7-102">SYNOPSIS</span></span>
<span data-ttu-id="112e7-103">작업에 대 한 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="112e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="112e7-104">SYNTAX</span></span>

### <span data-ttu-id="112e7-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="112e7-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="112e7-106">I</span><span class="sxs-lookup"><span data-stu-id="112e7-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112e7-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="112e7-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="112e7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="112e7-108">DESCRIPTION</span></span>
<span data-ttu-id="112e7-109">**Get-AzureBatchTask** Cmdlet은 일괄 작업에 대 한 Azure 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="112e7-110">*JobId* 매개 변수 또는 *작업* 매개 변수 중 하나를 통해 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="112e7-111">단일 작업을 가져오려면 *Id* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="112e7-112">*Filter* 매개 변수를 지정 하 여 OData (Open Data Protocol) 필터와 일치 하는 작업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="112e7-113">예제의</span><span class="sxs-lookup"><span data-stu-id="112e7-113">EXAMPLES</span></span>

### <span data-ttu-id="112e7-114">예제 1: ID로 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="112e7-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
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

<span data-ttu-id="112e7-115">이 명령은 작업 Job01에서 ID Task03를 사용 하 여 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="112e7-116">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="112e7-117">예제 2: 지정한 작업에서 완료 된 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="112e7-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
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

<span data-ttu-id="112e7-118">이 명령은 ID Job02가 있는 작업에서 완료 된 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="112e7-119">변수</span><span class="sxs-lookup"><span data-stu-id="112e7-119">PARAMETERS</span></span>

### <span data-ttu-id="112e7-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="112e7-120">-BatchContext</span></span>
<span data-ttu-id="112e7-121">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="112e7-122">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="112e7-123">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="112e7-124">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="112e7-125">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="112e7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112e7-126">-DefaultProfile</span></span>
<span data-ttu-id="112e7-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="112e7-128">-확장</span><span class="sxs-lookup"><span data-stu-id="112e7-128">-Expand</span></span>
<span data-ttu-id="112e7-129">OData expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="112e7-130">가져올 주 엔터티의 연결 된 엔터티를 가져오려면이 매개 변수에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112e7-131">-필터</span><span class="sxs-lookup"><span data-stu-id="112e7-131">-Filter</span></span>
<span data-ttu-id="112e7-132">작업에 대 한 OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="112e7-133">필터를 지정 하지 않으면이 cmdlet은 일괄 처리 계정 또는 작업에 대 한 모든 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112e7-134">-Id</span><span class="sxs-lookup"><span data-stu-id="112e7-134">-Id</span></span>
<span data-ttu-id="112e7-135">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="112e7-136">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112e7-137">-작업</span><span class="sxs-lookup"><span data-stu-id="112e7-137">-Job</span></span>
<span data-ttu-id="112e7-138">이 cmdlet이 가져오는 작업을 포함 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="112e7-139">**Pscloudjob** 개체를 가져오려면 Get-AzureBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-139">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="112e7-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="112e7-140">-JobId</span></span>
<span data-ttu-id="112e7-141">이 cmdlet이 가져오는 작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="112e7-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="112e7-142">-MaxCount</span></span>
<span data-ttu-id="112e7-143">반환할 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="112e7-144">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="112e7-145">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-145">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112e7-146">-선택</span><span class="sxs-lookup"><span data-stu-id="112e7-146">-Select</span></span>
<span data-ttu-id="112e7-147">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="112e7-148">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112e7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112e7-149">CommonParameters</span></span>
<span data-ttu-id="112e7-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112e7-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="112e7-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112e7-152">입력</span><span class="sxs-lookup"><span data-stu-id="112e7-152">INPUTS</span></span>

### <span data-ttu-id="112e7-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="112e7-153">BatchAccountContext</span></span>
<span data-ttu-id="112e7-154">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="112e7-155">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="112e7-155">PSCloudJob</span></span>
<span data-ttu-id="112e7-156">' Job ' 매개 변수는 파이프라인에서 ' PSCloudJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="112e7-156">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="112e7-157">출력</span><span class="sxs-lookup"><span data-stu-id="112e7-157">OUTPUTS</span></span>

### <span data-ttu-id="112e7-158">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="112e7-158">PSCloudTask</span></span>

## <span data-ttu-id="112e7-159">상속자</span><span class="sxs-lookup"><span data-stu-id="112e7-159">NOTES</span></span>

## <span data-ttu-id="112e7-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="112e7-160">RELATED LINKS</span></span>

[<span data-ttu-id="112e7-161">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="112e7-161">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="112e7-162">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="112e7-162">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="112e7-163">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="112e7-163">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="112e7-164">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="112e7-164">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="112e7-165">중지-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="112e7-165">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="112e7-166">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="112e7-166">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


