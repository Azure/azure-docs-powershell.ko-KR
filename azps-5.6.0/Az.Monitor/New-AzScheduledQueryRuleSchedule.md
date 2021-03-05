---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 231b9250509ed463f7f9b2a2d9563dbb1e378ee0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978416"
---
# <span data-ttu-id="828b5-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="828b5-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="828b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828b5-102">SYNOPSIS</span></span>
<span data-ttu-id="828b5-103">일정 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="828b5-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="828b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="828b5-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="828b5-105">설명</span><span class="sxs-lookup"><span data-stu-id="828b5-105">DESCRIPTION</span></span>
<span data-ttu-id="828b5-106">일정 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="828b5-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="828b5-107">이 개체는 로그 경고 규칙을 만드는 명령에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="828b5-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="828b5-108">예제</span><span class="sxs-lookup"><span data-stu-id="828b5-108">EXAMPLES</span></span>

### <span data-ttu-id="828b5-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="828b5-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="828b5-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="828b5-110">PARAMETERS</span></span>

### <span data-ttu-id="828b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828b5-111">-DefaultProfile</span></span>
<span data-ttu-id="828b5-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="828b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="828b5-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="828b5-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="828b5-114">경고 빈도</span><span class="sxs-lookup"><span data-stu-id="828b5-114">The alert frequency</span></span>

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

### <span data-ttu-id="828b5-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="828b5-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="828b5-116">경고 시간 창</span><span class="sxs-lookup"><span data-stu-id="828b5-116">The alert time window</span></span>

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

### <span data-ttu-id="828b5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828b5-117">CommonParameters</span></span>
<span data-ttu-id="828b5-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="828b5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828b5-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="828b5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828b5-120">입력</span><span class="sxs-lookup"><span data-stu-id="828b5-120">INPUTS</span></span>

### <span data-ttu-id="828b5-121">없음</span><span class="sxs-lookup"><span data-stu-id="828b5-121">None</span></span>

## <span data-ttu-id="828b5-122">출력</span><span class="sxs-lookup"><span data-stu-id="828b5-122">OUTPUTS</span></span>

### <span data-ttu-id="828b5-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="828b5-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="828b5-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="828b5-124">NOTES</span></span>

## <span data-ttu-id="828b5-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="828b5-125">RELATED LINKS</span></span>
