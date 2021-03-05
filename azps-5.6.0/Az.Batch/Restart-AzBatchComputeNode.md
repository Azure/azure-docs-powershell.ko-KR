---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: daf89fec73ed18cf5b67c4100556d490795708d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985343"
---
# <span data-ttu-id="67861-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="67861-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="67861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67861-102">SYNOPSIS</span></span>
<span data-ttu-id="67861-103">지정된 계산 노드를 다시 부트합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="67861-104">구문</span><span class="sxs-lookup"><span data-stu-id="67861-104">SYNTAX</span></span>

### <span data-ttu-id="67861-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="67861-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67861-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="67861-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67861-107">설명</span><span class="sxs-lookup"><span data-stu-id="67861-107">DESCRIPTION</span></span>
<span data-ttu-id="67861-108">**Restart-AzBatchComputeNode** cmdlet은 지정된 계산 노드를 다시 부트합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="67861-109">예제</span><span class="sxs-lookup"><span data-stu-id="67861-109">EXAMPLES</span></span>

### <span data-ttu-id="67861-110">예제 1: 계산 노드 다시 시작</span><span class="sxs-lookup"><span data-stu-id="67861-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="67861-111">이 명령은 풀 MyPool에서 "tvm-3257026573_2-20150813t200938z"를 사용하여 계산 노드를 다시 부트합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="67861-112">예제 2: 풀의 모든 계산 노드 다시 시작</span><span class="sxs-lookup"><span data-stu-id="67861-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="67861-113">이 명령은 풀 MyPool의 모든 계산 노드를 다시 부트합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="67861-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="67861-114">PARAMETERS</span></span>

### <span data-ttu-id="67861-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="67861-115">-BatchContext</span></span>
<span data-ttu-id="67861-116">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="67861-117">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="67861-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="67861-118">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67861-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="67861-119">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="67861-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="67861-120">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="67861-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="67861-121">-ComputeNode</span></span>
<span data-ttu-id="67861-122">다시 부팅할 계산 노드를 나타내는 **PSComputeNode** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="67861-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67861-123">-DefaultProfile</span></span>
<span data-ttu-id="67861-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67861-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67861-125">-Id</span><span class="sxs-lookup"><span data-stu-id="67861-125">-Id</span></span>
<span data-ttu-id="67861-126">재부팅할 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="67861-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="67861-127">-PoolId</span></span>
<span data-ttu-id="67861-128">계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="67861-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="67861-129">-RebootOption</span></span>
<span data-ttu-id="67861-130">노드를 다시 부팅할 때와 현재 실행 중인 태스크에서 수행할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="67861-131">기본값은 다시큐어입니다.</span><span class="sxs-lookup"><span data-stu-id="67861-131">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67861-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67861-132">CommonParameters</span></span>
<span data-ttu-id="67861-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67861-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67861-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67861-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67861-135">입력</span><span class="sxs-lookup"><span data-stu-id="67861-135">INPUTS</span></span>

### <span data-ttu-id="67861-136">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="67861-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="67861-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="67861-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="67861-138">출력</span><span class="sxs-lookup"><span data-stu-id="67861-138">OUTPUTS</span></span>

### <span data-ttu-id="67861-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="67861-139">System.Void</span></span>

## <span data-ttu-id="67861-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67861-140">NOTES</span></span>

## <span data-ttu-id="67861-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67861-141">RELATED LINKS</span></span>

[<span data-ttu-id="67861-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="67861-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="67861-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="67861-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="67861-144">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67861-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
