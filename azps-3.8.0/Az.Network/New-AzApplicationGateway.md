---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 46eb4979c62a5c1f2cb8277ddc1461ee09a339c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044846"
---
# <span data-ttu-id="7ecb5-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ecb5-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="7ecb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ecb5-102">SYNOPSIS</span></span>
<span data-ttu-id="7ecb5-103">응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-103">Creates an application gateway.</span></span>

## <span data-ttu-id="7ecb5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ecb5-104">SYNTAX</span></span>

### <span data-ttu-id="7ecb5-105">IdentityByUserAssignedIdentityId (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ecb5-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ecb5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ecb5-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ecb5-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7ecb5-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ecb5-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="7ecb5-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ecb5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7ecb5-109">DESCRIPTION</span></span>
<span data-ttu-id="7ecb5-110">**AzApplicationGateway** Cmdlet은 Azure application gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="7ecb5-111">응용 프로그램 게이트웨이에는 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="7ecb5-112">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="7ecb5-112">A resource group.</span></span>
- <span data-ttu-id="7ecb5-113">가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-113">A virtual network.</span></span>
- <span data-ttu-id="7ecb5-114">백 엔드 서버의 IP 주소를 포함 하는 백 엔드 서버 풀</span><span class="sxs-lookup"><span data-stu-id="7ecb5-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="7ecb5-115">백 엔드 서버 풀 설정</span><span class="sxs-lookup"><span data-stu-id="7ecb5-115">Back-end server pool settings.</span></span> <span data-ttu-id="7ecb5-116">각 풀에는 풀 내의 모든 서버에 적용 되는 포트, 프로토콜, 쿠키 기반 선호도 등의 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="7ecb5-117">응용 프로그램 게이트웨이에서 연 IP 주소 인 프런트 엔드 IP 주소</span><span class="sxs-lookup"><span data-stu-id="7ecb5-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="7ecb5-118">프런트 엔드 IP 주소는 공용 IP 주소 이거나 내부 IP 주소 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="7ecb5-119">응용 프로그램 게이트웨이에서 열리는 공용 포트 인 프런트 엔드 포트</span><span class="sxs-lookup"><span data-stu-id="7ecb5-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="7ecb5-120">이러한 포트에 도달 하는 트래픽은 백 엔드 서버로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="7ecb5-121">수신기 및 백 엔드 서버 풀을 바인딩하는 요청 라우팅 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="7ecb5-122">이 규칙은 트래픽이 특정 수신기에 도달 했을 때 리디렉션되는 데 사용할 백 엔드 서버 풀을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="7ecb5-123">수신기에는 프런트 엔드 포트, 프런트 엔드 IP 주소, 프로토콜 (HTTP 또는 HTTPS) 및 SSL (Secure Sockets layer) 인증서 이름 (SSL 오프 로드를 구성 하는 경우)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="7ecb5-124">예제의</span><span class="sxs-lookup"><span data-stu-id="7ecb5-124">EXAMPLES</span></span>

### <span data-ttu-id="7ecb5-125">예제 1: 응용 프로그램 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="7ecb5-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="7ecb5-126">다음 예제에서는 먼저 리소스 그룹과 가상 네트워크를 만들고 다음을 수행 하 여 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="7ecb5-127">백 엔드 서버 풀</span><span class="sxs-lookup"><span data-stu-id="7ecb5-127">A back-end server pool</span></span>
- <span data-ttu-id="7ecb5-128">백 엔드 서버 풀 설정</span><span class="sxs-lookup"><span data-stu-id="7ecb5-128">Back-end server pool settings</span></span>
- <span data-ttu-id="7ecb5-129">프런트 엔드 포트</span><span class="sxs-lookup"><span data-stu-id="7ecb5-129">Front-end ports</span></span>
- <span data-ttu-id="7ecb5-130">프런트 엔드 IP 주소</span><span class="sxs-lookup"><span data-stu-id="7ecb5-130">Front-end IP addresses</span></span>
- <span data-ttu-id="7ecb5-131">요청 라우팅 규칙 네 가지 명령으로 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="7ecb5-132">첫 번째 명령은 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="7ecb5-133">두 번째 명령은 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="7ecb5-134">세 번째 명령은 서브넷 구성을 확인 하 고 네 번째 명령은 가상 네트워크가 성공적으로 만들어졌는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="7ecb5-135">다음 명령은 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="7ecb5-136">첫 번째 명령은 이전에 만든 서브넷에 대 한 GatewayIp01 이라는 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="7ecb5-137">두 번째 명령은 백 엔드 IP 주소 목록을 사용 하 여 Pool01 이라는 백 엔드 서버 풀을 만들고이 풀을 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="7ecb5-138">세 번째 명령은 백 엔드 서버 풀에 대 한 설정을 만들고 $PoolSetting 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="7ecb5-139">위의 명령은 포트 80에 프런트 엔드 포트를 만들고, 이름을 FrontEndPort01로,, 포트를 $FrontEndPort 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="7ecb5-140">다섯 번째 명령은 New-AzPublicIpAddress를 사용 하 여 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="7ecb5-141">여섯 번째 명령은 $PublicIp를 사용 하 여 프런트 엔드 IP 구성을 만들고, 이름을 FrontEndPortConfig01로 $FrontEndIpConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="7ecb5-142">일곱 번째 명령은 이전에 만든 $FrontEndIpConfig $FrontEndPort를 사용 하 여 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="7ecb5-143">여덟 번째 명령은 수신기에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="7ecb5-144">아홉 번째 명령은 SKU를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="7ecb5-145">10 번째 명령은 이전 명령으로 설정 된 개체를 사용 하 여 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="7ecb5-146">예제 2: UserAssigned 된 Id를 사용 하 여 응용 프로그램 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="7ecb5-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="7ecb5-147">변수</span><span class="sxs-lookup"><span data-stu-id="7ecb5-147">PARAMETERS</span></span>

### <span data-ttu-id="7ecb5-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ecb5-148">-AsJob</span></span>
<span data-ttu-id="7ecb5-149">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7ecb5-149">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="7ecb5-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="7ecb5-151">Application gateway에 대 한 인증 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ecb5-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="7ecb5-153">자동 크기 조정 구성</span><span class="sxs-lookup"><span data-stu-id="7ecb5-153">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="7ecb5-154">-BackendAddressPools</span></span>
<span data-ttu-id="7ecb5-155">응용 프로그램 게이트웨이의 백 엔드 주소 풀 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="7ecb5-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="7ecb5-157">Application gateway에 대 한 백 엔드 HTTP 설정의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ecb5-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="7ecb5-159">Application gateway의 고객 오류</span><span class="sxs-lookup"><span data-stu-id="7ecb5-159">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="7ecb5-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ecb5-160">-DefaultProfile</span></span>
<span data-ttu-id="7ecb5-161">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ecb5-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="7ecb5-162">-EnableFIPS</span></span>
<span data-ttu-id="7ecb5-163">FIPS 사용 여부</span><span class="sxs-lookup"><span data-stu-id="7ecb5-163">Whether FIPS is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="7ecb5-164">-EnableHttp2</span></span>
<span data-ttu-id="7ecb5-165">HTTP2 사용 여부</span><span class="sxs-lookup"><span data-stu-id="7ecb5-165">Whether HTTP2 is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7ecb5-166">-FirewallPolicy</span></span>
<span data-ttu-id="7ecb5-167">방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="7ecb5-167">Firewall configuration</span></span>

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

### <span data-ttu-id="7ecb5-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7ecb5-168">-FirewallPolicyId</span></span>
<span data-ttu-id="7ecb5-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7ecb5-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="7ecb5-170">-Force</span><span class="sxs-lookup"><span data-stu-id="7ecb5-170">-Force</span></span>
<span data-ttu-id="7ecb5-171">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-171">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="7ecb5-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="7ecb5-173">강제 firewallPolicy 연결을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-173">Whether Force firewallPolicy association is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="7ecb5-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="7ecb5-175">응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP 구성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="7ecb5-176">-FrontendPorts</span></span>
<span data-ttu-id="7ecb5-177">응용 프로그램 게이트웨이에 대 한 프런트 엔드 포트 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="7ecb5-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="7ecb5-179">응용 프로그램 게이트웨이에 대 한 IP 구성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="7ecb5-180">-HttpListeners</span></span>
<span data-ttu-id="7ecb5-181">응용 프로그램 게이트웨이에 대 한 HTTP 수신기 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-182">-Id</span><span class="sxs-lookup"><span data-stu-id="7ecb5-182">-Identity</span></span>
<span data-ttu-id="7ecb5-183">응용 프로그램 게이트웨이에 할당할 응용 프로그램 게이트웨이 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-184">-위치</span><span class="sxs-lookup"><span data-stu-id="7ecb5-184">-Location</span></span>
<span data-ttu-id="7ecb5-185">응용 프로그램 게이트웨이를 만들 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-185">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-186">-이름</span><span class="sxs-lookup"><span data-stu-id="7ecb5-186">-Name</span></span>
<span data-ttu-id="7ecb5-187">Application gateway의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-187">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-188">-프로브</span><span class="sxs-lookup"><span data-stu-id="7ecb5-188">-Probes</span></span>
<span data-ttu-id="7ecb5-189">응용 프로그램 게이트웨이에 대 한 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-189">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-190">로 RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="7ecb5-190">-RedirectConfigurations</span></span>
<span data-ttu-id="7ecb5-191">리디렉션 구성 목록</span><span class="sxs-lookup"><span data-stu-id="7ecb5-191">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-192">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="7ecb5-192">-RequestRoutingRules</span></span>
<span data-ttu-id="7ecb5-193">응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-193">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-194">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ecb5-194">-ResourceGroupName</span></span>
<span data-ttu-id="7ecb5-195">응용 프로그램 게이트웨이를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-195">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-196">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ecb5-196">-RewriteRuleSet</span></span>
<span data-ttu-id="7ecb5-197">RewriteRuleSet 목록</span><span class="sxs-lookup"><span data-stu-id="7ecb5-197">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-198">-Sku</span><span class="sxs-lookup"><span data-stu-id="7ecb5-198">-Sku</span></span>
<span data-ttu-id="7ecb5-199">응용 프로그램 게이트웨이의 SKU (stock 유지 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-199">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-200">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="7ecb5-200">-SslCertificates</span></span>
<span data-ttu-id="7ecb5-201">응용 프로그램 게이트웨이의 SSL (Secure Sockets layer) 인증서 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-201">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-202">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="7ecb5-202">-SslPolicy</span></span>
<span data-ttu-id="7ecb5-203">Application gateway에 대 한 SSL 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-203">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-204">태그</span><span class="sxs-lookup"><span data-stu-id="7ecb5-204">-Tag</span></span>
<span data-ttu-id="7ecb5-205">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-205">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7ecb5-206">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7ecb5-206">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-207">-을 (를)로 하는 Rootcertificate</span><span class="sxs-lookup"><span data-stu-id="7ecb5-207">-TrustedRootCertificate</span></span>
<span data-ttu-id="7ecb5-208">신뢰할 수 있는 루트 인증서 목록</span><span class="sxs-lookup"><span data-stu-id="7ecb5-208">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-209">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="7ecb5-209">-UrlPathMaps</span></span>
<span data-ttu-id="7ecb5-210">Application gateway에 대 한 URL 경로 맵을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-210">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-211">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7ecb5-211">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7ecb5-212">응용 프로그램 게이트웨이에 할당할 사용자 지정 id의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-212">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-213">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ecb5-213">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="7ecb5-214">WAF (웹 응용 프로그램 방화벽) 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-214">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="7ecb5-215">Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet을 사용 하 여 WAF를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-215">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-216">-Zone</span><span class="sxs-lookup"><span data-stu-id="7ecb5-216">-Zone</span></span>
<span data-ttu-id="7ecb5-217">응용 프로그램 게이트웨이가 들어오는 위치를 나타내는 가용성 영역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-217">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="7ecb5-218">-확인</span><span class="sxs-lookup"><span data-stu-id="7ecb5-218">-Confirm</span></span>
<span data-ttu-id="7ecb5-219">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-219">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ecb5-220">-WhatIf</span></span>
<span data-ttu-id="7ecb5-221">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ecb5-222">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-222">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ecb5-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ecb5-223">CommonParameters</span></span>
<span data-ttu-id="7ecb5-224">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ecb5-225">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ecb5-226">입력</span><span class="sxs-lookup"><span data-stu-id="7ecb5-226">INPUTS</span></span>

### <span data-ttu-id="7ecb5-227">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7ecb5-227">System.String</span></span>

### <span data-ttu-id="7ecb5-228">Microsoft. \*. i m a. 모델. m i m m</span><span class="sxs-lookup"><span data-stu-id="7ecb5-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="7ecb5-229">PSApplicationGatewaySslPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="7ecb5-230">Microsoft. \* Psapplication게이트웨이 Ipconfiguration []</span><span class="sxs-lookup"><span data-stu-id="7ecb5-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="7ecb5-231">PSApplicationGatewaySslCertificate [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="7ecb5-232">Microsoft. \* Psapplication게이트웨이 Authenticationcertificate []</span><span class="sxs-lookup"><span data-stu-id="7ecb5-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="7ecb5-233">Microsoft. m a m/. m i m a. 모델. Psapplication네트워크</span><span class="sxs-lookup"><span data-stu-id="7ecb5-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="7ecb5-234">PSApplicationGatewayFrontendIPConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="7ecb5-235">PSApplicationGatewayFrontendPort [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="7ecb5-236">Microsoft. \* Psapplication네트워크 검색 []</span><span class="sxs-lookup"><span data-stu-id="7ecb5-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="7ecb5-237">PSApplicationGatewayBackendAddressPool [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="7ecb5-238">PSApplicationGatewayBackendHttpSettings [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="7ecb5-239">PSApplicationGatewayHttpListener [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="7ecb5-240">PSApplicationGatewayUrlPathMap [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="7ecb5-241">PSApplicationGatewayRequestRoutingRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="7ecb5-242">PSApplicationGatewayRewriteRuleSet [] (으)로</span><span class="sxs-lookup"><span data-stu-id="7ecb5-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="7ecb5-243">Microsoft. \* Psapplication네트워크 Redirectconfiguration []</span><span class="sxs-lookup"><span data-stu-id="7ecb5-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="7ecb5-244">PSApplicationGatewayWebApplicationFirewallConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="7ecb5-245">PSApplicationGatewayAutoscaleConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="7ecb5-246">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="7ecb5-246">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7ecb5-247">PSManagedServiceIdentity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7ecb5-247">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="7ecb5-248">출력</span><span class="sxs-lookup"><span data-stu-id="7ecb5-248">OUTPUTS</span></span>

### <span data-ttu-id="7ecb5-249">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ecb5-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ecb5-250">상속자</span><span class="sxs-lookup"><span data-stu-id="7ecb5-250">NOTES</span></span>

## <span data-ttu-id="7ecb5-251">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ecb5-251">RELATED LINKS</span></span>

[<span data-ttu-id="7ecb5-252">새로운 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7ecb5-252">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7ecb5-253">새로운 AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7ecb5-253">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="7ecb5-254">새로운 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7ecb5-254">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="7ecb5-255">새로운 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7ecb5-255">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7ecb5-256">새로운 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7ecb5-256">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7ecb5-257">새로운 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ecb5-257">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7ecb5-258">새로운 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7ecb5-258">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7ecb5-259">새로운 AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7ecb5-259">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="7ecb5-260">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7ecb5-260">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7ecb5-261">새로운 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7ecb5-261">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)