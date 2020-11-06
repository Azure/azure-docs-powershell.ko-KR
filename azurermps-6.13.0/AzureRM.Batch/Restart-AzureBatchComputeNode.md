---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 2b604b1bedf7843d21c9595227ab1ff446028133
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526287"
---
# <span data-ttu-id="6c54e-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6c54e-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="6c54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c54e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c54e-103">지정 된 계산 노드를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c54e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c54e-104">SYNTAX</span></span>

### <span data-ttu-id="6c54e-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="6c54e-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c54e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6c54e-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c54e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6c54e-107">DESCRIPTION</span></span>
<span data-ttu-id="6c54e-108">AzureBatchComputeNode cmdlet은 지정 된 계산 노드를 **다시** 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="6c54e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6c54e-109">EXAMPLES</span></span>

### <span data-ttu-id="6c54e-110">예제 1: 계산 노드 다시 시작</span><span class="sxs-lookup"><span data-stu-id="6c54e-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="6c54e-111">이 명령은 pool MyPool에서 ID "tvm-3257026573_2-20150813t200938z" 인 계산 노드를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="6c54e-112">예제 2: 풀의 모든 계산 노드 다시 시작</span><span class="sxs-lookup"><span data-stu-id="6c54e-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="6c54e-113">이 명령은 풀 MyPool의 모든 계산 노드를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="6c54e-114">변수</span><span class="sxs-lookup"><span data-stu-id="6c54e-114">PARAMETERS</span></span>

### <span data-ttu-id="6c54e-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6c54e-115">-BatchContext</span></span>
<span data-ttu-id="6c54e-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6c54e-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6c54e-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6c54e-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6c54e-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6c54e-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="6c54e-121">-ComputeNode</span></span>
<span data-ttu-id="6c54e-122">다시 부팅할 계산 노드를 나타내는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="6c54e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c54e-123">-DefaultProfile</span></span>
<span data-ttu-id="6c54e-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c54e-125">-Id</span><span class="sxs-lookup"><span data-stu-id="6c54e-125">-Id</span></span>
<span data-ttu-id="6c54e-126">다시 부팅할 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="6c54e-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="6c54e-127">-PoolId</span></span>
<span data-ttu-id="6c54e-128">계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="6c54e-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="6c54e-129">-RebootOption</span></span>
<span data-ttu-id="6c54e-130">노드를 다시 부팅 하는 시기와 현재 실행 중인 작업을 수행 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="6c54e-131">기본값은 Requeue입니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="6c54e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c54e-132">CommonParameters</span></span>
<span data-ttu-id="6c54e-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c54e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c54e-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c54e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c54e-135">입력</span><span class="sxs-lookup"><span data-stu-id="6c54e-135">INPUTS</span></span>

### <span data-ttu-id="6c54e-136">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="6c54e-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="6c54e-137">매개 변수: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c54e-137">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="6c54e-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6c54e-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6c54e-139">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c54e-139">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6c54e-140">출력</span><span class="sxs-lookup"><span data-stu-id="6c54e-140">OUTPUTS</span></span>

### <span data-ttu-id="6c54e-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6c54e-141">System.Void</span></span>

## <span data-ttu-id="6c54e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="6c54e-142">NOTES</span></span>

## <span data-ttu-id="6c54e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c54e-143">RELATED LINKS</span></span>

[<span data-ttu-id="6c54e-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6c54e-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="6c54e-145">다시 설정-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6c54e-145">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="6c54e-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6c54e-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


