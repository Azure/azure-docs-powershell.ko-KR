---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 3dc458c5b23e3bd6f8bde39e02152e8c2b76f6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532500"
---
# <span data-ttu-id="16bfe-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="16bfe-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="16bfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="16bfe-103">풀의 자동 크기 조정 수식 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16bfe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16bfe-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16bfe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="16bfe-106">**테스트-AzureBatchAutoScale 크기 조정** cmdlet은 지정 된 풀에 대 한 자동 크기 조정 수식의 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="16bfe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="16bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="16bfe-108">예제 1: 풀에서 자동 크기 조정 수식 평가</span><span class="sxs-lookup"><span data-stu-id="16bfe-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="16bfe-109">첫 번째 명령은 예제에서 사용할 $Formula 변수에 수식을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="16bfe-110">두 번째 명령은 ID ContosoPool가 있는 풀에서 자동 크기 조정 수식을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="16bfe-111">마지막 명령은 표준 도트 구문을 사용 하 여 **결과** 를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="16bfe-112">변수</span><span class="sxs-lookup"><span data-stu-id="16bfe-112">PARAMETERS</span></span>

### <span data-ttu-id="16bfe-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="16bfe-113">-AutoScaleFormula</span></span>
<span data-ttu-id="16bfe-114">풀에 있는 계산 노드의 원하는 수에 대 한 수식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16bfe-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="16bfe-115">-BatchContext</span></span>
<span data-ttu-id="16bfe-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16bfe-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="16bfe-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="16bfe-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="16bfe-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="16bfe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16bfe-121">-DefaultProfile</span></span>
<span data-ttu-id="16bfe-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16bfe-123">-Id</span><span class="sxs-lookup"><span data-stu-id="16bfe-123">-Id</span></span>
<span data-ttu-id="16bfe-124">자동 크기 조정을 테스트할 풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="16bfe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16bfe-125">CommonParameters</span></span>
<span data-ttu-id="16bfe-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16bfe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16bfe-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16bfe-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16bfe-128">입력</span><span class="sxs-lookup"><span data-stu-id="16bfe-128">INPUTS</span></span>

### <span data-ttu-id="16bfe-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16bfe-129">System.String</span></span>

### <span data-ttu-id="16bfe-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="16bfe-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="16bfe-131">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="16bfe-131">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="16bfe-132">출력</span><span class="sxs-lookup"><span data-stu-id="16bfe-132">OUTPUTS</span></span>

### <span data-ttu-id="16bfe-133">Microsoft.Azure.Commands.Batch. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="16bfe-133">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="16bfe-134">상속자</span><span class="sxs-lookup"><span data-stu-id="16bfe-134">NOTES</span></span>

## <span data-ttu-id="16bfe-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16bfe-135">RELATED LINKS</span></span>

[<span data-ttu-id="16bfe-136">Disable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="16bfe-136">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="16bfe-137">Enable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="16bfe-137">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="16bfe-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="16bfe-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="16bfe-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="16bfe-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


