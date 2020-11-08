---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042433"
---
# <span data-ttu-id="38bd3-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="38bd3-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="38bd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="38bd3-103">풀에서 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="38bd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="38bd3-104">SYNTAX</span></span>

### <span data-ttu-id="38bd3-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="38bd3-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38bd3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="38bd3-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38bd3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="38bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="38bd3-108">**Remove-AzBatchComputeNode** cmdlet은 풀에서 Azure 일괄 처리 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="38bd3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="38bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="38bd3-110">예제 1: 계산 노드 제거</span><span class="sxs-lookup"><span data-stu-id="38bd3-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="38bd3-111">이 명령은 ID Pool07가 있는 풀에서 지정 된 ID를 가진 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="38bd3-112">명령에서는 할당 취소 종료 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="38bd3-113">크기 조정 시간 초과 시간은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="38bd3-114">예제 2: 파이프라인을 사용 하 여 계산 노드 제거</span><span class="sxs-lookup"><span data-stu-id="38bd3-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="38bd3-115">이 명령은 Get-AzBatchComputeNode cmdlet을 사용 하 여 ID Pool07를 가진 풀에서 지정 된 ID를 갖는 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="38bd3-116">이 명령은 파이프라인을 사용 하 여 해당 노드를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="38bd3-117">현재 cmdlet은 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="38bd3-118">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="38bd3-119">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="38bd3-120">예제 3: 여러 노드 제거</span><span class="sxs-lookup"><span data-stu-id="38bd3-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="38bd3-121">이 명령은 ID Pool07가 있는 풀에서 두 개의 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="38bd3-122">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="38bd3-123">변수</span><span class="sxs-lookup"><span data-stu-id="38bd3-123">PARAMETERS</span></span>

### <span data-ttu-id="38bd3-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="38bd3-124">-BatchContext</span></span>
<span data-ttu-id="38bd3-125">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="38bd3-126">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="38bd3-127">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="38bd3-128">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="38bd3-129">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="38bd3-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="38bd3-130">-ComputeNode</span></span>
<span data-ttu-id="38bd3-131">이 cmdlet이 제거 하는 계산 노드를 나타내는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38bd3-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="38bd3-132">-DeallocationOption</span></span>
<span data-ttu-id="38bd3-133">이 cmdlet이 시작 하는 제거 작업에 대 한 할당 취소 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="38bd3-134">기본 값은 Requeue입니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-134">The default value is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bd3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bd3-135">-DefaultProfile</span></span>
<span data-ttu-id="38bd3-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38bd3-137">-Force</span><span class="sxs-lookup"><span data-stu-id="38bd3-137">-Force</span></span>
<span data-ttu-id="38bd3-138">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bd3-139">-Id</span><span class="sxs-lookup"><span data-stu-id="38bd3-139">-Ids</span></span>
<span data-ttu-id="38bd3-140">이 cmdlet이 풀에서 제거 하는 계산 노드의 Id 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bd3-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="38bd3-141">-PoolId</span></span>
<span data-ttu-id="38bd3-142">이 cmdlet이 제거 하는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38bd3-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="38bd3-143">-ResizeTimeout</span></span>
<span data-ttu-id="38bd3-144">풀에서 계산 노드 제거에 대 한 시간 초과 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="38bd3-145">기본값은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="38bd3-146">최 솟 값은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bd3-147">-확인</span><span class="sxs-lookup"><span data-stu-id="38bd3-147">-Confirm</span></span>
<span data-ttu-id="38bd3-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bd3-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bd3-149">-WhatIf</span></span>
<span data-ttu-id="38bd3-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38bd3-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bd3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bd3-152">CommonParameters</span></span>
<span data-ttu-id="38bd3-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38bd3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bd3-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="38bd3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bd3-155">입력</span><span class="sxs-lookup"><span data-stu-id="38bd3-155">INPUTS</span></span>

### <span data-ttu-id="38bd3-156">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="38bd3-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="38bd3-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="38bd3-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="38bd3-158">출력</span><span class="sxs-lookup"><span data-stu-id="38bd3-158">OUTPUTS</span></span>

### <span data-ttu-id="38bd3-159">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="38bd3-159">System.Void</span></span>

## <span data-ttu-id="38bd3-160">상속자</span><span class="sxs-lookup"><span data-stu-id="38bd3-160">NOTES</span></span>

## <span data-ttu-id="38bd3-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38bd3-161">RELATED LINKS</span></span>

[<span data-ttu-id="38bd3-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="38bd3-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="38bd3-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="38bd3-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="38bd3-164">다시 시작-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="38bd3-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


