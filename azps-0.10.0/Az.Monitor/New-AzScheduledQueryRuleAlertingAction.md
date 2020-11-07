---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 54da99c2aeb6909c1a08a98821f621ddfed5199e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875742"
---
# <span data-ttu-id="7916f-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7916f-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="7916f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7916f-102">SYNOPSIS</span></span>
<span data-ttu-id="7916f-103">경고 동작 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7916f-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="7916f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7916f-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7916f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7916f-105">DESCRIPTION</span></span>
<span data-ttu-id="7916f-106">로그 알림 규칙을 만드는 명령에이 개체가 전달 될 경고 동작 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7916f-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="7916f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7916f-107">EXAMPLES</span></span>

### <span data-ttu-id="7916f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7916f-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="7916f-109">변수</span><span class="sxs-lookup"><span data-stu-id="7916f-109">PARAMETERS</span></span>

### <span data-ttu-id="7916f-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="7916f-110">-AznsAction</span></span>
<span data-ttu-id="7916f-111">AzNS 작업 세부 정보</span><span class="sxs-lookup"><span data-stu-id="7916f-111">The AzNS action details</span></span>

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

### <span data-ttu-id="7916f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7916f-112">-DefaultProfile</span></span>
<span data-ttu-id="7916f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7916f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7916f-114">-심각도</span><span class="sxs-lookup"><span data-stu-id="7916f-114">-Severity</span></span>
<span data-ttu-id="7916f-115">이 알림에 대 한 심각도</span><span class="sxs-lookup"><span data-stu-id="7916f-115">The severity for this alert</span></span>

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

### <span data-ttu-id="7916f-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="7916f-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="7916f-117">알림을 제한 하는 기간 (분)</span><span class="sxs-lookup"><span data-stu-id="7916f-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="7916f-118">-트리거</span><span class="sxs-lookup"><span data-stu-id="7916f-118">-Trigger</span></span>
<span data-ttu-id="7916f-119">알림 트리거 조건</span><span class="sxs-lookup"><span data-stu-id="7916f-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="7916f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7916f-120">CommonParameters</span></span>
<span data-ttu-id="7916f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7916f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7916f-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7916f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7916f-123">입력</span><span class="sxs-lookup"><span data-stu-id="7916f-123">INPUTS</span></span>

### <span data-ttu-id="7916f-124">않아야</span><span class="sxs-lookup"><span data-stu-id="7916f-124">None</span></span>

## <span data-ttu-id="7916f-125">출력</span><span class="sxs-lookup"><span data-stu-id="7916f-125">OUTPUTS</span></span>

### <span data-ttu-id="7916f-126">PSScheduledQueryRuleAlertingAction를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7916f-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="7916f-127">상속자</span><span class="sxs-lookup"><span data-stu-id="7916f-127">NOTES</span></span>

## <span data-ttu-id="7916f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7916f-128">RELATED LINKS</span></span>
