---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 943089433ca7007ef81648846a48ebdd5684bab2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195308"
---
# <span data-ttu-id="9bfe7-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9bfe7-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="9bfe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bfe7-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfe7-103">Application Insights 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="9bfe7-103">Get application insights resources</span></span>

## <span data-ttu-id="9bfe7-104">구문</span><span class="sxs-lookup"><span data-stu-id="9bfe7-104">SYNTAX</span></span>

### <span data-ttu-id="9bfe7-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9bfe7-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9bfe7-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bfe7-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bfe7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bfe7-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bfe7-108">설명</span><span class="sxs-lookup"><span data-stu-id="9bfe7-108">DESCRIPTION</span></span>
<span data-ttu-id="9bfe7-109">리소스 그룹 또는 특정 리소스에서 Application Insights 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="9bfe7-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="9bfe7-110">예제</span><span class="sxs-lookup"><span data-stu-id="9bfe7-110">EXAMPLES</span></span>

### <span data-ttu-id="9bfe7-111">예제 1 Application Insights 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="9bfe7-111">Example 1 Get application insights resource</span></span>
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

<span data-ttu-id="9bfe7-112">리소스 그룹 "testgroup"에서 "test"라는 Application Insights 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="9bfe7-113">예제 2 가격 책정 계획 정보를 통해 Application Insights 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="9bfe7-113">Example 2 Get application insights resource with pricing plan information</span></span>
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

<span data-ttu-id="9bfe7-114">Application Insights 리소스를 확보하고 리소스 그룹 "testgroup"에서 "test"라는 리소스에 대한 가격 책정 계획 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="9bfe7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bfe7-115">PARAMETERS</span></span>

### <span data-ttu-id="9bfe7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfe7-116">-DefaultProfile</span></span>
<span data-ttu-id="9bfe7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bfe7-118">-Full</span><span class="sxs-lookup"><span data-stu-id="9bfe7-118">-Full</span></span>
<span data-ttu-id="9bfe7-119">지정된 경우 Application Insights 구성 요소의 가격 책정 계획/일일 한도 및 상태를 다시 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

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

### <span data-ttu-id="9bfe7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9bfe7-120">-Name</span></span>
<span data-ttu-id="9bfe7-121">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="9bfe7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bfe7-122">-ResourceGroupName</span></span>
<span data-ttu-id="9bfe7-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="9bfe7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bfe7-124">-ResourceId</span></span>
<span data-ttu-id="9bfe7-125">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9bfe7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfe7-126">CommonParameters</span></span>
<span data-ttu-id="9bfe7-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfe7-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9bfe7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfe7-129">입력</span><span class="sxs-lookup"><span data-stu-id="9bfe7-129">INPUTS</span></span>

### <span data-ttu-id="9bfe7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9bfe7-130">System.String</span></span>

## <span data-ttu-id="9bfe7-131">출력</span><span class="sxs-lookup"><span data-stu-id="9bfe7-131">OUTPUTS</span></span>

### <span data-ttu-id="9bfe7-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9bfe7-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="9bfe7-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9bfe7-133">NOTES</span></span>

## <span data-ttu-id="9bfe7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bfe7-134">RELATED LINKS</span></span>
