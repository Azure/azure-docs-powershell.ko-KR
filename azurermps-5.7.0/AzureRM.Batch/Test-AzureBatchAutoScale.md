---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 4258c5d83b15c2cecb6e2cd4e3edc216efec7a97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525347"
---
# <span data-ttu-id="8f43d-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8f43d-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="8f43d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f43d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f43d-103">풀의 자동 크기 조정 수식 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f43d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f43d-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f43d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8f43d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f43d-106">**테스트-AzureBatchAutoScale 크기 조정** cmdlet은 지정 된 풀에 대 한 자동 크기 조정 수식의 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="8f43d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8f43d-107">EXAMPLES</span></span>

### <span data-ttu-id="8f43d-108">예제 1: 풀에서 자동 크기 조정 수식 평가</span><span class="sxs-lookup"><span data-stu-id="8f43d-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="8f43d-109">첫 번째 명령은 예제에서 사용할 $Formula 변수에 수식을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="8f43d-110">두 번째 명령은 ID ContosoPool가 있는 풀에서 자동 크기 조정 수식을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="8f43d-111">마지막 명령은 표준 도트 구문을 사용 하 여 **결과** 를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="8f43d-112">변수</span><span class="sxs-lookup"><span data-stu-id="8f43d-112">PARAMETERS</span></span>

### <span data-ttu-id="8f43d-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="8f43d-113">-AutoScaleFormula</span></span>
<span data-ttu-id="8f43d-114">풀에 있는 계산 노드의 원하는 수에 대 한 수식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f43d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8f43d-115">-BatchContext</span></span>
<span data-ttu-id="8f43d-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8f43d-117">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8f43d-118">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8f43d-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8f43d-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f43d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f43d-121">-DefaultProfile</span></span>
<span data-ttu-id="8f43d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f43d-123">-Id</span><span class="sxs-lookup"><span data-stu-id="8f43d-123">-Id</span></span>
<span data-ttu-id="8f43d-124">자동 크기 조정을 테스트할 풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f43d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f43d-125">CommonParameters</span></span>
<span data-ttu-id="8f43d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f43d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f43d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f43d-128">입력</span><span class="sxs-lookup"><span data-stu-id="8f43d-128">INPUTS</span></span>

### <span data-ttu-id="8f43d-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8f43d-129">BatchAccountContext</span></span>
<span data-ttu-id="8f43d-130">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8f43d-131">이름</span><span class="sxs-lookup"><span data-stu-id="8f43d-131">String</span></span>
<span data-ttu-id="8f43d-132">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f43d-132">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8f43d-133">출력</span><span class="sxs-lookup"><span data-stu-id="8f43d-133">OUTPUTS</span></span>

### <span data-ttu-id="8f43d-134">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="8f43d-134">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="8f43d-135">상속자</span><span class="sxs-lookup"><span data-stu-id="8f43d-135">NOTES</span></span>

## <span data-ttu-id="8f43d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f43d-136">RELATED LINKS</span></span>

[<span data-ttu-id="8f43d-137">Disable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="8f43d-137">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="8f43d-138">Enable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="8f43d-138">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="8f43d-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8f43d-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8f43d-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8f43d-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


