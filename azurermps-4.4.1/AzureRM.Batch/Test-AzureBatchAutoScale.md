---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 2ab8ca197c1d78980e1683f9572f6d3f6d4d55fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702074"
---
# <span data-ttu-id="67a3f-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="67a3f-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="67a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="67a3f-103">풀의 자동 크기 조정 수식 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67a3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67a3f-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67a3f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="67a3f-106">**테스트-AzureBatchAutoScale 크기 조정** cmdlet은 지정 된 풀에 대 한 자동 크기 조정 수식의 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="67a3f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="67a3f-107">EXAMPLES</span></span>

### <span data-ttu-id="67a3f-108">예제 1: 풀에서 자동 크기 조정 수식 평가</span><span class="sxs-lookup"><span data-stu-id="67a3f-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="67a3f-109">첫 번째 명령은 예제에서 사용할 $Formula 변수에 수식을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="67a3f-110">두 번째 명령은 ID ContosoPool가 있는 풀에서 자동 크기 조정 수식을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="67a3f-111">마지막 명령은 표준 도트 구문을 사용 하 여 **결과** 를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="67a3f-112">변수</span><span class="sxs-lookup"><span data-stu-id="67a3f-112">PARAMETERS</span></span>

### <span data-ttu-id="67a3f-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="67a3f-113">-AutoScaleFormula</span></span>
<span data-ttu-id="67a3f-114">풀에 있는 계산 노드의 원하는 수에 대 한 수식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="67a3f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="67a3f-115">-BatchContext</span></span>
<span data-ttu-id="67a3f-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="67a3f-117">구독에 대 한 선택 키를 포함 하는 **Batchaccountcontext** 개체를 가져오려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="67a3f-118">-Id</span><span class="sxs-lookup"><span data-stu-id="67a3f-118">-Id</span></span>
<span data-ttu-id="67a3f-119">자동 크기 조정을 테스트할 풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-119">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="67a3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a3f-120">-DefaultProfile</span></span>
<span data-ttu-id="67a3f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67a3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a3f-122">CommonParameters</span></span>
<span data-ttu-id="67a3f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a3f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a3f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a3f-125">입력</span><span class="sxs-lookup"><span data-stu-id="67a3f-125">INPUTS</span></span>

### <span data-ttu-id="67a3f-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="67a3f-126">BatchAccountContext</span></span>
<span data-ttu-id="67a3f-127">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="67a3f-128">이름</span><span class="sxs-lookup"><span data-stu-id="67a3f-128">String</span></span>
<span data-ttu-id="67a3f-129">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a3f-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="67a3f-130">출력</span><span class="sxs-lookup"><span data-stu-id="67a3f-130">OUTPUTS</span></span>

### <span data-ttu-id="67a3f-131">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="67a3f-131">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="67a3f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="67a3f-132">NOTES</span></span>

## <span data-ttu-id="67a3f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67a3f-133">RELATED LINKS</span></span>

[<span data-ttu-id="67a3f-134">Disable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="67a3f-134">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="67a3f-135">Enable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="67a3f-135">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="67a3f-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="67a3f-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="67a3f-137">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67a3f-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


