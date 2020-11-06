---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 40eb6d3cfd3961c876a5da07ced1ebcf383166e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538031"
---
# <span data-ttu-id="179c7-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="179c7-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="179c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="179c7-102">SYNOPSIS</span></span>
<span data-ttu-id="179c7-103">지정 된 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="179c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="179c7-104">SYNTAX</span></span>

### <span data-ttu-id="179c7-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="179c7-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="179c7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="179c7-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="179c7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="179c7-107">DESCRIPTION</span></span>
<span data-ttu-id="179c7-108">**AzureBatchComputeNodeScheduling** cmdlet은 지정 된 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="179c7-109">계산 노드는 특정 응용 프로그램 작업을 전담 하는 Azure 가상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="179c7-110">계산 노드에서 작업 일정을 사용 하지 않도록 설정 하는 경우 현재 노드의 작업 큐에 있는 작업에 대해 할 일을 결정 하는 옵션도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="179c7-111">**Disable-AzureBatchComputeNodeScheduling** 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 

- <span data-ttu-id="179c7-112">작업을 종료 하 고 작업 큐에 다시 둡니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="179c7-113">이렇게 하면 다른 계산 노드에서 해당 작업의 일정을 재조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="179c7-114">작업을 종료 하 고 작업 큐에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="179c7-115">이 방법으로 중지 된 작업은 일정 조정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="179c7-116">현재 실행 중인 모든 작업이 완료 될 때까지 기다린 다음 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="179c7-117">실행 중인 모든 작업이 완료 될 때까지 기다렸다가 모든 데이터 보존 기간이 만료 되 면 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="179c7-118">예제의</span><span class="sxs-lookup"><span data-stu-id="179c7-118">EXAMPLES</span></span>

### <span data-ttu-id="179c7-119">예제 1: 계산 노드에서 작업 일정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="179c7-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="179c7-120">이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="179c7-121">이렇게 하려면 예제의 첫 번째 명령은 batch 계정 contosobatchaccount의 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="179c7-122">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-122">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="179c7-123">그런 다음 두 번째 명령은이 개체 참조 및 **AzureBatchComputeNodeScheduling** cmdlet을 사용 하 여 풀 myPool에 연결 하 고 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>

<span data-ttu-id="179c7-124">*DisableComputeNodeSchedulingOptions* 매개 변수가 포함 되지 않았으므로 계산 노드에서 현재 실행 중인 작업은 다시 착신으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="179c7-125">예제 2: 풀의 모든 계산 노드에서 작업 일정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="179c7-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="179c7-126">이러한 명령은 일괄 처리 풀 Pool06의 모든 컴퓨터 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="179c7-127">이 작업을 수행 하기 위해 예제의 첫 번째 명령은 일괄 계정 contosobatchaccount의 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="179c7-128">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-128">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="179c7-129">그런 다음이 예제의 두 번째 명령은이 개체 참조를 사용 하 여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환 합니다. **AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="179c7-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="179c7-130">그런 다음 해당 컬렉션을 파이프라인으로 **AzureBatchComputeNodeScheduling cmdlet을 사용 하지 않도록 설정** 하 여 컬렉션의 각 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>

<span data-ttu-id="179c7-131">*DisableComputeNodeSchedulingOptions* 매개 변수가 포함 되지 않았으므로 계산 노드에서 현재 실행 중인 작업은 다시 착신으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="179c7-132">변수</span><span class="sxs-lookup"><span data-stu-id="179c7-132">PARAMETERS</span></span>

### <span data-ttu-id="179c7-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="179c7-133">-BatchContext</span></span>
<span data-ttu-id="179c7-134">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="179c7-135">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-135">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="179c7-136">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-136">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="179c7-137">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="179c7-138">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="179c7-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="179c7-139">-ComputeNode</span></span>
<span data-ttu-id="179c7-140">작업 일정을 사용할 수 없는 계산 노드에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="179c7-141">이 개체 참조는 Get-AzureBatchComputeNode cmdlet을 사용 하 여 만들고 반환 된 계산 노드 개체를 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-141">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="179c7-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179c7-142">-DefaultProfile</span></span>
<span data-ttu-id="179c7-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="179c7-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="179c7-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="179c7-145">이 cmdlet이 예약을 사용 하지 않도록 설정 된 컴퓨터 노드에서 현재 실행 중인 작업을 처리 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="179c7-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="179c7-147">Requeue.</span><span class="sxs-lookup"><span data-stu-id="179c7-147">Requeue.</span></span>
<span data-ttu-id="179c7-148">작업이 즉시 중지 되 고 작업 큐에 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="179c7-149">이렇게 하면 다른 계산 노드에서 작업의 일정을 재조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="179c7-150">이 값이 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-150">This is the default value.</span></span> 
- <span data-ttu-id="179c7-151">종료.</span><span class="sxs-lookup"><span data-stu-id="179c7-151">Terminate.</span></span>
<span data-ttu-id="179c7-152">작업이 즉시 중지 되 고 작업 큐에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="179c7-153">이러한 작업의 일정이 조정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="179c7-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="179c7-154">TaskCompletion.</span></span>
<span data-ttu-id="179c7-155">계산 노드에서 작업 일정을 사용 하지 않도록 설정 하기 전에 현재 실행 중인 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="179c7-156">이 노드에는 새 작업이 예정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="179c7-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="179c7-157">RetainedData.</span></span>
<span data-ttu-id="179c7-158">현재 실행 중인 작업은 완료할 수 있으며 데이터 보존 기간은 계산 노드에서 작업 일정을 사용 하지 않도록 설정 하기 전에 만료 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="179c7-159">이 노드에는 새 작업이 예정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: DisableComputeNodeSchedulingOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179c7-160">-Id</span><span class="sxs-lookup"><span data-stu-id="179c7-160">-Id</span></span>
<span data-ttu-id="179c7-161">작업 일정을 사용할 수 없는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="179c7-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="179c7-162">-PoolId</span></span>
<span data-ttu-id="179c7-163">작업 일정을 사용 하지 않도록 설정 된 계산 노드를 포함 하는 일괄 처리 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>

<span data-ttu-id="179c7-164">*PoolId* 매개 변수를 사용 하는 경우 동일한 명령에서 *ComputeNode* 매개 변수를 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="179c7-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="179c7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179c7-165">CommonParameters</span></span>
<span data-ttu-id="179c7-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179c7-167">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="179c7-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179c7-168">입력</span><span class="sxs-lookup"><span data-stu-id="179c7-168">INPUTS</span></span>

### <span data-ttu-id="179c7-169">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="179c7-169">BatchAccountContext</span></span>
<span data-ttu-id="179c7-170">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-170">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="179c7-171">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="179c7-171">PSComputeNode</span></span>
<span data-ttu-id="179c7-172">' ComputeNode ' 매개 변수는 파이프라인에서 ' PSComputeNode ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="179c7-172">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="179c7-173">출력</span><span class="sxs-lookup"><span data-stu-id="179c7-173">OUTPUTS</span></span>

## <span data-ttu-id="179c7-174">상속자</span><span class="sxs-lookup"><span data-stu-id="179c7-174">NOTES</span></span>

## <span data-ttu-id="179c7-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="179c7-175">RELATED LINKS</span></span>

[<span data-ttu-id="179c7-176">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="179c7-176">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="179c7-177">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="179c7-177">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)


