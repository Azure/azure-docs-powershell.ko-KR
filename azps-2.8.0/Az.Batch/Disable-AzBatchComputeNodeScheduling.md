---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: ee515e9d92028f49235dc229f992f8c1d6274672
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880114"
---
# <span data-ttu-id="16c70-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="16c70-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="16c70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c70-102">SYNOPSIS</span></span>
<span data-ttu-id="16c70-103">지정 된 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="16c70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16c70-104">SYNTAX</span></span>

### <span data-ttu-id="16c70-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="16c70-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c70-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="16c70-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16c70-107">설명은</span><span class="sxs-lookup"><span data-stu-id="16c70-107">DESCRIPTION</span></span>
<span data-ttu-id="16c70-108">**AzBatchComputeNodeScheduling** cmdlet은 지정 된 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="16c70-109">계산 노드는 특정 응용 프로그램 작업을 전담 하는 Azure 가상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="16c70-110">계산 노드에서 작업 일정을 사용 하지 않도록 설정 하는 경우 현재 노드의 작업 큐에 있는 작업에 대해 할 일을 결정 하는 옵션도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="16c70-111">**Disable-AzBatchComputeNodeScheduling** 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="16c70-112">작업을 종료 하 고 작업 큐에 다시 둡니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="16c70-113">이렇게 하면 다른 계산 노드에서 해당 작업의 일정을 재조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="16c70-114">작업을 종료 하 고 작업 큐에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="16c70-115">이 방법으로 중지 된 작업은 일정 조정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="16c70-116">현재 실행 중인 모든 작업이 완료 될 때까지 기다린 다음 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="16c70-117">실행 중인 모든 작업이 완료 될 때까지 기다렸다가 모든 데이터 보존 기간이 만료 되 면 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="16c70-118">예제의</span><span class="sxs-lookup"><span data-stu-id="16c70-118">EXAMPLES</span></span>

### <span data-ttu-id="16c70-119">예제 1: 계산 노드에서 작업 일정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="16c70-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="16c70-120">이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="16c70-121">이렇게 하려면 예제의 첫 번째 명령은 batch 계정 contosobatchaccount의 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="16c70-122">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="16c70-123">그런 다음 두 번째 명령은이 개체 참조 및 **AzBatchComputeNodeScheduling** cmdlet을 사용 하 여 풀 myPool에 연결 하 고 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="16c70-124">*DisableComputeNodeSchedulingOptions* 매개 변수가 포함 되지 않았으므로 계산 노드에서 현재 실행 중인 작업은 다시 착신으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="16c70-125">예제 2: 풀의 모든 계산 노드에서 작업 일정 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="16c70-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="16c70-126">이러한 명령은 일괄 처리 풀 Pool06의 모든 컴퓨터 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="16c70-127">이 작업을 수행 하기 위해 예제의 첫 번째 명령은 일괄 계정 contosobatchaccount의 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="16c70-128">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="16c70-129">그런 다음이 예제의 두 번째 명령은이 개체 참조를 사용 하 여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환 합니다. **AzBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="16c70-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="16c70-130">그런 다음 해당 컬렉션을 파이프라인으로 **AzBatchComputeNodeScheduling cmdlet을 사용 하지 않도록 설정** 하 여 컬렉션의 각 계산 노드에서 작업 일정을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="16c70-131">*DisableComputeNodeSchedulingOptions* 매개 변수가 포함 되지 않았으므로 계산 노드에서 현재 실행 중인 작업은 다시 착신으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="16c70-132">변수</span><span class="sxs-lookup"><span data-stu-id="16c70-132">PARAMETERS</span></span>

### <span data-ttu-id="16c70-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="16c70-133">-BatchContext</span></span>
<span data-ttu-id="16c70-134">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16c70-135">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="16c70-136">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-136">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="16c70-137">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="16c70-138">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="16c70-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="16c70-139">-ComputeNode</span></span>
<span data-ttu-id="16c70-140">작업 일정을 사용할 수 없는 계산 노드에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="16c70-141">이 개체 참조는 Get-AzBatchComputeNode cmdlet을 사용 하 여 만들고 반환 된 계산 노드 개체를 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="16c70-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c70-142">-DefaultProfile</span></span>
<span data-ttu-id="16c70-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16c70-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="16c70-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="16c70-145">이 cmdlet이 예약을 사용 하지 않도록 설정 된 컴퓨터 노드에서 현재 실행 중인 작업을 처리 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="16c70-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16c70-147">Requeue.</span><span class="sxs-lookup"><span data-stu-id="16c70-147">Requeue.</span></span>
<span data-ttu-id="16c70-148">작업이 즉시 중지 되 고 작업 큐에 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="16c70-149">이렇게 하면 다른 계산 노드에서 작업의 일정을 재조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="16c70-150">이 값이 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-150">This is the default value.</span></span> 
- <span data-ttu-id="16c70-151">종료.</span><span class="sxs-lookup"><span data-stu-id="16c70-151">Terminate.</span></span>
<span data-ttu-id="16c70-152">작업이 즉시 중지 되 고 작업 큐에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="16c70-153">이러한 작업의 일정이 조정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="16c70-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="16c70-154">TaskCompletion.</span></span>
<span data-ttu-id="16c70-155">계산 노드에서 작업 일정을 사용 하지 않도록 설정 하기 전에 현재 실행 중인 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="16c70-156">이 노드에는 새 작업이 예정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="16c70-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="16c70-157">RetainedData.</span></span>
<span data-ttu-id="16c70-158">현재 실행 중인 작업은 완료할 수 있으며 데이터 보존 기간은 계산 노드에서 작업 일정을 사용 하지 않도록 설정 하기 전에 만료 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="16c70-159">이 노드에는 새 작업이 예정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c70-160">-Id</span><span class="sxs-lookup"><span data-stu-id="16c70-160">-Id</span></span>
<span data-ttu-id="16c70-161">작업 일정을 사용할 수 없는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="16c70-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="16c70-162">-PoolId</span></span>
<span data-ttu-id="16c70-163">작업 일정을 사용 하지 않도록 설정 된 계산 노드를 포함 하는 일괄 처리 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="16c70-164">*PoolId* 매개 변수를 사용 하는 경우 동일한 명령에서 *ComputeNode* 매개 변수를 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="16c70-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="16c70-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c70-165">CommonParameters</span></span>
<span data-ttu-id="16c70-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c70-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c70-167">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c70-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c70-168">입력</span><span class="sxs-lookup"><span data-stu-id="16c70-168">INPUTS</span></span>

### <span data-ttu-id="16c70-169">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="16c70-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="16c70-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="16c70-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="16c70-171">출력</span><span class="sxs-lookup"><span data-stu-id="16c70-171">OUTPUTS</span></span>

### <span data-ttu-id="16c70-172">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="16c70-172">System.Void</span></span>

## <span data-ttu-id="16c70-173">상속자</span><span class="sxs-lookup"><span data-stu-id="16c70-173">NOTES</span></span>

## <span data-ttu-id="16c70-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16c70-174">RELATED LINKS</span></span>

[<span data-ttu-id="16c70-175">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="16c70-175">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="16c70-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="16c70-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)

