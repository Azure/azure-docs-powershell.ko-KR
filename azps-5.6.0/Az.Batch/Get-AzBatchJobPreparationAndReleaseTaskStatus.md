---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: e85976b4d4b5de508e1a4f25338b21abdb0c097f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983467"
---
# <span data-ttu-id="8bb74-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="8bb74-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="8bb74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bb74-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb74-103">Batch 작업 준비 및 릴리스 작업 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="8bb74-104">구문</span><span class="sxs-lookup"><span data-stu-id="8bb74-104">SYNTAX</span></span>

### <span data-ttu-id="8bb74-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="8bb74-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bb74-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8bb74-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bb74-107">설명</span><span class="sxs-lookup"><span data-stu-id="8bb74-107">DESCRIPTION</span></span>
<span data-ttu-id="8bb74-108">**Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet은 Batch 작업에 대한 Azure Batch 작업 준비 및 릴리스 작업 상태를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="8bb74-109">이 cmdlet에 *ID* 매개 변수 또는 **PSCloudJob** 인스턴스를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="8bb74-110">예제</span><span class="sxs-lookup"><span data-stu-id="8bb74-110">EXAMPLES</span></span>

### <span data-ttu-id="8bb74-111">예제 1: 작업의 작업 준비 및 릴리스 상태 확인</span><span class="sxs-lookup"><span data-stu-id="8bb74-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="8bb74-112">이 명령은 작업 "Test"에 대한 작업 준비 및 릴리스 작업 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="8bb74-113">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8bb74-114">예제 2: 필터를 사용하여 작업 준비 및 릴리스 상태 확인 및 지정 선택</span><span class="sxs-lookup"><span data-stu-id="8bb74-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="8bb74-115">이 명령은 노드 "tvm-2316545714_1-20170613t201733z"에서 작업 준비 및 릴리스 작업 상태를 표시하고 Select 절을 사용하여 JobPreparationTaskExecutionInformation 정보만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="8bb74-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8bb74-116">PARAMETERS</span></span>

### <span data-ttu-id="8bb74-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8bb74-117">-BatchContext</span></span>
<span data-ttu-id="8bb74-118">Batch 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="8bb74-119">이 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="8bb74-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb74-120">-DefaultProfile</span></span>
<span data-ttu-id="8bb74-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bb74-122">-확장</span><span class="sxs-lookup"><span data-stu-id="8bb74-122">-Expand</span></span>
<span data-ttu-id="8bb74-123">OData(Open Data Protocol) 확장 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="8bb74-124">이 매개 변수에 대한 값을 지정하여 얻을 주 엔터티의 관련 엔터티를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="8bb74-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="8bb74-125">-Filter</span></span>
<span data-ttu-id="8bb74-126">OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="8bb74-127">필터를 지정하지 않으면 이 cmdlet은 작업에 대한 모든 작업 준비 및 릴리스 작업 상태'를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="8bb74-128">-Id</span><span class="sxs-lookup"><span data-stu-id="8bb74-128">-Id</span></span>
<span data-ttu-id="8bb74-129">준비 및 릴리스 작업을 검색해야 하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="8bb74-130">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb74-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bb74-131">-InputObject</span></span>
<span data-ttu-id="8bb74-132">준비 및 릴리스 작업 상태를 얻을 작업을 나타내는 **PSCloudJob** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="8bb74-133">**PSCloudJob** 개체를 얻은 경우 Get-AzBatchJob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb74-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8bb74-134">-MaxCount</span></span>
<span data-ttu-id="8bb74-135">반환할 작업 준비 및 릴리스 작업 상태의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="8bb74-136">0(0) 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8bb74-137">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-137">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb74-138">-Select</span><span class="sxs-lookup"><span data-stu-id="8bb74-138">-Select</span></span>
<span data-ttu-id="8bb74-139">OData select 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="8bb74-140">이 매개 변수에 대한 값을 지정하여 모든 개체 속성이 아닌 특정 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="8bb74-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb74-141">CommonParameters</span></span>
<span data-ttu-id="8bb74-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8bb74-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb74-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bb74-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb74-144">입력</span><span class="sxs-lookup"><span data-stu-id="8bb74-144">INPUTS</span></span>

### <span data-ttu-id="8bb74-145">Microsoft.Azure.Commands.Bat. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="8bb74-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="8bb74-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8bb74-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8bb74-147">출력</span><span class="sxs-lookup"><span data-stu-id="8bb74-147">OUTPUTS</span></span>

### <span data-ttu-id="8bb74-148">Microsoft.Azure.Commands.Bat. Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="8bb74-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="8bb74-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8bb74-149">NOTES</span></span>

## <span data-ttu-id="8bb74-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8bb74-150">RELATED LINKS</span></span>

[<span data-ttu-id="8bb74-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="8bb74-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="8bb74-152">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8bb74-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
