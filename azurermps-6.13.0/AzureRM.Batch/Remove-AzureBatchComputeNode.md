---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 39bbc9102d72c469730fe494869bffe5f726b41a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531450"
---
# <span data-ttu-id="a55c9-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a55c9-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="a55c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a55c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a55c9-103">풀에서 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a55c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a55c9-104">SYNTAX</span></span>

### <span data-ttu-id="a55c9-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="a55c9-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a55c9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a55c9-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a55c9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a55c9-107">DESCRIPTION</span></span>
<span data-ttu-id="a55c9-108">**Remove-AzureBatchComputeNode** cmdlet은 풀에서 Azure 일괄 처리 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="a55c9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a55c9-109">EXAMPLES</span></span>

### <span data-ttu-id="a55c9-110">예제 1: 계산 노드 제거</span><span class="sxs-lookup"><span data-stu-id="a55c9-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="a55c9-111">이 명령은 ID Pool07가 있는 풀에서 지정 된 ID를 가진 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="a55c9-112">명령에서는 할당 취소 종료 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="a55c9-113">크기 조정 시간 초과 시간은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="a55c9-114">예제 2: 파이프라인을 사용 하 여 계산 노드 제거</span><span class="sxs-lookup"><span data-stu-id="a55c9-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="a55c9-115">이 명령은 Get-AzureBatchComputeNode cmdlet을 사용 하 여 ID Pool07를 가진 풀에서 지정 된 ID를 갖는 계산 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="a55c9-116">이 명령은 파이프라인을 사용 하 여 해당 노드를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="a55c9-117">현재 cmdlet은 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="a55c9-118">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a55c9-119">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a55c9-120">예제 3: 여러 노드 제거</span><span class="sxs-lookup"><span data-stu-id="a55c9-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="a55c9-121">이 명령은 ID Pool07가 있는 풀에서 두 개의 계산 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="a55c9-122">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a55c9-123">변수</span><span class="sxs-lookup"><span data-stu-id="a55c9-123">PARAMETERS</span></span>

### <span data-ttu-id="a55c9-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a55c9-124">-BatchContext</span></span>
<span data-ttu-id="a55c9-125">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a55c9-126">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a55c9-127">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a55c9-128">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a55c9-129">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a55c9-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a55c9-130">-ComputeNode</span></span>
<span data-ttu-id="a55c9-131">이 cmdlet이 제거 하는 계산 노드를 나타내는 **PSComputeNode** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a55c9-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="a55c9-132">-DeallocationOption</span></span>
<span data-ttu-id="a55c9-133">이 cmdlet이 시작 하는 제거 작업에 대 한 할당 취소 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="a55c9-134">기본 값은 Requeue입니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="a55c9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55c9-135">-DefaultProfile</span></span>
<span data-ttu-id="a55c9-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a55c9-137">-Force</span><span class="sxs-lookup"><span data-stu-id="a55c9-137">-Force</span></span>
<span data-ttu-id="a55c9-138">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a55c9-139">-Id</span><span class="sxs-lookup"><span data-stu-id="a55c9-139">-Ids</span></span>
<span data-ttu-id="a55c9-140">이 cmdlet이 풀에서 제거 하는 계산 노드의 Id 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="a55c9-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a55c9-141">-PoolId</span></span>
<span data-ttu-id="a55c9-142">이 cmdlet이 제거 하는 계산 노드를 포함 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a55c9-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="a55c9-143">-ResizeTimeout</span></span>
<span data-ttu-id="a55c9-144">풀에서 계산 노드 제거에 대 한 시간 초과 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="a55c9-145">기본값은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="a55c9-146">최 솟 값은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="a55c9-147">-확인</span><span class="sxs-lookup"><span data-stu-id="a55c9-147">-Confirm</span></span>
<span data-ttu-id="a55c9-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a55c9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a55c9-149">-WhatIf</span></span>
<span data-ttu-id="a55c9-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a55c9-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a55c9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55c9-152">CommonParameters</span></span>
<span data-ttu-id="a55c9-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a55c9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55c9-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a55c9-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55c9-155">입력</span><span class="sxs-lookup"><span data-stu-id="a55c9-155">INPUTS</span></span>

### <span data-ttu-id="a55c9-156">Microsoft.Azure.Commands.Batch. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a55c9-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="a55c9-157">매개 변수: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a55c9-157">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="a55c9-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a55c9-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a55c9-159">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a55c9-159">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a55c9-160">출력</span><span class="sxs-lookup"><span data-stu-id="a55c9-160">OUTPUTS</span></span>

### <span data-ttu-id="a55c9-161">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="a55c9-161">System.Void</span></span>

## <span data-ttu-id="a55c9-162">상속자</span><span class="sxs-lookup"><span data-stu-id="a55c9-162">NOTES</span></span>

## <span data-ttu-id="a55c9-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a55c9-163">RELATED LINKS</span></span>

[<span data-ttu-id="a55c9-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a55c9-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a55c9-165">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a55c9-165">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="a55c9-166">다시 시작-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a55c9-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


