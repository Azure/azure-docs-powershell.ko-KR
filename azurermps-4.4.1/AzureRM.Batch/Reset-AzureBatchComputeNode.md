---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702882"
---
# <span data-ttu-id="2f650-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="2f650-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="2f650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f650-102">SYNOPSIS</span></span>
<span data-ttu-id="2f650-103">지정 된 계산 노드에 운영 체제를 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f650-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f650-104">SYNTAX</span></span>

### <span data-ttu-id="2f650-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="2f650-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f650-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2f650-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f650-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2f650-107">DESCRIPTION</span></span>
<span data-ttu-id="2f650-108">AzureBatchComputeNode cmdlet은 지정 된 계산 노드에 운영 체제를 **다시** 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="2f650-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2f650-109">EXAMPLES</span></span>

### <span data-ttu-id="2f650-110">예제 1: 노드를 이미지로</span><span class="sxs-lookup"><span data-stu-id="2f650-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="2f650-111">이 명령은 MyPool 이라는 풀에서 ID "tvm-3257026573_2-20150813t200938z" 인 계산 노드를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="2f650-112">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2f650-113">예제 2: 풀의 모든 노드를 이미지로,</span><span class="sxs-lookup"><span data-stu-id="2f650-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="2f650-114">이 명령은 MyPool 이라는 풀의 모든 compute 노드를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="2f650-115">변수</span><span class="sxs-lookup"><span data-stu-id="2f650-115">PARAMETERS</span></span>

### <span data-ttu-id="2f650-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2f650-116">-BatchContext</span></span>
<span data-ttu-id="2f650-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2f650-118">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="2f650-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="2f650-119">-ComputeNode</span></span>
<span data-ttu-id="2f650-120">이미지로 이동할 계산 노드를 나타내는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-121">-Id</span><span class="sxs-lookup"><span data-stu-id="2f650-121">-Id</span></span>
<span data-ttu-id="2f650-122">이미지로 연결할 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-122">Specifies the ID of the compute node to reimage.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="2f650-123">-PoolId</span></span>
<span data-ttu-id="2f650-124">계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="2f650-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="2f650-125">-ReimageOption</span></span>
<span data-ttu-id="2f650-126">노드를 이미지로, 그리고 현재 실행 중인 작업을 수행 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="2f650-127">기본값은 Requeue입니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-127">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f650-128">-DefaultProfile</span></span>
<span data-ttu-id="2f650-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f650-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f650-130">CommonParameters</span></span>
<span data-ttu-id="2f650-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f650-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f650-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f650-133">입력</span><span class="sxs-lookup"><span data-stu-id="2f650-133">INPUTS</span></span>

### <span data-ttu-id="2f650-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2f650-134">BatchAccountContext</span></span>
<span data-ttu-id="2f650-135">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2f650-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="2f650-136">PSComputeNode</span></span>
<span data-ttu-id="2f650-137">' ComputeNode ' 매개 변수는 파이프라인에서 ' PSComputeNode ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f650-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="2f650-138">출력</span><span class="sxs-lookup"><span data-stu-id="2f650-138">OUTPUTS</span></span>

## <span data-ttu-id="2f650-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2f650-139">NOTES</span></span>

## <span data-ttu-id="2f650-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f650-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f650-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="2f650-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="2f650-142">다시 시작-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="2f650-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="2f650-143">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f650-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


