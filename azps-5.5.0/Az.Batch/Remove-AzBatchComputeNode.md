---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205192"
---
# <span data-ttu-id="ab057-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ab057-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="ab057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab057-102">SYNOPSIS</span></span>
<span data-ttu-id="ab057-103">풀에서 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="ab057-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab057-104">SYNTAX</span></span>

### <span data-ttu-id="ab057-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab057-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab057-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ab057-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab057-107">설명</span><span class="sxs-lookup"><span data-stu-id="ab057-107">DESCRIPTION</span></span>
<span data-ttu-id="ab057-108">**Remove-AzBatchComputeNode** cmdlet은 풀에서 Azure Batch 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="ab057-109">예제</span><span class="sxs-lookup"><span data-stu-id="ab057-109">EXAMPLES</span></span>

### <span data-ttu-id="ab057-110">예제 1: 계산 노드 제거</span><span class="sxs-lookup"><span data-stu-id="ab057-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="ab057-111">이 명령은 ID Pool07이 있는 풀에서 지정된 ID가 있는 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="ab057-112">이 명령은 Deallocation 종료 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="ab057-113">시간제한은 10분입니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="ab057-114">예제 2: 파이프라인을 사용하여 계산 노드 제거</span><span class="sxs-lookup"><span data-stu-id="ab057-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="ab057-115">이 명령은 Get-AzBatchComputeNode cmdlet을 사용하여 ID Pool07이 있는 풀에서 지정된 ID가 있는 계산 노드를 Get-AzBatchComputeNode 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="ab057-116">이 명령은 파이프라인을 사용하여 해당 노드를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="ab057-117">현재 cmdlet은 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="ab057-118">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="ab057-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ab057-119">따라서 명령은 확인을 요청하는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ab057-120">예제 3: 여러 노드 제거</span><span class="sxs-lookup"><span data-stu-id="ab057-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="ab057-121">이 명령은 ID Pool07이 있는 풀에서 두 개의 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="ab057-122">이 명령은 확인을 요청하는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ab057-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab057-123">PARAMETERS</span></span>

### <span data-ttu-id="ab057-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ab057-124">-BatchContext</span></span>
<span data-ttu-id="ab057-125">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ab057-126">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ab057-127">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ab057-128">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ab057-129">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ab057-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ab057-130">-ComputeNode</span></span>
<span data-ttu-id="ab057-131">이 cmdlet에서 제거하는 계산 노드를 나타내는 **PSComputeNode** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ab057-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="ab057-132">-DeallocationOption</span></span>
<span data-ttu-id="ab057-133">이 cmdlet이 시작하는 제거 작업에 대한 재배치 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="ab057-134">기본값은 다시queue입니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="ab057-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab057-135">-DefaultProfile</span></span>
<span data-ttu-id="ab057-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab057-137">-Force</span><span class="sxs-lookup"><span data-stu-id="ab057-137">-Force</span></span>
<span data-ttu-id="ab057-138">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab057-139">-ID</span><span class="sxs-lookup"><span data-stu-id="ab057-139">-Ids</span></span>
<span data-ttu-id="ab057-140">이 cmdlet이 풀에서 제거하는 계산 노드의 ID 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="ab057-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ab057-141">-PoolId</span></span>
<span data-ttu-id="ab057-142">이 cmdlet에서 제거하는 계산 노드를 포함하는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ab057-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="ab057-143">-ResizeTimeout</span></span>
<span data-ttu-id="ab057-144">풀에서 계산 노드를 제거하기 위한 시간제한 간격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="ab057-145">기본값은 10분입니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="ab057-146">최소값은 5분입니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="ab057-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab057-147">-Confirm</span></span>
<span data-ttu-id="ab057-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab057-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab057-149">-WhatIf</span></span>
<span data-ttu-id="ab057-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ab057-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab057-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab057-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab057-152">CommonParameters</span></span>
<span data-ttu-id="ab057-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab057-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab057-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab057-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab057-155">입력</span><span class="sxs-lookup"><span data-stu-id="ab057-155">INPUTS</span></span>

### <span data-ttu-id="ab057-156">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ab057-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ab057-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab057-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ab057-158">출력</span><span class="sxs-lookup"><span data-stu-id="ab057-158">OUTPUTS</span></span>

### <span data-ttu-id="ab057-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="ab057-159">System.Void</span></span>

## <span data-ttu-id="ab057-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab057-160">NOTES</span></span>

## <span data-ttu-id="ab057-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab057-161">RELATED LINKS</span></span>

[<span data-ttu-id="ab057-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ab057-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ab057-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ab057-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ab057-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ab057-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


