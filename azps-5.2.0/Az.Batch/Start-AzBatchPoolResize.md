---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352226"
---
# <span data-ttu-id="8e769-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="8e769-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="8e769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e769-102">SYNOPSIS</span></span>
<span data-ttu-id="8e769-103">풀의 수를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="8e769-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e769-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e769-105">설명</span><span class="sxs-lookup"><span data-stu-id="8e769-105">DESCRIPTION</span></span>
<span data-ttu-id="8e769-106">**Start-AzBatchPoolResize** cmdlet은 풀에서 Azure Batch 크기 변경 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="8e769-107">예제</span><span class="sxs-lookup"><span data-stu-id="8e769-107">EXAMPLES</span></span>

### <span data-ttu-id="8e769-108">예제 1: 풀을 12개 노드로 다시 설정</span><span class="sxs-lookup"><span data-stu-id="8e769-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="8e769-109">이 명령은 ID ContosoPool06이 있는 풀에서 배정량 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="8e769-110">작업에 대한 대상은 12개 전용 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="8e769-111">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8e769-112">예제 2: 재배치 옵션을 사용하여 풀의 양조</span><span class="sxs-lookup"><span data-stu-id="8e769-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="8e769-113">이 cmdlet은 풀의 크기는 5개의 전용 계산 노드로 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="8e769-114">이 명령은 Get-AzBatchPool cmdlet을 사용하여 ContosoPool06 ID가 있는 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="8e769-115">이 명령은 파이프라인 연산자를 사용하여 해당 풀 개체를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e769-116">이 명령은 풀에 대한 [사소한 작업]을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="8e769-117">대상은 5개의 전용 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="8e769-118">이 명령은 1시간의 시간제한 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="8e769-119">이 명령은 Terminate의 재배치 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="8e769-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e769-120">PARAMETERS</span></span>

### <span data-ttu-id="8e769-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8e769-121">-BatchContext</span></span>
<span data-ttu-id="8e769-122">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e769-123">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8e769-124">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8e769-125">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8e769-126">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8e769-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="8e769-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="8e769-128">이 cmdlet이 시작하는 크기 조정 작업에 대한 재배치 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8e769-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e769-129">-DefaultProfile</span></span>
<span data-ttu-id="8e769-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e769-131">-Id</span><span class="sxs-lookup"><span data-stu-id="8e769-131">-Id</span></span>
<span data-ttu-id="8e769-132">이 cmdlet의 크기는 풀의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e769-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="8e769-133">-ResizeTimeout</span></span>
<span data-ttu-id="8e769-134">크기 조정 작업에 대한 시간제한 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="8e769-135">이 시간까지 풀이 대상 크기에 도달하지 않는 경우 크기 변경 작업이 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="8e769-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="8e769-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="8e769-137">대상 전용 계산 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e769-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="8e769-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="8e769-139">우선 순위가 낮은 대상 계산 노드의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e769-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e769-140">CommonParameters</span></span>
<span data-ttu-id="8e769-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e769-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e769-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e769-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e769-143">입력</span><span class="sxs-lookup"><span data-stu-id="8e769-143">INPUTS</span></span>

### <span data-ttu-id="8e769-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8e769-144">System.String</span></span>

### <span data-ttu-id="8e769-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e769-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e769-146">출력</span><span class="sxs-lookup"><span data-stu-id="8e769-146">OUTPUTS</span></span>

### <span data-ttu-id="8e769-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="8e769-147">System.Void</span></span>

## <span data-ttu-id="8e769-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e769-148">NOTES</span></span>

## <span data-ttu-id="8e769-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e769-149">RELATED LINKS</span></span>

[<span data-ttu-id="8e769-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8e769-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8e769-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8e769-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="8e769-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="8e769-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="8e769-153">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e769-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
