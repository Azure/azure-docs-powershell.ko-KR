---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 51d85ffa9c1181b45f7ea4aa45484a814759a953
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982635"
---
# <span data-ttu-id="b97a3-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b97a3-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b97a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b97a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b97a3-103">애플리케이션 게이트웨이에 HTTP 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="b97a3-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="b97a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="b97a3-104">SYNTAX</span></span>

### <span data-ttu-id="b97a3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b97a3-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b97a3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b97a3-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b97a3-107">설명</span><span class="sxs-lookup"><span data-stu-id="b97a3-107">DESCRIPTION</span></span>
<span data-ttu-id="b97a3-108">**Add-AzApplicationGatewayHttpListener** cmdlet은 애플리케이션 게이트웨이에 HTTP 수신기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="b97a3-109">예제</span><span class="sxs-lookup"><span data-stu-id="b97a3-109">EXAMPLES</span></span>

### <span data-ttu-id="b97a3-110">예제 1: HTTP 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="b97a3-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="b97a3-111">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $AppGw 변수에 저장합니다. 두 번째 명령은 애플리케이션 게이트웨이에 HTTP 수신기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="b97a3-112">예제 2: SSL을 통해 HTTPS 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="b97a3-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="b97a3-113">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b97a3-114">두 번째 명령은 애플리케이션 게이트웨이에 HTTPS 프로토콜을 사용하는 수신기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="b97a3-115">예제 3: SSL 및 HostNames를 통해 HTTPS 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="b97a3-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="b97a3-116">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b97a3-117">두 번째 명령은 애플리케이션 게이트웨이에 SSL 인증서 및 HostNames와 함께 HTTPS 프로토콜을 사용하는 수신기를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="b97a3-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b97a3-118">PARAMETERS</span></span>

### <span data-ttu-id="b97a3-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b97a3-119">-ApplicationGateway</span></span>
<span data-ttu-id="b97a3-120">이 cmdlet에서 HTTP 수신기를 추가하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="b97a3-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b97a3-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="b97a3-122">애플리케이션 게이트웨이의 고객 오류</span><span class="sxs-lookup"><span data-stu-id="b97a3-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97a3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97a3-123">-DefaultProfile</span></span>
<span data-ttu-id="b97a3-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b97a3-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b97a3-125">-FirewallPolicy</span></span>
<span data-ttu-id="b97a3-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b97a3-126">FirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97a3-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b97a3-127">-FirewallPolicyId</span></span>
<span data-ttu-id="b97a3-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b97a3-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="b97a3-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b97a3-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b97a3-130">애플리케이션 게이트웨이 프런트 엔드 IP 리소스 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-130">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97a3-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b97a3-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b97a3-132">애플리케이션 게이트웨이 프런트 엔드 IP ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="b97a3-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b97a3-133">-FrontendPort</span></span>
<span data-ttu-id="b97a3-134">애플리케이션 게이트웨이 프런트 엔드 포트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-134">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97a3-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b97a3-135">-FrontendPortId</span></span>
<span data-ttu-id="b97a3-136">애플리케이션 게이트웨이 프런트 엔드 포트 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="b97a3-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="b97a3-137">-HostName</span></span>
<span data-ttu-id="b97a3-138">이 cmdlet에서 HTTP 수신기를 추가하는 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="b97a3-139">-HostNames</span><span class="sxs-lookup"><span data-stu-id="b97a3-139">-HostNames</span></span>
<span data-ttu-id="b97a3-140">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="b97a3-140">Host names</span></span>

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

### <span data-ttu-id="b97a3-141">-Name</span><span class="sxs-lookup"><span data-stu-id="b97a3-141">-Name</span></span>
<span data-ttu-id="b97a3-142">이 명령이 추가하는 프런트 엔드 포트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="b97a3-143">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b97a3-143">-Protocol</span></span>
<span data-ttu-id="b97a3-144">HTTP 수신기 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="b97a3-145">HTTP 및 HTTPS는 모두 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-145">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97a3-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b97a3-146">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97a3-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b97a3-147">-SslCertificate</span></span>
<span data-ttu-id="b97a3-148">HTTP 수신기의 SSL 인증서를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="b97a3-149">HTTPS를 수신기 프로토콜로 선택한 경우 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97a3-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b97a3-150">-SslCertificateId</span></span>
<span data-ttu-id="b97a3-151">HTTP 수신기의 SSL 인증서 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="b97a3-152">HTTPS를 수신기 프로토콜로 선택한 경우 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="b97a3-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="b97a3-153">-SslProfile</span></span>
<span data-ttu-id="b97a3-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="b97a3-154">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97a3-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="b97a3-155">-SslProfileId</span></span>
<span data-ttu-id="b97a3-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="b97a3-156">SslProfileId</span></span>

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

### <span data-ttu-id="b97a3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97a3-157">CommonParameters</span></span>
<span data-ttu-id="b97a3-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b97a3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97a3-159">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b97a3-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97a3-160">입력</span><span class="sxs-lookup"><span data-stu-id="b97a3-160">INPUTS</span></span>

### <span data-ttu-id="b97a3-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b97a3-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b97a3-162">출력</span><span class="sxs-lookup"><span data-stu-id="b97a3-162">OUTPUTS</span></span>

### <span data-ttu-id="b97a3-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b97a3-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b97a3-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b97a3-164">NOTES</span></span>

## <span data-ttu-id="b97a3-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b97a3-165">RELATED LINKS</span></span>

[<span data-ttu-id="b97a3-166">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b97a3-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b97a3-167">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b97a3-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b97a3-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b97a3-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b97a3-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b97a3-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


