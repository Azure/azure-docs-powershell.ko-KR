---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: ff8c758b5e384fbab8f690030eb8a7fbe35c79f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217848"
---
# <span data-ttu-id="19164-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="19164-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="19164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19164-102">SYNOPSIS</span></span>
<span data-ttu-id="19164-103">지정 된 계산 노드에 운영 체제를 다시 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="19164-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19164-104">SYNTAX</span></span>

### <span data-ttu-id="19164-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="19164-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19164-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="19164-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19164-107">설명은</span><span class="sxs-lookup"><span data-stu-id="19164-107">DESCRIPTION</span></span>
<span data-ttu-id="19164-108">AzBatchComputeNode cmdlet은 지정 된 계산 노드에 운영 체제를 **다시** 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="19164-109">예제의</span><span class="sxs-lookup"><span data-stu-id="19164-109">EXAMPLES</span></span>

### <span data-ttu-id="19164-110">예제 1: 노드를 이미지로</span><span class="sxs-lookup"><span data-stu-id="19164-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="19164-111">이 명령은 MyPool 이라는 풀에서 ID "tvm-3257026573_2-20150813t200938z" 인 계산 노드를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="19164-112">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="19164-113">예제 2: 풀의 모든 노드를 이미지로,</span><span class="sxs-lookup"><span data-stu-id="19164-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="19164-114">이 명령은 MyPool 이라는 풀의 모든 compute 노드를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="19164-115">변수</span><span class="sxs-lookup"><span data-stu-id="19164-115">PARAMETERS</span></span>

### <span data-ttu-id="19164-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="19164-116">-BatchContext</span></span>
<span data-ttu-id="19164-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="19164-118">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19164-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="19164-119">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19164-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="19164-120">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19164-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="19164-121">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="19164-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="19164-122">-ComputeNode</span></span>
<span data-ttu-id="19164-123">이미지로 이동할 계산 노드를 나타내는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="19164-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19164-124">-DefaultProfile</span></span>
<span data-ttu-id="19164-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19164-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19164-126">-Id</span><span class="sxs-lookup"><span data-stu-id="19164-126">-Id</span></span>
<span data-ttu-id="19164-127">이미지로 연결할 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="19164-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="19164-128">-PoolId</span></span>
<span data-ttu-id="19164-129">계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="19164-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="19164-130">-ReimageOption</span></span>
<span data-ttu-id="19164-131">노드를 이미지로, 그리고 현재 실행 중인 작업을 수행 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="19164-132">기본값은 Requeue입니다.</span><span class="sxs-lookup"><span data-stu-id="19164-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="19164-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19164-133">CommonParameters</span></span>
<span data-ttu-id="19164-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19164-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19164-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19164-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19164-136">입력</span><span class="sxs-lookup"><span data-stu-id="19164-136">INPUTS</span></span>

### <span data-ttu-id="19164-137">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="19164-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="19164-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="19164-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="19164-139">출력</span><span class="sxs-lookup"><span data-stu-id="19164-139">OUTPUTS</span></span>

### <span data-ttu-id="19164-140">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="19164-140">System.Void</span></span>

## <span data-ttu-id="19164-141">상속자</span><span class="sxs-lookup"><span data-stu-id="19164-141">NOTES</span></span>

## <span data-ttu-id="19164-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19164-142">RELATED LINKS</span></span>

[<span data-ttu-id="19164-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="19164-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="19164-144">다시 시작-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="19164-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="19164-145">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="19164-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
