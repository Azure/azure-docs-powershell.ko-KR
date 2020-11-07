---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: 3f46445bbdf8f3b9e7a25f4ab5bda0fd11961e00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701652"
---
# <span data-ttu-id="62fec-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="62fec-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="62fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62fec-102">SYNOPSIS</span></span>
<span data-ttu-id="62fec-103">Application insights 리소스의 일일 데이터 볼륨 문자 집합 설정</span><span class="sxs-lookup"><span data-stu-id="62fec-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="62fec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62fec-104">SYNTAX</span></span>

### <span data-ttu-id="62fec-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="62fec-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62fec-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62fec-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62fec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62fec-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62fec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="62fec-108">DESCRIPTION</span></span>
<span data-ttu-id="62fec-109">Application insights 리소스의 일일 데이터 볼륨 문자 집합 설정</span><span class="sxs-lookup"><span data-stu-id="62fec-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="62fec-110">예제의</span><span class="sxs-lookup"><span data-stu-id="62fec-110">EXAMPLES</span></span>

### <span data-ttu-id="62fec-111">예제 1 application insights 리소스의 일일 데이터 볼륨 cap 설정</span><span class="sxs-lookup"><span data-stu-id="62fec-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="62fec-112">일일 데이터를 400GB en cap를 하루에 설정 하 고 리소스 그룹 "testgroup"의 리소스 "테스트"에 대 한 적중 cap에 대 한 알림 보내기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="62fec-113">변수</span><span class="sxs-lookup"><span data-stu-id="62fec-113">PARAMETERS</span></span>

### <span data-ttu-id="62fec-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="62fec-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="62fec-115">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="62fec-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="62fec-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="62fec-116">-DailyCapGB</span></span>
<span data-ttu-id="62fec-117">일일 Cap.</span><span class="sxs-lookup"><span data-stu-id="62fec-117">Daily Cap.</span></span>

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

### <span data-ttu-id="62fec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fec-118">-DefaultProfile</span></span>
<span data-ttu-id="62fec-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62fec-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="62fec-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="62fec-121">적중 한 끝이 들리면 알림 보내기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="62fec-122">-이름</span><span class="sxs-lookup"><span data-stu-id="62fec-122">-Name</span></span>
<span data-ttu-id="62fec-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="62fec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62fec-124">-ResourceGroupName</span></span>
<span data-ttu-id="62fec-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="62fec-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62fec-126">-ResourceId</span></span>
<span data-ttu-id="62fec-127">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="62fec-128">-확인</span><span class="sxs-lookup"><span data-stu-id="62fec-128">-Confirm</span></span>
<span data-ttu-id="62fec-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62fec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62fec-130">-WhatIf</span></span>
<span data-ttu-id="62fec-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62fec-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62fec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fec-133">CommonParameters</span></span>
<span data-ttu-id="62fec-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62fec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fec-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62fec-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fec-136">입력</span><span class="sxs-lookup"><span data-stu-id="62fec-136">INPUTS</span></span>

### <span data-ttu-id="62fec-137">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="62fec-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="62fec-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62fec-138">System.String</span></span>

## <span data-ttu-id="62fec-139">출력</span><span class="sxs-lookup"><span data-stu-id="62fec-139">OUTPUTS</span></span>

### <span data-ttu-id="62fec-140">PSPricingPlan-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="62fec-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="62fec-141">상속자</span><span class="sxs-lookup"><span data-stu-id="62fec-141">NOTES</span></span>

## <span data-ttu-id="62fec-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62fec-142">RELATED LINKS</span></span>