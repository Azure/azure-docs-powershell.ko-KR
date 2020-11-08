---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212776"
---
# <span data-ttu-id="8234f-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="8234f-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="8234f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8234f-102">SYNOPSIS</span></span>
<span data-ttu-id="8234f-103">규칙 엔진 규칙을 만들기 위한 PSRulesEngineAction 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="8234f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8234f-104">SYNTAX</span></span>

### <span data-ttu-id="8234f-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="8234f-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8234f-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8234f-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8234f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8234f-107">DESCRIPTION</span></span>
<span data-ttu-id="8234f-108">규칙 엔진 규칙을 만들기 위한 PSRulesEngineAction 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="8234f-109">Cmdlet "New-AzFrontDoorHeaderActionObject"를 사용 하 여 PSHeaderObjects를 만들어 매개 변수 "-RequestHeaderActions" 및 "-ResponseHeaderActions"에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="8234f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8234f-110">EXAMPLES</span></span>

### <span data-ttu-id="8234f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8234f-111">Example 1</span></span>
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

<span data-ttu-id="8234f-112">규칙 엔진 작업을 만들고 만든 규칙 엔진 작업의 속성을 보는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="8234f-113">변수</span><span class="sxs-lookup"><span data-stu-id="8234f-113">PARAMETERS</span></span>

### <span data-ttu-id="8234f-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="8234f-114">-BackendPoolName</span></span>
<span data-ttu-id="8234f-115">이 규칙이 회람 되는 BackendPool의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="8234f-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="8234f-116">-CustomForwardingPath</span></span>
<span data-ttu-id="8234f-117">이 규칙과 일치 하는 리소스 경로를 다시 작성 하는 데 사용 되는 사용자 지정 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="8234f-118">들어오는 경로를 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="8234f-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="8234f-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="8234f-119">-CustomFragment</span></span>
<span data-ttu-id="8234f-120">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="8234f-121">단편은 # 다음에 오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="8234f-122"># .를 포함 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="8234f-122">Do not include the #.</span></span>

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

### <span data-ttu-id="8234f-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="8234f-123">-CustomHost</span></span>
<span data-ttu-id="8234f-124">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-124">Host to redirect.</span></span>
<span data-ttu-id="8234f-125">들어오는 호스트를 대상 호스트로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="8234f-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="8234f-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="8234f-126">-CustomPath</span></span>
<span data-ttu-id="8234f-127">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-127">The full path to redirect.</span></span>
<span data-ttu-id="8234f-128">경로는 비워 둘 수 없으며/로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="8234f-129">들어오는 경로를 대상 경로로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="8234f-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="8234f-130">-CustomQueryString 쿼리</span><span class="sxs-lookup"><span data-stu-id="8234f-130">-CustomQueryString</span></span>
<span data-ttu-id="8234f-131">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="8234f-132">이 값을 설정 하면 기존 쿼리 문자열이 바뀝니다. 수신 쿼리 문자열을 보존 하려면 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="8234f-133">쿼리 문자열은 형식 이어야 합니다 \<key\> = \<value\> .</span><span class="sxs-lookup"><span data-stu-id="8234f-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="8234f-134">첫 번째?</span><span class="sxs-lookup"><span data-stu-id="8234f-134">The first ?</span></span>
<span data-ttu-id="8234f-135">및 &는 자동으로 추가 되므로 맨 앞에 포함 되지 않고 여러 쿼리 문자열을 &와 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="8234f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8234f-136">-DefaultProfile</span></span>
<span data-ttu-id="8234f-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8234f-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="8234f-138">-DynamicCompression</span></span>
<span data-ttu-id="8234f-139">캐시 된 콘텐츠에 대 한 동적 압축을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="8234f-140">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="8234f-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="8234f-141">-EnableCaching</span></span>
<span data-ttu-id="8234f-142">이 경로에 캐싱을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="8234f-143">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-143">Default value is false</span></span>

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

### <span data-ttu-id="8234f-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="8234f-144">-ForwardingProtocol</span></span>
<span data-ttu-id="8234f-145">이 규칙은 트래픽을 백 엔드로 전달할 때 사용할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="8234f-146">기본 값이 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="8234f-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8234f-147">-FrontDoorName</span></span>
<span data-ttu-id="8234f-148">이 라우팅 규칙이 속한 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="8234f-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="8234f-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="8234f-150">캐시 키를 형성할 때의 URL 쿼리 용어 처리입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="8234f-151">기본값은 StripAll입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="8234f-152">로 RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="8234f-152">-RedirectProtocol</span></span>
<span data-ttu-id="8234f-153">트래픽이 리디렉션되는 대상의 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="8234f-154">기본 값이 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="8234f-155">RedirectType</span><span class="sxs-lookup"><span data-stu-id="8234f-155">-RedirectType</span></span>
<span data-ttu-id="8234f-156">트래픽을 리디렉션하는 데 사용할 규칙의 리디렉션 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="8234f-157">기본 값이 이동 됨</span><span class="sxs-lookup"><span data-stu-id="8234f-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="8234f-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="8234f-158">-RequestHeaderAction</span></span>
<span data-ttu-id="8234f-159">요청에서 원점으로 시작 하는 데 적용 되는 헤더 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

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

### <span data-ttu-id="8234f-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8234f-160">-ResourceGroupName</span></span>
<span data-ttu-id="8234f-161">RoutingRule를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="8234f-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="8234f-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="8234f-163">응답에서 클라이언트로 클라이언트에 적용 되는 헤더 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-163">A list of header actions to apply from the response from AFD to the client.</span></span>

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

### <span data-ttu-id="8234f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8234f-164">CommonParameters</span></span>
<span data-ttu-id="8234f-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8234f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8234f-166">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8234f-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8234f-167">입력</span><span class="sxs-lookup"><span data-stu-id="8234f-167">INPUTS</span></span>

### <span data-ttu-id="8234f-168">않아야</span><span class="sxs-lookup"><span data-stu-id="8234f-168">None</span></span>

## <span data-ttu-id="8234f-169">출력</span><span class="sxs-lookup"><span data-stu-id="8234f-169">OUTPUTS</span></span>

### <span data-ttu-id="8234f-170">FrontDoor. PSRulesEngineAction/.</span><span class="sxs-lookup"><span data-stu-id="8234f-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="8234f-171">상속자</span><span class="sxs-lookup"><span data-stu-id="8234f-171">NOTES</span></span>

## <span data-ttu-id="8234f-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8234f-172">RELATED LINKS</span></span>
