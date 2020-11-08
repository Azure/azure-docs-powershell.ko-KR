---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 943089433ca7007ef81648846a48ebdd5684bab2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047979"
---
# <span data-ttu-id="684f1-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="684f1-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="684f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="684f1-102">SYNOPSIS</span></span>
<span data-ttu-id="684f1-103">Application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="684f1-103">Get application insights resources</span></span>

## <span data-ttu-id="684f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="684f1-104">SYNTAX</span></span>

### <span data-ttu-id="684f1-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="684f1-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="684f1-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="684f1-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="684f1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="684f1-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="684f1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="684f1-108">DESCRIPTION</span></span>
<span data-ttu-id="684f1-109">리소스 그룹 또는 특정 리소스의 application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="684f1-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="684f1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="684f1-110">EXAMPLES</span></span>

### <span data-ttu-id="684f1-111">예제 1 application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="684f1-111">Example 1 Get application insights resource</span></span>
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

<span data-ttu-id="684f1-112">리소스 그룹 "testgroup"에서 "test" 라는 application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="684f1-112">Get application insights resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="684f1-113">예제 2 가격 계획 정보가 포함 되어 있는 application insights 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="684f1-113">Example 2 Get application insights resource with pricing plan information</span></span>
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

<span data-ttu-id="684f1-114">Application insights 리소스를 가져오고 리소스 그룹 "testgroup"에서 "test" 리소스에 대 한 가격 계획 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="684f1-114">Get application insights resource and include pricing plan information for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="684f1-115">변수</span><span class="sxs-lookup"><span data-stu-id="684f1-115">PARAMETERS</span></span>

### <span data-ttu-id="684f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684f1-116">-DefaultProfile</span></span>
<span data-ttu-id="684f1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="684f1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="684f1-118">-전체</span><span class="sxs-lookup"><span data-stu-id="684f1-118">-Full</span></span>
<span data-ttu-id="684f1-119">지정 하는 경우 application insights 구성 요소에 대 한 자세한 가격 계획/일일 cap 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="684f1-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

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

### <span data-ttu-id="684f1-120">-이름</span><span class="sxs-lookup"><span data-stu-id="684f1-120">-Name</span></span>
<span data-ttu-id="684f1-121">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="684f1-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="684f1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684f1-122">-ResourceGroupName</span></span>
<span data-ttu-id="684f1-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="684f1-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="684f1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="684f1-124">-ResourceId</span></span>
<span data-ttu-id="684f1-125">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="684f1-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="684f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684f1-126">CommonParameters</span></span>
<span data-ttu-id="684f1-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="684f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684f1-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="684f1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684f1-129">입력</span><span class="sxs-lookup"><span data-stu-id="684f1-129">INPUTS</span></span>

### <span data-ttu-id="684f1-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="684f1-130">System.String</span></span>

## <span data-ttu-id="684f1-131">출력</span><span class="sxs-lookup"><span data-stu-id="684f1-131">OUTPUTS</span></span>

### <span data-ttu-id="684f1-132">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="684f1-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="684f1-133">상속자</span><span class="sxs-lookup"><span data-stu-id="684f1-133">NOTES</span></span>

## <span data-ttu-id="684f1-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="684f1-134">RELATED LINKS</span></span>
