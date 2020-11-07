---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: dcac72f8ca362ea87d464e024d6e77b2b3b61425
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880186"
---
# <span data-ttu-id="baa11-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="baa11-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="baa11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baa11-102">SYNOPSIS</span></span>
<span data-ttu-id="baa11-103">풀의 자동 크기 조정 수식 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="baa11-104">구문과</span><span class="sxs-lookup"><span data-stu-id="baa11-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baa11-105">설명은</span><span class="sxs-lookup"><span data-stu-id="baa11-105">DESCRIPTION</span></span>
<span data-ttu-id="baa11-106">**AzBatchAutoScale** cmdlet은 지정 된 풀에 대 한 자동 크기 조정 수식의 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="baa11-107">예제의</span><span class="sxs-lookup"><span data-stu-id="baa11-107">EXAMPLES</span></span>

### <span data-ttu-id="baa11-108">예제 1: 풀에서 자동 크기 조정 수식 평가</span><span class="sxs-lookup"><span data-stu-id="baa11-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="baa11-109">첫 번째 명령은 예제에서 사용할 $Formula 변수에 수식을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="baa11-110">두 번째 명령은 ID ContosoPool가 있는 풀에서 자동 크기 조정 수식을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="baa11-111">마지막 명령은 표준 도트 구문을 사용 하 여 **결과** 를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="baa11-112">변수</span><span class="sxs-lookup"><span data-stu-id="baa11-112">PARAMETERS</span></span>

### <span data-ttu-id="baa11-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="baa11-113">-AutoScaleFormula</span></span>
<span data-ttu-id="baa11-114">풀에 있는 계산 노드의 원하는 수에 대 한 수식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="baa11-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="baa11-115">-BatchContext</span></span>
<span data-ttu-id="baa11-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="baa11-117">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="baa11-118">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="baa11-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="baa11-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="baa11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa11-121">-DefaultProfile</span></span>
<span data-ttu-id="baa11-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baa11-123">-Id</span><span class="sxs-lookup"><span data-stu-id="baa11-123">-Id</span></span>
<span data-ttu-id="baa11-124">자동 크기 조정을 테스트할 풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="baa11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa11-125">CommonParameters</span></span>
<span data-ttu-id="baa11-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="baa11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa11-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa11-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa11-128">입력</span><span class="sxs-lookup"><span data-stu-id="baa11-128">INPUTS</span></span>

### <span data-ttu-id="baa11-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="baa11-129">System.String</span></span>

### <span data-ttu-id="baa11-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="baa11-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="baa11-131">출력</span><span class="sxs-lookup"><span data-stu-id="baa11-131">OUTPUTS</span></span>

### <span data-ttu-id="baa11-132">Microsoft.Azure.Commands.Batch. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="baa11-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="baa11-133">상속자</span><span class="sxs-lookup"><span data-stu-id="baa11-133">NOTES</span></span>

## <span data-ttu-id="baa11-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="baa11-134">RELATED LINKS</span></span>

[<span data-ttu-id="baa11-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="baa11-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="baa11-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="baa11-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="baa11-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="baa11-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="baa11-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="baa11-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


