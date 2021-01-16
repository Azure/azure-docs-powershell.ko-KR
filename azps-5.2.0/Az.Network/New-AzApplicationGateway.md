---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 0f3d65c629218fc903035cb9df669f1c3dc7a50c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361082"
---
# <span data-ttu-id="96c57-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96c57-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="96c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96c57-102">SYNOPSIS</span></span>
<span data-ttu-id="96c57-103">애플리케이션 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-103">Creates an application gateway.</span></span>

## <span data-ttu-id="96c57-104">구문</span><span class="sxs-lookup"><span data-stu-id="96c57-104">SYNTAX</span></span>

### <span data-ttu-id="96c57-105">IdentityByUserAssignedIdentityId(기본값)</span><span class="sxs-lookup"><span data-stu-id="96c57-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c57-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="96c57-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c57-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="96c57-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c57-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="96c57-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c57-109">설명</span><span class="sxs-lookup"><span data-stu-id="96c57-109">DESCRIPTION</span></span>
<span data-ttu-id="96c57-110">**New-AzApplicationGateway** cmdlet은 Azure 애플리케이션 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="96c57-111">애플리케이션 게이트웨이에는 다음이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="96c57-112">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-112">A resource group.</span></span>
- <span data-ttu-id="96c57-113">가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="96c57-113">A virtual network.</span></span>
- <span data-ttu-id="96c57-114">백 엔드 서버의 IP 주소를 포함하는 백 엔드 서버 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="96c57-115">백 엔드 서버 풀 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-115">Back-end server pool settings.</span></span> <span data-ttu-id="96c57-116">각 풀에는 풀 내의 모든 서버에 적용되는 포트, 프로토콜 및 쿠키 기반과 같은 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="96c57-117">애플리케이션 게이트웨이에서 연 IP 주소인 프런트 엔드 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="96c57-118">프런트 엔드 IP 주소는 공용 IP 주소 또는 내부 IP 주소일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="96c57-119">애플리케이션 게이트웨이에서 연 공용 포트인 프런트 엔드 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="96c57-120">이러한 포트에 적중하는 트래픽은 백 엔드 서버로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="96c57-121">수신기 및 백 엔드 서버 풀을 바인딩하는 요청 라우팅 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="96c57-122">규칙은 특정 수신기에 적중할 때 트래픽을 전송해야 하는 백 엔드 서버 풀을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="96c57-123">수신기에는 프런트 엔드 포트, 프런트 엔드 IP 주소, 프로토콜(HTTP 또는 HTTPS) 및 Secure Sockets Layer(SSL 오프로드를 구성하는 경우) 인증서 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="96c57-124">예제</span><span class="sxs-lookup"><span data-stu-id="96c57-124">EXAMPLES</span></span>

### <span data-ttu-id="96c57-125">예제 1: 애플리케이션 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="96c57-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="96c57-126">다음 예제에서는 먼저 다음뿐만 아니라 리소스 그룹 및 가상 네트워크를 만들어 애플리케이션 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="96c57-127">백 엔드 서버 풀</span><span class="sxs-lookup"><span data-stu-id="96c57-127">A back-end server pool</span></span>
- <span data-ttu-id="96c57-128">백 엔드 서버 풀 설정</span><span class="sxs-lookup"><span data-stu-id="96c57-128">Back-end server pool settings</span></span>
- <span data-ttu-id="96c57-129">프런트 엔드 포트</span><span class="sxs-lookup"><span data-stu-id="96c57-129">Front-end ports</span></span>
- <span data-ttu-id="96c57-130">프런트 엔드 IP 주소</span><span class="sxs-lookup"><span data-stu-id="96c57-130">Front-end IP addresses</span></span>
- <span data-ttu-id="96c57-131">요청 라우팅 규칙 이 네 가지 명령은 가상 네트워크를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="96c57-132">첫 번째 명령은 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="96c57-133">두 번째 명령은 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="96c57-134">세 번째 명령은 서브넷 구성을 확인하며, 네 번째 명령은 가상 네트워크가 성공적으로 만들어졌다고 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="96c57-135">다음 명령은 애플리케이션 게이트웨이를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="96c57-136">첫 번째 명령은 이전에 만든 서브넷에 대한 GatewayIp01이라는 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="96c57-137">두 번째 명령은 백 엔드 IP 주소 목록을 사용하여 Pool01이라는 백 엔드 서버 풀을 만들고 풀을 $Pool 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="96c57-138">세 번째 명령은 백 엔드 서버 풀에 대한 설정을 만들고 백 엔드 변수에 $PoolSetting 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="96c57-139">첫 번째 명령은 포트 80에 프런트 엔드 포트를 만들고, FrontEndPort01로 이름을 정하고, 포트를 $FrontEndPort 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="96c57-140">다섯 번째 명령은 New-AzPublicIpAddress를 사용하여 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="96c57-141">여섯 번째 명령은 $PublicIp 사용하여 프런트 엔드 IP 구성을 만들고, FrontEndPortConfig01로 이름을 지은 다음, $FrontEndIpConfig 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="96c57-142">일곱 번째 명령은 이전에 만든 수신기 $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="96c57-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="96c57-143">8번 명령은 수신기 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="96c57-144">9번째 명령은 SKU를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="96c57-145">10번째 명령은 이전 명령에서 설정한 개체를 사용하여 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="96c57-146">예제 2: UserAssigned ID를 사용하여 애플리케이션 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="96c57-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="96c57-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96c57-147">PARAMETERS</span></span>

### <span data-ttu-id="96c57-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96c57-148">-AsJob</span></span>
<span data-ttu-id="96c57-149">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="96c57-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96c57-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="96c57-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="96c57-151">애플리케이션 게이트웨이에 대한 인증 인증서를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-151">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c57-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="96c57-153">자동 조정 구성</span><span class="sxs-lookup"><span data-stu-id="96c57-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="96c57-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="96c57-154">-BackendAddressPools</span></span>
<span data-ttu-id="96c57-155">애플리케이션 게이트웨이에 대한 백 엔드 주소 풀 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-155">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="96c57-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="96c57-157">애플리케이션 게이트웨이에 대한 백 엔드 HTTP 설정 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c57-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="96c57-159">애플리케이션 게이트웨이의 고객 오류</span><span class="sxs-lookup"><span data-stu-id="96c57-159">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="96c57-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c57-160">-DefaultProfile</span></span>
<span data-ttu-id="96c57-161">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c57-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="96c57-162">-EnableFIPS</span></span>
<span data-ttu-id="96c57-163">FIPS를 사용할 수 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="96c57-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="96c57-164">-EnableHttp2</span></span>
<span data-ttu-id="96c57-165">HTTP2를 사용할 수 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="96c57-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="96c57-166">-FirewallPolicy</span></span>
<span data-ttu-id="96c57-167">방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="96c57-167">Firewall configuration</span></span>

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

### <span data-ttu-id="96c57-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="96c57-168">-FirewallPolicyId</span></span>
<span data-ttu-id="96c57-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="96c57-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="96c57-170">-Force</span><span class="sxs-lookup"><span data-stu-id="96c57-170">-Force</span></span>
<span data-ttu-id="96c57-171">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96c57-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="96c57-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="96c57-173">Force firewallPolicy 연결 사용 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="96c57-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="96c57-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="96c57-175">애플리케이션 게이트웨이에 대한 프런트 엔드 IP 구성 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="96c57-176">-FrontendPorts</span></span>
<span data-ttu-id="96c57-177">애플리케이션 게이트웨이에 대한 프런트 엔드 포트 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-177">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="96c57-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="96c57-179">애플리케이션 게이트웨이에 대한 IP 구성 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-179">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="96c57-180">-HttpListeners</span></span>
<span data-ttu-id="96c57-181">애플리케이션 게이트웨이에 대한 HTTP 수신기 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="96c57-182">-Identity</span></span>
<span data-ttu-id="96c57-183">Application Gateway에 할당할 Application Gateway ID입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="96c57-184">-Location</span><span class="sxs-lookup"><span data-stu-id="96c57-184">-Location</span></span>
<span data-ttu-id="96c57-185">애플리케이션 게이트웨이를 만들 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="96c57-186">-Name</span><span class="sxs-lookup"><span data-stu-id="96c57-186">-Name</span></span>
<span data-ttu-id="96c57-187">애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="96c57-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c57-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="96c57-189">privateLink 구성 목록</span><span class="sxs-lookup"><span data-stu-id="96c57-189">The list of privateLink Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c57-190">-Probes</span><span class="sxs-lookup"><span data-stu-id="96c57-190">-Probes</span></span>
<span data-ttu-id="96c57-191">애플리케이션 게이트웨이에 대한 프로브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-191">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="96c57-192">-RedirectConfigurations</span></span>
<span data-ttu-id="96c57-193">리디렉션 구성 목록</span><span class="sxs-lookup"><span data-stu-id="96c57-193">The list of redirect configuration</span></span>

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

### <span data-ttu-id="96c57-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="96c57-194">-RequestRoutingRules</span></span>
<span data-ttu-id="96c57-195">애플리케이션 게이트웨이에 대한 요청 라우팅 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-195">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c57-196">-ResourceGroupName</span></span>
<span data-ttu-id="96c57-197">애플리케이션 게이트웨이를 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="96c57-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96c57-198">-RewriteRuleSet</span></span>
<span data-ttu-id="96c57-199">RewriteRuleSet 목록</span><span class="sxs-lookup"><span data-stu-id="96c57-199">The list of RewriteRuleSet</span></span>

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

### <span data-ttu-id="96c57-200">-Sku</span><span class="sxs-lookup"><span data-stu-id="96c57-200">-Sku</span></span>
<span data-ttu-id="96c57-201">애플리케이션 게이트웨이의 SKU(Stock Keeping Unit)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="96c57-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="96c57-202">-SslCertificates</span></span>
<span data-ttu-id="96c57-203">애플리케이션 게이트웨이에 대한 Secure Sockets Layer(SSL) 인증서 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="96c57-204">-SslPolicy</span></span>
<span data-ttu-id="96c57-205">애플리케이션 게이트웨이에 대한 SSL 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-205">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-206">-SslProfiles</span><span class="sxs-lookup"><span data-stu-id="96c57-206">-SslProfiles</span></span>
<span data-ttu-id="96c57-207">ssl 프로필 목록</span><span class="sxs-lookup"><span data-stu-id="96c57-207">The list of ssl profiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c57-208">-Tag</span><span class="sxs-lookup"><span data-stu-id="96c57-208">-Tag</span></span>
<span data-ttu-id="96c57-209">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-209">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="96c57-210">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="96c57-210">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="96c57-211">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="96c57-211">-TrustedClientCertificates</span></span>
<span data-ttu-id="96c57-212">신뢰할 수 있는 클라이언트 CA 인증서 체인 목록</span><span class="sxs-lookup"><span data-stu-id="96c57-212">The list of trusted client CA certificate chains</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c57-213">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="96c57-213">-TrustedRootCertificate</span></span>
<span data-ttu-id="96c57-214">신뢰할 수 있는 루트 인증서 목록</span><span class="sxs-lookup"><span data-stu-id="96c57-214">The list of trusted root certificates</span></span>

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

### <span data-ttu-id="96c57-215">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="96c57-215">-UrlPathMaps</span></span>
<span data-ttu-id="96c57-216">애플리케이션 게이트웨이에 대한 URL 경로 맵을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-216">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="96c57-217">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="96c57-217">-UserAssignedIdentityId</span></span>
<span data-ttu-id="96c57-218">Application Gateway에 할당할 사용자 할당 ID의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-218">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="96c57-219">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c57-219">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="96c57-220">WAF(웹 애플리케이션 방화벽) 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-220">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="96c57-221">Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet을 사용하여 WAF를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-221">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="96c57-222">-Zone</span><span class="sxs-lookup"><span data-stu-id="96c57-222">-Zone</span></span>
<span data-ttu-id="96c57-223">애플리케이션 게이트웨이를 시작해야 하는 위치를 표시하는 가용성 영역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-223">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="96c57-224">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96c57-224">-Confirm</span></span>
<span data-ttu-id="96c57-225">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-225">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c57-226">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c57-226">-WhatIf</span></span>
<span data-ttu-id="96c57-227">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="96c57-227">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c57-228">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-228">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c57-229">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c57-229">CommonParameters</span></span>
<span data-ttu-id="96c57-230">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96c57-230">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c57-231">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="96c57-231">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c57-232">입력</span><span class="sxs-lookup"><span data-stu-id="96c57-232">INPUTS</span></span>

### <span data-ttu-id="96c57-233">System.String</span><span class="sxs-lookup"><span data-stu-id="96c57-233">System.String</span></span>

### <span data-ttu-id="96c57-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="96c57-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="96c57-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="96c57-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="96c57-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="96c57-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="96c57-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span><span class="sxs-lookup"><span data-stu-id="96c57-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="96c57-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span><span class="sxs-lookup"><span data-stu-id="96c57-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="96c57-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="96c57-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="96c57-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="96c57-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="96c57-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span><span class="sxs-lookup"><span data-stu-id="96c57-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="96c57-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span><span class="sxs-lookup"><span data-stu-id="96c57-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="96c57-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="96c57-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="96c57-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span><span class="sxs-lookup"><span data-stu-id="96c57-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="96c57-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span><span class="sxs-lookup"><span data-stu-id="96c57-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="96c57-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span><span class="sxs-lookup"><span data-stu-id="96c57-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="96c57-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span><span class="sxs-lookup"><span data-stu-id="96c57-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="96c57-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span><span class="sxs-lookup"><span data-stu-id="96c57-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="96c57-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="96c57-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="96c57-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c57-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="96c57-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c57-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="96c57-252">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="96c57-252">System.Collections.Hashtable</span></span>

### <span data-ttu-id="96c57-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="96c57-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="96c57-254">출력</span><span class="sxs-lookup"><span data-stu-id="96c57-254">OUTPUTS</span></span>

### <span data-ttu-id="96c57-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96c57-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96c57-256">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96c57-256">NOTES</span></span>

## <span data-ttu-id="96c57-257">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96c57-257">RELATED LINKS</span></span>

[<span data-ttu-id="96c57-258">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="96c57-258">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="96c57-259">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="96c57-259">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="96c57-260">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="96c57-260">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="96c57-261">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="96c57-261">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="96c57-262">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="96c57-262">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="96c57-263">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c57-263">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="96c57-264">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96c57-264">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="96c57-265">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="96c57-265">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="96c57-266">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="96c57-266">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="96c57-267">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="96c57-267">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
