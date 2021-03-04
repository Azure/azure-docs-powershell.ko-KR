---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 7e2b2bca042573ec96fefdf85e5077ec1138d1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956027"
---
# <span data-ttu-id="beabe-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="beabe-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="beabe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beabe-102">SYNOPSIS</span></span>
<span data-ttu-id="beabe-103">풀에서 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="beabe-104">구문</span><span class="sxs-lookup"><span data-stu-id="beabe-104">SYNTAX</span></span>

### <span data-ttu-id="beabe-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="beabe-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="beabe-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="beabe-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="beabe-107">설명</span><span class="sxs-lookup"><span data-stu-id="beabe-107">DESCRIPTION</span></span>
<span data-ttu-id="beabe-108">**Remove-AzBatchComputeNode** cmdlet은 풀에서 Azure Batch 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="beabe-109">예제</span><span class="sxs-lookup"><span data-stu-id="beabe-109">EXAMPLES</span></span>

### <span data-ttu-id="beabe-110">예제 1: 계산 노드 제거</span><span class="sxs-lookup"><span data-stu-id="beabe-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="beabe-111">이 명령은 ID Pool07이 있는 풀에서 지정된 ID가 있는 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="beabe-112">명령은 거래 위치 종료 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="beabe-113">시간의 재조정 시간은 10분입니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="beabe-114">예제 2: 파이프라인을 사용하여 계산 노드 제거</span><span class="sxs-lookup"><span data-stu-id="beabe-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="beabe-115">이 명령은 Get-AzBatchComputeNode cmdlet을 사용하여 ID Pool07이 있는 풀에서 지정된 ID가 있는 계산 노드를 Get-AzBatchComputeNode 합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="beabe-116">명령은 파이프라인을 사용하여 해당 노드를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="beabe-117">현재 cmdlet은 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="beabe-118">명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="beabe-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="beabe-119">따라서 명령을 확인하라는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="beabe-120">예제 3: 여러 노드 제거</span><span class="sxs-lookup"><span data-stu-id="beabe-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="beabe-121">이 명령은 ID Pool07이 있는 풀에서 두 개의 계산 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="beabe-122">명령은 확인을 묻는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="beabe-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="beabe-123">PARAMETERS</span></span>

### <span data-ttu-id="beabe-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="beabe-124">-BatchContext</span></span>
<span data-ttu-id="beabe-125">Batch 서비스와 상호 작용하는 데 이 cmdlet이 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="beabe-126">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻으면 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="beabe-127">대신 공유 키 인증을 사용 Get-AzBatchAccountKey cmdlet을 사용하여 액세스 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="beabe-128">공유 키 인증을 사용하는 경우 기본 액세스 키는 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="beabe-129">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="beabe-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="beabe-130">-ComputeNode</span></span>
<span data-ttu-id="beabe-131">이 cmdlet이 제거한 계산 노드를 나타내는 **PSComputeNode** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="beabe-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="beabe-132">-DeallocationOption</span></span>
<span data-ttu-id="beabe-133">이 cmdlet이 시작하는 제거 작업에 대한 대리점 지정 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="beabe-134">기본값은 다시 큐어입니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="beabe-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beabe-135">-DefaultProfile</span></span>
<span data-ttu-id="beabe-136">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beabe-137">-Force</span><span class="sxs-lookup"><span data-stu-id="beabe-137">-Force</span></span>
<span data-ttu-id="beabe-138">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="beabe-139">-ID</span><span class="sxs-lookup"><span data-stu-id="beabe-139">-Ids</span></span>
<span data-ttu-id="beabe-140">이 cmdlet이 풀에서 제거하는 계산 노드의 ID 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="beabe-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="beabe-141">-PoolId</span></span>
<span data-ttu-id="beabe-142">이 cmdlet이 제거하는 계산 노드가 포함된 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="beabe-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="beabe-143">-ResizeTimeout</span></span>
<span data-ttu-id="beabe-144">풀에서 계산 노드를 제거하기 위한 시간제한 간격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="beabe-145">기본값은 10분입니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="beabe-146">최소 값은 5분입니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="beabe-147">-확인</span><span class="sxs-lookup"><span data-stu-id="beabe-147">-Confirm</span></span>
<span data-ttu-id="beabe-148">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beabe-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beabe-149">-WhatIf</span></span>
<span data-ttu-id="beabe-150">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beabe-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beabe-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beabe-152">CommonParameters</span></span>
<span data-ttu-id="beabe-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="beabe-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beabe-154">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="beabe-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beabe-155">입력</span><span class="sxs-lookup"><span data-stu-id="beabe-155">INPUTS</span></span>

### <span data-ttu-id="beabe-156">Microsoft.Azure.Commands.Bat. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="beabe-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="beabe-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="beabe-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="beabe-158">출력</span><span class="sxs-lookup"><span data-stu-id="beabe-158">OUTPUTS</span></span>

### <span data-ttu-id="beabe-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="beabe-159">System.Void</span></span>

## <span data-ttu-id="beabe-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="beabe-160">NOTES</span></span>

## <span data-ttu-id="beabe-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="beabe-161">RELATED LINKS</span></span>

[<span data-ttu-id="beabe-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="beabe-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="beabe-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="beabe-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="beabe-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="beabe-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


