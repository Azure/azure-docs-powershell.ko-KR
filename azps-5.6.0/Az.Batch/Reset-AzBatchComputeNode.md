---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: c6ad25e5c6ba327ddcd5b4877cbac39937ec4feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985357"
---
# <span data-ttu-id="73fc4-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="73fc4-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="73fc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="73fc4-103">지정된 계산 노드에 운영 체제를 다시 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="73fc4-104">구문</span><span class="sxs-lookup"><span data-stu-id="73fc4-104">SYNTAX</span></span>

### <span data-ttu-id="73fc4-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="73fc4-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73fc4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="73fc4-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73fc4-107">설명</span><span class="sxs-lookup"><span data-stu-id="73fc4-107">DESCRIPTION</span></span>
<span data-ttu-id="73fc4-108">**Reset-AzBatchComputeNode** cmdlet은 지정된 계산 노드에 운영 체제를 다시 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="73fc4-109">예제</span><span class="sxs-lookup"><span data-stu-id="73fc4-109">EXAMPLES</span></span>

### <span data-ttu-id="73fc4-110">예제 1: 노드 다시 생성</span><span class="sxs-lookup"><span data-stu-id="73fc4-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="73fc4-111">이 명령은 MyPool이라는 풀의 ID "tvm-3257026573_2-20150813t200938z"로 계산 노드를 다시 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="73fc4-112">Get-AzBatchAccountKey cmdlet을 사용하여 변수 변수에 컨텍스트를 $Context 합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="73fc4-113">예제 2: 풀의 모든 노드 다시 생성</span><span class="sxs-lookup"><span data-stu-id="73fc4-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="73fc4-114">이 명령은 MyPool이라는 풀의 모든 계산 노드를 다시 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="73fc4-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="73fc4-115">PARAMETERS</span></span>

### <span data-ttu-id="73fc4-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="73fc4-116">-BatchContext</span></span>
<span data-ttu-id="73fc4-117">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="73fc4-118">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="73fc4-119">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="73fc4-120">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="73fc4-121">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="73fc4-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="73fc4-122">-ComputeNode</span></span>
<span data-ttu-id="73fc4-123">다시 계산 노드를 나타내는 **PSComputeNode** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="73fc4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73fc4-124">-DefaultProfile</span></span>
<span data-ttu-id="73fc4-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73fc4-126">-Id</span><span class="sxs-lookup"><span data-stu-id="73fc4-126">-Id</span></span>
<span data-ttu-id="73fc4-127">다시 계산할 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="73fc4-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="73fc4-128">-PoolId</span></span>
<span data-ttu-id="73fc4-129">계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="73fc4-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="73fc4-130">-ReimageOption</span></span>
<span data-ttu-id="73fc4-131">노드를 다시 구성할 때와 현재 실행 중인 태스크에서 수행할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="73fc4-132">기본값은 다시큐어입니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="73fc4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73fc4-133">CommonParameters</span></span>
<span data-ttu-id="73fc4-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73fc4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73fc4-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73fc4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73fc4-136">입력</span><span class="sxs-lookup"><span data-stu-id="73fc4-136">INPUTS</span></span>

### <span data-ttu-id="73fc4-137">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="73fc4-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="73fc4-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="73fc4-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="73fc4-139">출력</span><span class="sxs-lookup"><span data-stu-id="73fc4-139">OUTPUTS</span></span>

### <span data-ttu-id="73fc4-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="73fc4-140">System.Void</span></span>

## <span data-ttu-id="73fc4-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="73fc4-141">NOTES</span></span>

## <span data-ttu-id="73fc4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73fc4-142">RELATED LINKS</span></span>

[<span data-ttu-id="73fc4-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="73fc4-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="73fc4-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="73fc4-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="73fc4-145">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="73fc4-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
