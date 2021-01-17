---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492275"
---
# <span data-ttu-id="ecc02-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ecc02-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="ecc02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc02-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc02-103">Schedule 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecc02-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="ecc02-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecc02-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecc02-105">설명</span><span class="sxs-lookup"><span data-stu-id="ecc02-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc02-106">Schedule 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecc02-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="ecc02-107">이 개체는 로그 경고 규칙을 만드는 명령에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecc02-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="ecc02-108">예제</span><span class="sxs-lookup"><span data-stu-id="ecc02-108">EXAMPLES</span></span>

### <span data-ttu-id="ecc02-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecc02-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="ecc02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecc02-110">PARAMETERS</span></span>

### <span data-ttu-id="ecc02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc02-111">-DefaultProfile</span></span>
<span data-ttu-id="ecc02-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecc02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc02-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="ecc02-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="ecc02-114">경고 빈도</span><span class="sxs-lookup"><span data-stu-id="ecc02-114">The alert frequency</span></span>

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

### <span data-ttu-id="ecc02-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="ecc02-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="ecc02-116">경고 시간 창</span><span class="sxs-lookup"><span data-stu-id="ecc02-116">The alert time window</span></span>

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

### <span data-ttu-id="ecc02-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc02-117">CommonParameters</span></span>
<span data-ttu-id="ecc02-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecc02-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc02-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecc02-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc02-120">입력</span><span class="sxs-lookup"><span data-stu-id="ecc02-120">INPUTS</span></span>

### <span data-ttu-id="ecc02-121">없음</span><span class="sxs-lookup"><span data-stu-id="ecc02-121">None</span></span>

## <span data-ttu-id="ecc02-122">출력</span><span class="sxs-lookup"><span data-stu-id="ecc02-122">OUTPUTS</span></span>

### <span data-ttu-id="ecc02-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ecc02-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="ecc02-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecc02-124">NOTES</span></span>

## <span data-ttu-id="ecc02-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecc02-125">RELATED LINKS</span></span>
