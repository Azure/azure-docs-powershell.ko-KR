---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: b0335fd0700b256650809c4548efe4d1e620442b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043787"
---
# <span data-ttu-id="198e3-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="198e3-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="198e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="198e3-102">SYNOPSIS</span></span>
<span data-ttu-id="198e3-103">응용 프로그램 게이트웨이에 요청 라우팅 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="198e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="198e3-104">SYNTAX</span></span>

### <span data-ttu-id="198e3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="198e3-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="198e3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="198e3-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="198e3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="198e3-107">DESCRIPTION</span></span>
<span data-ttu-id="198e3-108">**Add-AzApplicationGatewayRequestRoutingRule** cmdlet은 응용 프로그램 게이트웨이에 요청 라우팅 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="198e3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="198e3-109">EXAMPLES</span></span>

### <span data-ttu-id="198e3-110">예제 1: 응용 프로그램 게이트웨이에 요청 라우팅 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="198e3-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="198e3-111">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="198e3-112">두 번째 명령은 응용 프로그램 게이트웨이에 요청 라우팅 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="198e3-113">변수</span><span class="sxs-lookup"><span data-stu-id="198e3-113">PARAMETERS</span></span>

### <span data-ttu-id="198e3-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="198e3-114">-ApplicationGateway</span></span>
<span data-ttu-id="198e3-115">이 cmdlet이 요청 라우팅 규칙을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="198e3-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="198e3-116">-BackendAddressPool</span></span>
<span data-ttu-id="198e3-117">응용 프로그램 게이트웨이 백 엔드 주소 풀 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="198e3-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="198e3-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="198e3-119">응용 프로그램 게이트웨이 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="198e3-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="198e3-120">-BackendHttpSettings</span></span>
<span data-ttu-id="198e3-121">응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="198e3-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="198e3-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="198e3-123">응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="198e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198e3-124">-DefaultProfile</span></span>
<span data-ttu-id="198e3-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="198e3-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="198e3-126">-HttpListener</span></span>
<span data-ttu-id="198e3-127">Application gateway HTTP 수신기 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="198e3-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="198e3-128">-HttpListenerId</span></span>
<span data-ttu-id="198e3-129">Application gateway HTTP 수신기 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="198e3-130">-이름</span><span class="sxs-lookup"><span data-stu-id="198e3-130">-Name</span></span>
<span data-ttu-id="198e3-131">이 cmdlet에 추가 되는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="198e3-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="198e3-132">-RedirectConfiguration</span></span>
<span data-ttu-id="198e3-133">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="198e3-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="198e3-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="198e3-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="198e3-135">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="198e3-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="198e3-136">-RewriteRuleSet</span></span>
<span data-ttu-id="198e3-137">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="198e3-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="198e3-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="198e3-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="198e3-139">응용 프로그램 게이트웨이 RewriteRuleSet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="198e3-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="198e3-140">-RuleType</span></span>
<span data-ttu-id="198e3-141">요청 라우팅 규칙 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="198e3-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="198e3-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="198e3-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="198e3-143">-UrlPathMapId</span></span>
<span data-ttu-id="198e3-144">라우팅 규칙에 대 한 URL 경로 맵 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-144">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="198e3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198e3-145">CommonParameters</span></span>
<span data-ttu-id="198e3-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="198e3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198e3-147">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="198e3-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198e3-148">입력</span><span class="sxs-lookup"><span data-stu-id="198e3-148">INPUTS</span></span>

### <span data-ttu-id="198e3-149">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="198e3-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="198e3-150">출력</span><span class="sxs-lookup"><span data-stu-id="198e3-150">OUTPUTS</span></span>

### <span data-ttu-id="198e3-151">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="198e3-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="198e3-152">상속자</span><span class="sxs-lookup"><span data-stu-id="198e3-152">NOTES</span></span>

## <span data-ttu-id="198e3-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="198e3-153">RELATED LINKS</span></span>

[<span data-ttu-id="198e3-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="198e3-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="198e3-155">새로운 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="198e3-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="198e3-156">제거-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="198e3-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="198e3-157">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="198e3-157">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


