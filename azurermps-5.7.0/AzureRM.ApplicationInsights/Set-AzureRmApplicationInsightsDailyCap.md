---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 12e8e4f76f623391e6046f4f8b0bd424e7b9334d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702391"
---
# <span data-ttu-id="4dc94-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="4dc94-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="4dc94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc94-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc94-103">Application insights 리소스의 일일 데이터 볼륨 문자 집합 설정</span><span class="sxs-lookup"><span data-stu-id="4dc94-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dc94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4dc94-104">SYNTAX</span></span>

### <span data-ttu-id="4dc94-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4dc94-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4dc94-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dc94-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc94-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dc94-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dc94-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4dc94-108">DESCRIPTION</span></span>
<span data-ttu-id="4dc94-109">Application insights 리소스의 일일 데이터 볼륨 문자 집합 설정</span><span class="sxs-lookup"><span data-stu-id="4dc94-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="4dc94-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4dc94-110">EXAMPLES</span></span>

### <span data-ttu-id="4dc94-111">예제 1 application insights 리소스의 일일 데이터 볼륨 cap 설정</span><span class="sxs-lookup"><span data-stu-id="4dc94-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="4dc94-112">일일 데이터를 400GB en cap를 하루에 설정 하 고 리소스 그룹 "testgroup"의 리소스 "테스트"에 대 한 적중 cap에 대 한 알림 보내기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="4dc94-113">변수</span><span class="sxs-lookup"><span data-stu-id="4dc94-113">PARAMETERS</span></span>

### <span data-ttu-id="4dc94-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4dc94-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4dc94-115">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="4dc94-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc94-116">-확인</span><span class="sxs-lookup"><span data-stu-id="4dc94-116">-Confirm</span></span>
<span data-ttu-id="4dc94-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc94-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="4dc94-118">-DailyCapGB</span></span>
<span data-ttu-id="4dc94-119">일일 Cap.</span><span class="sxs-lookup"><span data-stu-id="4dc94-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc94-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc94-120">-DefaultProfile</span></span>
<span data-ttu-id="4dc94-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc94-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="4dc94-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="4dc94-123">적중 한 끝이 들리면 알림 보내기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-123">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="4dc94-124">-이름</span><span class="sxs-lookup"><span data-stu-id="4dc94-124">-Name</span></span>
<span data-ttu-id="4dc94-125">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc94-126">-ResourceGroupName</span></span>
<span data-ttu-id="4dc94-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc94-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dc94-128">-ResourceId</span></span>
<span data-ttu-id="4dc94-129">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc94-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc94-130">-WhatIf</span></span>
<span data-ttu-id="4dc94-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dc94-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc94-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc94-133">CommonParameters</span></span>
<span data-ttu-id="4dc94-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dc94-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc94-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dc94-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc94-136">입력</span><span class="sxs-lookup"><span data-stu-id="4dc94-136">INPUTS</span></span>

### <span data-ttu-id="4dc94-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4dc94-137">System.String</span></span>
<span data-ttu-id="4dc94-138">시스템. a 2/부울</span><span class="sxs-lookup"><span data-stu-id="4dc94-138">System.Double System.Boolean</span></span>

## <span data-ttu-id="4dc94-139">출력</span><span class="sxs-lookup"><span data-stu-id="4dc94-139">OUTPUTS</span></span>

### <span data-ttu-id="4dc94-140">PSPricingTier-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="4dc94-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="4dc94-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4dc94-141">NOTES</span></span>

## <span data-ttu-id="4dc94-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dc94-142">RELATED LINKS</span></span>

