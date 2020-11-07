---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd6888402a2e3a88b9d3d19da752b0ac18d20f32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871105"
---
# <span data-ttu-id="0810b-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0810b-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="0810b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0810b-102">SYNOPSIS</span></span>
<span data-ttu-id="0810b-103">Application gateway에 대 한 요청 라우팅 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="0810b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0810b-104">SYNTAX</span></span>

### <span data-ttu-id="0810b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0810b-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0810b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0810b-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0810b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0810b-107">DESCRIPTION</span></span>
<span data-ttu-id="0810b-108">**Set-AzApplicationGatewayRequestRoutingRule** cmdlet은 요청 라우팅 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="0810b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0810b-109">EXAMPLES</span></span>

### <span data-ttu-id="0810b-110">예제 1: 요청 라우팅 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="0810b-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="0810b-111">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0810b-112">두 번째 명령은 $Setting 변수에 지정 된 백 엔드 HTTP 설정, $Listener 변수에 지정 된 HTTP 수신기 및 $Pool 변수에 지정 된 백 엔드 주소 풀을 사용 하도록 응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="0810b-113">변수</span><span class="sxs-lookup"><span data-stu-id="0810b-113">PARAMETERS</span></span>

### <span data-ttu-id="0810b-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0810b-114">-ApplicationGateway</span></span>
<span data-ttu-id="0810b-115">이 cmdlet이 요청 라우팅 규칙을 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="0810b-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0810b-116">-BackendAddressPool</span></span>
<span data-ttu-id="0810b-117">응용 프로그램 게이트웨이 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="0810b-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0810b-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="0810b-119">응용 프로그램 게이트웨이 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="0810b-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0810b-120">-BackendHttpSettings</span></span>
<span data-ttu-id="0810b-121">응용 프로그램 게이트웨이 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="0810b-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0810b-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="0810b-123">응용 프로그램 게이트웨이 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="0810b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0810b-124">-DefaultProfile</span></span>
<span data-ttu-id="0810b-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0810b-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="0810b-126">-HttpListener</span></span>
<span data-ttu-id="0810b-127">응용 프로그램 게이트웨이 HTTP 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="0810b-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="0810b-128">-HttpListenerId</span></span>
<span data-ttu-id="0810b-129">응용 프로그램 게이트웨이 HTTP 수신기 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="0810b-130">-이름</span><span class="sxs-lookup"><span data-stu-id="0810b-130">-Name</span></span>
<span data-ttu-id="0810b-131">이 cmdlet이 수정 하는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0810b-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0810b-132">-RedirectConfiguration</span></span>
<span data-ttu-id="0810b-133">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0810b-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="0810b-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0810b-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="0810b-135">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="0810b-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0810b-136">-RewriteRuleSet</span></span>
<span data-ttu-id="0810b-137">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0810b-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0810b-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="0810b-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="0810b-139">응용 프로그램 게이트웨이 RewriteRuleSet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0810b-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="0810b-140">-RuleType</span></span>
<span data-ttu-id="0810b-141">요청 라우팅 규칙 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="0810b-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="0810b-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="0810b-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="0810b-143">-UrlPathMapId</span></span>
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

### <span data-ttu-id="0810b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0810b-144">CommonParameters</span></span>
<span data-ttu-id="0810b-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0810b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0810b-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0810b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0810b-147">입력</span><span class="sxs-lookup"><span data-stu-id="0810b-147">INPUTS</span></span>

### <span data-ttu-id="0810b-148">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0810b-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0810b-149">출력</span><span class="sxs-lookup"><span data-stu-id="0810b-149">OUTPUTS</span></span>

### <span data-ttu-id="0810b-150">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0810b-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0810b-151">상속자</span><span class="sxs-lookup"><span data-stu-id="0810b-151">NOTES</span></span>

## <span data-ttu-id="0810b-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0810b-152">RELATED LINKS</span></span>

[<span data-ttu-id="0810b-153">추가-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0810b-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0810b-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0810b-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0810b-155">새로운 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0810b-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0810b-156">제거-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0810b-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


