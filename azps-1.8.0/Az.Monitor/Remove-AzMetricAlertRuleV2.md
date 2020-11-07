---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 698f05840df6578d8595e2ca8e31c9f0a11bc722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700791"
---
# <span data-ttu-id="e3e79-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e3e79-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="e3e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3e79-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e79-103">V2 (비 클래식) 메트릭 알림 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="e3e79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3e79-104">SYNTAX</span></span>

### <span data-ttu-id="e3e79-105">ByMetricRuleResourceName</span><span class="sxs-lookup"><span data-stu-id="e3e79-105">ByMetricRuleResourceName</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e79-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e79-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e79-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="e3e79-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e79-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e3e79-108">DESCRIPTION</span></span>
<span data-ttu-id="e3e79-109">**제거-AzMetricAlertRuleV2** cmdlet은 경고 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="e3e79-110">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e3e79-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e3e79-111">EXAMPLES</span></span>

### <span data-ttu-id="e3e79-112">예제 1: 이름으로 알림 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="e3e79-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="e3e79-113">이 명령은 PsSdk 이라는 경고 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="e3e79-114">예제 2: ID 별 알림 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="e3e79-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="e3e79-115">이 명령은 리소스 ID가 #b0 인 경고 규칙을 제거 합니다. `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="e3e79-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>
### <span data-ttu-id="e3e79-116">예제 3: 알림 가져오기 및 제거</span><span class="sxs-lookup"><span data-stu-id="e3e79-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="e3e79-117">이 명령은 알림을 가져와 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="e3e79-118">변수</span><span class="sxs-lookup"><span data-stu-id="e3e79-118">PARAMETERS</span></span>

### <span data-ttu-id="e3e79-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3e79-119">-AsJob</span></span>
<span data-ttu-id="e3e79-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3e79-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e3e79-121">-Confirm</span></span>
<span data-ttu-id="e3e79-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e79-123">-DefaultProfile</span></span>
<span data-ttu-id="e3e79-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3e79-125">-InputObject</span></span>
<span data-ttu-id="e3e79-126">메트릭 규칙 개체</span><span class="sxs-lookup"><span data-stu-id="e3e79-126">The Metric rule object</span></span>

```yaml
Type: PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-127">-이름</span><span class="sxs-lookup"><span data-stu-id="e3e79-127">-Name</span></span>
<span data-ttu-id="e3e79-128">메트릭 알림 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-128">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3e79-129">-PassThru</span></span>
<span data-ttu-id="e3e79-130">삭제에 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-130">Return true upon successful deletion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e79-131">-ResourceGroupName</span></span>
<span data-ttu-id="e3e79-132">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e79-132">The ResourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e79-133">-ResourceId</span></span>
<span data-ttu-id="e3e79-134">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e79-134">The RuleResourceId</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e79-135">-WhatIf</span></span>
<span data-ttu-id="e3e79-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3e79-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e79-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e79-138">CommonParameters</span></span>
<span data-ttu-id="e3e79-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e3e79-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3e79-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e79-141">입력</span><span class="sxs-lookup"><span data-stu-id="e3e79-141">INPUTS</span></span>

### <span data-ttu-id="e3e79-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3e79-142">System.String</span></span>

### <span data-ttu-id="e3e79-143">PSMetricAlertRuleV2를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3e79-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="e3e79-144">출력</span><span class="sxs-lookup"><span data-stu-id="e3e79-144">OUTPUTS</span></span>

### <span data-ttu-id="e3e79-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e3e79-145">System.Boolean</span></span>

## <span data-ttu-id="e3e79-146">상속자</span><span class="sxs-lookup"><span data-stu-id="e3e79-146">NOTES</span></span>

## <span data-ttu-id="e3e79-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3e79-147">RELATED LINKS</span></span>
