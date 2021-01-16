---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362986"
---
# <span data-ttu-id="bf97f-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf97f-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="bf97f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf97f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf97f-103">애플리케이션 게이트웨이에 요청 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="bf97f-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf97f-104">SYNTAX</span></span>

### <span data-ttu-id="bf97f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf97f-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf97f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bf97f-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf97f-107">설명</span><span class="sxs-lookup"><span data-stu-id="bf97f-107">DESCRIPTION</span></span>
<span data-ttu-id="bf97f-108">**Add-AzApplicationGatewayRequestRoutingRule** cmdlet은 애플리케이션 게이트웨이에 요청 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="bf97f-109">예제</span><span class="sxs-lookup"><span data-stu-id="bf97f-109">EXAMPLES</span></span>

### <span data-ttu-id="bf97f-110">예제 1: 애플리케이션 게이트웨이에 요청 라우팅 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="bf97f-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="bf97f-111">첫 번째 명령은 애플리케이션 게이트웨이를 사용하여 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bf97f-112">두 번째 명령은 애플리케이션 게이트웨이에 요청 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="bf97f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf97f-113">PARAMETERS</span></span>

### <span data-ttu-id="bf97f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf97f-114">-ApplicationGateway</span></span>
<span data-ttu-id="bf97f-115">이 cmdlet이 요청 라우팅 규칙을 추가하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="bf97f-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf97f-116">-BackendAddressPool</span></span>
<span data-ttu-id="bf97f-117">애플리케이션 게이트웨이 백 엔드 주소 풀 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bf97f-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="bf97f-119">애플리케이션 게이트웨이 백 엔드 주소 풀 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bf97f-120">-BackendHttpSettings</span></span>
<span data-ttu-id="bf97f-121">애플리케이션 게이트웨이에 대한 백 엔드 HTTP 설정 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="bf97f-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="bf97f-123">애플리케이션 게이트웨이에 대한 백end HTTP 설정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf97f-124">-DefaultProfile</span></span>
<span data-ttu-id="bf97f-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf97f-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="bf97f-126">-HttpListener</span></span>
<span data-ttu-id="bf97f-127">애플리케이션 게이트웨이 HTTP 수신기 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="bf97f-128">-HttpListenerId</span></span>
<span data-ttu-id="bf97f-129">애플리케이션 게이트웨이 HTTP 수신기 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="bf97f-130">-Name</span></span>
<span data-ttu-id="bf97f-131">이 cmdlet이 추가하는 요청 라우팅 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="bf97f-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="bf97f-132">-Priority</span></span>
<span data-ttu-id="bf97f-133">규칙의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="bf97f-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf97f-134">-RedirectConfiguration</span></span>
<span data-ttu-id="bf97f-135">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf97f-135">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bf97f-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="bf97f-137">Application Gateway RedirectConfiguration의 ID</span><span class="sxs-lookup"><span data-stu-id="bf97f-137">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf97f-138">-RewriteRuleSet</span></span>
<span data-ttu-id="bf97f-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bf97f-139">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="bf97f-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="bf97f-141">Application Gateway RewriteRuleSet의 ID</span><span class="sxs-lookup"><span data-stu-id="bf97f-141">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="bf97f-142">-RuleType</span></span>
<span data-ttu-id="bf97f-143">요청 라우팅 규칙의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-143">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="bf97f-144">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="bf97f-145">-UrlPathMapId</span></span>
<span data-ttu-id="bf97f-146">라우팅 규칙에 대한 URL 경로 맵 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-146">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf97f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf97f-147">CommonParameters</span></span>
<span data-ttu-id="bf97f-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf97f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf97f-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf97f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf97f-150">입력</span><span class="sxs-lookup"><span data-stu-id="bf97f-150">INPUTS</span></span>

### <span data-ttu-id="bf97f-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf97f-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf97f-152">출력</span><span class="sxs-lookup"><span data-stu-id="bf97f-152">OUTPUTS</span></span>

### <span data-ttu-id="bf97f-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf97f-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf97f-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf97f-154">NOTES</span></span>

## <span data-ttu-id="bf97f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf97f-155">RELATED LINKS</span></span>

[<span data-ttu-id="bf97f-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf97f-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bf97f-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf97f-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bf97f-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf97f-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bf97f-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bf97f-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

