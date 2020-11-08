---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: c68911de8d01a654593e72b98ba5d53bf40c76ed
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880190"
---
# <span data-ttu-id="daf5f-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="daf5f-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="daf5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daf5f-102">SYNOPSIS</span></span>
<span data-ttu-id="daf5f-103">풀의 크기를 조정 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="daf5f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="daf5f-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daf5f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="daf5f-105">DESCRIPTION</span></span>
<span data-ttu-id="daf5f-106">**AzBatchPoolResize** cmdlet은 풀에서 Azure 일괄 처리 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="daf5f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="daf5f-107">EXAMPLES</span></span>

### <span data-ttu-id="daf5f-108">예제 1: 풀을 12 개 노드로 크기 조정</span><span class="sxs-lookup"><span data-stu-id="daf5f-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="daf5f-109">이 명령은 ID ContosoPool06가 있는 풀에서 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="daf5f-110">작업의 대상은 12 전용 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="daf5f-111">Get-AzBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="daf5f-112">예제 2: 할당 취소 옵션을 사용 하 여 풀 크기 조정</span><span class="sxs-lookup"><span data-stu-id="daf5f-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="daf5f-113">이 cmdlet은 풀을 5 개의 전용 계산 노드로 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="daf5f-114">명령은 Get-AzBatchPool cmdlet을 사용 하 여 ID ContosoPool06 있는 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="daf5f-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 풀 개체를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="daf5f-116">이 명령은 풀에서 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="daf5f-117">대상은 5 전용 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="daf5f-118">명령에서 1 시간의 시간 초과 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="daf5f-119">명령에서 종료의 할당 취소 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="daf5f-120">변수</span><span class="sxs-lookup"><span data-stu-id="daf5f-120">PARAMETERS</span></span>

### <span data-ttu-id="daf5f-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="daf5f-121">-BatchContext</span></span>
<span data-ttu-id="daf5f-122">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="daf5f-123">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="daf5f-124">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-124">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="daf5f-125">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="daf5f-126">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="daf5f-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="daf5f-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="daf5f-128">이 cmdlet이 시작 하는 크기 조정 작업에 대 한 할당 취소 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="daf5f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf5f-129">-DefaultProfile</span></span>
<span data-ttu-id="daf5f-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daf5f-131">-Id</span><span class="sxs-lookup"><span data-stu-id="daf5f-131">-Id</span></span>
<span data-ttu-id="daf5f-132">이 cmdlet이 크기를 조정 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="daf5f-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="daf5f-133">-ResizeTimeout</span></span>
<span data-ttu-id="daf5f-134">크기 조정 작업에 대 한 시간 초과 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="daf5f-135">이 시간에 따라 풀이 대상 크기에 도달 하지 않으면 크기 조정 작업이 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="daf5f-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="daf5f-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="daf5f-137">대상 전용 계산 노드의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="daf5f-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="daf5f-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="daf5f-139">대상 우선 순위가 낮은 계산 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="daf5f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf5f-140">CommonParameters</span></span>
<span data-ttu-id="daf5f-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf5f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf5f-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf5f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf5f-143">입력</span><span class="sxs-lookup"><span data-stu-id="daf5f-143">INPUTS</span></span>

### <span data-ttu-id="daf5f-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="daf5f-144">System.String</span></span>

### <span data-ttu-id="daf5f-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="daf5f-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="daf5f-146">출력</span><span class="sxs-lookup"><span data-stu-id="daf5f-146">OUTPUTS</span></span>

### <span data-ttu-id="daf5f-147">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="daf5f-147">System.Void</span></span>

## <span data-ttu-id="daf5f-148">상속자</span><span class="sxs-lookup"><span data-stu-id="daf5f-148">NOTES</span></span>

## <span data-ttu-id="daf5f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daf5f-149">RELATED LINKS</span></span>

[<span data-ttu-id="daf5f-150">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="daf5f-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="daf5f-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="daf5f-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="daf5f-152">중지-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="daf5f-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="daf5f-153">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="daf5f-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

