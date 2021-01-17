---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489719"
---
# <span data-ttu-id="631e6-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="631e6-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="631e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631e6-102">SYNOPSIS</span></span>
<span data-ttu-id="631e6-103">Front Door 만들기를 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="631e6-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="631e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="631e6-104">SYNTAX</span></span>

### <span data-ttu-id="631e6-105">ByFieldsWithForwardingParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="631e6-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="631e6-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="631e6-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="631e6-107">설명</span><span class="sxs-lookup"><span data-stu-id="631e6-107">DESCRIPTION</span></span>
<span data-ttu-id="631e6-108">Front Door 만들기를 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="631e6-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="631e6-109">예제</span><span class="sxs-lookup"><span data-stu-id="631e6-109">EXAMPLES</span></span>

### <span data-ttu-id="631e6-110">예제 1: 전달 규칙을 사용하여 Front Door를 만들기 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="631e6-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
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

### <span data-ttu-id="631e6-111">예제 2: 리디렉션 규칙을 사용하여 Front Door 만들기를 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="631e6-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
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

<span data-ttu-id="631e6-112">Front Door 만들기를 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="631e6-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="631e6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631e6-113">PARAMETERS</span></span>

### <span data-ttu-id="631e6-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="631e6-114">-AcceptedProtocol</span></span>
<span data-ttu-id="631e6-115">이 규칙과 일치하는 프로토콜 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="631e6-116">기본값은 {Https, Http}입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-116">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="631e6-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="631e6-117">-BackendPoolName</span></span>
<span data-ttu-id="631e6-118">이 규칙이 라우팅하는 BackendPool의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="631e6-118">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="631e6-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="631e6-119">-CustomForwardingPath</span></span>
<span data-ttu-id="631e6-120">이 규칙과 일치하는 리소스 경로를 다시 쓰는 데 사용되는 사용자 지정 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="631e6-121">들어오는 경로를 사용할 수 있는 비워 두기.</span><span class="sxs-lookup"><span data-stu-id="631e6-121">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="631e6-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="631e6-122">-CustomFragment</span></span>
<span data-ttu-id="631e6-123">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="631e6-124">조각은 #다음에 오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="631e6-125">#을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-125">Do not include the #.</span></span>

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

### <span data-ttu-id="631e6-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="631e6-126">-CustomHost</span></span>
<span data-ttu-id="631e6-127">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-127">Host to redirect.</span></span> <span data-ttu-id="631e6-128">들어오는 호스트를 대상 호스트로 사용하길 빈 채로 하세요.</span><span class="sxs-lookup"><span data-stu-id="631e6-128">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="631e6-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="631e6-129">-CustomPath</span></span>
<span data-ttu-id="631e6-130">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-130">The full path to redirect.</span></span> <span data-ttu-id="631e6-131">경로는 비어 있을 수 없습니다. /로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="631e6-132">들어오는 경로를 대상 경로로 사용하길 빈 채로 하세요.</span><span class="sxs-lookup"><span data-stu-id="631e6-132">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="631e6-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="631e6-133">-CustomQueryString</span></span>
<span data-ttu-id="631e6-134">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="631e6-135">이 값을 설정하면 기존 쿼리 문자열이 대체됩니다. 들어오는 쿼리 문자열을 보존하기 위해 비워 두기</span><span class="sxs-lookup"><span data-stu-id="631e6-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="631e6-136">쿼리 문자열은 <key>=</span><span class="sxs-lookup"><span data-stu-id="631e6-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="631e6-137">형식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-137">format.</span></span> <span data-ttu-id="631e6-138">첫 번째?</span><span class="sxs-lookup"><span data-stu-id="631e6-138">The first ?</span></span> <span data-ttu-id="631e6-139">그리고 & 자동으로 추가됩니다. 따라서 앞에 포함하지 말고 여러 쿼리 문자열을 다른 쿼리 문자열로 &.</span><span class="sxs-lookup"><span data-stu-id="631e6-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="631e6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631e6-140">-DefaultProfile</span></span>
<span data-ttu-id="631e6-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="631e6-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="631e6-142">-DynamicCompression</span></span>
<span data-ttu-id="631e6-143">캐싱을 사용할 때 캐시된 콘텐츠에 동적 압축을 사용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="631e6-144">기본값이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-144">Default value is Enabled</span></span>

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

### <span data-ttu-id="631e6-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="631e6-145">-EnableCaching</span></span>
<span data-ttu-id="631e6-146">이 경로에 대해 캐싱을 사용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="631e6-147">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-147">Default value is false</span></span>

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

### <span data-ttu-id="631e6-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="631e6-148">-EnabledState</span></span>
<span data-ttu-id="631e6-149">이 규칙을 사용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="631e6-150">기본값이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-150">Default value is Enabled</span></span>

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

### <span data-ttu-id="631e6-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="631e6-151">-ForwardingProtocol</span></span>
<span data-ttu-id="631e6-152">이 규칙이 백end에 트래픽을 전달할 때 사용할 프로토콜의 기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

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

### <span data-ttu-id="631e6-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="631e6-153">-FrontDoorName</span></span>
<span data-ttu-id="631e6-154">이 라우팅 규칙이 속한 Front Door의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="631e6-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="631e6-155">-FrontendEndpointName</span></span>
<span data-ttu-id="631e6-156">이 규칙과 연결된 프런트 엔드 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="631e6-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="631e6-157">-Name</span><span class="sxs-lookup"><span data-stu-id="631e6-157">-Name</span></span>
<span data-ttu-id="631e6-158">RoutingRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="631e6-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="631e6-159">-PatternToMatch</span></span>
<span data-ttu-id="631e6-160">규칙의 경로 패턴은 경로 끝에 있는 최종/다음을 제외하고 \*를 두지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="631e6-161">기본값은 /\*</span><span class="sxs-lookup"><span data-stu-id="631e6-161">Default value is /\*</span></span>

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

### <span data-ttu-id="631e6-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="631e6-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="631e6-163">캐시 키를 형성할 때 URL 쿼리 용어를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="631e6-164">기본값은 StripAll입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-164">Default value is StripAll</span></span>

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

### <span data-ttu-id="631e6-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="631e6-165">-RedirectProtocol</span></span>
<span data-ttu-id="631e6-166">트래픽이 리디렉션되는 대상의 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="631e6-167">기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-167">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="631e6-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="631e6-168">-RedirectType</span></span>
<span data-ttu-id="631e6-169">트래픽을 리디렉션할 때 규칙이 사용할 리디렉션 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="631e6-170">기본값 이동</span><span class="sxs-lookup"><span data-stu-id="631e6-170">Default Value is Moved</span></span>

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

### <span data-ttu-id="631e6-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631e6-171">-ResourceGroupName</span></span>
<span data-ttu-id="631e6-172">RoutingRule을 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="631e6-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="631e6-173">-RulesEngineName</span></span>
<span data-ttu-id="631e6-174">이 경로에 적용할 특정 규칙 엔진 구성에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="631e6-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631e6-175">CommonParameters</span></span>
<span data-ttu-id="631e6-176">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="631e6-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631e6-177">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="631e6-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631e6-178">입력</span><span class="sxs-lookup"><span data-stu-id="631e6-178">INPUTS</span></span>

### <span data-ttu-id="631e6-179">없음</span><span class="sxs-lookup"><span data-stu-id="631e6-179">None</span></span>

## <span data-ttu-id="631e6-180">출력</span><span class="sxs-lookup"><span data-stu-id="631e6-180">OUTPUTS</span></span>

### <span data-ttu-id="631e6-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="631e6-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="631e6-182">참고 사항</span><span class="sxs-lookup"><span data-stu-id="631e6-182">NOTES</span></span>

## <span data-ttu-id="631e6-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="631e6-183">RELATED LINKS</span></span>

<span data-ttu-id="631e6-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="631e6-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
