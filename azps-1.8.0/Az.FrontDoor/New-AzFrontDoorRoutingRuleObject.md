---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868366"
---
# <span data-ttu-id="9b255-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="9b255-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="9b255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b255-102">SYNOPSIS</span></span>
<span data-ttu-id="9b255-103">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="9b255-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="9b255-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b255-104">SYNTAX</span></span>

### <span data-ttu-id="9b255-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b255-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b255-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b255-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b255-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9b255-107">DESCRIPTION</span></span>
<span data-ttu-id="9b255-108">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="9b255-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="9b255-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9b255-109">EXAMPLES</span></span>

### <span data-ttu-id="9b255-110">예제 1: 전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="9b255-110">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="9b255-111">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="9b255-111">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="9b255-112">변수</span><span class="sxs-lookup"><span data-stu-id="9b255-112">PARAMETERS</span></span>

### <span data-ttu-id="9b255-113">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="9b255-113">-AcceptedProtocol</span></span>
<span data-ttu-id="9b255-114">이 규칙에 대해 일치 시킬 프로토콜 스키마입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-114">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="9b255-115">기본값은 {Https, Http}입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-115">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="9b255-116">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="9b255-116">-BackendPoolName</span></span>
<span data-ttu-id="9b255-117">이 규칙이 회람 되는 BackendPool의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-117">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="9b255-118">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="9b255-118">-CustomForwardingPath</span></span>
<span data-ttu-id="9b255-119">이 규칙과 일치 하는 리소스 경로를 다시 작성 하는 데 사용 되는 사용자 지정 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-119">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="9b255-120">들어오는 경로를 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="9b255-120">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="9b255-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="9b255-121">-CustomFragment</span></span>
<span data-ttu-id="9b255-122">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-122">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="9b255-123">단편은 # 다음에 오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-123">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="9b255-124"># .를 포함 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="9b255-124">Do not include the #.</span></span>

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

### <span data-ttu-id="9b255-125">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="9b255-125">-CustomHost</span></span>
<span data-ttu-id="9b255-126">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-126">Host to redirect.</span></span> <span data-ttu-id="9b255-127">들어오는 호스트를 대상 호스트로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="9b255-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="9b255-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="9b255-128">-CustomPath</span></span>
<span data-ttu-id="9b255-129">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-129">The full path to redirect.</span></span> <span data-ttu-id="9b255-130">경로는 비워 둘 수 없으며/로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-130">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="9b255-131">들어오는 경로를 대상 경로로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="9b255-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="9b255-132">-CustomQueryString 쿼리</span><span class="sxs-lookup"><span data-stu-id="9b255-132">-CustomQueryString</span></span>
<span data-ttu-id="9b255-133">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-133">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="9b255-134">이 값을 설정 하면 기존 쿼리 문자열이 바뀝니다. 수신 쿼리 문자열을 보존 하려면 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="9b255-135">쿼리 문자열은 <key>=</span><span class="sxs-lookup"><span data-stu-id="9b255-135">Query string must be in <key>=</span></span><value> <span data-ttu-id="9b255-136">포맷할.</span><span class="sxs-lookup"><span data-stu-id="9b255-136">format.</span></span> <span data-ttu-id="9b255-137">첫 번째?</span><span class="sxs-lookup"><span data-stu-id="9b255-137">The first ?</span></span> <span data-ttu-id="9b255-138">및 &는 자동으로 추가 되므로 맨 앞에 포함 되지 않고 여러 쿼리 문자열을 &와 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-138">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="9b255-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b255-139">-DefaultProfile</span></span>
<span data-ttu-id="9b255-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b255-141">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="9b255-141">-DynamicCompression</span></span>
<span data-ttu-id="9b255-142">캐싱이 설정 된 경우 캐시 된 콘텐츠에 대 한 동적 압축을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-142">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="9b255-143">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-143">Default value is Enabled</span></span>

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

### <span data-ttu-id="9b255-144">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="9b255-144">-EnableCaching</span></span>
<span data-ttu-id="9b255-145">이 경로에 캐싱을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-145">Whether to enable caching for this route.</span></span> <span data-ttu-id="9b255-146">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-146">Default value is false</span></span>

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

### <span data-ttu-id="9b255-147">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="9b255-147">-EnabledState</span></span>
<span data-ttu-id="9b255-148">이 규칙의 사용 가능 여부</span><span class="sxs-lookup"><span data-stu-id="9b255-148">Whether to enable use of this rule.</span></span>
<span data-ttu-id="9b255-149">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-149">Default value is Enabled</span></span>

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

### <span data-ttu-id="9b255-150">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="9b255-150">-ForwardingProtocol</span></span>
<span data-ttu-id="9b255-151">이 규칙은 트래픽을 백 엔드로 전달할 때 사용할 프로토콜입니다. 기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-151">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b255-152">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="9b255-152">-FrontDoorName</span></span>
<span data-ttu-id="9b255-153">이 라우팅 규칙이 속한 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-153">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="9b255-154">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="9b255-154">-FrontendEndpointName</span></span>
<span data-ttu-id="9b255-155">이 규칙과 연결 된 프런트 엔드 끝점의 이름</span><span class="sxs-lookup"><span data-stu-id="9b255-155">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="9b255-156">-이름</span><span class="sxs-lookup"><span data-stu-id="9b255-156">-Name</span></span>
<span data-ttu-id="9b255-157">RoutingRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-157">RoutingRule name.</span></span>

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

### <span data-ttu-id="9b255-158">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="9b255-158">-PatternToMatch</span></span>
<span data-ttu-id="9b255-159">규칙의 경로 패턴에는 경로 끝/마지막/이후를 제외한 아무 \*도 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-159">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="9b255-160">기본값은/\*입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-160">Default value is /\*</span></span>

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

### <span data-ttu-id="9b255-161">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="9b255-161">-QueryParameterStripDirective</span></span>
<span data-ttu-id="9b255-162">캐시 키를 형성할 때의 URL 쿼리 용어 처리입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-162">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="9b255-163">기본값은 StripAll입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-163">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b255-164">로 RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="9b255-164">-RedirectProtocol</span></span>
<span data-ttu-id="9b255-165">트래픽이 리디렉션되는 대상의 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-165">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="9b255-166">기본 값이 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-166">Default value is MatchRequest</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b255-167">RedirectType</span><span class="sxs-lookup"><span data-stu-id="9b255-167">-RedirectType</span></span>
<span data-ttu-id="9b255-168">트래픽을 리디렉션하는 데 사용할 규칙의 리디렉션 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-168">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="9b255-169">기본 값이 이동 됨</span><span class="sxs-lookup"><span data-stu-id="9b255-169">Default Value is Moved</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b255-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b255-170">-ResourceGroupName</span></span>
<span data-ttu-id="9b255-171">RoutingRule를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-171">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="9b255-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b255-172">CommonParameters</span></span>
<span data-ttu-id="9b255-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b255-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b255-174">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b255-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b255-175">입력</span><span class="sxs-lookup"><span data-stu-id="9b255-175">INPUTS</span></span>

### <span data-ttu-id="9b255-176">않아야</span><span class="sxs-lookup"><span data-stu-id="9b255-176">None</span></span>

## <span data-ttu-id="9b255-177">출력</span><span class="sxs-lookup"><span data-stu-id="9b255-177">OUTPUTS</span></span>

### <span data-ttu-id="9b255-178">FrontDoor. PSRoutingRule/.</span><span class="sxs-lookup"><span data-stu-id="9b255-178">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="9b255-179">상속자</span><span class="sxs-lookup"><span data-stu-id="9b255-179">NOTES</span></span>

## <span data-ttu-id="9b255-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b255-180">RELATED LINKS</span></span>

<span data-ttu-id="9b255-181">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="9b255-181">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
