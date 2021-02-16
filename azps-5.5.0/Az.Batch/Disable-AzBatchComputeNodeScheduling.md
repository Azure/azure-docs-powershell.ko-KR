---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199572"
---
# <span data-ttu-id="3e150-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="3e150-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="3e150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e150-102">SYNOPSIS</span></span>
<span data-ttu-id="3e150-103">지정된 계산 노드에서 태스크를 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="3e150-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e150-104">SYNTAX</span></span>

### <span data-ttu-id="3e150-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="3e150-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e150-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3e150-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e150-107">설명</span><span class="sxs-lookup"><span data-stu-id="3e150-107">DESCRIPTION</span></span>
<span data-ttu-id="3e150-108">**Disable-AzBatchComputeNodeScheduling** cmdlet은 지정된 계산 노드에서 태스크를 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="3e150-109">계산 노드는 특정 애플리케이션 워크로드 전용 Azure 가상 머신입니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="3e150-110">계산 노드에서 태스크를 사용하지 않도록 설정하면 현재 노드의 태스크 큐에 있는 작업에 대해 어떤 작업을 할지 결정하는 옵션도 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="3e150-111">**Disable-AzBatchComputeNodeScheduling을** 사용하면 다음을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="3e150-112">태스크를 종료하고 작업 큐에 다시 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="3e150-113">이렇게 하면 해당 작업을 다른 계산 노드에서 다시 계획할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="3e150-114">태스크를 종료하고 작업 큐에서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="3e150-115">이러한 방식으로 중지된 작업은 다시 예정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="3e150-116">현재 실행 중인 모든 태스크가 완료될 때까지 기다렸다가 계산 노드에서 작업 예정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="3e150-117">실행 중인 모든 태스크가 완료되고 모든 데이터 보존 기간이 만료될 때까지 기다렸다가 계산 노드에서 작업 예정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="3e150-118">예제</span><span class="sxs-lookup"><span data-stu-id="3e150-118">EXAMPLES</span></span>

### <span data-ttu-id="3e150-119">예제 1: 계산 노드에서 작업 예정 사용 안</span><span class="sxs-lookup"><span data-stu-id="3e150-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="3e150-120">이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="3e150-121">이를 위해 예제의 첫 번째 명령은 배치 계정 contosobatchaccount에 대한 계정 키에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="3e150-122">이 개체 참조는 $context.</span><span class="sxs-lookup"><span data-stu-id="3e150-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="3e150-123">두 번째 명령은 이 개체 참조 및 **Disable-AzBatchComputeNodeScheduling** cmdlet을 사용하여 myPool 풀에 연결하고 노드 tvm-1783593343_34-20151117t222514z에서 작업 예정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="3e150-124">*DisableComputeNodeSchedulingOptions* 매개 변수가 포함되지 않은 경우 계산 노드에서 현재 실행 중인 태스크가 다시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="3e150-125">예제 2: 풀의 모든 계산 노드에서 작업 예정 사용 안</span><span class="sxs-lookup"><span data-stu-id="3e150-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="3e150-126">이러한 명령은 일괄 처리 풀 Pool06의 모든 컴퓨터 노드에서 작업 예정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="3e150-127">이 작업을 수행하기 위해 예제의 첫 번째 명령은 배치 계정 contosobatchaccount에 대한 계정 키에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="3e150-128">이 개체 참조는 $context.</span><span class="sxs-lookup"><span data-stu-id="3e150-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="3e150-129">이 예제의 두 번째 명령은 이 개체 참조 및 **Get-AzBatchComputeNode를** 사용하여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="3e150-130">그런 다음 해당 컬렉션이 **Disable-AzBatchComputeNodeScheduling** cmdlet으로 파이프되어 컬렉션의 각 계산 노드에서 태스크를 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="3e150-131">*DisableComputeNodeSchedulingOptions* 매개 변수가 포함되지 않은 경우 계산 노드에서 현재 실행 중인 태스크가 다시 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="3e150-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e150-132">PARAMETERS</span></span>

### <span data-ttu-id="3e150-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3e150-133">-BatchContext</span></span>
<span data-ttu-id="3e150-134">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3e150-135">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3e150-136">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3e150-137">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3e150-138">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3e150-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e150-139">-ComputeNode</span></span>
<span data-ttu-id="3e150-140">태스크를 사용할 수 없는 계산 노드에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="3e150-141">이 개체 참조는 Get-AzBatchComputeNode cmdlet을 사용하고 반환된 계산 노드 개체를 변수에 저장하여 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="3e150-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e150-142">-DefaultProfile</span></span>
<span data-ttu-id="3e150-143">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e150-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="3e150-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="3e150-145">이 cmdlet이 예약이 비활성화된 컴퓨터 노드에서 현재 실행 중인 모든 작업을 처리하는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="3e150-146">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3e150-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e150-147">다시 queue를 습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-147">Requeue.</span></span>
<span data-ttu-id="3e150-148">태스크가 즉시 중지되어 작업 큐로 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="3e150-149">이렇게 하면 다른 계산 노드에서 작업을 다시 계획할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="3e150-150">기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-150">This is the default value.</span></span> 
- <span data-ttu-id="3e150-151">종료합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-151">Terminate.</span></span>
<span data-ttu-id="3e150-152">태스크가 즉시 중지되고 작업 큐에서 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="3e150-153">이러한 작업은 다시 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="3e150-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="3e150-154">TaskCompletion.</span></span>
<span data-ttu-id="3e150-155">현재 실행 중인 태스크는 계산 노드에서 태스크를 사용하지 않도록 설정하기 전에 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="3e150-156">이 노드에는 새 작업이 예약되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="3e150-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="3e150-157">RetainedData.</span></span>
<span data-ttu-id="3e150-158">현재 실행 중인 태스크는 완료할 수 있으며, 데이터 보존 기간은 계산 노드에서 작업 계획이 비활성화되기 전에 만료될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="3e150-159">이 노드에는 새 작업이 예약되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="3e150-160">-Id</span><span class="sxs-lookup"><span data-stu-id="3e150-160">-Id</span></span>
<span data-ttu-id="3e150-161">태스크를 사용할 수 없는 계산 노드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="3e150-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3e150-162">-PoolId</span></span>
<span data-ttu-id="3e150-163">태스크를 사용할 수 없는 계산 노드를 포함하는 일괄 처리 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="3e150-164">*PoolId* 매개 변수를 사용하는 경우 동일한 명령에서 *ComputeNode* 매개 변수를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="3e150-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e150-165">CommonParameters</span></span>
<span data-ttu-id="3e150-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e150-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e150-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e150-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e150-168">입력</span><span class="sxs-lookup"><span data-stu-id="3e150-168">INPUTS</span></span>

### <span data-ttu-id="3e150-169">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e150-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="3e150-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e150-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3e150-171">출력</span><span class="sxs-lookup"><span data-stu-id="3e150-171">OUTPUTS</span></span>

### <span data-ttu-id="3e150-172">System.Void</span><span class="sxs-lookup"><span data-stu-id="3e150-172">System.Void</span></span>

## <span data-ttu-id="3e150-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e150-173">NOTES</span></span>

## <span data-ttu-id="3e150-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e150-174">RELATED LINKS</span></span>

[<span data-ttu-id="3e150-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3e150-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3e150-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="3e150-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


