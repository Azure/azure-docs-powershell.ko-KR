---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: 6732fb89775cea289bf82a5675a482f94b7f95ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358338"
---
# <span data-ttu-id="3d652-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3d652-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="3d652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d652-102">SYNOPSIS</span></span>
<span data-ttu-id="3d652-103">풀에서 자동 크기 조정 수식의 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="3d652-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d652-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d652-105">설명</span><span class="sxs-lookup"><span data-stu-id="3d652-105">DESCRIPTION</span></span>
<span data-ttu-id="3d652-106">**Test-AzBatchAutoScale** cmdlet은 지정된 풀에서 자동 크기 조정 수식의 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="3d652-107">예제</span><span class="sxs-lookup"><span data-stu-id="3d652-107">EXAMPLES</span></span>

### <span data-ttu-id="3d652-108">예제 1: 풀에서 자동 조정 수식 평가</span><span class="sxs-lookup"><span data-stu-id="3d652-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="3d652-109">첫 번째 명령은 예제에서 사용할 수 $Formula 변수에 수식을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="3d652-110">두 번째 명령은 ID ContosoPool이 있는 풀에서 자동 조정 수식을 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="3d652-111">마지막 명령은 표준 **점** 구문을 사용하여 결과를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="3d652-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d652-112">PARAMETERS</span></span>

### <span data-ttu-id="3d652-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="3d652-113">-AutoScaleFormula</span></span>
<span data-ttu-id="3d652-114">풀에서 원하는 계산 노드 수에 대한 수식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="3d652-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3d652-115">-BatchContext</span></span>
<span data-ttu-id="3d652-116">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3d652-117">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3d652-118">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3d652-119">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3d652-120">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3d652-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d652-121">-DefaultProfile</span></span>
<span data-ttu-id="3d652-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d652-123">-Id</span><span class="sxs-lookup"><span data-stu-id="3d652-123">-Id</span></span>
<span data-ttu-id="3d652-124">자동 크기 조정을 테스트할 풀의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="3d652-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d652-125">CommonParameters</span></span>
<span data-ttu-id="3d652-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d652-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d652-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d652-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d652-128">입력</span><span class="sxs-lookup"><span data-stu-id="3d652-128">INPUTS</span></span>

### <span data-ttu-id="3d652-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3d652-129">System.String</span></span>

### <span data-ttu-id="3d652-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3d652-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3d652-131">출력</span><span class="sxs-lookup"><span data-stu-id="3d652-131">OUTPUTS</span></span>

### <span data-ttu-id="3d652-132">Microsoft.Azure.Commands.Batch. Models.PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="3d652-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="3d652-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d652-133">NOTES</span></span>

## <span data-ttu-id="3d652-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d652-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d652-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3d652-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="3d652-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3d652-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="3d652-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3d652-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3d652-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d652-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
