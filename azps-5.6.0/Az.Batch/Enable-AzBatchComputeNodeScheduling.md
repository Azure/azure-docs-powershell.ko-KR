---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995722"
---
# <span data-ttu-id="aba5e-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="aba5e-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="aba5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aba5e-102">SYNOPSIS</span></span>
<span data-ttu-id="aba5e-103">지정된 계산 노드에서 작업 일정을 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="aba5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="aba5e-104">SYNTAX</span></span>

### <span data-ttu-id="aba5e-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="aba5e-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aba5e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="aba5e-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aba5e-107">설명</span><span class="sxs-lookup"><span data-stu-id="aba5e-107">DESCRIPTION</span></span>
<span data-ttu-id="aba5e-108">**Enable-AzBatchComputeNodeScheduling** cmdlet을 사용하면 지정된 계산 노드에서 태스크를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="aba5e-109">계산 노드는 특정 애플리케이션 워크로드 전용 Azure 가상 머신입니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="aba5e-110">예제</span><span class="sxs-lookup"><span data-stu-id="aba5e-110">EXAMPLES</span></span>

### <span data-ttu-id="aba5e-111">예제 1: 계산 노드에서 작업 예정 사용</span><span class="sxs-lookup"><span data-stu-id="aba5e-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="aba5e-112">이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 태스크를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="aba5e-113">이를 위해 예제의 첫 번째 명령은 일괄 처리 계정 contosobatchaccount에 대한 계정 키를 포함하는 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="aba5e-114">이 개체 참조는 이라는 변수에 $context.</span><span class="sxs-lookup"><span data-stu-id="aba5e-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="aba5e-115">그런 다음, 두 번째 명령은 이 개체 참조와 **enable-AzBatchComputeNodeScheduling** cmdlet을 사용하여 풀 myPool에 연결하고 tvm-1783593343_34-20151117t222514z에서 작업 예정을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="aba5e-116">예제 2: 풀의 계산 노드에서 작업 예정 사용</span><span class="sxs-lookup"><span data-stu-id="aba5e-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="aba5e-117">이러한 명령은 풀 풀06에서 찾은 모든 계산 노드에서 태스크를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="aba5e-118">이 작업을 수행하려면 예제의 첫 번째 명령은 일괄 처리 계정 contosobatchaccount에 대한 계정 키를 포함하는 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="aba5e-119">이 개체 참조는 이라는 변수에 $context.</span><span class="sxs-lookup"><span data-stu-id="aba5e-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="aba5e-120">예제의 두 번째 명령은 이 개체 참조 및 **Get-AzBatchComputeNode를** 사용하여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="aba5e-121">그런 다음 해당 컬렉션은 **Enable-AzBatchComputeNodeScheduling** cmdlet에 파이프됩니다. 이는 컬렉션의 각 계산 노드에서 태스크를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="aba5e-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aba5e-122">PARAMETERS</span></span>

### <span data-ttu-id="aba5e-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aba5e-123">-BatchContext</span></span>
<span data-ttu-id="aba5e-124">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aba5e-125">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="aba5e-126">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="aba5e-127">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="aba5e-128">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="aba5e-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="aba5e-129">-ComputeNode</span></span>
<span data-ttu-id="aba5e-130">작업일정이 활성화된 계산 노드에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="aba5e-131">이 개체 참조는 Get-AzBatchComputeNode cmdlet을 사용하고 반환된 계산 노드 개체를 변수에 저장하여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="aba5e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba5e-132">-DefaultProfile</span></span>
<span data-ttu-id="aba5e-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aba5e-134">-Id</span><span class="sxs-lookup"><span data-stu-id="aba5e-134">-Id</span></span>
<span data-ttu-id="aba5e-135">작업일정이 활성화된 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="aba5e-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="aba5e-136">-PoolId</span></span>
<span data-ttu-id="aba5e-137">작업 일괄 처리가 활성화된 계산 노드가 포함된 일괄 처리 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="aba5e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba5e-138">CommonParameters</span></span>
<span data-ttu-id="aba5e-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aba5e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba5e-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aba5e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba5e-141">입력</span><span class="sxs-lookup"><span data-stu-id="aba5e-141">INPUTS</span></span>

### <span data-ttu-id="aba5e-142">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="aba5e-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="aba5e-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aba5e-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="aba5e-144">출력</span><span class="sxs-lookup"><span data-stu-id="aba5e-144">OUTPUTS</span></span>

### <span data-ttu-id="aba5e-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="aba5e-145">System.Void</span></span>

## <span data-ttu-id="aba5e-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aba5e-146">NOTES</span></span>

## <span data-ttu-id="aba5e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aba5e-147">RELATED LINKS</span></span>

[<span data-ttu-id="aba5e-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="aba5e-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


