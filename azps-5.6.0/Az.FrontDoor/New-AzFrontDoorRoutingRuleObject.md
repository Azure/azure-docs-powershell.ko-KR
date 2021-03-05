---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 3d66db0baeca0e371800c4544f2f0360c448b108
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970987"
---
# <span data-ttu-id="66a29-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="66a29-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="66a29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66a29-102">SYNOPSIS</span></span>
<span data-ttu-id="66a29-103">Front Door 만들기를 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="66a29-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="66a29-104">구문</span><span class="sxs-lookup"><span data-stu-id="66a29-104">SYNTAX</span></span>

### <span data-ttu-id="66a29-105">ByFieldsWithForwardingParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="66a29-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66a29-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a29-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a29-107">설명</span><span class="sxs-lookup"><span data-stu-id="66a29-107">DESCRIPTION</span></span>
<span data-ttu-id="66a29-108">Front Door 만들기를 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="66a29-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="66a29-109">예제</span><span class="sxs-lookup"><span data-stu-id="66a29-109">EXAMPLES</span></span>

### <span data-ttu-id="66a29-110">예제 1: 전달 규칙으로 Front Door 만들기에 대한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="66a29-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="66a29-111">예제 2: 리디렉션 규칙으로 Front Door 만들기에 대한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="66a29-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="66a29-112">Front Door 만들기를 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="66a29-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="66a29-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="66a29-113">PARAMETERS</span></span>

### <span data-ttu-id="66a29-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="66a29-114">-AcceptedProtocol</span></span>
<span data-ttu-id="66a29-115">이 규칙에 일치할 프로토콜 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="66a29-116">기본값은 {Https, Http}입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="66a29-117">-BackendPoolName</span></span>
<span data-ttu-id="66a29-118">이 규칙이 라우팅하는 BackendPool의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="66a29-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="66a29-119">-CustomForwardingPath</span></span>
<span data-ttu-id="66a29-120">이 규칙과 일치하는 리소스 경로를 다시 쓰는 데 사용되는 사용자 지정 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="66a29-121">들어오는 경로를 사용하기 위해 비워 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="66a29-122">-CustomFragment</span></span>
<span data-ttu-id="66a29-123">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="66a29-124">조각은 #에 나오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="66a29-125">#을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="66a29-126">-CustomHost</span></span>
<span data-ttu-id="66a29-127">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-127">Host to redirect.</span></span> <span data-ttu-id="66a29-128">수신 호스트를 대상 호스트로 사용하기 위해 비워 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="66a29-129">-CustomPath</span></span>
<span data-ttu-id="66a29-130">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-130">The full path to redirect.</span></span> <span data-ttu-id="66a29-131">경로는 비어 있을 수 없습니다. /로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="66a29-132">들어오는 경로를 대상 경로로 사용하기 위해 비워 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="66a29-133">-CustomQueryString</span></span>
<span data-ttu-id="66a29-134">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="66a29-135">이 값을 설정하면 기존 쿼리 문자열이 대체됩니다. 들어오는 쿼리 문자열을 보존하기 위해 비워 두면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="66a29-136">쿼리 문자열이 에 있어야 합니다. <key>=</span><span class="sxs-lookup"><span data-stu-id="66a29-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="66a29-137">형식입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-137">format.</span></span> <span data-ttu-id="66a29-138">첫 번째?</span><span class="sxs-lookup"><span data-stu-id="66a29-138">The first ?</span></span> <span data-ttu-id="66a29-139">및 & 자동으로 추가될 수 있으므로 프런트에 포함하지 않지만 여러 쿼리 문자열을 사용하여 별도의 여러 쿼리 문자열을 &.</span><span class="sxs-lookup"><span data-stu-id="66a29-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a29-140">-DefaultProfile</span></span>
<span data-ttu-id="66a29-141">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a29-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="66a29-142">-DynamicCompression</span></span>
<span data-ttu-id="66a29-143">캐싱을 사용할 때 캐시된 콘텐츠에 대해 동적 압축을 사용하도록 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="66a29-144">기본값이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="66a29-145">-EnableCaching</span></span>
<span data-ttu-id="66a29-146">이 경로에 대해 캐싱을 사용하도록 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="66a29-147">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="66a29-148">-EnabledState</span></span>
<span data-ttu-id="66a29-149">이 규칙을 사용하도록 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="66a29-150">기본값이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="66a29-151">-ForwardingProtocol</span></span>
<span data-ttu-id="66a29-152">이 규칙은 백end에 트래픽을 전달할 때 사용할 프로토콜 기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="66a29-153">-FrontDoorName</span></span>
<span data-ttu-id="66a29-154">이 라우팅 규칙이 속한 Front Door의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-154">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-155">-FrontendpointName</span><span class="sxs-lookup"><span data-stu-id="66a29-155">-FrontendEndpointName</span></span>
<span data-ttu-id="66a29-156">이 규칙과 연결된 Frontend 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="66a29-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-157">-Name</span><span class="sxs-lookup"><span data-stu-id="66a29-157">-Name</span></span>
<span data-ttu-id="66a29-158">라우팅Rule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-158">RoutingRule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="66a29-159">-PatternToMatch</span></span>
<span data-ttu-id="66a29-160">규칙의 경로 패턴은 경로의 끝에 있는 최종 /을 제외하고 \* 를 를 들이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="66a29-161">기본값은 /\*</span><span class="sxs-lookup"><span data-stu-id="66a29-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="66a29-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="66a29-163">캐시 키를 구성할 때 URL 쿼리 용어 처리</span><span class="sxs-lookup"><span data-stu-id="66a29-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="66a29-164">기본값은 StripAll입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="66a29-165">-RedirectProtocol</span></span>
<span data-ttu-id="66a29-166">트래픽이 리디렉션되는 대상의 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="66a29-167">기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="66a29-168">-RedirectType</span></span>
<span data-ttu-id="66a29-169">트래픽을 리디렉션할 때 규칙이 사용할 리디렉션 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="66a29-170">기본값이 이동됩니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a29-171">-ResourceGroupName</span></span>
<span data-ttu-id="66a29-172">RoutingRule이 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-172">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="66a29-173">-RulesEngineName</span></span>
<span data-ttu-id="66a29-174">이 경로에 적용할 특정 규칙 엔진 구성에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a29-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a29-175">CommonParameters</span></span>
<span data-ttu-id="66a29-176">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66a29-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a29-177">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66a29-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a29-178">입력</span><span class="sxs-lookup"><span data-stu-id="66a29-178">INPUTS</span></span>

### <span data-ttu-id="66a29-179">없음</span><span class="sxs-lookup"><span data-stu-id="66a29-179">None</span></span>

## <span data-ttu-id="66a29-180">출력</span><span class="sxs-lookup"><span data-stu-id="66a29-180">OUTPUTS</span></span>

### <span data-ttu-id="66a29-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="66a29-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="66a29-182">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66a29-182">NOTES</span></span>

## <span data-ttu-id="66a29-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66a29-183">RELATED LINKS</span></span>

<span data-ttu-id="66a29-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="66a29-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
