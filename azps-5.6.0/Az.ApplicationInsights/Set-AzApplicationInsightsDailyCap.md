---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: ce4c9d8fd297b53eb628ffcc32ad9479e0647dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014331"
---
# <span data-ttu-id="16b27-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="16b27-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="16b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16b27-102">SYNOPSIS</span></span>
<span data-ttu-id="16b27-103">애플리케이션 인사이트 리소스에 대한 일일 데이터 볼륨 한도 설정</span><span class="sxs-lookup"><span data-stu-id="16b27-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="16b27-104">구문</span><span class="sxs-lookup"><span data-stu-id="16b27-104">SYNTAX</span></span>

### <span data-ttu-id="16b27-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="16b27-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16b27-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16b27-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b27-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16b27-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16b27-108">설명</span><span class="sxs-lookup"><span data-stu-id="16b27-108">DESCRIPTION</span></span>
<span data-ttu-id="16b27-109">애플리케이션 인사이트 리소스에 대한 일일 데이터 볼륨 한도 설정</span><span class="sxs-lookup"><span data-stu-id="16b27-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="16b27-110">예제</span><span class="sxs-lookup"><span data-stu-id="16b27-110">EXAMPLES</span></span>

### <span data-ttu-id="16b27-111">예제 1 애플리케이션 인사이트 리소스에 대한 일일 데이터 볼륨 한도 설정</span><span class="sxs-lookup"><span data-stu-id="16b27-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="16b27-112">리소스 그룹 "testgroup"에서 리소스 "테스트"에 대해 일일 데이터 볼륨 한도를 하루 400GB로 설정하고 알림 보내기 중지</span><span class="sxs-lookup"><span data-stu-id="16b27-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="16b27-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="16b27-113">PARAMETERS</span></span>

### <span data-ttu-id="16b27-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="16b27-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="16b27-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="16b27-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="16b27-116">-DailyCapGB</span></span>
<span data-ttu-id="16b27-117">일일 한도입니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-117">Daily Cap.</span></span>

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

### <span data-ttu-id="16b27-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b27-118">-DefaultProfile</span></span>
<span data-ttu-id="16b27-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16b27-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="16b27-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="16b27-121">한도 적중 시 알림 보내기 중지</span><span class="sxs-lookup"><span data-stu-id="16b27-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="16b27-122">-Name</span><span class="sxs-lookup"><span data-stu-id="16b27-122">-Name</span></span>
<span data-ttu-id="16b27-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="16b27-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b27-124">-ResourceGroupName</span></span>
<span data-ttu-id="16b27-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="16b27-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16b27-126">-ResourceId</span></span>
<span data-ttu-id="16b27-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="16b27-128">-확인</span><span class="sxs-lookup"><span data-stu-id="16b27-128">-Confirm</span></span>
<span data-ttu-id="16b27-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b27-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b27-130">-WhatIf</span></span>
<span data-ttu-id="16b27-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16b27-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b27-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b27-133">CommonParameters</span></span>
<span data-ttu-id="16b27-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16b27-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b27-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16b27-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b27-136">입력</span><span class="sxs-lookup"><span data-stu-id="16b27-136">INPUTS</span></span>

### <span data-ttu-id="16b27-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="16b27-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="16b27-138">System.String</span><span class="sxs-lookup"><span data-stu-id="16b27-138">System.String</span></span>

## <span data-ttu-id="16b27-139">출력</span><span class="sxs-lookup"><span data-stu-id="16b27-139">OUTPUTS</span></span>

### <span data-ttu-id="16b27-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="16b27-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="16b27-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16b27-141">NOTES</span></span>

## <span data-ttu-id="16b27-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16b27-142">RELATED LINKS</span></span>
