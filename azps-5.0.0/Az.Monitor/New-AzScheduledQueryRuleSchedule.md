---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217288"
---
# <span data-ttu-id="dd6e1-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="dd6e1-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="dd6e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6e1-103">일정 유형의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd6e1-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="dd6e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd6e1-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd6e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dd6e1-105">DESCRIPTION</span></span>
<span data-ttu-id="dd6e1-106">일정 유형의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd6e1-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="dd6e1-107">이 개체는 로그 경고 규칙을 만드는 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd6e1-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="dd6e1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dd6e1-108">EXAMPLES</span></span>

### <span data-ttu-id="dd6e1-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="dd6e1-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="dd6e1-110">변수</span><span class="sxs-lookup"><span data-stu-id="dd6e1-110">PARAMETERS</span></span>

### <span data-ttu-id="dd6e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6e1-111">-DefaultProfile</span></span>
<span data-ttu-id="dd6e1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd6e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd6e1-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="dd6e1-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="dd6e1-114">알림 빈도</span><span class="sxs-lookup"><span data-stu-id="dd6e1-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6e1-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="dd6e1-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="dd6e1-116">알림 시간 창</span><span class="sxs-lookup"><span data-stu-id="dd6e1-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6e1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6e1-117">CommonParameters</span></span>
<span data-ttu-id="dd6e1-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd6e1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6e1-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dd6e1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6e1-120">입력</span><span class="sxs-lookup"><span data-stu-id="dd6e1-120">INPUTS</span></span>

### <span data-ttu-id="dd6e1-121">않아야</span><span class="sxs-lookup"><span data-stu-id="dd6e1-121">None</span></span>

## <span data-ttu-id="dd6e1-122">출력</span><span class="sxs-lookup"><span data-stu-id="dd6e1-122">OUTPUTS</span></span>

### <span data-ttu-id="dd6e1-123">PSScheduledQueryRuleSchedule를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd6e1-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="dd6e1-124">상속자</span><span class="sxs-lookup"><span data-stu-id="dd6e1-124">NOTES</span></span>

## <span data-ttu-id="dd6e1-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd6e1-125">RELATED LINKS</span></span>
