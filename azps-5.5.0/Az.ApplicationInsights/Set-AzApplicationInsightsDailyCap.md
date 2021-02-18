---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201241"
---
# <span data-ttu-id="a5e1e-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="a5e1e-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="a5e1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e1e-103">Application Insights 리소스에 대한 일일 데이터 볼륨 한도 설정</span><span class="sxs-lookup"><span data-stu-id="a5e1e-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="a5e1e-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5e1e-104">SYNTAX</span></span>

### <span data-ttu-id="a5e1e-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5e1e-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5e1e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e1e-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e1e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e1e-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5e1e-108">설명</span><span class="sxs-lookup"><span data-stu-id="a5e1e-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e1e-109">Application Insights 리소스에 대한 일일 데이터 볼륨 한도 설정</span><span class="sxs-lookup"><span data-stu-id="a5e1e-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="a5e1e-110">예제</span><span class="sxs-lookup"><span data-stu-id="a5e1e-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e1e-111">예제 1 Application Insights 리소스에 대한 일일 데이터 볼륨 한도 설정</span><span class="sxs-lookup"><span data-stu-id="a5e1e-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="a5e1e-112">일일 데이터 볼륨 한도는 하루 400GB로 설정하고 리소스 그룹 "testgroup"에서 리소스 "테스트"에 대한 한도에 적중하면 보내기 알림을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a5e1e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5e1e-113">PARAMETERS</span></span>

### <span data-ttu-id="a5e1e-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a5e1e-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a5e1e-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="a5e1e-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="a5e1e-116">-DailyCapGB</span></span>
<span data-ttu-id="a5e1e-117">일일 한도입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-117">Daily Cap.</span></span>

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

### <span data-ttu-id="a5e1e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e1e-118">-DefaultProfile</span></span>
<span data-ttu-id="a5e1e-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5e1e-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="a5e1e-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="a5e1e-121">한도에 맞을 때 알림 보내기 중지</span><span class="sxs-lookup"><span data-stu-id="a5e1e-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="a5e1e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a5e1e-122">-Name</span></span>
<span data-ttu-id="a5e1e-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="a5e1e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e1e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5e1e-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a5e1e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e1e-126">-ResourceId</span></span>
<span data-ttu-id="a5e1e-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="a5e1e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5e1e-128">-Confirm</span></span>
<span data-ttu-id="a5e1e-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e1e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e1e-130">-WhatIf</span></span>
<span data-ttu-id="a5e1e-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a5e1e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5e1e-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e1e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e1e-133">CommonParameters</span></span>
<span data-ttu-id="a5e1e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e1e-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a5e1e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e1e-136">입력</span><span class="sxs-lookup"><span data-stu-id="a5e1e-136">INPUTS</span></span>

### <span data-ttu-id="a5e1e-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a5e1e-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a5e1e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a5e1e-138">System.String</span></span>

## <span data-ttu-id="a5e1e-139">출력</span><span class="sxs-lookup"><span data-stu-id="a5e1e-139">OUTPUTS</span></span>

### <span data-ttu-id="a5e1e-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="a5e1e-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="a5e1e-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5e1e-141">NOTES</span></span>

## <span data-ttu-id="a5e1e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5e1e-142">RELATED LINKS</span></span>
