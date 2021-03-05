---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 1399dba141cb885e0ad184a588707e7c4f4efe7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997243"
---
# <span data-ttu-id="37dff-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="37dff-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="37dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37dff-102">SYNOPSIS</span></span>
<span data-ttu-id="37dff-103">애플리케이션 게이트웨이에 대한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="37dff-104">구문</span><span class="sxs-lookup"><span data-stu-id="37dff-104">SYNTAX</span></span>

### <span data-ttu-id="37dff-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="37dff-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37dff-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="37dff-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37dff-107">설명</span><span class="sxs-lookup"><span data-stu-id="37dff-107">DESCRIPTION</span></span>
<span data-ttu-id="37dff-108">**New-AzApplicationGatewayHttpListener** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="37dff-109">예제</span><span class="sxs-lookup"><span data-stu-id="37dff-109">EXAMPLES</span></span>

### <span data-ttu-id="37dff-110">예제 1: HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="37dff-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="37dff-111">이 명령은 Listener01이라는 HTTP 수신기를 만들고 결과를 변수에 $Listener.</span><span class="sxs-lookup"><span data-stu-id="37dff-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="37dff-112">예제 2: SSL을 사용하여 HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="37dff-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="37dff-113">이 명령은 SSL 오프로드를 사용하여 SSL 인증서를 제공하는 HTTP 수신기 $SSLCert 01 변수에 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="37dff-114">명령은 결과를 변수라는 변수에 $Listener.</span><span class="sxs-lookup"><span data-stu-id="37dff-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="37dff-115">예제 3: 방화벽 정책으로 HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="37dff-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="37dff-116">이 명령은 Listener01이라는 HTTP 수신기, FirewallPolicy를 $firewallPolicy 을 만들고 결과를 100000000000000000000으로 $Listener.</span><span class="sxs-lookup"><span data-stu-id="37dff-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="37dff-117">예제 4: SSL 및 HostNames를 통해 HTTPS 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="37dff-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="37dff-118">이 명령은 SSL 오프로드를 사용하는 HTTP 수신기를 만들고 두 HostNames와 함께 $SSLCert 01 변수에 SSL 인증서를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="37dff-119">명령은 결과를 변수라는 변수에 $Listener.</span><span class="sxs-lookup"><span data-stu-id="37dff-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="37dff-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="37dff-120">PARAMETERS</span></span>

### <span data-ttu-id="37dff-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="37dff-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="37dff-122">애플리케이션 게이트웨이의 고객 오류</span><span class="sxs-lookup"><span data-stu-id="37dff-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="37dff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dff-123">-DefaultProfile</span></span>
<span data-ttu-id="37dff-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37dff-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="37dff-125">-FirewallPolicy</span></span>
<span data-ttu-id="37dff-126">최상위 방화벽 정책에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="37dff-127">개체 참조는 cmdlet을 사용하여 New-AzApplicationGatewayWebApplicationFirewallPolicy 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="37dff-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" 위의 명령줄을 사용하여 만든 방화벽 정책을 경로 규칙 수준에서 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="37dff-129">위의 명령은 기본 정책 설정 및 관리되는 규칙을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="37dff-130">사용자는 기본 값 대신 각각 New-AzApplicationGatewayFirewallPolicySettings 사용하여 PolicySettings, ManagedRules를 New-AzApplicationGatewayFirewallPolicySettings New-AzApplicationGatewayFirewallPolicyManagedRules 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="37dff-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="37dff-131">-FirewallPolicyId</span></span>
<span data-ttu-id="37dff-132">기존 최상위 웹 애플리케이션 방화벽 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="37dff-133">방화벽 정책 신분은 cmdlet을 사용하여 Get-AzApplicationGatewayWebApplicationFirewallPolicy 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="37dff-134">ID가 있는 후 FirewallPolicy 매개 변수 대신 *FirewallPolicyId* 매개 변수를 *사용할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="37dff-135">예를 들어 -FirewallPolicyId /subscriptions/<구독-id>/resourceGroups/<리소스-그룹 id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="37dff-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="37dff-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="37dff-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="37dff-137">HTTP 수신기에 대한 프런트 엔드 IP 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="37dff-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="37dff-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="37dff-139">HTTP 수신기에 대한 프런트 엔드 IP 구성의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="37dff-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="37dff-140">-FrontendPort</span></span>
<span data-ttu-id="37dff-141">HTTP 수신기에 대한 프런트 엔드 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="37dff-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="37dff-142">-FrontendPortId</span></span>
<span data-ttu-id="37dff-143">HTTP 수신기에 대한 프런트 엔드 포트 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="37dff-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="37dff-144">-HostName</span></span>
<span data-ttu-id="37dff-145">애플리케이션 게이트웨이 HTTP 수신기의 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="37dff-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="37dff-146">-HostNames</span></span>
<span data-ttu-id="37dff-147">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="37dff-147">Host names</span></span>

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

### <span data-ttu-id="37dff-148">-Name</span><span class="sxs-lookup"><span data-stu-id="37dff-148">-Name</span></span>
<span data-ttu-id="37dff-149">이 cmdlet이 만드는 HTTP 수신기 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="37dff-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="37dff-150">-Protocol</span></span>
<span data-ttu-id="37dff-151">HTTP 수신기에서 사용하는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="37dff-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="37dff-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dff-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="37dff-153">-SslCertificate</span></span>
<span data-ttu-id="37dff-154">HTTP 수신기에 대한 SSL 인증서 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="37dff-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="37dff-155">-SslCertificateId</span></span>
<span data-ttu-id="37dff-156">HTTP 수신기에 대한 SSL 인증서의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="37dff-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="37dff-157">-SslProfile</span></span>
<span data-ttu-id="37dff-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="37dff-158">SslProfile</span></span>

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

### <span data-ttu-id="37dff-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="37dff-159">-SslProfileId</span></span>
<span data-ttu-id="37dff-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="37dff-160">SslProfileId</span></span>

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

### <span data-ttu-id="37dff-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dff-161">CommonParameters</span></span>
<span data-ttu-id="37dff-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37dff-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dff-163">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37dff-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dff-164">입력</span><span class="sxs-lookup"><span data-stu-id="37dff-164">INPUTS</span></span>

### <span data-ttu-id="37dff-165">없음</span><span class="sxs-lookup"><span data-stu-id="37dff-165">None</span></span>

## <span data-ttu-id="37dff-166">출력</span><span class="sxs-lookup"><span data-stu-id="37dff-166">OUTPUTS</span></span>

### <span data-ttu-id="37dff-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="37dff-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="37dff-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37dff-168">NOTES</span></span>

## <span data-ttu-id="37dff-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37dff-169">RELATED LINKS</span></span>

[<span data-ttu-id="37dff-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="37dff-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="37dff-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="37dff-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="37dff-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="37dff-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="37dff-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="37dff-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


