---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179948"
---
# <span data-ttu-id="6ceb8-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6ceb8-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="6ceb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ceb8-102">SYNOPSIS</span></span>
<span data-ttu-id="6ceb8-103">백end 서버 풀에 URL 경로 매핑 배열을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="6ceb8-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ceb8-104">SYNTAX</span></span>

### <span data-ttu-id="6ceb8-105">BackendSetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ceb8-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ceb8-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ceb8-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ceb8-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="6ceb8-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ceb8-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ceb8-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ceb8-109">설명</span><span class="sxs-lookup"><span data-stu-id="6ceb8-109">DESCRIPTION</span></span>
<span data-ttu-id="6ceb8-110">**Add-AzApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 URL 경로 매핑 배열을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="6ceb8-111">예제</span><span class="sxs-lookup"><span data-stu-id="6ceb8-111">EXAMPLES</span></span>

### <span data-ttu-id="6ceb8-112">예제 1: 애플리케이션 게이트웨이에 URL 경로 매핑을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="6ceb8-113">첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 $appgw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="6ceb8-114">두 번째 명령은 백드 주소 풀을 사용하여 백 $pool 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="6ceb8-115">세 번째 명령은 백end http 설정을 사용하여 변수에 $poolSettings 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="6ceb8-116">네 번째 명령은 rule01이라는 새 경로 규칙 구성을 만들고 변수에 $pathRule 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="6ceb8-117">다섯 번째 명령은 url01이라는 URL 경로 매핑 구성을 애플리케이션 게이트웨이에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="6ceb8-118">여섯 번째 명령은 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="6ceb8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ceb8-119">PARAMETERS</span></span>

### <span data-ttu-id="6ceb8-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ceb8-120">-ApplicationGateway</span></span>
<span data-ttu-id="6ceb8-121">이 cmdlet이 URL 경로 맵 구성을 추가하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="6ceb8-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6ceb8-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="6ceb8-123">*pathRules* 매개 변수에 지정된 규칙이 일치하지 않는 경우 라우팅할 기본 백end 주소 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="6ceb8-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6ceb8-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="6ceb8-125">기본 백end 주소 풀 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="6ceb8-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6ceb8-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="6ceb8-127">*pathRules* 매개 변수에 지정된 규칙이 일치하지 않는 경우 사용할 기본 백end HTTP 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="6ceb8-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6ceb8-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="6ceb8-129">기본 백end HTTP 설정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="6ceb8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ceb8-130">-DefaultProfile</span></span>
<span data-ttu-id="6ceb8-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ceb8-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ceb8-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="6ceb8-133">Application Gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ceb8-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="6ceb8-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6ceb8-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="6ceb8-135">Application Gateway 기본 RedirectConfiguration의 ID</span><span class="sxs-lookup"><span data-stu-id="6ceb8-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="6ceb8-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ceb8-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="6ceb8-137">Application Gateway 기본 다시 필기 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="6ceb8-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="6ceb8-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="6ceb8-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="6ceb8-139">애플리케이션 게이트웨이 기본 다시 덮기 규칙 집합의 ID</span><span class="sxs-lookup"><span data-stu-id="6ceb8-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="6ceb8-140">-Name</span><span class="sxs-lookup"><span data-stu-id="6ceb8-140">-Name</span></span>
<span data-ttu-id="6ceb8-141">이 cmdlet이 백end 서버 풀에 추가하는 URL 경로 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="6ceb8-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="6ceb8-142">-PathRules</span></span>
<span data-ttu-id="6ceb8-143">경로 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="6ceb8-144">경로 규칙은 순서에 민감하고 지정된 순서대로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="6ceb8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ceb8-145">CommonParameters</span></span>
<span data-ttu-id="6ceb8-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ceb8-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6ceb8-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ceb8-148">입력</span><span class="sxs-lookup"><span data-stu-id="6ceb8-148">INPUTS</span></span>

### <span data-ttu-id="6ceb8-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ceb8-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ceb8-150">출력</span><span class="sxs-lookup"><span data-stu-id="6ceb8-150">OUTPUTS</span></span>

### <span data-ttu-id="6ceb8-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ceb8-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ceb8-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ceb8-152">NOTES</span></span>

## <span data-ttu-id="6ceb8-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ceb8-153">RELATED LINKS</span></span>

[<span data-ttu-id="6ceb8-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6ceb8-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6ceb8-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6ceb8-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6ceb8-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6ceb8-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6ceb8-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6ceb8-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

