---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 2bc6a8eed22660d966256afbc9783e4edfc04947
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986776"
---
# <span data-ttu-id="63840-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="63840-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="63840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63840-102">SYNOPSIS</span></span>
<span data-ttu-id="63840-103">백던드 서버 풀에 URL 경로 매핑 배열을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="63840-104">구문</span><span class="sxs-lookup"><span data-stu-id="63840-104">SYNTAX</span></span>

### <span data-ttu-id="63840-105">BackendSetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="63840-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63840-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63840-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63840-107">리디렉션SetByResource</span><span class="sxs-lookup"><span data-stu-id="63840-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63840-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63840-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63840-109">설명</span><span class="sxs-lookup"><span data-stu-id="63840-109">DESCRIPTION</span></span>
<span data-ttu-id="63840-110">**Add-AzApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 URL 경로 매핑의 배열을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="63840-111">예제</span><span class="sxs-lookup"><span data-stu-id="63840-111">EXAMPLES</span></span>

### <span data-ttu-id="63840-112">예제 1: 애플리케이션 게이트웨이에 URL 경로 매핑을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="63840-113">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 얻게 하여 $appgw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="63840-114">두 번째 명령은 백던드 주소 풀을 얻게 하여 $pool 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="63840-115">세 번째 명령은 백end http 설정을 얻게 하여 $poolSettings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="63840-116">네 번째 명령은 rule01이라는 새 경로 규칙 구성을 만들고 변수에 $pathRule 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="63840-117">다섯 번째 명령은 url01이라는 URL 경로 매핑 구성을 애플리케이션 게이트웨이에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="63840-118">여섯 번째 명령은 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="63840-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="63840-119">PARAMETERS</span></span>

### <span data-ttu-id="63840-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63840-120">-ApplicationGateway</span></span>
<span data-ttu-id="63840-121">이 cmdlet에서 URL 경로 맵 구성을 추가하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63840-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63840-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="63840-123">*pathRules* 매개 변수에 지정된 규칙이 일치하지 않는 경우 라우팅할 기본 백던드 주소 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="63840-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="63840-125">기본 백던드 주소 풀 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="63840-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="63840-127">*pathRules* 매개 변수에 지정된 규칙이 일치하지 않는 경우 사용할 기본 백end HTTP 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="63840-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="63840-129">기본 백end HTTP 설정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63840-130">-DefaultProfile</span></span>
<span data-ttu-id="63840-131">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63840-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63840-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="63840-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="63840-133">애플리케이션 게이트웨이 기본 리디렉션 구성</span><span class="sxs-lookup"><span data-stu-id="63840-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="63840-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="63840-135">애플리케이션 게이트웨이 기본 리디렉션 구성의 ID</span><span class="sxs-lookup"><span data-stu-id="63840-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="63840-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="63840-137">애플리케이션 게이트웨이 기본 다시 덮기 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="63840-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="63840-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="63840-139">애플리케이션 게이트웨이 기본 다시 덮기 규칙 집합의 ID</span><span class="sxs-lookup"><span data-stu-id="63840-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-140">-Name</span><span class="sxs-lookup"><span data-stu-id="63840-140">-Name</span></span>
<span data-ttu-id="63840-141">이 cmdlet이 백던드 서버 풀에 추가하는 URL 경로 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="63840-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="63840-142">-PathRules</span></span>
<span data-ttu-id="63840-143">경로 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="63840-144">경로 규칙은 순서가 중요하고 지정된 순서대로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="63840-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63840-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63840-145">CommonParameters</span></span>
<span data-ttu-id="63840-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="63840-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63840-147">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="63840-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63840-148">입력</span><span class="sxs-lookup"><span data-stu-id="63840-148">INPUTS</span></span>

### <span data-ttu-id="63840-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63840-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63840-150">출력</span><span class="sxs-lookup"><span data-stu-id="63840-150">OUTPUTS</span></span>

### <span data-ttu-id="63840-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63840-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63840-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="63840-152">NOTES</span></span>

## <span data-ttu-id="63840-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63840-153">RELATED LINKS</span></span>

[<span data-ttu-id="63840-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="63840-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="63840-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="63840-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="63840-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="63840-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="63840-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="63840-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


