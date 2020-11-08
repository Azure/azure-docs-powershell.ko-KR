---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216420"
---
# <span data-ttu-id="c0b41-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c0b41-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="c0b41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0b41-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b41-103">지정 된 계산 노드를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="c0b41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0b41-104">SYNTAX</span></span>

### <span data-ttu-id="c0b41-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0b41-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0b41-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c0b41-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0b41-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c0b41-107">DESCRIPTION</span></span>
<span data-ttu-id="c0b41-108">AzBatchComputeNode cmdlet은 지정 된 계산 노드를 **다시** 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="c0b41-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c0b41-109">EXAMPLES</span></span>

### <span data-ttu-id="c0b41-110">예제 1: 계산 노드 다시 시작</span><span class="sxs-lookup"><span data-stu-id="c0b41-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="c0b41-111">이 명령은 pool MyPool에서 ID "tvm-3257026573_2-20150813t200938z" 인 계산 노드를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="c0b41-112">예제 2: 풀의 모든 계산 노드 다시 시작</span><span class="sxs-lookup"><span data-stu-id="c0b41-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="c0b41-113">이 명령은 풀 MyPool의 모든 계산 노드를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="c0b41-114">변수</span><span class="sxs-lookup"><span data-stu-id="c0b41-114">PARAMETERS</span></span>

### <span data-ttu-id="c0b41-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c0b41-115">-BatchContext</span></span>
<span data-ttu-id="c0b41-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c0b41-117">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c0b41-118">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c0b41-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c0b41-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c0b41-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c0b41-121">-ComputeNode</span></span>
<span data-ttu-id="c0b41-122">다시 부팅할 계산 노드를 나타내는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="c0b41-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b41-123">-DefaultProfile</span></span>
<span data-ttu-id="c0b41-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0b41-125">-Id</span><span class="sxs-lookup"><span data-stu-id="c0b41-125">-Id</span></span>
<span data-ttu-id="c0b41-126">다시 부팅할 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="c0b41-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c0b41-127">-PoolId</span></span>
<span data-ttu-id="c0b41-128">계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="c0b41-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="c0b41-129">-RebootOption</span></span>
<span data-ttu-id="c0b41-130">노드를 다시 부팅 하는 시기와 현재 실행 중인 작업을 수행 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="c0b41-131">기본값은 Requeue입니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="c0b41-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b41-132">CommonParameters</span></span>
<span data-ttu-id="c0b41-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0b41-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b41-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0b41-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b41-135">입력</span><span class="sxs-lookup"><span data-stu-id="c0b41-135">INPUTS</span></span>

### <span data-ttu-id="c0b41-136">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c0b41-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="c0b41-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c0b41-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c0b41-138">출력</span><span class="sxs-lookup"><span data-stu-id="c0b41-138">OUTPUTS</span></span>

### <span data-ttu-id="c0b41-139">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c0b41-139">System.Void</span></span>

## <span data-ttu-id="c0b41-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c0b41-140">NOTES</span></span>

## <span data-ttu-id="c0b41-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0b41-141">RELATED LINKS</span></span>

[<span data-ttu-id="c0b41-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c0b41-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="c0b41-143">다시 설정-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c0b41-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="c0b41-144">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0b41-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
