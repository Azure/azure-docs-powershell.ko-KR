---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491891"
---
# <span data-ttu-id="cb0b8-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cb0b8-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="cb0b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0b8-103">트리거 조건 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb0b8-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="cb0b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb0b8-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb0b8-105">설명</span><span class="sxs-lookup"><span data-stu-id="cb0b8-105">DESCRIPTION</span></span>
<span data-ttu-id="cb0b8-106">트리거 조건 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb0b8-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="cb0b8-107">이 개체는 경고 작업 개체를 만드는 명령에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb0b8-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="cb0b8-108">예제</span><span class="sxs-lookup"><span data-stu-id="cb0b8-108">EXAMPLES</span></span>

### <span data-ttu-id="cb0b8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb0b8-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="cb0b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb0b8-110">PARAMETERS</span></span>

### <span data-ttu-id="cb0b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0b8-111">-DefaultProfile</span></span>
<span data-ttu-id="cb0b8-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb0b8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb0b8-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cb0b8-113">-MetricTrigger</span></span>
<span data-ttu-id="cb0b8-114">메트릭 쿼리 규칙에 대한 트리거 조건</span><span class="sxs-lookup"><span data-stu-id="cb0b8-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b8-115">-Threshold</span><span class="sxs-lookup"><span data-stu-id="cb0b8-115">-Threshold</span></span>
<span data-ttu-id="cb0b8-116">경고가 발생되는 임계값을 초과합니다.</span><span class="sxs-lookup"><span data-stu-id="cb0b8-116">The threshold above which alert gets fired</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b8-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="cb0b8-117">-ThresholdOperator</span></span>
<span data-ttu-id="cb0b8-118">임계값 연산자: GreaterThan, LessThan 또는 Equal</span><span class="sxs-lookup"><span data-stu-id="cb0b8-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0b8-119">CommonParameters</span></span>
<span data-ttu-id="cb0b8-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb0b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0b8-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb0b8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0b8-122">입력</span><span class="sxs-lookup"><span data-stu-id="cb0b8-122">INPUTS</span></span>

### <span data-ttu-id="cb0b8-123">없음</span><span class="sxs-lookup"><span data-stu-id="cb0b8-123">None</span></span>

## <span data-ttu-id="cb0b8-124">출력</span><span class="sxs-lookup"><span data-stu-id="cb0b8-124">OUTPUTS</span></span>

### <span data-ttu-id="cb0b8-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cb0b8-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="cb0b8-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb0b8-126">NOTES</span></span>

## <span data-ttu-id="cb0b8-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb0b8-127">RELATED LINKS</span></span>
