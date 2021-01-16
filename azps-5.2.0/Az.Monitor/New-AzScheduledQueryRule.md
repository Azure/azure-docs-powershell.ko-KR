---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331550"
---
# <span data-ttu-id="9c786-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9c786-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="9c786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c786-102">SYNOPSIS</span></span>
<span data-ttu-id="9c786-103">로그 경고 규칙(예약된 쿼리 규칙 유형)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c786-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="9c786-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c786-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c786-105">설명</span><span class="sxs-lookup"><span data-stu-id="9c786-105">DESCRIPTION</span></span>
<span data-ttu-id="9c786-106">로그 경고 규칙(예약된 쿼리 규칙 유형)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c786-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="9c786-107">예제</span><span class="sxs-lookup"><span data-stu-id="9c786-107">EXAMPLES</span></span>

### <span data-ttu-id="9c786-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c786-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="9c786-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c786-109">PARAMETERS</span></span>

### <span data-ttu-id="9c786-110">-Action</span><span class="sxs-lookup"><span data-stu-id="9c786-110">-Action</span></span>
<span data-ttu-id="9c786-111">예약된 쿼리 규칙 경고 작업</span><span class="sxs-lookup"><span data-stu-id="9c786-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c786-112">-AsJob</span></span>
<span data-ttu-id="9c786-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9c786-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c786-114">-DefaultProfile</span></span>
<span data-ttu-id="9c786-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c786-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c786-116">-Description</span><span class="sxs-lookup"><span data-stu-id="9c786-116">-Description</span></span>
<span data-ttu-id="9c786-117">이 경고에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="9c786-117">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9c786-118">-Enabled</span></span>
<span data-ttu-id="9c786-119">Azure 경고 상태 - 유효한 값 - $true $false</span><span class="sxs-lookup"><span data-stu-id="9c786-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-120">-Location</span><span class="sxs-lookup"><span data-stu-id="9c786-120">-Location</span></span>
<span data-ttu-id="9c786-121">이 경고의 위치</span><span class="sxs-lookup"><span data-stu-id="9c786-121">The location for this alert</span></span>

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

### <span data-ttu-id="9c786-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9c786-122">-Name</span></span>
<span data-ttu-id="9c786-123">경고 이름</span><span class="sxs-lookup"><span data-stu-id="9c786-123">The alert name</span></span>

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

### <span data-ttu-id="9c786-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c786-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c786-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9c786-125">The resource group name</span></span>

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

### <span data-ttu-id="9c786-126">-Schedule</span><span class="sxs-lookup"><span data-stu-id="9c786-126">-Schedule</span></span>
<span data-ttu-id="9c786-127">예약된 쿼리 규칙 일정</span><span class="sxs-lookup"><span data-stu-id="9c786-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-128">-Source</span><span class="sxs-lookup"><span data-stu-id="9c786-128">-Source</span></span>
<span data-ttu-id="9c786-129">예약된 쿼리 규칙 원본</span><span class="sxs-lookup"><span data-stu-id="9c786-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c786-130">-Tag</span></span>
<span data-ttu-id="9c786-131">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="9c786-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c786-132">-Confirm</span></span>
<span data-ttu-id="9c786-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c786-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c786-134">-WhatIf</span></span>
<span data-ttu-id="9c786-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9c786-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c786-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c786-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c786-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c786-137">CommonParameters</span></span>
<span data-ttu-id="9c786-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c786-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c786-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c786-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c786-140">입력</span><span class="sxs-lookup"><span data-stu-id="9c786-140">INPUTS</span></span>

### <span data-ttu-id="9c786-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9c786-141">System.String</span></span>

## <span data-ttu-id="9c786-142">출력</span><span class="sxs-lookup"><span data-stu-id="9c786-142">OUTPUTS</span></span>

### <span data-ttu-id="9c786-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="9c786-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="9c786-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c786-144">NOTES</span></span>

## <span data-ttu-id="9c786-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c786-145">RELATED LINKS</span></span>
