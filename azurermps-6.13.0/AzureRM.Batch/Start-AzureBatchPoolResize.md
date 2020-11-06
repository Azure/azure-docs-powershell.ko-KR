---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/start-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: c635061ac19b0fcc9543222da176324f84bea3a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531440"
---
# <span data-ttu-id="fd425-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="fd425-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="fd425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd425-102">SYNOPSIS</span></span>
<span data-ttu-id="fd425-103">풀의 크기를 조정 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd425-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd425-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd425-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fd425-105">DESCRIPTION</span></span>
<span data-ttu-id="fd425-106">**시작-AzureBatchPoolResize** cmdlet은 풀에서 Azure 일괄 처리 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="fd425-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fd425-107">EXAMPLES</span></span>

### <span data-ttu-id="fd425-108">예제 1: 풀을 12 개 노드로 크기 조정</span><span class="sxs-lookup"><span data-stu-id="fd425-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="fd425-109">이 명령은 ID ContosoPool06가 있는 풀에서 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="fd425-110">작업의 대상은 12 전용 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="fd425-111">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fd425-112">예제 2: 할당 취소 옵션을 사용 하 여 풀 크기 조정</span><span class="sxs-lookup"><span data-stu-id="fd425-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="fd425-113">이 cmdlet은 풀을 5 개의 전용 계산 노드로 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="fd425-114">명령은 Get-AzureBatchPool cmdlet을 사용 하 여 ID ContosoPool06 있는 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="fd425-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 풀 개체를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fd425-116">이 명령은 풀에서 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="fd425-117">대상은 5 전용 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="fd425-118">명령에서 1 시간의 시간 초과 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="fd425-119">명령에서 종료의 할당 취소 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="fd425-120">변수</span><span class="sxs-lookup"><span data-stu-id="fd425-120">PARAMETERS</span></span>

### <span data-ttu-id="fd425-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fd425-121">-BatchContext</span></span>
<span data-ttu-id="fd425-122">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fd425-123">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-123">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fd425-124">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-124">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fd425-125">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fd425-126">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fd425-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="fd425-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="fd425-128">이 cmdlet이 시작 하는 크기 조정 작업에 대 한 할당 취소 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="fd425-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd425-129">-DefaultProfile</span></span>
<span data-ttu-id="fd425-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd425-131">-Id</span><span class="sxs-lookup"><span data-stu-id="fd425-131">-Id</span></span>
<span data-ttu-id="fd425-132">이 cmdlet이 크기를 조정 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="fd425-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="fd425-133">-ResizeTimeout</span></span>
<span data-ttu-id="fd425-134">크기 조정 작업에 대 한 시간 초과 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="fd425-135">이 시간에 따라 풀이 대상 크기에 도달 하지 않으면 크기 조정 작업이 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="fd425-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="fd425-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="fd425-137">대상 전용 계산 노드의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="fd425-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="fd425-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="fd425-139">대상 우선 순위가 낮은 계산 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="fd425-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd425-140">CommonParameters</span></span>
<span data-ttu-id="fd425-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd425-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd425-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd425-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd425-143">입력</span><span class="sxs-lookup"><span data-stu-id="fd425-143">INPUTS</span></span>

### <span data-ttu-id="fd425-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd425-144">System.String</span></span>

### <span data-ttu-id="fd425-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fd425-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="fd425-146">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd425-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="fd425-147">출력</span><span class="sxs-lookup"><span data-stu-id="fd425-147">OUTPUTS</span></span>

### <span data-ttu-id="fd425-148">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="fd425-148">System.Void</span></span>

## <span data-ttu-id="fd425-149">상속자</span><span class="sxs-lookup"><span data-stu-id="fd425-149">NOTES</span></span>

## <span data-ttu-id="fd425-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd425-150">RELATED LINKS</span></span>

[<span data-ttu-id="fd425-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fd425-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fd425-152">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="fd425-152">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="fd425-153">중지-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="fd425-153">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="fd425-154">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fd425-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


