---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsights.md
ms.openlocfilehash: 917c40d5ec4939e3b6c8b5dc31f68088d4380290
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526359"
---
# <span data-ttu-id="ea45b-101">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ea45b-101">Get-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="ea45b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea45b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea45b-103">Application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea45b-103">Get application insights resources</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea45b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea45b-104">SYNTAX</span></span>

### <span data-ttu-id="ea45b-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea45b-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea45b-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea45b-106">ComponentNameParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea45b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea45b-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea45b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ea45b-108">DESCRIPTION</span></span>
<span data-ttu-id="ea45b-109">리소스 그룹 또는 특정 리소스의 application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea45b-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="ea45b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ea45b-110">EXAMPLES</span></span>

### <span data-ttu-id="ea45b-111">예제 1 application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea45b-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="ea45b-112">Resoruce 그룹 "testgroup"에서 "test" 라는 application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea45b-112">Get application insights resource named "test" in resoruce group "testgroup"</span></span>

### <span data-ttu-id="ea45b-113">예제 2 가격 계획 정보가 포함 되어 있는 application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea45b-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="ea45b-114">Application insights 리소스를 가져오고 "test" 리소스에 대 한 가격 계획 정보를 resoruce 그룹 "testgroup"에 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea45b-114">Get application insights resource and include pricing plan information for resource named "test" in resoruce group "testgroup"</span></span>

## <span data-ttu-id="ea45b-115">변수</span><span class="sxs-lookup"><span data-stu-id="ea45b-115">PARAMETERS</span></span>

### <span data-ttu-id="ea45b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea45b-116">-DefaultProfile</span></span>
<span data-ttu-id="ea45b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea45b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea45b-118">-전체</span><span class="sxs-lookup"><span data-stu-id="ea45b-118">-Full</span></span>
<span data-ttu-id="ea45b-119">지정 하는 경우 application insights 구성 요소에 대 한 자세한 가격 계획/일일 cap 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea45b-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea45b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ea45b-120">-Name</span></span>
<span data-ttu-id="ea45b-121">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea45b-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="ea45b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea45b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea45b-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea45b-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="ea45b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea45b-124">-ResourceId</span></span>
<span data-ttu-id="ea45b-125">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea45b-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ea45b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea45b-126">CommonParameters</span></span>
<span data-ttu-id="ea45b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea45b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea45b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea45b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea45b-129">입력</span><span class="sxs-lookup"><span data-stu-id="ea45b-129">INPUTS</span></span>

### <span data-ttu-id="ea45b-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea45b-130">System.String</span></span>

## <span data-ttu-id="ea45b-131">출력</span><span class="sxs-lookup"><span data-stu-id="ea45b-131">OUTPUTS</span></span>

### <span data-ttu-id="ea45b-132">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ea45b-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="ea45b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="ea45b-133">NOTES</span></span>

## <span data-ttu-id="ea45b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea45b-134">RELATED LINKS</span></span>
