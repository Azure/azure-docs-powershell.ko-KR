---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360522"
---
# <span data-ttu-id="52c88-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="52c88-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="52c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52c88-102">SYNOPSIS</span></span>
<span data-ttu-id="52c88-103">풀의 자동 크기 조정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="52c88-104">구문</span><span class="sxs-lookup"><span data-stu-id="52c88-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52c88-105">설명</span><span class="sxs-lookup"><span data-stu-id="52c88-105">DESCRIPTION</span></span>
<span data-ttu-id="52c88-106">**Enable-AzBatchAutoScale** cmdlet을 사용하면 지정된 풀의 자동 크기 조정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="52c88-107">예제</span><span class="sxs-lookup"><span data-stu-id="52c88-107">EXAMPLES</span></span>

### <span data-ttu-id="52c88-108">예제 1: 풀에 대한 자동 크기 조정 사용</span><span class="sxs-lookup"><span data-stu-id="52c88-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="52c88-109">첫 번째 명령은 수식을 정의한 다음, 수식을 $Formula 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="52c88-110">두 번째 명령은 명령에서 수식을 사용하여 MyPool이라는 풀에서 자동 크기 조정을 $Formula.</span><span class="sxs-lookup"><span data-stu-id="52c88-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="52c88-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52c88-111">PARAMETERS</span></span>

### <span data-ttu-id="52c88-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="52c88-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="52c88-113">풀 크기가 자동 크기 조정 수식에 따라 자동으로 조정되기 전에 경과하는 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="52c88-114">기본값은 15분, 최소값은 5분입니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="52c88-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="52c88-115">-AutoScaleFormula</span></span>
<span data-ttu-id="52c88-116">풀에서 원하는 계산 노드 수에 대한 수식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="52c88-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="52c88-117">-BatchContext</span></span>
<span data-ttu-id="52c88-118">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="52c88-119">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="52c88-120">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="52c88-121">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="52c88-122">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="52c88-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c88-123">-DefaultProfile</span></span>
<span data-ttu-id="52c88-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52c88-125">-Id</span><span class="sxs-lookup"><span data-stu-id="52c88-125">-Id</span></span>
<span data-ttu-id="52c88-126">자동 크기 조정을 사용하도록 설정할 풀의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="52c88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c88-127">CommonParameters</span></span>
<span data-ttu-id="52c88-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52c88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c88-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52c88-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c88-130">입력</span><span class="sxs-lookup"><span data-stu-id="52c88-130">INPUTS</span></span>

### <span data-ttu-id="52c88-131">System.String</span><span class="sxs-lookup"><span data-stu-id="52c88-131">System.String</span></span>

### <span data-ttu-id="52c88-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="52c88-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="52c88-133">출력</span><span class="sxs-lookup"><span data-stu-id="52c88-133">OUTPUTS</span></span>

### <span data-ttu-id="52c88-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="52c88-134">System.Void</span></span>

## <span data-ttu-id="52c88-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52c88-135">NOTES</span></span>

## <span data-ttu-id="52c88-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52c88-136">RELATED LINKS</span></span>

[<span data-ttu-id="52c88-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="52c88-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="52c88-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="52c88-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="52c88-139">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="52c88-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
