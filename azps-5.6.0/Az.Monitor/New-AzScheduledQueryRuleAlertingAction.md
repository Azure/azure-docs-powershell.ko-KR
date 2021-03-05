---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 0394aa7c2db880bbb10c8d68c9d502560c1035bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961808"
---
# <span data-ttu-id="76960-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="76960-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="76960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76960-102">SYNOPSIS</span></span>
<span data-ttu-id="76960-103">경고 작업 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76960-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="76960-104">구문</span><span class="sxs-lookup"><span data-stu-id="76960-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76960-105">설명</span><span class="sxs-lookup"><span data-stu-id="76960-105">DESCRIPTION</span></span>
<span data-ttu-id="76960-106">경고 작업 형식의 개체를 만듭니다. 이 개체는 Log Alert Rule을 만드는 명령에 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76960-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="76960-107">예제</span><span class="sxs-lookup"><span data-stu-id="76960-107">EXAMPLES</span></span>

### <span data-ttu-id="76960-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="76960-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="76960-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="76960-109">PARAMETERS</span></span>

### <span data-ttu-id="76960-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="76960-110">-AznsAction</span></span>
<span data-ttu-id="76960-111">AzNS 작업 세부 정보</span><span class="sxs-lookup"><span data-stu-id="76960-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76960-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76960-112">-DefaultProfile</span></span>
<span data-ttu-id="76960-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76960-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76960-114">-심각도</span><span class="sxs-lookup"><span data-stu-id="76960-114">-Severity</span></span>
<span data-ttu-id="76960-115">이 경고의 심각도</span><span class="sxs-lookup"><span data-stu-id="76960-115">The severity for this alert</span></span>

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

### <span data-ttu-id="76960-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="76960-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="76960-117">경고를 제한해야 하는 분의 기간</span><span class="sxs-lookup"><span data-stu-id="76960-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76960-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="76960-118">-Trigger</span></span>
<span data-ttu-id="76960-119">경고 트리거 조건</span><span class="sxs-lookup"><span data-stu-id="76960-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76960-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76960-120">CommonParameters</span></span>
<span data-ttu-id="76960-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76960-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76960-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76960-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76960-123">입력</span><span class="sxs-lookup"><span data-stu-id="76960-123">INPUTS</span></span>

### <span data-ttu-id="76960-124">없음</span><span class="sxs-lookup"><span data-stu-id="76960-124">None</span></span>

## <span data-ttu-id="76960-125">출력</span><span class="sxs-lookup"><span data-stu-id="76960-125">OUTPUTS</span></span>

### <span data-ttu-id="76960-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="76960-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="76960-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76960-127">NOTES</span></span>

## <span data-ttu-id="76960-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76960-128">RELATED LINKS</span></span>
