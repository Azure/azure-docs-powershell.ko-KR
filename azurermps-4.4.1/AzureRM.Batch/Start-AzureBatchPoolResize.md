---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531840"
---
# <span data-ttu-id="57e8d-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="57e8d-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="57e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="57e8d-103">풀의 크기를 조정 하기 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57e8d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57e8d-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57e8d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57e8d-105">DESCRIPTION</span></span>
<span data-ttu-id="57e8d-106">**시작-AzureBatchPoolResize** cmdlet은 풀에서 Azure 일괄 처리 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="57e8d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="57e8d-107">EXAMPLES</span></span>

### <span data-ttu-id="57e8d-108">예제 1: 풀을 12 개 노드로 크기 조정</span><span class="sxs-lookup"><span data-stu-id="57e8d-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="57e8d-109">이 명령은 ID ContosoPool06가 있는 풀에서 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="57e8d-110">작업의 대상은 12 전용 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="57e8d-111">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="57e8d-112">예제 2: 할당 취소 옵션을 사용 하 여 풀 크기 조정</span><span class="sxs-lookup"><span data-stu-id="57e8d-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="57e8d-113">이 cmdlet은 풀을 5 개의 전용 계산 노드로 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="57e8d-114">명령은 Get-AzureBatchPool cmdlet을 사용 하 여 ID ContosoPool06 있는 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="57e8d-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 풀 개체를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="57e8d-116">이 명령은 풀에서 크기 조정 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="57e8d-117">대상은 5 전용 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="57e8d-118">명령에서 1 시간의 시간 초과 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="57e8d-119">명령에서 종료의 할당 취소 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="57e8d-120">변수</span><span class="sxs-lookup"><span data-stu-id="57e8d-120">PARAMETERS</span></span>

### <span data-ttu-id="57e8d-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="57e8d-121">-BatchContext</span></span>
<span data-ttu-id="57e8d-122">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="57e8d-123">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="57e8d-124">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="57e8d-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="57e8d-125">이 cmdlet이 시작 하는 크기 조정 작업에 대 한 할당 취소 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="57e8d-126">-Id</span><span class="sxs-lookup"><span data-stu-id="57e8d-126">-Id</span></span>
<span data-ttu-id="57e8d-127">이 cmdlet이 크기를 조정 하는 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="57e8d-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="57e8d-128">-ResizeTimeout</span></span>
<span data-ttu-id="57e8d-129">크기 조정 작업에 대 한 시간 초과 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="57e8d-130">이 시간에 따라 풀이 대상 크기에 도달 하지 않으면 크기 조정 작업이 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="57e8d-131">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="57e8d-131">-TargetDedicated</span></span>
<span data-ttu-id="57e8d-132">전용 계산 노드의 대상 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57e8d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e8d-133">-DefaultProfile</span></span>
<span data-ttu-id="57e8d-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57e8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e8d-135">CommonParameters</span></span>
<span data-ttu-id="57e8d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e8d-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e8d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e8d-138">입력</span><span class="sxs-lookup"><span data-stu-id="57e8d-138">INPUTS</span></span>

### <span data-ttu-id="57e8d-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="57e8d-139">BatchAccountContext</span></span>
<span data-ttu-id="57e8d-140">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="57e8d-141">이름</span><span class="sxs-lookup"><span data-stu-id="57e8d-141">String</span></span>
<span data-ttu-id="57e8d-142">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8d-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="57e8d-143">출력</span><span class="sxs-lookup"><span data-stu-id="57e8d-143">OUTPUTS</span></span>

## <span data-ttu-id="57e8d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="57e8d-144">NOTES</span></span>

## <span data-ttu-id="57e8d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57e8d-145">RELATED LINKS</span></span>

[<span data-ttu-id="57e8d-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="57e8d-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="57e8d-147">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="57e8d-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="57e8d-148">중지-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="57e8d-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="57e8d-149">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="57e8d-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


