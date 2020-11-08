---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216271"
---
# <span data-ttu-id="413d4-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="413d4-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="413d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="413d4-102">SYNOPSIS</span></span>
<span data-ttu-id="413d4-103">지정 된 계산 노드에서 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="413d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="413d4-104">SYNTAX</span></span>

### <span data-ttu-id="413d4-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="413d4-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="413d4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="413d4-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="413d4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="413d4-107">DESCRIPTION</span></span>
<span data-ttu-id="413d4-108">AzBatchComputeNodeScheduling cmdlet을 **사용** 하면 지정 된 계산 노드에서 작업을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="413d4-109">계산 노드는 특정 응용 프로그램 작업을 전담 하는 Azure 가상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="413d4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="413d4-110">EXAMPLES</span></span>

### <span data-ttu-id="413d4-111">예제 1: 계산 노드에서 작업 일정 사용</span><span class="sxs-lookup"><span data-stu-id="413d4-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="413d4-112">이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="413d4-113">이렇게 하려면 예제의 첫 번째 명령은 batch 계정 contosobatchaccount의 계정 키를 포함 하는 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="413d4-114">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="413d4-115">그런 다음 두 번째 명령은이 개체 참조 및 **enable-AzBatchComputeNodeScheduling** cmdlet을 사용 하 여 tvm-1783593343_34-20151117t222514z에서 풀 myPool에 연결 하 고 작업 예약을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="413d4-116">예제 2: 풀의 계산 노드에서 작업 예약 사용</span><span class="sxs-lookup"><span data-stu-id="413d4-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="413d4-117">이러한 명령을 사용 하면 풀 Pool06에 있는 모든 계산 노드에서 작업을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="413d4-118">이 작업을 수행 하기 위해 예제의 첫 번째 명령은 일괄 계정 contosobatchaccount의 계정 키를 포함 하는 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="413d4-119">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="413d4-120">그런 다음이 예제의 두 번째 명령은이 개체 참조를 사용 하 여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환 합니다. **AzBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="413d4-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="413d4-121">그런 다음 컬렉션의 각 계산 노드에서 작업 일정을 예약할 수 있도록 하는 **AzBatchComputeNodeScheduling** cmdlet으로 해당 컬렉션을 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="413d4-122">변수</span><span class="sxs-lookup"><span data-stu-id="413d4-122">PARAMETERS</span></span>

### <span data-ttu-id="413d4-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="413d4-123">-BatchContext</span></span>
<span data-ttu-id="413d4-124">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="413d4-125">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="413d4-126">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="413d4-127">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="413d4-128">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="413d4-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="413d4-129">-ComputeNode</span></span>
<span data-ttu-id="413d4-130">작업 일정을 사용할 수 있는 계산 노드에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="413d4-131">이 개체 참조는 Get-AzBatchComputeNode cmdlet을 사용 하 여 만들고 반환 된 계산 노드 개체를 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="413d4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413d4-132">-DefaultProfile</span></span>
<span data-ttu-id="413d4-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="413d4-134">-Id</span><span class="sxs-lookup"><span data-stu-id="413d4-134">-Id</span></span>
<span data-ttu-id="413d4-135">작업 일정을 사용할 수 있는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="413d4-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="413d4-136">-PoolId</span></span>
<span data-ttu-id="413d4-137">작업 일정을 사용할 수 있는 계산 노드를 포함 하는 일괄 처리 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="413d4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413d4-138">CommonParameters</span></span>
<span data-ttu-id="413d4-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="413d4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413d4-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="413d4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413d4-141">입력</span><span class="sxs-lookup"><span data-stu-id="413d4-141">INPUTS</span></span>

### <span data-ttu-id="413d4-142">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="413d4-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="413d4-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="413d4-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="413d4-144">출력</span><span class="sxs-lookup"><span data-stu-id="413d4-144">OUTPUTS</span></span>

### <span data-ttu-id="413d4-145">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="413d4-145">System.Void</span></span>

## <span data-ttu-id="413d4-146">상속자</span><span class="sxs-lookup"><span data-stu-id="413d4-146">NOTES</span></span>

## <span data-ttu-id="413d4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="413d4-147">RELATED LINKS</span></span>

[<span data-ttu-id="413d4-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="413d4-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


