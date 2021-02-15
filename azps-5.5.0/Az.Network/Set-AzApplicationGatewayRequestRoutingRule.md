---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f815994a6f60490bd930a17748cd00167c2b52ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189545"
---
# <span data-ttu-id="6a8ae-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a8ae-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6a8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8ae-103">애플리케이션 게이트웨이에 대한 요청 라우팅 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="6a8ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a8ae-104">SYNTAX</span></span>

### <span data-ttu-id="6a8ae-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a8ae-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a8ae-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6a8ae-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a8ae-107">설명</span><span class="sxs-lookup"><span data-stu-id="6a8ae-107">DESCRIPTION</span></span>
<span data-ttu-id="6a8ae-108">**Set-AzApplicationGatewayRequestRoutingRule** cmdlet은 요청 라우팅 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="6a8ae-109">예제</span><span class="sxs-lookup"><span data-stu-id="6a8ae-109">EXAMPLES</span></span>

### <span data-ttu-id="6a8ae-110">예제 1: 요청 라우팅 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="6a8ae-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6a8ae-111">첫 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6a8ae-112">두 번째 명령은 $Setting 변수에 지정된 백 엔드 HTTP 설정, $Listener 변수에 지정된 HTTP 수신기 및 $Pool 변수에 지정된 백 엔드 주소 풀을 사용하기 위해 애플리케이션 게이트웨이에 대한 요청 라우팅 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="6a8ae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a8ae-113">PARAMETERS</span></span>

### <span data-ttu-id="6a8ae-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a8ae-114">-ApplicationGateway</span></span>
<span data-ttu-id="6a8ae-115">이 cmdlet이 요청 라우팅 규칙을 연결한 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="6a8ae-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a8ae-116">-BackendAddressPool</span></span>
<span data-ttu-id="6a8ae-117">애플리케이션 게이트웨이 백 엔드 주소 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="6a8ae-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6a8ae-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6a8ae-119">애플리케이션 게이트웨이 백 엔드 주소 풀 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="6a8ae-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6a8ae-120">-BackendHttpSettings</span></span>
<span data-ttu-id="6a8ae-121">애플리케이션 게이트웨이 백드 HTTP 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="6a8ae-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6a8ae-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6a8ae-123">애플리케이션 게이트웨이 백 엔드 HTTP 설정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="6a8ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8ae-124">-DefaultProfile</span></span>
<span data-ttu-id="6a8ae-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a8ae-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="6a8ae-126">-HttpListener</span></span>
<span data-ttu-id="6a8ae-127">애플리케이션 게이트웨이 HTTP 수신기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="6a8ae-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="6a8ae-128">-HttpListenerId</span></span>
<span data-ttu-id="6a8ae-129">애플리케이션 게이트웨이 HTTP 수신기 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="6a8ae-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6a8ae-130">-Name</span></span>
<span data-ttu-id="6a8ae-131">이 cmdlet이 수정하는 요청 라우팅 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6a8ae-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="6a8ae-132">-Priority</span></span>
<span data-ttu-id="6a8ae-133">규칙의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="6a8ae-133">The priority of the rule</span></span>

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

### <span data-ttu-id="6a8ae-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a8ae-134">-RedirectConfiguration</span></span>
<span data-ttu-id="6a8ae-135">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a8ae-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6a8ae-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6a8ae-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="6a8ae-137">Application Gateway RedirectConfiguration의 ID</span><span class="sxs-lookup"><span data-stu-id="6a8ae-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6a8ae-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a8ae-138">-RewriteRuleSet</span></span>
<span data-ttu-id="6a8ae-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a8ae-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6a8ae-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="6a8ae-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="6a8ae-141">Application Gateway RewriteRuleSet의 ID</span><span class="sxs-lookup"><span data-stu-id="6a8ae-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6a8ae-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6a8ae-142">-RuleType</span></span>
<span data-ttu-id="6a8ae-143">요청 라우팅 규칙의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="6a8ae-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6a8ae-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="6a8ae-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6a8ae-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6a8ae-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8ae-146">CommonParameters</span></span>
<span data-ttu-id="6a8ae-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8ae-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8ae-149">입력</span><span class="sxs-lookup"><span data-stu-id="6a8ae-149">INPUTS</span></span>

### <span data-ttu-id="6a8ae-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a8ae-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a8ae-151">출력</span><span class="sxs-lookup"><span data-stu-id="6a8ae-151">OUTPUTS</span></span>

### <span data-ttu-id="6a8ae-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a8ae-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a8ae-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a8ae-153">NOTES</span></span>

## <span data-ttu-id="6a8ae-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a8ae-154">RELATED LINKS</span></span>

[<span data-ttu-id="6a8ae-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a8ae-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6a8ae-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a8ae-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6a8ae-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a8ae-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6a8ae-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a8ae-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


