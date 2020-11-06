---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 5f24e55042a8be7f36b1a9946c4bd5b87209a0f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534851"
---
# <span data-ttu-id="58e90-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="58e90-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="58e90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e90-102">SYNOPSIS</span></span>
<span data-ttu-id="58e90-103">일괄 작업 준비 및 릴리스 작업 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-103">Gets Batch job preparation and release task status.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58e90-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58e90-104">SYNTAX</span></span>

### <span data-ttu-id="58e90-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="58e90-105">Id (Default)</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58e90-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="58e90-106">InputObject</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58e90-107">설명은</span><span class="sxs-lookup"><span data-stu-id="58e90-107">DESCRIPTION</span></span>
<span data-ttu-id="58e90-108">**AzureBatchJobPreparationAndReleaseTaskStatus** Cmdlet은 일괄 작업에 대 한 Azure batch 작업 준비 및 릴리스 작업 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-108">The **Get-AzureBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="58e90-109">*Id* 매개 변수 또는이 Cmdlet에 **pscloudjob** 인스턴스를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="58e90-110">예제의</span><span class="sxs-lookup"><span data-stu-id="58e90-110">EXAMPLES</span></span>

### <span data-ttu-id="58e90-111">예제 1: 작업 준비 및 작업 릴리스 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="58e90-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="58e90-112">이 명령은 작업 준비 및 작업 상태 "테스트"를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="58e90-113">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="58e90-114">예제 2: 필터가 있는 작업의 작업 준비 및 릴리스 상태를 가져오고 지정 된 것을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="58e90-115">이 명령은 "tvm-2316545714_1-20170613t201733z" 노드에서 "Test" 작업에 대 한 작업 준비 및 릴리스 작업 상태를 가져오고 Select 절을 사용 하 여 JobPreparationTaskExecutionInformation 정보만 반환 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="58e90-116">변수</span><span class="sxs-lookup"><span data-stu-id="58e90-116">PARAMETERS</span></span>

### <span data-ttu-id="58e90-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="58e90-117">-BatchContext</span></span>
<span data-ttu-id="58e90-118">일괄 처리 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="58e90-119">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-119">Use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="58e90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e90-120">-DefaultProfile</span></span>
<span data-ttu-id="58e90-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58e90-122">-확장</span><span class="sxs-lookup"><span data-stu-id="58e90-122">-Expand</span></span>
<span data-ttu-id="58e90-123">OData (Open Data Protocol) expand 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="58e90-124">이 매개 변수에 대 한 값을 지정 하 여 가져올 기본 엔터티의 연결 된 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="58e90-125">-필터</span><span class="sxs-lookup"><span data-stu-id="58e90-125">-Filter</span></span>
<span data-ttu-id="58e90-126">OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="58e90-127">필터를 지정 하지 않으면이 cmdlet은 작업에 대 한 모든 작업 준비 및 릴리스 작업 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="58e90-128">-Id</span><span class="sxs-lookup"><span data-stu-id="58e90-128">-Id</span></span>
<span data-ttu-id="58e90-129">준비 및 릴리스 작업을 검색 해야 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="58e90-130">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e90-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58e90-131">-InputObject</span></span>
<span data-ttu-id="58e90-132">준비 및 릴리스 작업 상태를 가져오는 작업을 나타내는 **Pscloudjob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="58e90-133">**Pscloudjob** 개체를 가져오려면 Get-AzureBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-133">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58e90-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="58e90-134">-MaxCount</span></span>
<span data-ttu-id="58e90-135">반환할 최대 작업 준비 및 릴리즈 작업 상태 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="58e90-136">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="58e90-137">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-137">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e90-138">-선택</span><span class="sxs-lookup"><span data-stu-id="58e90-138">-Select</span></span>
<span data-ttu-id="58e90-139">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="58e90-140">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="58e90-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e90-141">CommonParameters</span></span>
<span data-ttu-id="58e90-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58e90-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e90-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e90-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e90-144">입력</span><span class="sxs-lookup"><span data-stu-id="58e90-144">INPUTS</span></span>

### <span data-ttu-id="58e90-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58e90-145">System.String</span></span>
<span data-ttu-id="58e90-146">Microsoft.Azure.Commands.Batch. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58e90-146">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="58e90-147">출력</span><span class="sxs-lookup"><span data-stu-id="58e90-147">OUTPUTS</span></span>

### <span data-ttu-id="58e90-148">Microsoft.Azure.Commands.Batch. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="58e90-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="58e90-149">상속자</span><span class="sxs-lookup"><span data-stu-id="58e90-149">NOTES</span></span>

## <span data-ttu-id="58e90-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58e90-150">RELATED LINKS</span></span>

[<span data-ttu-id="58e90-151">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="58e90-151">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="58e90-152">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58e90-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
