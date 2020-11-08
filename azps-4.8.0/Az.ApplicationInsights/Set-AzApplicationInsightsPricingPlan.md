---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: e044d8a086833ad94ed01267adf08469941a32a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213728"
---
# <span data-ttu-id="db213-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="db213-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="db213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db213-102">SYNOPSIS</span></span>
<span data-ttu-id="db213-103">Application insights 리소스에 대 한 가격 계획 및 일일 데이터 볼륨 정보 설정</span><span class="sxs-lookup"><span data-stu-id="db213-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="db213-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db213-104">SYNTAX</span></span>

### <span data-ttu-id="db213-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="db213-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db213-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db213-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db213-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db213-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db213-108">설명은</span><span class="sxs-lookup"><span data-stu-id="db213-108">DESCRIPTION</span></span>
<span data-ttu-id="db213-109">Application insights 리소스에 대 한 가격 계획 및 일일 데이터 볼륨 정보 설정</span><span class="sxs-lookup"><span data-stu-id="db213-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="db213-110">예제의</span><span class="sxs-lookup"><span data-stu-id="db213-110">EXAMPLES</span></span>

### <span data-ttu-id="db213-111">예제 1 application insights 리소스에 대 한 가격 계획 및 일일 데이터 볼륨 정보 설정</span><span class="sxs-lookup"><span data-stu-id="db213-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="db213-112">가격 책정 계획을 "기본"으로 설정 하 고 일일 데이터 볼륨의 cap를 하루에 400GB 설정 하 고 리소스 그룹 "testgroup"의 리소스 "테스트"에 대 한 적중 캡이 없는 경우 알림 보내기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="db213-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="db213-113">변수</span><span class="sxs-lookup"><span data-stu-id="db213-113">PARAMETERS</span></span>

### <span data-ttu-id="db213-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="db213-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="db213-115">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="db213-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="db213-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="db213-116">-DailyCapGB</span></span>
<span data-ttu-id="db213-117">일일 Cap.</span><span class="sxs-lookup"><span data-stu-id="db213-117">Daily Cap.</span></span>

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

### <span data-ttu-id="db213-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db213-118">-DefaultProfile</span></span>
<span data-ttu-id="db213-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db213-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db213-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="db213-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="db213-121">적중 한 끝이 들리면 알림 보내기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="db213-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="db213-122">-이름</span><span class="sxs-lookup"><span data-stu-id="db213-122">-Name</span></span>
<span data-ttu-id="db213-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db213-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="db213-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="db213-124">-PricingPlan</span></span>
<span data-ttu-id="db213-125">가격 계획 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db213-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="db213-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db213-126">-ResourceGroupName</span></span>
<span data-ttu-id="db213-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db213-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="db213-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db213-128">-ResourceId</span></span>
<span data-ttu-id="db213-129">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db213-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="db213-130">-확인</span><span class="sxs-lookup"><span data-stu-id="db213-130">-Confirm</span></span>
<span data-ttu-id="db213-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db213-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db213-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db213-132">-WhatIf</span></span>
<span data-ttu-id="db213-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db213-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db213-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db213-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db213-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db213-135">CommonParameters</span></span>
<span data-ttu-id="db213-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db213-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db213-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db213-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db213-138">입력</span><span class="sxs-lookup"><span data-stu-id="db213-138">INPUTS</span></span>

### <span data-ttu-id="db213-139">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="db213-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="db213-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="db213-140">System.String</span></span>

## <span data-ttu-id="db213-141">출력</span><span class="sxs-lookup"><span data-stu-id="db213-141">OUTPUTS</span></span>

### <span data-ttu-id="db213-142">PSPricingPlan-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="db213-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="db213-143">상속자</span><span class="sxs-lookup"><span data-stu-id="db213-143">NOTES</span></span>

## <span data-ttu-id="db213-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db213-144">RELATED LINKS</span></span>
