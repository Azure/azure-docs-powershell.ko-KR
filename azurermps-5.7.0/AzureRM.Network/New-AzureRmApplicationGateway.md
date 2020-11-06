---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: a9751806760a8e2265737e72d726fb491191fa5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532748"
---
# <span data-ttu-id="442a9-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="442a9-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="442a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="442a9-102">SYNOPSIS</span></span>
<span data-ttu-id="442a9-103">응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="442a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="442a9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
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
 [-EnableHttp2] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="442a9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="442a9-105">DESCRIPTION</span></span>
<span data-ttu-id="442a9-106">**AzureRmApplicationGateway** Cmdlet은 Azure application gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="442a9-107">응용 프로그램 게이트웨이에는 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="442a9-108">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="442a9-108">A resource group.</span></span>
- <span data-ttu-id="442a9-109">가상 네트워크.</span><span class="sxs-lookup"><span data-stu-id="442a9-109">A virtual network.</span></span>
- <span data-ttu-id="442a9-110">백 엔드 서버의 IP 주소를 포함 하는 백 엔드 서버 풀</span><span class="sxs-lookup"><span data-stu-id="442a9-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="442a9-111">백 엔드 서버 풀 설정</span><span class="sxs-lookup"><span data-stu-id="442a9-111">Back-end server pool settings.</span></span> <span data-ttu-id="442a9-112">각 풀에는 풀 내의 모든 서버에 적용 되는 포트, 프로토콜, 쿠키 기반 선호도 등의 설정이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="442a9-113">응용 프로그램 게이트웨이에서 연 IP 주소 인 프런트 엔드 IP 주소</span><span class="sxs-lookup"><span data-stu-id="442a9-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="442a9-114">프런트 엔드 IP 주소는 공용 IP 주소 이거나 내부 IP 주소 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="442a9-115">응용 프로그램 게이트웨이에서 열리는 공용 포트 인 프런트 엔드 포트</span><span class="sxs-lookup"><span data-stu-id="442a9-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="442a9-116">이러한 포트에 도달 하는 트래픽은 백 엔드 서버로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="442a9-117">수신기 및 백 엔드 서버 풀을 바인딩하는 요청 라우팅 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="442a9-118">이 규칙은 트래픽이 특정 수신기에 도달 했을 때 리디렉션되는 데 사용할 백 엔드 서버 풀을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="442a9-119">수신기에는 프런트 엔드 포트, 프런트 엔드 IP 주소, 프로토콜 (HTTP 또는 HTTPS) 및 SSL (Secure Sockets layer) 인증서 이름 (SSL 오프 로드를 구성 하는 경우)이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="442a9-120">예제의</span><span class="sxs-lookup"><span data-stu-id="442a9-120">EXAMPLES</span></span>

### <span data-ttu-id="442a9-121">예제 1: 응용 프로그램 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="442a9-121">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="442a9-122">다음 예제에서는 먼저 리소스 그룹과 가상 네트워크를 만들고 다음을 수행 하 여 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="442a9-123">백 엔드 서버 풀</span><span class="sxs-lookup"><span data-stu-id="442a9-123">A back-end server pool</span></span>
- <span data-ttu-id="442a9-124">백 엔드 서버 풀 설정</span><span class="sxs-lookup"><span data-stu-id="442a9-124">Back-end server pool settings</span></span>
- <span data-ttu-id="442a9-125">프런트 엔드 포트</span><span class="sxs-lookup"><span data-stu-id="442a9-125">Front-end ports</span></span>
- <span data-ttu-id="442a9-126">프런트 엔드 IP 주소</span><span class="sxs-lookup"><span data-stu-id="442a9-126">Front-end IP addresses</span></span>
- <span data-ttu-id="442a9-127">요청 라우팅 규칙</span><span class="sxs-lookup"><span data-stu-id="442a9-127">A request routing rule</span></span>

<span data-ttu-id="442a9-128">이러한 네 가지 명령으로 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="442a9-129">첫 번째 명령은 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="442a9-130">두 번째 명령은 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="442a9-131">세 번째 명령은 서브넷 구성을 확인 하 고 네 번째 명령은 가상 네트워크가 성공적으로 만들어졌는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="442a9-132">다음 명령은 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="442a9-133">첫 번째 명령은 이전에 만든 서브넷에 대 한 GatewayIp01 이라는 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="442a9-134">두 번째 명령은 백 엔드 IP 주소 목록을 사용 하 여 Pool01 이라는 백 엔드 서버 풀을 만들고이 풀을 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="442a9-135">세 번째 명령은 백 엔드 서버 풀에 대 한 설정을 만들고 $PoolSetting 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="442a9-136">위의 명령은 포트 80에 프런트 엔드 포트를 만들고, 이름을 FrontEndPort01로,, 포트를 $FrontEndPort 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="442a9-137">다섯 번째 명령은 New-AzureRmPublicIpAddress를 사용 하 여 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="442a9-138">여섯 번째 명령은 $PublicIp를 사용 하 여 프런트 엔드 IP 구성을 만들고, 이름을 FrontEndPortConfig01로 $FrontEndIpConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="442a9-139">일곱 번째 명령은 이전에 만든 $FrontEndIpConfig $FrontEndPort를 사용 하 여 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="442a9-140">여덟 번째 명령은 수신기에 대 한 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="442a9-141">아홉 번째 명령은 SKU를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="442a9-142">10 번째 명령은 이전 명령으로 설정 된 개체를 사용 하 여 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="442a9-143">변수</span><span class="sxs-lookup"><span data-stu-id="442a9-143">PARAMETERS</span></span>

### <span data-ttu-id="442a9-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="442a9-144">-AsJob</span></span>
<span data-ttu-id="442a9-145">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="442a9-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="442a9-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="442a9-147">Application gateway에 대 한 인증 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-147">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="442a9-148">-BackendAddressPools</span></span>
<span data-ttu-id="442a9-149">응용 프로그램 게이트웨이의 백 엔드 주소 풀 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-149">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="442a9-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="442a9-151">Application gateway에 대 한 백 엔드 HTTP 설정의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442a9-152">-DefaultProfile</span></span>
<span data-ttu-id="442a9-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-154">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="442a9-154">-EnableHttp2</span></span>
<span data-ttu-id="442a9-155">HTTP2 사용 여부</span><span class="sxs-lookup"><span data-stu-id="442a9-155">Whether HTTP2 is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-156">-Force</span><span class="sxs-lookup"><span data-stu-id="442a9-156">-Force</span></span>
<span data-ttu-id="442a9-157">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-157">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-158">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="442a9-158">-FrontendIPConfigurations</span></span>
<span data-ttu-id="442a9-159">응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP 구성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-159">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-160">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="442a9-160">-FrontendPorts</span></span>
<span data-ttu-id="442a9-161">응용 프로그램 게이트웨이에 대 한 프런트 엔드 포트 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-161">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-162">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="442a9-162">-GatewayIPConfigurations</span></span>
<span data-ttu-id="442a9-163">응용 프로그램 게이트웨이에 대 한 IP 구성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-163">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-164">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="442a9-164">-HttpListeners</span></span>
<span data-ttu-id="442a9-165">응용 프로그램 게이트웨이에 대 한 HTTP 수신기 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-165">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-166">-위치</span><span class="sxs-lookup"><span data-stu-id="442a9-166">-Location</span></span>
<span data-ttu-id="442a9-167">응용 프로그램 게이트웨이를 만들 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-167">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-168">-이름</span><span class="sxs-lookup"><span data-stu-id="442a9-168">-Name</span></span>
<span data-ttu-id="442a9-169">Application gateway의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-169">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-170">-프로브</span><span class="sxs-lookup"><span data-stu-id="442a9-170">-Probes</span></span>
<span data-ttu-id="442a9-171">응용 프로그램 게이트웨이에 대 한 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-171">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-172">로 RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="442a9-172">-RedirectConfigurations</span></span>
<span data-ttu-id="442a9-173">리디렉션 구성 목록</span><span class="sxs-lookup"><span data-stu-id="442a9-173">The list of redirect configuration</span></span>

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

### <span data-ttu-id="442a9-174">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="442a9-174">-RequestRoutingRules</span></span>
<span data-ttu-id="442a9-175">응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-175">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442a9-176">-ResourceGroupName</span></span>
<span data-ttu-id="442a9-177">응용 프로그램 게이트웨이를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-177">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-178">-Sku</span><span class="sxs-lookup"><span data-stu-id="442a9-178">-Sku</span></span>
<span data-ttu-id="442a9-179">응용 프로그램 게이트웨이의 SKU (stock 유지 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-179">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-180">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="442a9-180">-SslCertificates</span></span>
<span data-ttu-id="442a9-181">응용 프로그램 게이트웨이의 SSL (Secure Sockets layer) 인증서 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-181">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-182">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="442a9-182">-SslPolicy</span></span>
<span data-ttu-id="442a9-183">Application gateway에 대 한 SSL 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-183">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-184">태그</span><span class="sxs-lookup"><span data-stu-id="442a9-184">-Tag</span></span>
<span data-ttu-id="442a9-185">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="442a9-186">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="442a9-186">For example:</span></span>

<span data-ttu-id="442a9-187">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="442a9-187">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-188">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="442a9-188">-UrlPathMaps</span></span>
<span data-ttu-id="442a9-189">Application gateway에 대 한 URL 경로 맵을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-189">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="442a9-190">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="442a9-190">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="442a9-191">WAF (웹 응용 프로그램 방화벽) 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-191">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="442a9-192">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet을 사용 하 여 WAF를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-192">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-193">-확인</span><span class="sxs-lookup"><span data-stu-id="442a9-193">-Confirm</span></span>
<span data-ttu-id="442a9-194">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-194">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="442a9-195">-WhatIf</span></span>
<span data-ttu-id="442a9-196">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="442a9-197">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-197">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442a9-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442a9-198">CommonParameters</span></span>
<span data-ttu-id="442a9-199">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442a9-200">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442a9-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442a9-201">입력</span><span class="sxs-lookup"><span data-stu-id="442a9-201">INPUTS</span></span>

### <span data-ttu-id="442a9-202">않아야</span><span class="sxs-lookup"><span data-stu-id="442a9-202">None</span></span>
<span data-ttu-id="442a9-203">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="442a9-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="442a9-204">출력</span><span class="sxs-lookup"><span data-stu-id="442a9-204">OUTPUTS</span></span>

### <span data-ttu-id="442a9-205">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="442a9-205">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="442a9-206">상속자</span><span class="sxs-lookup"><span data-stu-id="442a9-206">NOTES</span></span>

## <span data-ttu-id="442a9-207">관련 링크</span><span class="sxs-lookup"><span data-stu-id="442a9-207">RELATED LINKS</span></span>

[<span data-ttu-id="442a9-208">새로운 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="442a9-208">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="442a9-209">새로운 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="442a9-209">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="442a9-210">새로운 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="442a9-210">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="442a9-211">새로운 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="442a9-211">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="442a9-212">새로운 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="442a9-212">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="442a9-213">새로운 AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="442a9-213">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="442a9-214">새로운 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="442a9-214">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="442a9-215">새로운 AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="442a9-215">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="442a9-216">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="442a9-216">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="442a9-217">새로운 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="442a9-217">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
