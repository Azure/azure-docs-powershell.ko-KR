---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531989"
---
# <span data-ttu-id="cac3e-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="cac3e-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="cac3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cac3e-102">SYNOPSIS</span></span>
<span data-ttu-id="cac3e-103">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="cac3e-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cac3e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cac3e-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cac3e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cac3e-105">DESCRIPTION</span></span>
<span data-ttu-id="cac3e-106">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="cac3e-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="cac3e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cac3e-107">EXAMPLES</span></span>

### <span data-ttu-id="cac3e-108">예제 1: 전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="cac3e-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

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

<span data-ttu-id="cac3e-109">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="cac3e-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="cac3e-110">변수</span><span class="sxs-lookup"><span data-stu-id="cac3e-110">PARAMETERS</span></span>

### <span data-ttu-id="cac3e-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="cac3e-111">-AcceptedProtocol</span></span>
<span data-ttu-id="cac3e-112">이 규칙에 대해 일치 시킬 프로토콜 스키마입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="cac3e-113">기본값은 {Https, Http}입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-113">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="cac3e-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="cac3e-114">-BackendPoolName</span></span>
<span data-ttu-id="cac3e-115">이 규칙이 회람 되는 BackendPool의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="cac3e-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="cac3e-116">-CustomForwardingPath</span></span>
<span data-ttu-id="cac3e-117">이 규칙과 일치 하는 리소스 경로를 다시 작성 하는 데 사용 되는 사용자 지정 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="cac3e-118">들어오는 경로를 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="cac3e-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="cac3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac3e-119">-DefaultProfile</span></span>
<span data-ttu-id="cac3e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cac3e-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="cac3e-121">-DynamicCompression</span></span>
<span data-ttu-id="cac3e-122">캐싱이 설정 된 경우 캐시 된 콘텐츠에 대 한 동적 압축을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="cac3e-123">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="cac3e-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="cac3e-124">-EnableCaching</span></span>
<span data-ttu-id="cac3e-125">이 경로에 캐싱을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="cac3e-126">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac3e-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cac3e-127">-EnabledState</span></span>
<span data-ttu-id="cac3e-128">이 규칙의 사용 가능 여부</span><span class="sxs-lookup"><span data-stu-id="cac3e-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="cac3e-129">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="cac3e-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="cac3e-130">-ForwardingProtocol</span></span>
<span data-ttu-id="cac3e-131">이 규칙은 트래픽을 백 엔드로 전달할 때 사용할 프로토콜입니다. 기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac3e-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="cac3e-132">-FrontDoorName</span></span>
<span data-ttu-id="cac3e-133">이 라우팅 규칙이 속한 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="cac3e-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="cac3e-134">-FrontendEndpointName</span></span>
<span data-ttu-id="cac3e-135">이 규칙과 연결 된 프런트 엔드 끝점의 이름</span><span class="sxs-lookup"><span data-stu-id="cac3e-135">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="cac3e-136">-이름</span><span class="sxs-lookup"><span data-stu-id="cac3e-136">-Name</span></span>
<span data-ttu-id="cac3e-137">RoutingRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="cac3e-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="cac3e-138">-PatternToMatch</span></span>
<span data-ttu-id="cac3e-139">규칙의 경로 패턴에는 경로 끝/마지막/이후를 제외한 아무 \*도 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="cac3e-140">기본값은/\*입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-140">Default value is /\*</span></span>

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

### <span data-ttu-id="cac3e-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="cac3e-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="cac3e-142">캐시 키를 형성할 때의 URL 쿼리 용어 처리입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="cac3e-143">기본값은 StripAll입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac3e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac3e-144">-ResourceGroupName</span></span>
<span data-ttu-id="cac3e-145">RoutingRule를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="cac3e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac3e-146">CommonParameters</span></span>
<span data-ttu-id="cac3e-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cac3e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac3e-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac3e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac3e-149">입력</span><span class="sxs-lookup"><span data-stu-id="cac3e-149">INPUTS</span></span>

### <span data-ttu-id="cac3e-150">않아야</span><span class="sxs-lookup"><span data-stu-id="cac3e-150">None</span></span>

## <span data-ttu-id="cac3e-151">출력</span><span class="sxs-lookup"><span data-stu-id="cac3e-151">OUTPUTS</span></span>

### <span data-ttu-id="cac3e-152">FrontDoor. PSRoutingRule/.</span><span class="sxs-lookup"><span data-stu-id="cac3e-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="cac3e-153">상속자</span><span class="sxs-lookup"><span data-stu-id="cac3e-153">NOTES</span></span>

## <span data-ttu-id="cac3e-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cac3e-154">RELATED LINKS</span></span>

<span data-ttu-id="cac3e-155">[새로운 AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="cac3e-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
