---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 73c1efe9e25fa02dc06f367eae1d010562eba56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538023"
---
# <span data-ttu-id="0fda1-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0fda1-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="0fda1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fda1-102">SYNOPSIS</span></span>
<span data-ttu-id="0fda1-103">풀의 자동 크기 조정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fda1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fda1-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fda1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0fda1-105">DESCRIPTION</span></span>
<span data-ttu-id="0fda1-106">**-AzureBatchAutoScale 크기 조정** Cmdlet을 사용 하면 지정 된 풀의 크기를 자동으로 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="0fda1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0fda1-107">EXAMPLES</span></span>

### <span data-ttu-id="0fda1-108">예제 1: 풀에 자동 크기 조정 사용</span><span class="sxs-lookup"><span data-stu-id="0fda1-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="0fda1-109">첫 번째 명령은 수식을 정의한 다음 $Formula 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="0fda1-110">두 번째 명령은 $Formula의 수식을 사용 하 여 MyPool 이라는 풀에서 자동 크기 조정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="0fda1-111">변수</span><span class="sxs-lookup"><span data-stu-id="0fda1-111">PARAMETERS</span></span>

### <span data-ttu-id="0fda1-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="0fda1-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="0fda1-113">크기 자동 조정 수식에 따라 풀 크기가 자동으로 조정 되기 전 까지의 경과 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="0fda1-114">기본값은 15 분 이며 최소 값은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fda1-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="0fda1-115">-AutoScaleFormula</span></span>
<span data-ttu-id="0fda1-116">풀에 있는 계산 노드의 원하는 수에 대 한 수식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fda1-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0fda1-117">-BatchContext</span></span>
<span data-ttu-id="0fda1-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0fda1-119">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0fda1-120">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0fda1-121">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0fda1-122">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0fda1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fda1-123">-DefaultProfile</span></span>
<span data-ttu-id="0fda1-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fda1-125">-Id</span><span class="sxs-lookup"><span data-stu-id="0fda1-125">-Id</span></span>
<span data-ttu-id="0fda1-126">자동 크기 조정을 사용할 풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="0fda1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fda1-127">CommonParameters</span></span>
<span data-ttu-id="0fda1-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fda1-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fda1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fda1-130">입력</span><span class="sxs-lookup"><span data-stu-id="0fda1-130">INPUTS</span></span>

### <span data-ttu-id="0fda1-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0fda1-131">BatchAccountContext</span></span>
<span data-ttu-id="0fda1-132">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0fda1-133">이름</span><span class="sxs-lookup"><span data-stu-id="0fda1-133">String</span></span>
<span data-ttu-id="0fda1-134">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fda1-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0fda1-135">출력</span><span class="sxs-lookup"><span data-stu-id="0fda1-135">OUTPUTS</span></span>

## <span data-ttu-id="0fda1-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0fda1-136">NOTES</span></span>

## <span data-ttu-id="0fda1-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fda1-137">RELATED LINKS</span></span>

[<span data-ttu-id="0fda1-138">Disable-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="0fda1-138">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="0fda1-139">Test-AzureBatchAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="0fda1-139">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="0fda1-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0fda1-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


