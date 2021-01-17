---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362048"
---
# <span data-ttu-id="0ccfd-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0ccfd-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="0ccfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ccfd-102">SYNOPSIS</span></span>
<span data-ttu-id="0ccfd-103">로그 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="0ccfd-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ccfd-104">SYNTAX</span></span>

### <span data-ttu-id="0ccfd-105">ByRuleName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ccfd-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ccfd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0ccfd-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ccfd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ccfd-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ccfd-108">설명</span><span class="sxs-lookup"><span data-stu-id="0ccfd-108">DESCRIPTION</span></span>
<span data-ttu-id="0ccfd-109">로그 경고 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="0ccfd-110">예제</span><span class="sxs-lookup"><span data-stu-id="0ccfd-110">EXAMPLES</span></span>

### <span data-ttu-id="0ccfd-111">예제 1: 규칙 이름으로 제거</span><span class="sxs-lookup"><span data-stu-id="0ccfd-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="0ccfd-112">예제 2: 입력 개체로 제거</span><span class="sxs-lookup"><span data-stu-id="0ccfd-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="0ccfd-113">예제 3: 리소스 ID로 제거</span><span class="sxs-lookup"><span data-stu-id="0ccfd-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="0ccfd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ccfd-114">PARAMETERS</span></span>

### <span data-ttu-id="0ccfd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ccfd-115">-DefaultProfile</span></span>
<span data-ttu-id="0ccfd-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ccfd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ccfd-117">-InputObject</span></span>
<span data-ttu-id="0ccfd-118">예약된 쿼리 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="0ccfd-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ccfd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0ccfd-119">-Name</span></span>
<span data-ttu-id="0ccfd-120">경고 이름</span><span class="sxs-lookup"><span data-stu-id="0ccfd-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ccfd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ccfd-121">-PassThru</span></span>
<span data-ttu-id="0ccfd-122">성공 또는 실패를 나타내는 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="0ccfd-123">이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0ccfd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ccfd-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ccfd-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0ccfd-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ccfd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ccfd-126">-ResourceId</span></span>
<span data-ttu-id="0ccfd-127">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0ccfd-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ccfd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ccfd-128">-Confirm</span></span>
<span data-ttu-id="0ccfd-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ccfd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ccfd-130">-WhatIf</span></span>
<span data-ttu-id="0ccfd-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0ccfd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ccfd-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ccfd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ccfd-133">CommonParameters</span></span>
<span data-ttu-id="0ccfd-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ccfd-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ccfd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ccfd-136">입력</span><span class="sxs-lookup"><span data-stu-id="0ccfd-136">INPUTS</span></span>

### <span data-ttu-id="0ccfd-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="0ccfd-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="0ccfd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0ccfd-138">System.String</span></span>

## <span data-ttu-id="0ccfd-139">출력</span><span class="sxs-lookup"><span data-stu-id="0ccfd-139">OUTPUTS</span></span>

### <span data-ttu-id="0ccfd-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ccfd-140">System.Boolean</span></span>

## <span data-ttu-id="0ccfd-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ccfd-141">NOTES</span></span>

## <span data-ttu-id="0ccfd-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ccfd-142">RELATED LINKS</span></span>
