---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328670"
---
# <span data-ttu-id="e7705-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="e7705-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="e7705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7705-102">SYNOPSIS</span></span>
<span data-ttu-id="e7705-103">규칙 엔진 규칙을 만들기 위한 PSRulesEngineAction 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="e7705-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7705-104">SYNTAX</span></span>

### <span data-ttu-id="e7705-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7705-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7705-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7705-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7705-107">설명</span><span class="sxs-lookup"><span data-stu-id="e7705-107">DESCRIPTION</span></span>
<span data-ttu-id="e7705-108">규칙 엔진 규칙을 만들기 위한 PSRulesEngineAction 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="e7705-109">cmdlet "New-AzFrontDoorHeaderActionObject"를 사용하여 PSHeaderObjects를 만들어 "-RequestHeaderActions" 및 "-ResponseHeaderActions" 매개 변수에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="e7705-110">예제</span><span class="sxs-lookup"><span data-stu-id="e7705-110">EXAMPLES</span></span>

### <span data-ttu-id="e7705-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7705-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="e7705-112">규칙 엔진 작업을 만들고 만든 규칙 엔진 작업의 속성을 보는 방법을 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="e7705-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="e7705-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7705-113">PARAMETERS</span></span>

### <span data-ttu-id="e7705-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="e7705-114">-BackendPoolName</span></span>
<span data-ttu-id="e7705-115">이 규칙이 라우팅하는 BackendPool의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="e7705-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="e7705-116">-CustomForwardingPath</span></span>
<span data-ttu-id="e7705-117">이 규칙과 일치하는 리소스 경로를 다시 쓰는 데 사용되는 사용자 지정 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="e7705-118">들어오는 경로를 사용할 수 있는 비워 두기.</span><span class="sxs-lookup"><span data-stu-id="e7705-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="e7705-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="e7705-119">-CustomFragment</span></span>
<span data-ttu-id="e7705-120">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="e7705-121">조각은 #다음에 오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="e7705-122">#을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-122">Do not include the #.</span></span>

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

### <span data-ttu-id="e7705-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="e7705-123">-CustomHost</span></span>
<span data-ttu-id="e7705-124">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-124">Host to redirect.</span></span>
<span data-ttu-id="e7705-125">들어오는 호스트를 대상 호스트로 사용하길 빈 채로 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7705-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="e7705-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="e7705-126">-CustomPath</span></span>
<span data-ttu-id="e7705-127">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-127">The full path to redirect.</span></span>
<span data-ttu-id="e7705-128">경로는 비어 있을 수 없습니다. /로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="e7705-129">들어오는 경로를 대상 경로로 사용하길 빈 채로 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7705-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="e7705-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="e7705-130">-CustomQueryString</span></span>
<span data-ttu-id="e7705-131">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="e7705-132">이 값을 설정하면 기존 쿼리 문자열이 대체됩니다. 들어오는 쿼리 문자열을 보존하기 위해 비워 두기</span><span class="sxs-lookup"><span data-stu-id="e7705-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="e7705-133">쿼리 문자열은 형식이 있어야 \<key\> = \<value\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="e7705-134">첫 번째?</span><span class="sxs-lookup"><span data-stu-id="e7705-134">The first ?</span></span>
<span data-ttu-id="e7705-135">그리고 & 자동으로 추가됩니다. 따라서 앞에 포함하지 말고 여러 쿼리 문자열을 다른 쿼리 문자열로 &.</span><span class="sxs-lookup"><span data-stu-id="e7705-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="e7705-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7705-136">-DefaultProfile</span></span>
<span data-ttu-id="e7705-137">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7705-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="e7705-138">-DynamicCompression</span></span>
<span data-ttu-id="e7705-139">캐시된 콘텐츠에 동적 압축을 사용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="e7705-140">기본값이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="e7705-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="e7705-141">-EnableCaching</span></span>
<span data-ttu-id="e7705-142">이 경로에 대해 캐싱을 사용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="e7705-143">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-143">Default value is false</span></span>

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

### <span data-ttu-id="e7705-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="e7705-144">-ForwardingProtocol</span></span>
<span data-ttu-id="e7705-145">이 규칙이 트래픽을 백드에 전달할 때 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="e7705-146">기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="e7705-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e7705-147">-FrontDoorName</span></span>
<span data-ttu-id="e7705-148">이 라우팅 규칙이 속한 Front Door의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="e7705-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="e7705-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="e7705-150">캐시 키를 형성할 때 URL 쿼리 용어를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="e7705-151">기본값은 StripAll입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="e7705-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="e7705-152">-RedirectProtocol</span></span>
<span data-ttu-id="e7705-153">트래픽이 리디렉션되는 대상의 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="e7705-154">기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="e7705-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="e7705-155">-RedirectType</span></span>
<span data-ttu-id="e7705-156">트래픽을 리디렉션할 때 규칙이 사용할 리디렉션 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="e7705-157">기본값 이동</span><span class="sxs-lookup"><span data-stu-id="e7705-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="e7705-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="e7705-158">-RequestHeaderAction</span></span>
<span data-ttu-id="e7705-159">AFD에서 원본으로 요청에서 적용할 헤더 작업의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7705-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7705-160">-ResourceGroupName</span></span>
<span data-ttu-id="e7705-161">RoutingRule을 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="e7705-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="e7705-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="e7705-163">AFD에서 클라이언트로의 응답에서 적용할 헤더 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7705-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7705-164">CommonParameters</span></span>
<span data-ttu-id="e7705-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7705-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7705-166">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7705-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7705-167">입력</span><span class="sxs-lookup"><span data-stu-id="e7705-167">INPUTS</span></span>

### <span data-ttu-id="e7705-168">없음</span><span class="sxs-lookup"><span data-stu-id="e7705-168">None</span></span>

## <span data-ttu-id="e7705-169">출력</span><span class="sxs-lookup"><span data-stu-id="e7705-169">OUTPUTS</span></span>

### <span data-ttu-id="e7705-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="e7705-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="e7705-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7705-171">NOTES</span></span>

## <span data-ttu-id="e7705-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7705-172">RELATED LINKS</span></span>
