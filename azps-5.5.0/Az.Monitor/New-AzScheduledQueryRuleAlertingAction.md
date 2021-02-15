---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184932"
---
# <span data-ttu-id="b8a33-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b8a33-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="b8a33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a33-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a33-103">경고 작업 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8a33-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="b8a33-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8a33-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a33-105">설명</span><span class="sxs-lookup"><span data-stu-id="b8a33-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a33-106">경고 작업 유형의 개체를 만듭니다. 이 개체는 로그 경고 규칙을 만드는 명령에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8a33-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="b8a33-107">예제</span><span class="sxs-lookup"><span data-stu-id="b8a33-107">EXAMPLES</span></span>

### <span data-ttu-id="b8a33-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8a33-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="b8a33-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8a33-109">PARAMETERS</span></span>

### <span data-ttu-id="b8a33-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="b8a33-110">-AznsAction</span></span>
<span data-ttu-id="b8a33-111">AzNS 작업 세부 정보</span><span class="sxs-lookup"><span data-stu-id="b8a33-111">The AzNS action details</span></span>

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

### <span data-ttu-id="b8a33-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a33-112">-DefaultProfile</span></span>
<span data-ttu-id="b8a33-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8a33-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a33-114">-심각도</span><span class="sxs-lookup"><span data-stu-id="b8a33-114">-Severity</span></span>
<span data-ttu-id="b8a33-115">이 경고의 심각도</span><span class="sxs-lookup"><span data-stu-id="b8a33-115">The severity for this alert</span></span>

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

### <span data-ttu-id="b8a33-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="b8a33-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="b8a33-117">경고를 제한해야 하는 시간(분)입니다.</span><span class="sxs-lookup"><span data-stu-id="b8a33-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="b8a33-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="b8a33-118">-Trigger</span></span>
<span data-ttu-id="b8a33-119">경고 트리거 조건</span><span class="sxs-lookup"><span data-stu-id="b8a33-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="b8a33-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a33-120">CommonParameters</span></span>
<span data-ttu-id="b8a33-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a33-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a33-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b8a33-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a33-123">입력</span><span class="sxs-lookup"><span data-stu-id="b8a33-123">INPUTS</span></span>

### <span data-ttu-id="b8a33-124">없음</span><span class="sxs-lookup"><span data-stu-id="b8a33-124">None</span></span>

## <span data-ttu-id="b8a33-125">출력</span><span class="sxs-lookup"><span data-stu-id="b8a33-125">OUTPUTS</span></span>

### <span data-ttu-id="b8a33-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b8a33-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="b8a33-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8a33-127">NOTES</span></span>

## <span data-ttu-id="b8a33-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8a33-128">RELATED LINKS</span></span>
