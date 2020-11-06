---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 998d559265aaa590cb62f72c9e6b9ec9dc5914df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526288"
---
# <span data-ttu-id="640d9-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="640d9-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="640d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="640d9-102">SYNOPSIS</span></span>
<span data-ttu-id="640d9-103">지정 된 계산 노드에 운영 체제를 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="640d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="640d9-104">SYNTAX</span></span>

### <span data-ttu-id="640d9-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="640d9-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="640d9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="640d9-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="640d9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="640d9-107">DESCRIPTION</span></span>
<span data-ttu-id="640d9-108">AzureBatchComputeNode cmdlet은 지정 된 계산 노드에 운영 체제를 **다시** 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="640d9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="640d9-109">EXAMPLES</span></span>

### <span data-ttu-id="640d9-110">예제 1: 노드를 이미지로</span><span class="sxs-lookup"><span data-stu-id="640d9-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="640d9-111">이 명령은 MyPool 이라는 풀에서 ID "tvm-3257026573_2-20150813t200938z" 인 계산 노드를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="640d9-112">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="640d9-113">예제 2: 풀의 모든 노드를 이미지로,</span><span class="sxs-lookup"><span data-stu-id="640d9-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="640d9-114">이 명령은 MyPool 이라는 풀의 모든 compute 노드를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="640d9-115">변수</span><span class="sxs-lookup"><span data-stu-id="640d9-115">PARAMETERS</span></span>

### <span data-ttu-id="640d9-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="640d9-116">-BatchContext</span></span>
<span data-ttu-id="640d9-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="640d9-118">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="640d9-119">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="640d9-120">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="640d9-121">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="640d9-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="640d9-122">-ComputeNode</span></span>
<span data-ttu-id="640d9-123">이미지로 이동할 계산 노드를 나타내는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="640d9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640d9-124">-DefaultProfile</span></span>
<span data-ttu-id="640d9-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="640d9-126">-Id</span><span class="sxs-lookup"><span data-stu-id="640d9-126">-Id</span></span>
<span data-ttu-id="640d9-127">이미지로 연결할 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="640d9-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="640d9-128">-PoolId</span></span>
<span data-ttu-id="640d9-129">계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="640d9-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="640d9-130">-ReimageOption</span></span>
<span data-ttu-id="640d9-131">노드를 이미지로, 그리고 현재 실행 중인 작업을 수행 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="640d9-132">기본값은 Requeue입니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="640d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640d9-133">CommonParameters</span></span>
<span data-ttu-id="640d9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="640d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640d9-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="640d9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640d9-136">입력</span><span class="sxs-lookup"><span data-stu-id="640d9-136">INPUTS</span></span>

### <span data-ttu-id="640d9-137">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="640d9-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="640d9-138">매개 변수: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="640d9-138">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="640d9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="640d9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="640d9-140">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="640d9-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="640d9-141">출력</span><span class="sxs-lookup"><span data-stu-id="640d9-141">OUTPUTS</span></span>

### <span data-ttu-id="640d9-142">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="640d9-142">System.Void</span></span>

## <span data-ttu-id="640d9-143">상속자</span><span class="sxs-lookup"><span data-stu-id="640d9-143">NOTES</span></span>

## <span data-ttu-id="640d9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="640d9-144">RELATED LINKS</span></span>

[<span data-ttu-id="640d9-145">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="640d9-145">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="640d9-146">다시 시작-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="640d9-146">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="640d9-147">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="640d9-147">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

