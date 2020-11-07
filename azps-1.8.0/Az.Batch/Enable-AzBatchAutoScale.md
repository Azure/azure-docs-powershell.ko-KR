---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 72ba9a2d78ab343b44267c09a7c1524cab7278a9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93701908"
---
# <span data-ttu-id="45a20-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="45a20-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="45a20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45a20-102">SYNOPSIS</span></span>
<span data-ttu-id="45a20-103">풀의 자동 크기 조정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="45a20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45a20-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45a20-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45a20-105">DESCRIPTION</span></span>
<span data-ttu-id="45a20-106">AzBatchAutoScale cmdlet을 **사용** 하면 지정 된 풀의 자동 크기를 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="45a20-107">예제의</span><span class="sxs-lookup"><span data-stu-id="45a20-107">EXAMPLES</span></span>

### <span data-ttu-id="45a20-108">예제 1: 풀에 자동 크기 조정 사용</span><span class="sxs-lookup"><span data-stu-id="45a20-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="45a20-109">첫 번째 명령은 수식을 정의한 다음 $Formula 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="45a20-110">두 번째 명령은 $Formula의 수식을 사용 하 여 MyPool 이라는 풀에서 자동 크기 조정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="45a20-111">변수</span><span class="sxs-lookup"><span data-stu-id="45a20-111">PARAMETERS</span></span>

### <span data-ttu-id="45a20-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="45a20-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="45a20-113">크기 자동 조정 수식에 따라 풀 크기가 자동으로 조정 되기 전 까지의 경과 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="45a20-114">기본값은 15 분 이며 최소 값은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a20-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="45a20-115">-AutoScaleFormula</span></span>
<span data-ttu-id="45a20-116">풀에 있는 계산 노드의 원하는 수에 대 한 수식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a20-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="45a20-117">-BatchContext</span></span>
<span data-ttu-id="45a20-118">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="45a20-119">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="45a20-120">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="45a20-121">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="45a20-122">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="45a20-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a20-123">-DefaultProfile</span></span>
<span data-ttu-id="45a20-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45a20-125">-Id</span><span class="sxs-lookup"><span data-stu-id="45a20-125">-Id</span></span>
<span data-ttu-id="45a20-126">자동 크기 조정을 사용할 풀의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="45a20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a20-127">CommonParameters</span></span>
<span data-ttu-id="45a20-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45a20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a20-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a20-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a20-130">입력</span><span class="sxs-lookup"><span data-stu-id="45a20-130">INPUTS</span></span>

### <span data-ttu-id="45a20-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="45a20-131">System.String</span></span>

### <span data-ttu-id="45a20-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="45a20-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="45a20-133">출력</span><span class="sxs-lookup"><span data-stu-id="45a20-133">OUTPUTS</span></span>

### <span data-ttu-id="45a20-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="45a20-134">System.Void</span></span>

## <span data-ttu-id="45a20-135">상속자</span><span class="sxs-lookup"><span data-stu-id="45a20-135">NOTES</span></span>

## <span data-ttu-id="45a20-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45a20-136">RELATED LINKS</span></span>

[<span data-ttu-id="45a20-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="45a20-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="45a20-138">테스트-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="45a20-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="45a20-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="45a20-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


