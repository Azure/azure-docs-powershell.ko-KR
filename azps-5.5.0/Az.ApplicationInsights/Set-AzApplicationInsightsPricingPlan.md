---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182244"
---
# <span data-ttu-id="2db7f-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="2db7f-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="2db7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db7f-102">SYNOPSIS</span></span>
<span data-ttu-id="2db7f-103">Application Insights 리소스에 대한 가격 책정 계획 및 일일 데이터 볼륨 정보 설정</span><span class="sxs-lookup"><span data-stu-id="2db7f-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="2db7f-104">구문</span><span class="sxs-lookup"><span data-stu-id="2db7f-104">SYNTAX</span></span>

### <span data-ttu-id="2db7f-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2db7f-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db7f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db7f-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db7f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db7f-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2db7f-108">설명</span><span class="sxs-lookup"><span data-stu-id="2db7f-108">DESCRIPTION</span></span>
<span data-ttu-id="2db7f-109">Application Insights 리소스에 대한 가격 책정 계획 및 일일 데이터 볼륨 정보를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="2db7f-110">2018년 4월 이후에 만든 Application Insights의 가격 책정 계획은 다음 cmdlet에서 설정할 수 없습니다. https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="2db7f-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="2db7f-111">예제</span><span class="sxs-lookup"><span data-stu-id="2db7f-111">EXAMPLES</span></span>

### <span data-ttu-id="2db7f-112">예제 1 Application Insights 리소스에 대한 가격 책정 계획 및 일일 데이터 볼륨 정보 설정</span><span class="sxs-lookup"><span data-stu-id="2db7f-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="2db7f-113">가격 책정 계획을 "기본"으로 설정하고, 일일 데이터 볼륨 한도는 400GB로 설정하고, 리소스 그룹 "testgroup"에서 리소스 "테스트"에 대한 한도에 적중하면 알림 보내기 중지</span><span class="sxs-lookup"><span data-stu-id="2db7f-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="2db7f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2db7f-114">PARAMETERS</span></span>

### <span data-ttu-id="2db7f-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2db7f-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="2db7f-116">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2db7f-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="2db7f-117">-DailyCapGB</span></span>
<span data-ttu-id="2db7f-118">일일 한도입니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-118">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db7f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db7f-119">-DefaultProfile</span></span>
<span data-ttu-id="2db7f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2db7f-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="2db7f-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="2db7f-122">한도에 맞을 때 알림 보내기 중지</span><span class="sxs-lookup"><span data-stu-id="2db7f-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="2db7f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2db7f-123">-Name</span></span>
<span data-ttu-id="2db7f-124">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-124">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db7f-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="2db7f-125">-PricingPlan</span></span>
<span data-ttu-id="2db7f-126">가격 책정 계획 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-126">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db7f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db7f-127">-ResourceGroupName</span></span>
<span data-ttu-id="2db7f-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db7f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2db7f-129">-ResourceId</span></span>
<span data-ttu-id="2db7f-130">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-130">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2db7f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2db7f-131">-Confirm</span></span>
<span data-ttu-id="2db7f-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db7f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db7f-133">-WhatIf</span></span>
<span data-ttu-id="2db7f-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2db7f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2db7f-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db7f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db7f-136">CommonParameters</span></span>
<span data-ttu-id="2db7f-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2db7f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db7f-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2db7f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db7f-139">입력</span><span class="sxs-lookup"><span data-stu-id="2db7f-139">INPUTS</span></span>

### <span data-ttu-id="2db7f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2db7f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="2db7f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2db7f-141">System.String</span></span>

## <span data-ttu-id="2db7f-142">출력</span><span class="sxs-lookup"><span data-stu-id="2db7f-142">OUTPUTS</span></span>

### <span data-ttu-id="2db7f-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="2db7f-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="2db7f-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2db7f-144">NOTES</span></span>

## <span data-ttu-id="2db7f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2db7f-145">RELATED LINKS</span></span>
