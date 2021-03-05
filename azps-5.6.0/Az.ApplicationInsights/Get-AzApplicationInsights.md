---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: f208722a065399c12facce6907bbcad3b64d46e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965275"
---
# <span data-ttu-id="fbc40-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fbc40-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="fbc40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbc40-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc40-103">애플리케이션 인사이트 리소스 확보</span><span class="sxs-lookup"><span data-stu-id="fbc40-103">Get application insights resources</span></span>

## <span data-ttu-id="fbc40-104">구문</span><span class="sxs-lookup"><span data-stu-id="fbc40-104">SYNTAX</span></span>

### <span data-ttu-id="fbc40-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fbc40-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbc40-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbc40-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbc40-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbc40-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbc40-108">설명</span><span class="sxs-lookup"><span data-stu-id="fbc40-108">DESCRIPTION</span></span>
<span data-ttu-id="fbc40-109">리소스 그룹 또는 특정 리소스에서 애플리케이션 인사이트 리소스 확보</span><span class="sxs-lookup"><span data-stu-id="fbc40-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="fbc40-110">예제</span><span class="sxs-lookup"><span data-stu-id="fbc40-110">EXAMPLES</span></span>

### <span data-ttu-id="fbc40-111">예제 1 애플리케이션 인사이트 리소스 확보</span><span class="sxs-lookup"><span data-stu-id="fbc40-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test"

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

<span data-ttu-id="fbc40-112">리소스 그룹 "testgroup"에서 "test"라는 애플리케이션 인사이트 리소스 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fbc40-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="fbc40-113">예제 2 가격 책정 계획 정보를 통해 애플리케이션 인사이트 리소스 확보</span><span class="sxs-lookup"><span data-stu-id="fbc40-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

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

<span data-ttu-id="fbc40-114">애플리케이션 인사이트 리소스를 확보하고 리소스 그룹 "testgroup"에서 "test"라는 리소스에 대한 가격 책정 계획 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="fbc40-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="fbc40-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fbc40-115">PARAMETERS</span></span>

### <span data-ttu-id="fbc40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc40-116">-DefaultProfile</span></span>
<span data-ttu-id="fbc40-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc40-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbc40-118">-Full</span><span class="sxs-lookup"><span data-stu-id="fbc40-118">-Full</span></span>
<span data-ttu-id="fbc40-119">지정된 경우 가격 책정 계획/일일 한도 및 애플리케이션 인사이트 구성 요소의 상태를 다시 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbc40-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

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

### <span data-ttu-id="fbc40-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fbc40-120">-Name</span></span>
<span data-ttu-id="fbc40-121">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc40-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="fbc40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc40-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbc40-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc40-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="fbc40-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbc40-124">-ResourceId</span></span>
<span data-ttu-id="fbc40-125">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc40-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="fbc40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc40-126">CommonParameters</span></span>
<span data-ttu-id="fbc40-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fbc40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc40-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbc40-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc40-129">입력</span><span class="sxs-lookup"><span data-stu-id="fbc40-129">INPUTS</span></span>

### <span data-ttu-id="fbc40-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fbc40-130">System.String</span></span>

## <span data-ttu-id="fbc40-131">출력</span><span class="sxs-lookup"><span data-stu-id="fbc40-131">OUTPUTS</span></span>

### <span data-ttu-id="fbc40-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fbc40-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="fbc40-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fbc40-133">NOTES</span></span>

## <span data-ttu-id="fbc40-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbc40-134">RELATED LINKS</span></span>
