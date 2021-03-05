---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 1fcafb0eb9e4bd1cfb0cf5b3f5ec770c35ea92d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996590"
---
# <span data-ttu-id="adb3a-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="adb3a-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="adb3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="adb3a-103">트리거 조건 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adb3a-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="adb3a-104">구문</span><span class="sxs-lookup"><span data-stu-id="adb3a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adb3a-105">설명</span><span class="sxs-lookup"><span data-stu-id="adb3a-105">DESCRIPTION</span></span>
<span data-ttu-id="adb3a-106">트리거 조건 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="adb3a-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="adb3a-107">이 개체는 경고 작업 개체를 만드는 명령에 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="adb3a-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="adb3a-108">예제</span><span class="sxs-lookup"><span data-stu-id="adb3a-108">EXAMPLES</span></span>

### <span data-ttu-id="adb3a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="adb3a-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="adb3a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="adb3a-110">PARAMETERS</span></span>

### <span data-ttu-id="adb3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb3a-111">-DefaultProfile</span></span>
<span data-ttu-id="adb3a-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adb3a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb3a-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="adb3a-113">-MetricTrigger</span></span>
<span data-ttu-id="adb3a-114">메트릭 쿼리 규칙에 대한 트리거 조건</span><span class="sxs-lookup"><span data-stu-id="adb3a-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="adb3a-115">-임계값</span><span class="sxs-lookup"><span data-stu-id="adb3a-115">-Threshold</span></span>
<span data-ttu-id="adb3a-116">경고가 발생되는 위의 임계값</span><span class="sxs-lookup"><span data-stu-id="adb3a-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="adb3a-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="adb3a-117">-ThresholdOperator</span></span>
<span data-ttu-id="adb3a-118">임계값 연산자: GreaterThan, LessThan 또는 Equal</span><span class="sxs-lookup"><span data-stu-id="adb3a-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="adb3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb3a-119">CommonParameters</span></span>
<span data-ttu-id="adb3a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="adb3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb3a-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adb3a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb3a-122">입력</span><span class="sxs-lookup"><span data-stu-id="adb3a-122">INPUTS</span></span>

### <span data-ttu-id="adb3a-123">없음</span><span class="sxs-lookup"><span data-stu-id="adb3a-123">None</span></span>

## <span data-ttu-id="adb3a-124">출력</span><span class="sxs-lookup"><span data-stu-id="adb3a-124">OUTPUTS</span></span>

### <span data-ttu-id="adb3a-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="adb3a-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="adb3a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="adb3a-126">NOTES</span></span>

## <span data-ttu-id="adb3a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adb3a-127">RELATED LINKS</span></span>
