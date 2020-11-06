---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: 67da94a783d932501413008523c744f6695f6024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529514"
---
# <span data-ttu-id="22015-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22015-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="22015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22015-102">SYNOPSIS</span></span>
<span data-ttu-id="22015-103">응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22015-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22015-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22015-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22015-105">DESCRIPTION</span></span>
<span data-ttu-id="22015-106">**AzureRmApplicationGateway** Cmdlet은 Azure application gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="22015-107">응용 프로그램 게이트웨이에는 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-107">An application gateway requires the following:</span></span>
- <span data-ttu-id="22015-108">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="22015-108">A resource group.</span></span>
- <span data-ttu-id="22015-109">가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="22015-109">A virtual network.</span></span>
- <span data-ttu-id="22015-110">백 엔드 서버의 IP 주소를 포함 하는 백 엔드 서버 풀</span><span class="sxs-lookup"><span data-stu-id="22015-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="22015-111">백 엔드 서버 풀 설정</span><span class="sxs-lookup"><span data-stu-id="22015-111">Back-end server pool settings.</span></span> <span data-ttu-id="22015-112">각 풀에는 풀 내의 모든 서버에 적용 되는 포트, 프로토콜, 쿠키 기반 선호도 등의 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22015-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="22015-113">응용 프로그램 게이트웨이에서 연 IP 주소 인 프런트 엔드 IP 주소</span><span class="sxs-lookup"><span data-stu-id="22015-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="22015-114">프런트 엔드 IP 주소는 공용 IP 주소 이거나 내부 IP 주소 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22015-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="22015-115">응용 프로그램 게이트웨이에서 열리는 공용 포트 인 프런트 엔드 포트</span><span class="sxs-lookup"><span data-stu-id="22015-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="22015-116">이러한 포트에 도달 하는 트래픽은 백 엔드 서버로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="22015-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="22015-117">수신기 및 백 엔드 서버 풀을 바인딩하는 요청 라우팅 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="22015-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="22015-118">이 규칙은 트래픽이 특정 수신기에 도달 했을 때 리디렉션되는 데 사용할 백 엔드 서버 풀을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="22015-119">수신기에는 프런트 엔드 포트, 프런트 엔드 IP 주소, 프로토콜 (HTTP 또는 HTTPS) 및 SSL (Secure Sockets layer) 인증서 이름 (SSL 오프 로드를 구성 하는 경우)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22015-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="22015-120">예제의</span><span class="sxs-lookup"><span data-stu-id="22015-120">EXAMPLES</span></span>

### <span data-ttu-id="22015-121">예제 1: 응용 프로그램 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="22015-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="22015-122">다음 예제에서는 먼저 리소스 그룹과 가상 네트워크를 만들고 다음을 수행 하 여 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="22015-123">백 엔드 서버 풀</span><span class="sxs-lookup"><span data-stu-id="22015-123">A back-end server pool</span></span>
- <span data-ttu-id="22015-124">백 엔드 서버 풀 설정</span><span class="sxs-lookup"><span data-stu-id="22015-124">Back-end server pool settings</span></span>
- <span data-ttu-id="22015-125">프런트 엔드 포트</span><span class="sxs-lookup"><span data-stu-id="22015-125">Front-end ports</span></span>
- <span data-ttu-id="22015-126">프런트 엔드 IP 주소</span><span class="sxs-lookup"><span data-stu-id="22015-126">Front-end IP addresses</span></span>
- <span data-ttu-id="22015-127">요청 라우팅 규칙 네 가지 명령으로 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-127">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="22015-128">첫 번째 명령은 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-128">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="22015-129">두 번째 명령은 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-129">The second command creates a virtual network.</span></span>
<span data-ttu-id="22015-130">세 번째 명령은 서브넷 구성을 확인 하 고 네 번째 명령은 가상 네트워크가 성공적으로 만들어졌는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-130">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="22015-131">다음 명령은 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-131">The following commands create the application gateway.</span></span>
<span data-ttu-id="22015-132">첫 번째 명령은 이전에 만든 서브넷에 대 한 GatewayIp01 이라는 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-132">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="22015-133">두 번째 명령은 백 엔드 IP 주소 목록을 사용 하 여 Pool01 이라는 백 엔드 서버 풀을 만들고이 풀을 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-133">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="22015-134">세 번째 명령은 백 엔드 서버 풀에 대 한 설정을 만들고 $PoolSetting 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-134">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="22015-135">위의 명령은 포트 80에 프런트 엔드 포트를 만들고, 이름을 FrontEndPort01로,, 포트를 $FrontEndPort 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-135">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="22015-136">다섯 번째 명령은 New-AzureRmPublicIpAddress를 사용 하 여 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-136">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="22015-137">여섯 번째 명령은 $PublicIp를 사용 하 여 프런트 엔드 IP 구성을 만들고, 이름을 FrontEndPortConfig01로 $FrontEndIpConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-137">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="22015-138">일곱 번째 명령은 이전에 만든 $FrontEndIpConfig $FrontEndPort를 사용 하 여 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-138">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="22015-139">여덟 번째 명령은 수신기에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-139">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="22015-140">아홉 번째 명령은 SKU를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-140">The ninth command sets the SKU.</span></span>
<span data-ttu-id="22015-141">10 번째 명령은 이전 명령으로 설정 된 개체를 사용 하 여 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22015-141">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="22015-142">변수</span><span class="sxs-lookup"><span data-stu-id="22015-142">PARAMETERS</span></span>

### <span data-ttu-id="22015-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22015-143">-AsJob</span></span>
<span data-ttu-id="22015-144">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="22015-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22015-145">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="22015-145">-AuthenticationCertificates</span></span>
<span data-ttu-id="22015-146">Application gateway에 대 한 인증 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-146">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-147">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="22015-147">-AutoscaleConfiguration</span></span>
<span data-ttu-id="22015-148">자동 크기 조정 구성</span><span class="sxs-lookup"><span data-stu-id="22015-148">Autoscale Configuration</span></span>

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

### <span data-ttu-id="22015-149">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="22015-149">-BackendAddressPools</span></span>
<span data-ttu-id="22015-150">응용 프로그램 게이트웨이의 백 엔드 주소 풀 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-150">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-151">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="22015-151">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="22015-152">Application gateway에 대 한 백 엔드 HTTP 설정의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-152">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22015-153">-DefaultProfile</span></span>
<span data-ttu-id="22015-154">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22015-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22015-155">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="22015-155">-EnableFIPS</span></span>
<span data-ttu-id="22015-156">FIPS 사용 여부</span><span class="sxs-lookup"><span data-stu-id="22015-156">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="22015-157">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="22015-157">-EnableHttp2</span></span>
<span data-ttu-id="22015-158">HTTP2 사용 여부</span><span class="sxs-lookup"><span data-stu-id="22015-158">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="22015-159">-Force</span><span class="sxs-lookup"><span data-stu-id="22015-159">-Force</span></span>
<span data-ttu-id="22015-160">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-160">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22015-161">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="22015-161">-FrontendIPConfigurations</span></span>
<span data-ttu-id="22015-162">응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP 구성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-162">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-163">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="22015-163">-FrontendPorts</span></span>
<span data-ttu-id="22015-164">응용 프로그램 게이트웨이에 대 한 프런트 엔드 포트 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-164">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-165">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="22015-165">-GatewayIPConfigurations</span></span>
<span data-ttu-id="22015-166">응용 프로그램 게이트웨이에 대 한 IP 구성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-166">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-167">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="22015-167">-HttpListeners</span></span>
<span data-ttu-id="22015-168">응용 프로그램 게이트웨이에 대 한 HTTP 수신기 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-168">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-169">-위치</span><span class="sxs-lookup"><span data-stu-id="22015-169">-Location</span></span>
<span data-ttu-id="22015-170">응용 프로그램 게이트웨이를 만들 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-170">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="22015-171">-이름</span><span class="sxs-lookup"><span data-stu-id="22015-171">-Name</span></span>
<span data-ttu-id="22015-172">Application gateway의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-172">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="22015-173">-프로브</span><span class="sxs-lookup"><span data-stu-id="22015-173">-Probes</span></span>
<span data-ttu-id="22015-174">응용 프로그램 게이트웨이에 대 한 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-174">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-175">로 RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="22015-175">-RedirectConfigurations</span></span>
<span data-ttu-id="22015-176">리디렉션 구성 목록</span><span class="sxs-lookup"><span data-stu-id="22015-176">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-177">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="22015-177">-RequestRoutingRules</span></span>
<span data-ttu-id="22015-178">응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-178">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22015-179">-ResourceGroupName</span></span>
<span data-ttu-id="22015-180">응용 프로그램 게이트웨이를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-180">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="22015-181">-Sku</span><span class="sxs-lookup"><span data-stu-id="22015-181">-Sku</span></span>
<span data-ttu-id="22015-182">응용 프로그램 게이트웨이의 SKU (stock 유지 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-182">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="22015-183">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="22015-183">-SslCertificates</span></span>
<span data-ttu-id="22015-184">응용 프로그램 게이트웨이의 SSL (Secure Sockets layer) 인증서 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-184">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-185">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="22015-185">-SslPolicy</span></span>
<span data-ttu-id="22015-186">Application gateway에 대 한 SSL 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-186">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="22015-187">태그</span><span class="sxs-lookup"><span data-stu-id="22015-187">-Tag</span></span>
<span data-ttu-id="22015-188">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="22015-188">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22015-189">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="22015-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="22015-190">-을 (를)로 하는 Rootcertificate</span><span class="sxs-lookup"><span data-stu-id="22015-190">-TrustedRootCertificate</span></span>
<span data-ttu-id="22015-191">신뢰할 수 있는 루트 인증서 목록</span><span class="sxs-lookup"><span data-stu-id="22015-191">The list of trusted root certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-192">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="22015-192">-UrlPathMaps</span></span>
<span data-ttu-id="22015-193">Application gateway에 대 한 URL 경로 맵을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-193">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22015-194">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="22015-194">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="22015-195">WAF (웹 응용 프로그램 방화벽) 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-195">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="22015-196">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet을 사용 하 여 WAF를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22015-196">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="22015-197">-Zone</span><span class="sxs-lookup"><span data-stu-id="22015-197">-Zone</span></span>
<span data-ttu-id="22015-198">응용 프로그램 게이트웨이가 들어오는 위치를 나타내는 가용성 영역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="22015-198">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22015-199">-확인</span><span class="sxs-lookup"><span data-stu-id="22015-199">-Confirm</span></span>
<span data-ttu-id="22015-200">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22015-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22015-201">-WhatIf</span></span>
<span data-ttu-id="22015-202">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22015-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22015-203">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22015-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22015-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22015-204">CommonParameters</span></span>
<span data-ttu-id="22015-205">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22015-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22015-206">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22015-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22015-207">입력</span><span class="sxs-lookup"><span data-stu-id="22015-207">INPUTS</span></span>

### <span data-ttu-id="22015-208">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22015-208">System.String</span></span>

### <span data-ttu-id="22015-209">Microsoft. \*. i m a. 모델. m i m m</span><span class="sxs-lookup"><span data-stu-id="22015-209">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="22015-210">PSApplicationGatewaySslPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="22015-210">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="22015-211">System.webserver. List ' 1 [[Microsoft Azure. 모델]. Psapplication의 Ipconfiguration, Microsoft Azure. 명령인. 네트워크, 버전 = 6.4.1.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-211">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-212">System.webserver. List ' 1 [[PSApplicationGatewaySslCertificate, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-212">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-213">System.webserver. List ' 1 [[Microsoft Azure. 모델]. Psapplication의 Authenticationcertificate, Microsoft Azure. Network, Version = 6.4.1.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-213">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-214">System.webserver. List ' 1 [[PSApplicationGatewayFrontendIPConfiguration, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-214">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-215">System.webserver. List ' 1 [[PSApplicationGatewayFrontendPort, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-215">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-216">System.webserver. List ' 1 [[Microsoft Azure. e. 모델]. Psapplication네트워크 검색, Microsoft Azure. 6.4.1.0, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-216">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-217">System.webserver. List ' 1 [[PSApplicationGatewayBackendAddressPool, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-217">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-218">System.webserver. List ' 1 [[PSApplicationGatewayBackendHttpSettings, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-218">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-219">System.webserver. List ' 1 [[PSApplicationGatewayHttpListener, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-219">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-220">System.webserver. List ' 1 [[PSApplicationGatewayUrlPathMap, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-220">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-221">System.webserver. List ' 1 [[PSApplicationGatewayRequestRoutingRule, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22015-221">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-222">System.webserver. List ' 1 [[Microsoft Azure. 모델]. Psapplication게이트웨이 Redirectconfiguration, Microsoft Azure. 명령인. 네트워크, 버전 = 6.4.1.0, Culture = 중립, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="22015-222">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22015-223">PSApplicationGatewayWebApplicationFirewallConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="22015-223">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="22015-224">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="22015-224">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22015-225">출력</span><span class="sxs-lookup"><span data-stu-id="22015-225">OUTPUTS</span></span>

### <span data-ttu-id="22015-226">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22015-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22015-227">상속자</span><span class="sxs-lookup"><span data-stu-id="22015-227">NOTES</span></span>

## <span data-ttu-id="22015-228">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22015-228">RELATED LINKS</span></span>

[<span data-ttu-id="22015-229">새로운 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="22015-229">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="22015-230">새로운 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="22015-230">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="22015-231">새로운 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="22015-231">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="22015-232">새로운 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="22015-232">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="22015-233">새로운 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="22015-233">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="22015-234">새로운 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="22015-234">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="22015-235">새로운 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="22015-235">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="22015-236">새로운 AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="22015-236">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="22015-237">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="22015-237">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="22015-238">새로운 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="22015-238">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
